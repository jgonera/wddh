---
title: Wikistream
year: 2012
date: 2014/05/09
url: http://wikistream.wmflabs.org/
images:
  - one
description: >
  Wikistream is a Node.js webapp for helping visualize current
  editing activity in Wikipedia. It uses Node.js, socket.io and Redis to sit
  in the wikimedia IRC chat rooms (where updates are published), and makes
  them available on the Web in realtime.
authors:
  - name: Ed Summers
    url: https://twitter.com/edsu
  - name: Sean Hannan
    url: https://twitter.com/mrdys
  - name: Delphine Ménard
    url: https://twitter.com/notafish
code: https://github.com/edsu/wikistream
data_types:
  - recent_changes
  - user_contributions
  - article_revisions
data_sources:
  - rcstream
---

A table:

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

Code:

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
