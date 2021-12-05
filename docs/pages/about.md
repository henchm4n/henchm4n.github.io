---
layout: page
title: About
permalink: /about/
weight: 3
---

# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>
I have a Bachelor of Computer Science at the University of Queensland, majoring in Cyber Security.

My interests include cyber security, specifically offensive security and detecting network mis-actors, blockchain and programming.

I also like to spend time hiking, running and swimming as well as reading.

<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills" source=site.data.other-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>