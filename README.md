# Syntax Highlighting for Sass
This is a new syntax highlighting package for Sass (separately support both SCSS and Sass) for Sublime Text / TextMate. Compared with other packages, this will match the structure of `property name` and `property value` instead of matching keywords, so these two parts will be perfectly highlighted and no need to add keywords in the future. Other features including: added support for attribute selector, variables, interpolation syntax, directives and directive shorthand (`=` `+`), functions, operators… etc; improved the highlighting rule for `@media`; and also added `Completion Rules.tmPreferences` file, completions will not be offered when typing in selectors.

Syntax such like `something(…)` will be matched as **function**, this will effect some CSS property values, Sass build-in functions, Compass/Bourbon functions, and custom functions.

The `Preferences` and `Completions` two folders are directly copied from [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime) with a little bit of modifications. In this package, `property-name` scope selector only works in `@media` directive, then I removed the `Sass - Properties.sublime-completions` file.

As always, if you have any problems with this package or suggestions for improvement, please feel free to [fill an issue](https://github.com/P233/Syntax-highlighting-for-Sass/issues/new), and you are also more than welcome to fork this repo and pull request.

## Installation

### Sublime Text

Now you can install this package through Package Control.

Or download this package and rename the downloaded folder as you like, then move it into the Packages folder of Sublime Text.

### TextMate

Firstly, move the `Solarized (Light).tmTheme` file into `~/Library/Application Support/TextMate/Themes/`, then add `.tmbundle` extension to the downloaded folder and move it in to `~/Library/Application Support/TextMate/Bundles/`. If the folder doesn't exist, create one.

## Modify Color Scheme

I have shared a custom `Solarized (Light).tmTheme` file in Color Scheme folder, so that you can see how this highlighting package works. If you'd like to use other color schemes, this package works fine, but not perfect. You can take the following steps to learn how to modify a color scheme.

### Highlight Punctuations

Most highlighting packages will ignore punctuations (`:` `;` `( )` and `{ }`)，but in this package some punctuations cannot be ignored. By default, they will be treated as same as comment.  You can use the following code to restyle them if you want. Copy and paste the code anywhere between `<array> </array>` in your favorite color scheme file, and replace `#000000` with the foreground color which should appear near the top of the file.

```
<dict>
	<key>name</key>
	<string>Sass: Punctuations</string>
	<key>scope</key>
	<string>comment.punctuation</string>
	<key>settings</key>
	<dict>
		<key>foreground</key>
		<string>#000000</string>
	</dict>
</dict>
```

If you want to add extra style, you can edit the following code and paste it after `<key>foreground</key>`.

```
<key>fontStyle</key>
<string>italic</string>
<key>background</key>
<string>#000000</string>
```

### Highlight Variable

Some color scheme may not support variables. The following code could solve this problem.

```
<dict>
	<key>name</key>
	<string>Sass: Variable</string>
	<key>scope</key>
	<string>source.sass variable</string>
	<key>settings</key>
	<dict>
		<key>foreground</key>
		<string>#000000</string>
	</dict>
</dict>
```

### Highlight everything

With the following scope selectors, you can modify anything in this package. Learn more about Scope Selectors and Color Scheme, take a look at [Textmate Scope Selectors](http://manual.macromates.com/en/scope_selectors) and [Textmate Themes](http://manual.macromates.com/en/themes.html).

You can even build a new color scheme for this package. If you make one, please [let me know](mailto:40132147@qq.com). I'd like to add a link here.

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
Property Name | support.type.property-name.css.sass
Property Value | meta.property-value.css.sass, support.constant.property-value.css.sass
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
Sass Directive, Directive Shorthand | keyword.control.at-rule.css.sass
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