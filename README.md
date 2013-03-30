# Syntax Highlighting for Sass
This is a new syntax highlighting package for Sass (separately support both SCSS and Sass) for Sublime Text / TextMate. Compared with other packages, this will match the structure of `property name` and `property value` instead of matching keywords (`property name` will be matched under `source.sass` scope selector), so these two parts will be perfectly highlighted and no need to add keywords in the future. Other features including: added support for attribute selector, variables, interpolation syntax, directives and directive shorthand (`=` `+`), functions, operators… etc; improved the highlighting rule for `@media`; and also added `Completion Rules.tmPreferences` file, completions will not be offered when typing in selectors.

Syntax such like `something(…)` will be matched as **function**, this will effect some CSS property values, Sass build-in functions, Compass/Bourbon functions, and custom functions.

Sass at-rules (e.g. `@function`) still have room for improvement.

The `Preferences` and `Completions` two folders are directly copied from [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime) with a little bit of modifications. In this package, `property-name.sass` scope selector only works in `@media` directive, then I removed the `Sass - Properties.sublime-completions` file.

As always, if you have any problems with this package or suggestions for improvement, please feel free to [fill an issue](https://github.com/P233/Syntax-highlighting-for-Sass/issues/new), and you are also more than welcome to fork this repo and pull request.

## Installation

### Sublime Text

Now you can install this package through Package Control.

Or download this package and rename the downloaded folder as you like, then move it into the Packages folder of Sublime Text.

### TextMate
Firstly, move the `Solarized (Light).tmTheme` file into `~/Library/Application Support/TextMate/Themes/`, then add `.tmbundle` extension to the downloaded folder and move it in to `~/Library/Application Support/TextMate/Bundles/`. If the folder doesn't exist, create one.

## Scope Selectors

I have shared a custom `Solarized (Light).tmTheme` in Color Scheme folder, so that you can see how this highlighting package works. And you can also build/modify your own color scheme with the following scope selectors. (Learn more about Scope Selectors and Color Scheme, take a look at [Textmate Scope Selectors](http://manual.macromates.com/en/scope_selectors) and [Textmate Themes](http://manual.macromates.com/en/themes.html).) If you make a color scheme for this package, please [let me know](mailto:40132147@qq.com). I'd like to add a link here.

Element      | Scope Selector
:----------- | :--------------
Block Comment | comment.block.sass
Double Dash Comment | comment.line.double-dash.sass
At-rule | keyword.control.at-rule.css.sass
Type Selector | entity.name.tag.css.sass
Id Selector | entity.other.attribute-name.id.css.sass
Class Selector | entity.other.attribute-name.class.css.sass
Placeholder Selector | entity.other.attribute-name.placeholder-selector.sass
Attribute Selector | entity.other.attribute-selector.sass
Regex | keyword.other.regex.sass
Pseudo Class | entity.other.attribute-name.pseudo-class.css.sass
Pseudo Element | entity.other.attribute-name.pseudo-element.css.sass
Property Name | source.sass, support.constant.property-name.css.sass
Property Value | support.constant.property-value.css.sass
Double Quoted | string.quoted.double.css.sass
Ampersand | keyword.other.ampersand.sass
Colon | comment.punctuation.colon.sass
Comma | comment.punctuation.comma.sass
Round Brackets | comment.punctuation.round-brackets.sass
Numeric | constant.numeric.css.sass
Unit | keyword.other.unit.css.sass
Rgb Color | constant.other.color.rgb-value.css.sass
Literal Color | support.constant.color.css.sass
Font Name | support.constant.font-name.css.sass
Function Name | support.function.name.sass
Sass Variable | variable
Sass Directive | keyword.control.at-rule.css.directive.sass
Sass Directive Shorthand | keyword.control.at-rule.css.shorthand.sass
Sass Interpolation | support.function.interpolation.sass
Sass Flag | keyword.other.important.css.sass
Sass Operator | keyword.operator.sass
SCSS Semicolon | comment.punctuation.semicolon.sass
SCSS Curly Brackets | comment.punctuation.curly-brackets.sass
Sass Semicolon | invalid
Sass Curly Brackets | invalid

## Contributors

[mannieschumpert](https://github.com/mannieschumpert)

## Credit
[nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime)

[Textmate Language Grammars](http://manual.macromates.com/en/language_grammars.html)

[Solarized](http://ethanschoonover.com/solarized)