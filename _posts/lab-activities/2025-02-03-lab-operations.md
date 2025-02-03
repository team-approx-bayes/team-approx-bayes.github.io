---
title: Lab Operations
date: 2025-2-3
categories:
  - lab-activities
affiliation_profile: false
author_profile: false
---

<h2>Tasks Assignments</h2>
<table class="table">
   <tr>
    <th>Meeting</th>
    <th>Name</th>
  </tr>
  <tr>
    <td>Reading Group</td>
    <td>Thomas</td>
  </tr>
  <tr>
    <td>Tech Coffee</td>
    <td>Keigo</td>
  </tr>
  <tr>
    <td>Writeups</td>
    <td>Yohan</td>
  </tr>
  <tr>
    <td>Bayes Duality Seminar</td>
    <td>Hugo</td>
  </tr>
  <tr>
    <td>Meta Meal</td>
    <td>Hugo</td>
  </tr>
  <tr>
    <td>Intern Writeups</td>
    <td>Anita</td>
  </tr>
  <tr>
    <th>General Affairs</th>
    <th>Name</th>
  </tr>
  <tr>
    <td>Hiring</td>
    <td>Emti</td>
  </tr>
  <tr>
    <td>Intern</td>
    <td>Emti, Thomas</td>
  </tr>
  <tr>
    <td>Wiki</td>
    <td>Christopher</td>
  </tr>
  <tr>
    <td>Homepage</td>
    <td>Keigo, Sin-Han</td>
  </tr>
  <tr>
    <td>Purchase</td>
    <td>Hugo, Emti, Thomas</td>
  </tr>
  <tr>
    <td>Servers</td>
    <td>Christopher, Hugo</td>
  </tr>
  <tr>
    <th>Public Relations</th>
    <th>Name</th>
  </tr>
  <tr>
    <td>Visitor</td>
    <td>TBD</td>
  </tr>
  <tr>
    <td>Social Activity</td>
    <td>Hugo</td>
  </tr>
</table>

{% assign posts = site.posts | where: 'categories', 'lab-activities' | sort: 'date' | reverse %}
{% assign latest_post = posts.first %}
{% assign other_posts = posts | where_exp: "post", "post != latest_post" %}


<button id="toggle-past-operators">Past Operations</button>

<div id="past-operators" style="display:none;">
    {% for post in other_posts %}
    <div class="post">
        <h3>
            <a href="{{ post.url | prepend: site.baseurl }}" class="post-link">{{ post.date | date: '%B %d, %Y' }}</a>
        </h3>
    </div>
    {% endfor %}
</div>

<script>
    document.getElementById('toggle-past-operators').onclick = function() {
        var pastOperators = document.getElementById('past-operators');
        if (pastOperators.style.display === 'none') {
            pastOperators.style.display = 'block';
        } else {
            pastOperators.style.display = 'none';
        }
    };
</script>