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

HTML5 template by `html`

```html
<!DOCTYPE html>
<html>
<head>
	<title>$1</title>
	<meta charset="UTF-8">
</head>
<body>
	$0
</body>
</html>
```

jQuery include by `script:jq`

```html
<script src="//code.jquery.com/jquery-${1:latest}.min.js"></script>
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

Cross-browser gradient by `bgi:lg`

```css
background-image:-webkit-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%});
background-image:-moz-linear-gradient($1, $2 $3, $4 $5);
background-image:-ms-linear-gradient($1, $2 $3, $4 $5);
background-image:-o-linear-gradient($1, $2 $3, $4 $5);
background-image:linear-gradient($1, $2 $3, $4 $5);
```

Cross-browser transition by `tr=`

```css
-webkit-transition:${1:all} ${2:linear} ${3:1s};
-moz-transition:$1 $2 $3;
-ms-transition:$1 $2 $3;
-o-transition:$1 $2 $3;
transition:$1 $2 $3;
```