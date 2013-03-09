# Syntax Highlighting for Sass
This is a new syntax highlighting package for Sass (both SCSS and Sass syntaxes) for Sublime Text. Compared with other packages, this will match the structure of `property name` and `property value` instead of matching keywords (actually nothing will match `property name`, it will be treated as basic Sass text), so those two parts will be perfectly highlighted. Also added support for attribute selector, variables, interpolation syntax, directives and directive shorthand (`=` `+`), build-in functions… etc. And also  improved the highlighting rule for `@media`.

The Preferences and Completions two folders are directly copied from [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime) with a little bit of modifications. In this package the `property-name.sass` scope selector is only used to fix keyword conflict, so the `Sass - Properties.sublime-completions` file is removed.

I have shared a custom `Solarized (Light).tmTheme` in Color Scheme folder, so you can see how this highlighting package works. And you can also build your own colour scheme with the following scope selectors. (Learn more about Scope Selectors and Color Scheme, you can have a look at [Textmate Scope Selectors](http://manual.macromates.com/en/scope_selectors) and [Textmate Themes](http://manual.macromates.com/en/themes.html).)

As always, if you have any problems with this package or suggestions for improvement, please feel free to [fill an issue](https://github.com/P233/Syntax-highlighting-for-Sass/issues/new), and you are also more than welcome to fork this repo and pull request.

## Installation

Rename the downloaded folder as you like, and then move it into the Packages folder of Sublime Text.

## Scope Selectors
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
URL | support.function.url.sass
Rgb Color | constant.other.color.rgb-value.sass
Literal Color | support.constant.color.sass
Font Name | support.constant.font-name.sass
Sass Variable | support.variable.sass
Sass Directive | support.function.directive.sass
Sass Directive Shorthand | support.function.directive-shorthand.sass
Sass Build-in Function | support.function.buildin.sass
Sass Interpolation | support.function.interpolation.sass
Sass Flag | keyword.other.flag.sass
Sass Operator | keyword.operator.sass
SCSS Semicolon | keyword.other.semicolon.sass
SCSS Curly Brackets | keyword.other.curly-brackets.sass

## Credit
[nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime)

[Textmate Language Grammars](http://manual.macromates.com/en/language_grammars.html)

[Solarized](http://ethanschoonover.com/solarized)