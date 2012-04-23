# Zen Coding snippets for HTML
# Copyright © 2008–2012 Vadim Makeev, http://pepelsbey.net
# Licensed under MIT license
# 
# Head
# Sections
# Grouping
# Tables
# Forms
# Interactive
# Edits
# Embedded
# Text

## Head • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

doc
<!DOCTYPE html>

html
<html>
	$0
</html>

html5
<!DOCTYPE html>
<html>
<head>
	<title>$1</title>
	<meta charset="utf-8">
</head>
<body>
	$0
</body>
</html>

h5bp
<!DOCTYPE html>
<!--[if lt IE 7]><html class="no-js ie6 oldie"><![endif]-->
<!--[if IE 7]><html class="no-js ie7 oldie"><![endif]-->
<!--[if IE 8]><html class="no-js ie8 oldie"><![endif]-->
<!--[if gt IE 8]><!--><html class="no-js"><!--<![endif]-->
<head>
	<title>$1</title>
	<meta charset="utf-8">
</head>
<body>
	$0
</body>
</html>

head
<head>
	$0
</head>

title
<title>$1</title>

base
<base href="$1">

link
<link$1>

link:css
<link rel="stylesheet" href="${1:screen.css}">

link:ico
<link rel="icon" sizes="${1:16x16}" href="${2:favicon.ico}">

link:ati
<link rel="apple-touch-icon" href="favicon.png">

link:atip
<link rel="apple-touch-icon-precomposed" href="favicon.png">

link:rss
<link rel="alternate" type="application/rss+xml" title="${1:RSS}" href="${2:rss}">

link:atom
<link rel="alternate" type="application/atom+xml" title="${1:Atom}" href="${2:atom}">

meta
<meta$1>

meta:utf
<meta charset="utf-8">

meta:win
<meta charset="win-1251">

meta:desc
<meta name="description" content="$1">

meta:key
<meta name="keywords" content="$1">

meta:comp
<meta http-equiv="x-ua-compatible" content="${1:ie=edge}">

meta:chrome
<meta http-equiv="x-ua-compatible" content="${1:chrome=1}">

meta:view
<meta name="viewport" content="${1:width=device-width}">

style
<style>
	$0
</style>

script
<script>
	$0
</script>

script:src
<script src="${1:script.js}"></script>

script:jq
<script src="//code.jquery.com/jquery-${1:latest}.min.js"></script>

script:jqg
<script src="//ajax.googleapis.com/ajax/libs/jquery/${1:1.6.2}/jquery.min.js"></script>

script:jqy
<script src="//yandex.st/jquery/${1:1.6.2}/jquery.min.js"></script>

noscript
<noscript>
	$0
</noscript>

cc:ie
<!--[if IE]>
	$0
<![endif]-->

cc:lt
<!--[if lt IE ${1:6}]>
	$0
<![endif]-->

cc:lte
<!--[if lte IE ${1:6}]>
	$0
<![endif]-->

cc:gt
<!--[if gt IE ${1:6}]>
	$0
<![endif]-->

cc:gte
<!--[if gte IE ${1:6}]>
	$0
<![endif]-->

cc:noie
<!--[if !IE]><!-->
	$0
<!--<![endif]-->

## Sections • • • • • • • • • • • • • • • • • • • • • • • • • • • •

body
<body>
	$0
</body>

article
<article>
	$0
</article>

nav
<nav>
	$0
</nav>

aside
<aside>
	$0
</aside>

section
<section>
	$0
</section>

header
<header>
	$0
</header>

footer
<footer>
	$0
</footer>

h
<h${1:1}>$2</h${1}>

h1
<h1>$1</h1>

h2
<h2>$1</h2>

h3
<h3>$1</h3>

h4
<h4>$1</h4>

h5
<h5>$1</h5>

h6
<h6>$1</h6>

hgroup
<hgroup>
	$0
</hgroup>

address
<address>
	$0
</address>

## Grouping • • • • • • • • • • • • • • • • • • • • • • • • • • • •

p
<p>$1</p>

hr
<hr>

pre
<pre>
	$0
</pre>

pre+
<pre>
	<code>$1</code>
</pre>

blockquote
<blockquote>
	$0
</blockquote>

ol
<ol>
	$0
</ol>

ol+
<ol>
	<li>$1</li>$0
</ol>

ul
<ul>
	$0
</ul>

ul+
<ul>
	<li>$1</li>$0
</ul>

li
<li>$1</li>

dl
<dl>
	$0
</dl>

dl+
<dl>
	<dt>$1</dt>
	<dd>$2</dd>
</dl>

dt
<dt>$1</dt>

dd
<dd>$1</dd>

figure
<figure>
	$0
</figure>

figure+
<figure>
	<figcaption>$1</figcaption>
	$0
</figure>

figcaption
<figcaption>$1</figcaption>

div
<div>$1</div>

## Tables • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

table
<table>
	$0
</table>

table+
<table>
<tr>
	<td>$1</td>$0
</tr>
</table>

caption
<caption>$1</caption>

thead
<thead>
	$0
</thead>

tbody
<tbody>
	$0
</tbody>

tfoot
<tfoot>
	$0
</tfoot>

