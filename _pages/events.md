---
layout: single
title: Events
permalink: /events/
author_profile: false
---

<ul class="w3-ul team-event-types">
  <li>
    <i class="fa fa-book" aria-hidden="true"></i>
    <span>
      <strong><em>Reading Group</em></strong>:
      A group member takes the lead, moderating a discussion on a chosen paper.
    </span>
  </li>
  <li>
    <i class="fa fa-coffee" aria-hidden="true"></i>
    <span>
      <strong><em>Tech Coffee</em></strong>:
      A group member takes the lead, discussing technical aspects of
      their ongoing research project.
    </span>
  </li>
  <li>
    <i class="fa fa-chalkboard-teacher" aria-hidden="true"></i>
    <span>
      <strong><em>Seminar</em></strong>:
      We frequently invite external speakers to give talks or tutorials.
    </span>
  </li>
  <li>
    <i class="fa fa-pizza-slice" aria-hidden="true"></i>
    <span>
      <strong><em>Meta Meals</em></strong>:
      We hold guided discussions over lunch on research and more general topics.
    </span>
  </li>
  <li>
    <i class="fa fa-edit" aria-hidden="true"></i>
    <span>
      <strong><em>Write-Up Meeting</em></strong>:
      We discuss members' research write-ups every other Friday.
    </span>
  </li>
  <li>
    <i class="fa fa-comments" aria-hidden="true"></i>
    <span>
      <strong><em>1on1 Meetings</em></strong>:
      Individual research discussions on the Monday following each write-up
      meeting, with intern and part-timer meetings on the following Wednesday.
    </span>
  </li>
</ul>

<style>
  ul.team-event-types {
    list-style: none;
    padding-left: 0;
    margin-left: 0;
  }

  ul.team-event-types > li {
    display: flex;
    align-items: baseline;
    gap: 0.65em;
    list-style: none;
    padding: 0.5em 0;
  }

  ul.team-event-types > li > .fa {
    flex: 0 0 1.3em;
    width: 1.3em;
    font-size: 25px;
    text-align: center;
  }

  ul.team-event-types > li > span {
    flex: 1;
    min-width: 0;
  }
</style>

<h2>Upcoming</h2>

<section class="page__content cf" id="upcoming-meetings">

{% assign curDate = site.time | date: '%F' %}
{% assign postsAscending = site.posts | reverse %}

{% for post in postsAscending %}
  {% assign postStartDate = post.date | date: '%F' %}
  {% if post.categories contains "seminar" and postStartDate >= curDate %}
    <div class="news" data-meeting-date="{{ postStartDate }}">
      <b class="news-title">
        <i class="fa {{ post.logo | escape }}"
           style="font-size: 25px;"
           aria-hidden="true"></i>
        {{ post.date | date: '%B %d, %Y' }}
        {% if post.time %} @ {{ post.time | escape }} {% endif %}
      </b>
      <br>
      {{ post.content }}
    </div>
  {% endif %}
{% endfor %}

</section>

<noscript>
  <p>
    Write-up meetings take place every other Friday, starting October 2,
    2026, at 17:15 JST. The following Monday has 1-on-1 meetings
    (16:15–19:00 JST), and the following Wednesday has intern / part-timer
    1-on-1 meetings (17:15–19:00 JST).
  </p>
</noscript>

<style>
  #upcoming-meetings .recurring-meeting {
    border-left: 3px solid #52adc8;
    padding-left: 1em;
    margin-bottom: 1.5em;
  }

  #upcoming-meetings .recurring-meeting .fa {
    color: #52adc8;
    font-size: 25px;
    margin-right: 0.25em;
  }

  #upcoming-meetings .recurring-meeting p {
    margin: 0.35em 0 0;
  }
</style>

<script>
(() => {
  const container = document.getElementById("upcoming-meetings");
  if (!container) return;

  const DAY = 24 * 60 * 60 * 1000;
  const PERIOD = 14 * DAY;
  const JST = 9 * 60 * 60 * 1000;

  // Midnight at the start of today in Japan.
  // Meetings remain visible throughout their scheduled day.
  const today = Math.floor((Date.now() + JST) / DAY) * DAY - JST;

  const firstFriday = Date.parse("2026-10-02T00:00:00+09:00");

  const dateKey = timestamp =>
    new Date(timestamp + JST).toISOString().slice(0, 10);

  const dateFormat = new Intl.DateTimeFormat("en-US", {
    timeZone: "Asia/Tokyo",
    weekday: "long",
    month: "long",
    day: "2-digit",
    year: "numeric"
  });

  // Offsets are measured from the Friday write-up meeting.
  const meetings = [
    {
      offset: 0,
      title: "Write-up meeting",
      time: "17:15 JST",
      icon: "fa-edit"
    },
    {
      offset: 3,
      title: "1on1 meetings",
      time: "16:15–19:00 JST",
      icon: "fa-comments"
    },
    {
      offset: 5,
      title: "Intern 1on1 meetings",
      time: "17:15–19:00 JST",
      icon: "fa-users"
    }
  ];

  // Find the next occurrence of each meeting independently.
  meetings.forEach(meeting => {
    const first = firstFriday + meeting.offset * DAY;
    const cycle = Math.max(0, Math.ceil((today - first) / PERIOD));
    const nextDate = first + cycle * PERIOD;

    const entry = document.createElement("div");
    entry.className = "news";
    entry.dataset.meetingDate = dateKey(nextDate);

    entry.innerHTML = `
      <b class="news-title">
        <i class="fa ${meeting.icon}"
          style="font-size: 25px;"
          aria-hidden="true"></i>
        ${dateFormat.format(nextDate)} @ ${meeting.time}
      </b>
      <br>
      <p><em>${meeting.title}.</em></p>
    `;

    container.appendChild(entry);
  });

  // Merge recurring meetings with seminar posts in date order.
  // Also remove seminar entries that have expired since the last build.
  const todayKey = dateKey(today);

  const entries = Array.from(
    container.querySelectorAll(".news[data-meeting-date]")
  );

  entries
    .filter(entry => {
      if (entry.dataset.meetingDate < todayKey) {
        entry.remove();
        return false;
      }
      return true;
    })
    .sort((a, b) =>
      a.dataset.meetingDate.localeCompare(b.dataset.meetingDate)
    )
    .forEach(entry => container.appendChild(entry));
})();
</script>

<h2>Past Meetings</h2>

<section class="page__content cf">

{% assign i = 0 %}
{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "seminar" and postStartDate < curDate and i < 9 %}
    <div class="news">
    <b class="news-title"> <i class="fa {{post.logo}}" style="font-size: 25px;"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
    {{ post.content }}
    </div>
    {% assign i = i | plus:1 %}
  {% endif %}
{% endfor %}

</section>

<details>
<summary>Show all reading group meetings</summary>
<section class="page__content cf">
<br>
{% assign i = 0 %}
{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "seminar" and postStartDate < curDate %}
    {% if i >= 9 %}
     <div class="news">
      <b class="news-title"> <i class="fa {{post.logo}}" style="font-size: 25px;"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
      {{ post.content }}
    </div>
	{% endif %}
    {% assign i = i | plus:1 %}
  {% endif %}
{% endfor %}
</section>
</details>
 
<!-- <br>
{% assign posts = site.posts | where: 'categories', 'lab-activities' | sort: 'date' | reverse %}
{% assign latest_post = posts.first %}
<div class="post">
      <h3>
      <a href="{{ latest_post.url | prepend: site.baseurl }}" class="post-link">{{ latest_post.title }} </a>
	</h3>
</div> -->