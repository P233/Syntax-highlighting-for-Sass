# Syntax Highlighting for Sass
用过几个版本的 Sass 代码高亮插件，效果都不太理想，所以参考 [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle) 自己也写了一个。采用匹配语句结构的方式代替匹配关键词，因此不会出现某些词不能高亮的问题，但有些根据 Scope Selector 的 snippets 可能会失效。添加了 Attribute Selector 高亮，优化了 `@media` 高亮效果，此外，支持 Sass 专有语句，包括 Variable, Directive, Directive Shorthand (`=` `+`), Placeholder Selector, Build-in Function, Interpolation 等等。目前除了运算符与自定义函数，其他部分应该完美显示。

Color Scheme 文件夹中附上了针对这个插件修改后的 `Solarized (Light).tmTheme`，大家可以根据其中的 Sass 部分，或者下面的 Scope Selector List 修改自己喜欢的高亮颜色。

Preferences 文件夹提供了 Sublime Text 2 快捷键注释以及符号跳转功能，两个文件拷贝自 [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle)。

Completions 文件夹直接拷贝自 [nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle)，由于匹配方式的变化，`Sass - Properties.sublime-completions` 将会在文件的任意位置提示，因此将其删除。

**请注意，这个插件只支持 Sass 语句，不支持 SCSS 语句。任何想法建议欢迎联系我，大家一起交流！**

## 安装
将下载的文件夹移动到 Sublime Text 2 的 Package 文件夹内。

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

## 致谢
[nathos's sass-textmate-bundle](https://github.com/nathos/sass-textmate-bundle)

[Textmate Language Grammars](http://manual.macromates.com/en/language_grammars.html)

[Solarized](http://ethanschoonover.com/solarized)
