# Zen Coding Snippets

HTML and CSS snippets for [Zen Coding](https://github.com/sergeche/zen-coding) project.

Special repository for creating new snippets and polishing old ones. Syntax of the snippets is compatible with [TextMate snippets](http://manual.macromates.com/en/snippets).

Bug reports and suggestions [are welcome](https://github.com/pepelsbey/zen-coding-snippets/issues).

## HTML

Example: `video+` will be expanded into

```html
<video width="${1:640}" height="${2:480}"${3: controls}>
	<source src="${4:video}.mp4" type="video/mp4">
	<source src="$4.webm" type="video/webm">
	<source src="$4.ogv" type="video/ogg">
</video>
```

## CSS

Example: `@f+` will be expanded into

```css
@font-face {
	font-family:${1:FontFamily};
	src:url(${2:font}.eot);
	src:
		url($2.eot?iefix) format('eot'),
		url($2.woff) format('woff'),
		url($2.ttf) format('truetype'),
		url($2.svg#$2) format('svg');
	}
```