tr
<tr>
	$0
</tr>

th
<th>$1</th>

td
<td>$1</td>

col
<col>

colgroup
<colgroup>
	$0
</colgroup>

colgroup+
<colgroup>
	<col>$0
</colgroup>

## Forms  • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

form
<form action="$1">
	$0
</form>

fieldset
<fieldset>
	$0
</fieldset>

legend
<legend>$1</legend>

label
<label for="$1">$2</label>

input
<input type="$1" name="$2">

input:hidden
<input type="hidden" name="$1" value="$2">

input:text
<input type="text" name="$1" value="$2">

input:search
<input type="search" name="$1" value="$2">

input:url
<input type="url" name="$1" value="$2">

input:email
<input type="email" name="$1" value="$2">

input:password
<input type="password" name="$1" value="$2">

input:date
<input type="date" name="$1" value="$2">

input:datetime
<input type="datetime" name="$1" value="$2">

input:datetime-local
<input type="datetime-local" name="$1" value="$2">

input:month
<input type="month" name="$1" value="$2">

input:week
<input type="week" name="$1" value="$2">

input:time
<input type="time" name="$1" value="$2">

input:number
<input type="number" name="$1" value="$2">

input:range
<input type="range" name="$1" value="$2">

input:color
<input type="color" name="$1" value="$2">

input:checkbox
<input type="checkbox" name="$1" value="$2"${3: checked}>

input:radio
<input type="radio" name="$1" value="$2"${3: checked}>

input:file
<input type="file" name="$1" value="$2"${3: multiple}>

input:submit
<input type="submit" value="$1">

input:image
<input type="image" src="$1" alt="$2">

input:reset
<input type="reset" value="$1">

input:button
<input type="button" value="$1">

button
<button>$1</button>

select
<select>
	$0
</select>

select+
<select>
	<option name="$1">$2</option>$0
</select>

datalist
<datalist>
	$0
</datalist>

datalist+
<datalist>
	<option label="$1" value="$2">$0
</datalist>

optgroup
<optgroup>
	$0
</optgroup>

option
<option name="$1">$2</option>

textarea
<textarea name="$1" cols="${2:20}" rows="${3:10}">$4</textarea>

keygen
<keygen name="$1">

output
<output name="$1" for="$2">$3</output>

progress
<progress name="$1" value="$2">

meter
<meter name="$1" value="$2">

## Interactive  • • • • • • • • • • • • • • • • • • • • • • • • • •

details
<details>
	$0
</details>

details+
<details>
	<summary>$1</summary>
	$0
</details>

summary
<summary>$1</summary>

menu
<menu type="$1">
	$0
</menu>

command
<command type="$1" label="$2">$1</command>

## Edits  • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

del
<del${1: datetime="$2"}>$3</del>

ins
<ins${1: datetime="$2"}>$3</ins>

## Embedded • • • • • • • • • • • • • • • • • • • • • • • • • • • •

img
<img src="$1" alt="$2">

iframe
<iframe src="$1" height="$2" width="$3"></iframe>

embed
<embed src="$1">

object
<object data="$1" type="$2">
	$0
</object>

param
<param name="$1" value="$2">

video
<video${1: src="$2"}${3: controls}>$4</video>

video+
<video width="${1:640}" height="${2:480}"${3: controls}>
	<source src="${4:video}.mp4" type="video/mp4">
	<source src="$4.webm" type="video/webm">
	<source src="$4.ogv" type="video/ogg">
</video>

audio
<audio${1: src="$2"}${3: controls}>$4</audio>

audio+
<audio${1: controls}>
	<source src="${2:audio}.mp3" type="audio/mpeg">
	<source src="$2.ogg" type="audio/ogg">
</audio>

source
<source src="$1" type="$2">

track
<track src="$1" label="$4">

canvas
<canvas id="${1:canvas}" width="${2:640}" height="${3:480}"></canvas>

map
<map name="$1">
	$0
</map>

map+
<map name="$1">
	<area href="$2" shape="${3:rect}" coords="$4" alt="$5">
</map>

area
<area href="$1" shape="$2" coords="$3" alt="$4">

## Text • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

a
<a href="$1">$2</a>

a:link
<a href="${1:http://}">$2</a>

a:mail
<a href="${1:mailto:}">$2</a>

em
<em>$1</em>

strong
<strong>$1</strong>

i
<i>$1</i>

b
<b>$1</b>

u
<u>$1</u>

s
<s>$1</s>

small
<small>$1</small>

abbr
<abbr>$1</abbr>

q
<q>$1</q>

cite
<cite>$1</cite>

dfn
<dfn>$1</dfn>

sub
<sub>$1</sub>

sup
<sup>$1</sup>

time
<time>$1</time>

code
<code>$1</code>

kbd
<kbd>$1</kbd>

samp
<samp>$1</samp>

var
<var>$1</var>

mark
<mark>$1</mark>

bdi
<bdi>$1</bdi>

bdo
<bdo>$1</bdo>

ruby
<ruby>$1</ruby>

rt
<rt>$1</rt>

rp
<rp>$1</rp>

span
<span>$1</span>

br
<br>

wbr
<wbr>$1</wbr>