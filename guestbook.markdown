---
layout: page
title: Guestbook
permalink: /guestbook
---

<form method="POST" action="https://dev.staticman.net/v3/entry/github/harryyoud/dhbb-site/master/comments">
  <input name="options[redirect]" type="hidden" value="{{ link 'contact-us.markdown' }}">

  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <label><input name="fields[name]" type="text">Name</label>
  <label><textarea name="fields[message]"></textarea>Message</label>

  <button type="submit">Go!</button>
</form>
