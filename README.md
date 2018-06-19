# Syntax Highlighting for Sass

This is a Sublime Text 3 package which purely forced on highlighting both Sass and SCSS syntax as accuracy as possible. Please make sure your Sublime Text 3 version is above Build 3103.

This package has taken over the package name "Sass", please search keyword "sass" from Package Control to install this package.

Known issues:

1. If you updated this package from the [original Sass package](https://github.com/nathos/sass-textmate-bundle) you might notice SCSS files are highlighted with the Sass syntax, to solve this issue, please open any `.scss` file and reset its highlighting syntax with the "Open all with current extension as..." option.

2. If you need the Emmet CSS abbreviation popup window to work well with the Sass syntax, you probably need to add the following code to your Emmet settings file.
  ``` json
  {
      "css_completions_scope": "source.scss - comment - variable - keyword.control - entity.other, source.sass - comment - variable - keyword.control - entity.other",
  }
  ```

## New Features

* Added support for CSS4 variables
* Enhanced Sass map highlighting
* Enhanced CSS functions and Sass functions highlighting
* Enhanced Sass mixin/function name highlighting and their "Goto Definition" support
* Removed built-in completions

## Generating snippets

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
