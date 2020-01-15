---
layout: page
title: Guestbook
permalink: /guestbook
---

{% assign posts = site.data.guestbook | sort %}
{% for post in posts reversed %}
  {% assign timestamp = post[0] | replace_first: 'entry', '' | date: "%B %d, %Y at %H:%M" %}
<p>
By {{ post[1].name }} on {{ timestamp }}
<blockquote style="font-style: italic;">{{ post[1].message }}</blockquote>
<hr/>
</p>
{% endfor %}

# Add your own entry

<form method="POST" action="https://dev.staticman.net/v3/entry/github/harryyoud/dhbb-site/master/comments">
  <input name="options[redirect]" type="hidden" value="{% link contact-us.markdown %}">

  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <label><input name="fields[name]" type="text">Name</label>
  <label><textarea name="fields[message]"></textarea>Message</label>

  <button type="submit">Go!</button>
</form>
