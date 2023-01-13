---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---


{% for member in site.data.pi %}
<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.info }}</i></h4>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}
  {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}
  {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a> {% endif %}

  <ul style="overflow: hidden">
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 3 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 4 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education4 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 5 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education4 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education5 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 6 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education4 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education5 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education6 | replace: "-","&#8211;"}} </li>
  {% endif %}
  </ul>
</div>
</div>
</div>
{% endfor %}

<div class="jumbotron">
I am a Senior Research Fellow in the AI and Autonomy Lab of the School of Computing and Information Systems at the University of Melbourne, Australia (2012-present). I completed my PhD in Computer Science at the University of Melbourne in 2011. I have rather diverse research interests that include election integrity (with a focus on post-election audits), combinatorial optimization (with a focus on algorithms for solving large problems through decomposition, local search, and the use of mathematical programming), applications of reinforcement learning, and Explainable AI.  For more detail on my work in some of these areas, head over to the Research tab!
</div>

  <h3>PhD Opportunities</h3>
  
  I am currently accepting new PhD students. If you are interested in my any facets of my work, and feel that you meet the requirements for entry into the PhD program with the Faculty of Engineering and IT (see <a href="https://study.unimelb.edu.au/find/courses/graduate/doctor-of-philosophy-engineering-and-it/how-to-apply/">here</a> for details on eligibility), please feel free to reach out to me. I am particularly interested in students who wish to work on post-election audits (see below). 
  
  <div class="jumbotron">
<b>Election Integrity through Post-Election Audits</b>

Interested in election integrity, and doing a PhD (full or part-time) in Australia? Then we want you! Our team is actively working towards risk-limiting post-election audits for Single Transferable Vote (STV) elections. If you are unfamiliar with the term, this is how we elect our Senators to the Australian Senate. It's also used in a smattering of other places world-wide, including some elections in the United States and the United Kingdom. The ballots cast in our Senate election here in Australia are not manually counted. The way in which STV works is just too complex for manual counting to be practical. Ballot scanning technology is used to digitise the preferences expressed by a voter on their ballot, with these digitised preferences then fed into software that performs the tabulation, and determines which candidates are elected. Such technology is not perfect, there will always be some chance of misinterpretation, or errors, between paper ballots and their digitisation. We have found in prior work that even random errors during ballot scanning can impact certain candidates more than others. A post-election audit is designed to give us a certain degree of confidence that the outcome announced by the systems used is in fact the correct outcome. Practical and meaningful post-election audits for STV elections is the current 'holy grail' of our work in this space, and we are looking for PhD students to work on this goal. We have recently been awarded an ARC Discovery Project on the topic, and top-up scholarships of up to 10,000 AUD per year are a possibility.  
</div>

{% if site.data.grants %}
<div class="jumbotron">
### Grants
<ul>
{% for grant in site.data.grants %}
 <li> {{ grant.name }} </li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="jumbotron">
### Awards
<ul>
{% for award in site.data.awards %}
 <li> {{ award.name | replace: "-","&#8211;"}} </li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.people %}
<div class="jumbotron">
### Students and mentoring
<ul>
{% for student in site.data.people %}
 <li> {{ student.name }}, {{student.location}} ({{student.degree}}, {{student.year}}) </li>
{% endfor %}
</ul>
</div>
{% endif %}


