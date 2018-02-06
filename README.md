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

## Scopes list

Here is a list of which syntax part is capable to highlight and its scope name. All scope names are following the suggestions of https://www.sublimetext.com/docs/3/scope_naming.html. If any part from the list down below is not highlighted as expected with your current color scheme, please try to contact the color scheme author to add support for the corresponding scope or modify the color scheme by yourself. Learn more about "color schemes" please take a look at https://www.sublimetext.com/docs/3/color_schemes.html.

Element      | Scope
:----------- | :--------------
Block Comment | `comment.block.css.sass`
Sass Line Comment | `comment.line.sass`
CSS4 Variable | `variable.parameter.sass`
Sass Variable | `variable.parameter.sass`
At-rule, Sass Directive, Directive Shorthand | `keyword.control.at-rule.css.sass`
Type Selector, Universal Selector | `entity.name.tag.css.sass`
Id Selector | `entity.other.attribute-name.id.css.sass`
Class Selector, Sass Placeholder Selector | `entity.other.attribute-name.class.css.sass`
Attribute Selector | `entity.other.attribute-name.css.sass`
Attribute Selector RegEx | `keyword.operator.attribute-selector.css.sass`
Pseudo Class, Pseudo Element | `entity.other.pseudo-class.css.sass`
Property Name | `support.type.property-name.css.sass`
Property Value | `support.constant.property-value.css.sass`
Quoted String | `string.quoted.css.sass`
Numeric | `constant.numeric.css.sass`
Unit | `keyword.other.unit.css.sass`
Rgb Color | `constant.other.color.rgb-valueb.css.sass`
Sass Parent Selector | `keyword.other.parent-selector.sass`
Sass Operator | `keyword.operator.css.sass`
Sass Mixin and Function Definition | `entity.name.function.sass`
Sass Mixin and Function Calling Name | `support.function.sass`
Sass Interpolation | `keyword.control.interpolation.sass`
Sass Flag | `keyword.other.important.css.sass`
Sass Reserved Word | `keyword.other.reserved.sass`
Sass Indented Syntax Semicolon | `invalid`
Sass Indented Syntax Curly Brackets | `invalid`

## License

MIT License
