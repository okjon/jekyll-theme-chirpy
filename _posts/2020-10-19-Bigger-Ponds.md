---
title: Bigger Ponds (2015)
date: 2020-10-19 

categories: [poem]
---

[![Green sea turtle (Penang, Malaysia)](/assets/img/turtle.jpg){: width="300" class="left"}](https://www.instagram.com/p/B2Gejv_n3pN/)

<br clear="left"/>

> I wrote this for her who was starting a new job as a teacher in a new school. 

My love absconds to bigger ponds 

In a new role to feed tadpoles 

To let eggs grow their legs 

And watch hatchlings turn to fledglings 

Like a mother over ducklings

She spreads her wings and sings  

To ears unpierced and eyes that prize   

The love of story and tales of glory 

She opens minds in due time 

And makes way for come what may  
<br />
<br />
<br />
test


<!-- Comments -->
{% if site.data.comments[page.slug] %}
    <h3>
    {% if site.data.comments[page.slug].size > 1 %}
      {{ site.data.comments[page.slug] | size }}
    {% endif %}
    Comments:
    </h3>
  {% assign comments = site.data.comments[page.slug] | sort %}
    {% for comment in comments %}
      <label>
        {% if comment[1].url %}
          <a href="{{ comment[1].url }}">
        {% endif %}
        <strong>{{ comment[1].name }}</strong>
        {% if comment[1].url %}
          </a>
        {% endif %}
      </label>
      <em>{{ comment[1].date | date: "%B %d, %Y" }}</em>
      <p>{{ comment[1].message | markdownify }}</p>
    {% endfor %}
{% endif %}
<!-- Comments Form -->
  <form method="POST" action="{{ site.staticman_url }}">
    <input name="options[redirect]" type="hidden" value="https://example.com">
    <input name="options[slug]" type="hidden" value="{{ page.slug }}">
      <label>Name</label>
      <input name="fields[name]" type="text">
      <label>E-mail (optional)</label>
      <input name="fields[email]" type="email">
      <label>Website (optional)</label>
      <input name="fields[url]" type="url">
      <label>Message</label>
      <textarea style="width:100%" name="fields[message]" rows="12"></textarea>
      <small>Comments will appear after moderation.</small>
      <button type="submit">Submit comment</button>
  </form>
