# Generating snippets

Functions are documented on [sass-lang.com](https://sass-lang.com/documentation/Sass/Script/Functions.html). Copy them to a file and whip them into a json:

```json
[{
    "trigger": "blue",
    "category": "sass color",
    "contents": "blue(${1:color})"
}]
```

A little python script generates the snippet files:

```py
import json
import sys

template = """<snippet>
<content><![CDATA[
{snippet}
]]></content>
<tabTrigger>{trigger}</tabTrigger>
<description>{category}</description>
<scope>source.css.scss</scope>
</snippet>
"""

data = json.load(open(sys.argv[1]))

for entry in data:
    snippet = open('Snippets/' + entry.get('trigger') + '.sublime-snippet', 'w')
    snippet.write(template.format(
        snippet=entry.get('contents'),
        trigger=entry.get('trigger'),
        category=entry.get('category')
        ))
    snippet.close()
```
