# Syntax Highlighting for Sass
This is a new Sass syntax highlighting package (separately support both SCSS and Sass) for Sublime Text / TextMate. Compared with other packages, *this will match syntax structure instead of matching keywords, so everything will be perfectly highlighted!*

## Features:
* Highlight Sass variables, functions, interpolation syntax, directives and directive shorthand (`=` `+`), operators, attribute selector… etc;
* Better highlighting result for Media Queries;
* Completions will not be offered when typing in selectors.
* Added Sass build-in functions and Compass CSS3 completions (still under working progress)

The `Preferences` and `Completions` two folders are directly copied from [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime) with a little bit of modifications. `Sass - Properties.sublime-completions` will not work with this package, so I removed it.

As always, if you have any problems with this package or suggestions for improvement, please feel free to [fill an issue](https://github.com/P233/Syntax-highlighting-for-Sass/issues/new), and you are also more than welcome to fork this repo and pull request.

## Installation

### Sublime Text

Recommend to install this package through **Package Control** (use the keyword `SHS` to find this plugin). Or download this package and rename it as you like, then move it into the Packages folder of Sublime Text.

### TextMate

Download the [bundle file](https://github.com/P233/Syntax-highlighting-for-Sass/tree/textmate) and then move it in to `~/Library/Application Support/TextMate/Bundles/`. If the folder doesn't exist, create one.

## Color Scheme

### Recommended Color Schemes

I have shared a custom `Solarized (Light).tmTheme` file in Color Scheme folder, so that you can see how this highlighting package works. If you'd like to use other color schemes, this package works fine, may not perfect. Here are some recommended Color Schemes:

* [Perv Color Schemes](https://github.com/FlavourSys/Perv-ColorScheme) Thanks [Mick](https://github.com/micck) for adding support for this package
* [Tomorrow Theme](https://github.com/chriskempson/tomorrow-theme)

### Modify Color Scheme

With the following scope selectors, you can change the color for everything in this package. For example, if a color scheme doesn't support variables, copy and paste the following code anywhere between `<array> </array>` in the file could solve this problem.

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

Learn more about Scope Selectors and Color Scheme, take a look at [Textmate Scope Selectors](http://manual.macromates.com/en/scope_selectors) and [Textmate Themes](http://manual.macromates.com/en/themes.html).

You can even build a new color scheme for this package. If you make one, please [let me know](mailto:40132147@qq.com). I'd like to add a link here.

Element      | Scope Selector
:----------- | :--------------
Block Comment | comment.block.sass
Double Dash Comment | comment.line.double-dash.sass
At-rule | keyword.control.at-rule.css.sass
Type Selector, Ampersand | entity.name.tag.css.sass
Id Selector | entity.other.attribute-name.id.css.sass
Class Selector | entity.other.attribute-name.class.css.sass
Placeholder Selector | entity.other.attribute-name.placeholder-selector.sass
Attribute Selector | entity.other.attribute-selector.sass
Regex | keyword.other.regex.sass
Pseudo Class, Pseudo Element | entity.other.attribute-name.pseudo-class.css.sass
Property Name | support.type.property-name.css.sass
Property Value | meta.property-value.css.sass, support.constant.property-value.css.sass
Double Quoted | string.quoted.double.css.sass
Comma | comment.punctuation.comma.sass
Numeric | constant.numeric.css.sass
Unit | keyword.other.unit.css.sass
Rgb Color | constant.other.color.rgb-value.css.sass
Function Name | support.function.name.sass
Sass Variable | variable
Sass Directive, Directive Shorthand | keyword.control.at-rule.css.sass
Sass Interpolation | support.function.interpolation.sass
Sass Flag | keyword.other.important.css.sass
Sass Operator | keyword.operator.sass
SCSS Semicolon | comment.punctuation.semicolon.sass
Sass Semicolon | invalid
Sass Curly Brackets | invalid

## Contributors

[mannieschumpert](https://github.com/mannieschumpert)

## Credit
[nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle/tree/sublime)

[Textmate Language Grammars](http://manual.macromates.com/en/language_grammars.html)

[Solarized](http://ethanschoonover.com/solarized)