---
title: Current Team Members
layout: single
permalink: /people/
affiliation_profile: false
entries_layout: grid
custom_css: people
<!-- classes: wide -->
<!-- show_excerpts: true -->
---

<section class="page__content cf">
<div class="entries-{{ entries_layout }}">
  {% assign groups = site['people'] | group_by: 'rank' | sort: 'name' %}
  {% for group in groups %}
    {% assign entriesInGroup = group.items | sort: 'date' %}
    {% for post in entriesInGroup %}
      {% include people-single.html type=page.entries_layout %}
    {%- endfor -%}
  {% endfor %}
</div>
</section>



# **Past Members**

<div class="w3-container">
<br>
Lucie Perrotta <span class="affiliation">(Sep 2019-Mar2020, Intern from EPFL, Switzerland)</span><br>
<br>
Xiangming Meng  <span class="affiliation">(July 2019-Mar 2020, Postdoc)</span><br>
<br>
Farzaneh Mahdisoltani  <span class="affiliation">(Sep 2019-Feb 2020, Intern from UToronto and Vector Institute, Canada)</span><br>
<br>
Alexander Immer  <span class="affiliation">(March 2019- March 2020, Intern from EPFL, Switzerland)</span><br>
<br>
Roman Bachmann  <span class="affiliation">(July-Feb 2019, Intern from EPFL, Switzerland)</span><br>
<br>
Kazuki Osawa  <span class="affiliation">(Nov 2019-Feb 2020, Trainee from Tokyo Tech)</span><br>
<br>
Vincent Tan  <span class="affiliation">(May 2019-Jan 2020, Research assistant, went to pursue PhD at UOxford)</span><br>
<br>
Hongyi Ding  <span class="affiliation">(July 2019-Jan 2020, Postdoc)</span><br>
<br>
Anshuk Uppal  <span class="affiliation">(June-Dec 2019, Intern from IIIT Bangalore)</span><br>
<br>
Michael Przystupa  <span class="affiliation">(July-Dec 2019, Intern from UBC Vancouver)</span><br>
<br>
Maciej Korzepa  <span class="affiliation">(Feb-Dec 2019, Intern from DTU, Copenhagen)</span><br>
<br>
Matthias Bauer  <span class="affiliation">(Sep-Oct 2019, Intern from Max-Planck Institute)</span><br>
<br>
Pingbo Pan  <span class="affiliation">(May-Sep 2019, Intern from UT Sydney)</span><br>
<br>
Pierre Orenstein  <span class="affiliation">(May-Sep 2019, Intern from France)</span><br>
<br>
Benjamin Bray  <span class="affiliation">(May-August 2019, Intern from Georgia Tech)</span><br>
<br>
Ehsan Abedi  <span class="affiliation">(March-August 2019, Intern from EPFL, Switzerland)</span><br>
<br>
Mark Goldstein  <span class="affiliation">(June-Sep 2019, Intern from NYU)</span><br>
<br>
Anirudh Jain  <span class="affiliation">(Dec 2018-July 2019, Intern from ISM, India)</span><br>
<br>
Runa Eschenhagen  <span class="affiliation">(Oct 2018-May 2019, Intern from University of Osnabrück, Germany)</span><br>
<br>
Anand Subramanian  <span class="affiliation">(Feb-May 2019, Intern from JAIST, Japan)</span><br>
<br>
Ohiremen Dibua  <span class="affiliation">(Intern from Stanford University between July 2018 to Aug 2018)</span><br>
<br>
Jiaxin Shi  <span class="affiliation">(Intern from Tsinghua University between July 2018 to Sep 2018)</span><br>
<br>
Hanna Tseran  <span class="affiliation">(Intern from University of Tokyo from Nov. 2017 to Aug. 2018)</span><br>
<br>
Si Kai Lee  <span class="affiliation">(Research Assistant from Dec 2017 to August 2018)</span><br>
<br>
Frederik Kunster  <span class="affiliation">(Intern from EPFL from Feb 2018 to August 2018)</span><br>
<br>
Didrik Nielsen  <span class="affiliation">(Research assistant from March 2017 to August 2018, joined DTU
Copenhagen in Ole Winther's group)</span><br>
<br>
Aaron Mishkin  <span class="affiliation">(Intern from UBC during Jan-Jun 2018, joined UBC as a Master student)</span><br>
<br>
Wu Lin  <span class="affiliation">(Research assistant from Jan-Dec 2017, joined UBC as a PhD student)</span><br>
<br>
Nicolas Hubacher  <span class="affiliation">(Research Assistant from Jan-Dec 2017)</span><br>
<br>
Zuozhu Liu  <span class="affiliation">(Intern from SUTD during June-Dec 2017)</span><br>
<br>
Vaden Masrani  <span class="affiliation">(Intern from UBC during May-Oct 2017)</span><br>
<br>
Salma El Aloui  <span class="affiliation">(Intern from École Polytechnique during Jun-Sep 2017)</span><br>
<br>
Kimia Nadjahi  <span class="affiliation">(Intern from ENS Cachan during May-Sep 2017)</span><br>
<br>
Arnaud Robert  <span class="affiliation">(Intern from EPFL during Oct 2016 to April 2017)</span><br>
<br>
Heiko Strathman  <span class="affiliation">(from UCL)</span><br>

</div>
