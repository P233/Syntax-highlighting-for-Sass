# Syntax Highlighting for Sass
This is a new syntax highlighting package for Sass (separately support both SCSS and Sass) for Sublime Text / TextMate. Compared with other packages, this will match the structure of `property name` and `property value` instead of matching keywords (actually, nothing will match `property name`, it will be treated as basic Sass text), so these two parts will be perfectly highlighted and no need to add keywords in the future. Other features including: added support for attribute selector, variables, interpolation syntax, directives and directive shorthand (`=` `+`), functions, operators… etc; and also improved the highlighting rule for `@media`.

Syntax such like `something(…)` will be matched as **function**, this will effect `url()`, `format()`, some CSS property values, Sass build-in functions, Compass/Bourbon functions, and even custom functions. And Sass at-rules (e.g. `@function`) will be matched as **directive**. These two parts still have room for improvement.

The `Preferences` and `Completions` two folders are directly copied from [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime) with a little bit of modifications. In this package, `property-name.sass` scope selector only works in `@media` directive, then I removed the `Sass - Properties.sublime-completions` file.

As always, if you have any problems with this package or suggestions for improvement, please feel free to [fill an issue](https://github.com/P233/Syntax-highlighting-for-Sass/issues/new), and you are also more than welcome to fork this repo and pull request.

## Installation

### Sublime Text
Rename the downloaded folder as you like, and then move it into the Packages folder of Sublime Text.

## Scope Selectors

I have shared a custom `Solarized (Light).tmTheme` in Color Scheme folder, so that you can see how this highlighting package works. And you can also build/modify your own color scheme with the following scope selectors. (Learn more about Scope Selectors and Color Scheme, take a look at [Textmate Scope Selectors](http://manual.macromates.com/en/scope_selectors) and [Textmate Themes](http://manual.macromates.com/en/themes.html).) If you make a color scheme for this package, please [let me know](mailto:40132147@qq.com). I'd like to add a link here.

Element      | Scope Selector
:----------- | :--------------
Block Comment | comment.block.sass
Double Dash Comment | comment.line.double-dash.sass
At-rule | keyword.control.at-rule.sass
Type Selector | entity.name.tag.sass
Id Selector | entity.other.attribute-name.id.sass
Class Selector | entity.other.attribute-name.class.sass
Placeholder Selector | entity.other.attribute-name.placeholder-selector.sass
Attribute Selector | entity.other.attribute-selector.sass
Regex | keyword.other.regex.sass
Pseudo Class | entity.other.attribute-name.pseudo-class.sass
Pseudo Element | entity.other.attribute-name.pseudo-element.sass
Property Name | source.sass, support.constant.property-name.sass
Property Value | support.constant.property-value.sass
Double Quoted | string.quoted.double.sass
Ampersand | keyword.other.ampersand.sass
Colon | keyword.other.colon.sass
Comma | keyword.other.comma.sass
Round Brackets | keyword.other.round-brackets.sass
Numeric | constant.numeric.sass
Unit | keyword.other.unit.sass
Rgb Color | constant.other.color.rgb-value.sass
Literal Color | support.constant.color.sass
Font Name | support.constant.font-name.sass
Function Name | support.function.name.sass
Sass Variable | support.variable.sass
Sass Directive | support.function.directive.sass
Sass Directive Shorthand | support.function.directive-shorthand.sass
Sass Interpolation | support.function.interpolation.sass
Sass Flag | keyword.other.flag.sass
Sass Operator | keyword.operator.sass
SCSS Semicolon | keyword.other.semicolon.sass
SCSS Curly Brackets | keyword.other.curly-brackets.sass

## Credit
[nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime)

[Textmate Language Grammars](http://manual.macromates.com/en/language_grammars.html)

[Solarized](http://ethanschoonover.com/solarized)