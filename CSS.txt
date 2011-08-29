# Zen Coding snippets for CSS
# Copyright © 2008–2011 Vadim Makeev, http://pepelsbey.net
# Licensed under MIT license

- @rules
- Pseudo
- Special
- Positioning
- Block
- Dimensions
- Colors
- Content
- Text
- Visual
- Layout
- Document

## @rules • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

@c
@charset 'utf-8';

@n
@namespace '$1';

@i
@import url($1);

### Media

@m
@media {
	$1
	}

@m:a
@media all and $1 {
	$2
	}

@m:s
@media screen and $1 {
	$2
	}

@m:p
@media print and $1 {
	$2
	}

### Font

@f
@font-face {
	font-family:$1;
	src:local($2), url($3) format($4);
	}

@f+
@font-face {
	font-family:${1:FontFamily};
	src:url(${2:font}.eot);
	src:
		url($2.eot?iefix) format('eot'),
		url($2.woff) format('woff'),
		url($2.ttf) format('truetype'),
		url($2.svg#$2) format('svg');
	}

### Keyframes

@k
@keyframes ${1:name} {
	$2
	}

@k:w
@-webkit-keyframes ${1:name} {
	$2
	}

@k:m
@-moz-keyframes ${1:name} {
	$2
	}

@k:o
@-o-keyframes ${1:name} {
	$2
	}

### Page

@p
@page {
	$1
	}

@v
@viewport {
	$1
	}

@v:o
@-o-viewport {
	$1
	}

## Pseudo • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

:r
:root

:fc
:first-child

:lc
:last-child

:fot
:first-of-type

:lot
:last-of-type

:oc
:only-child

:oot
:only-of-type

:em
:empty

:l
:link

:v
:visited

:a
:active

:h
:hover

:f
:focus

:t
:target

:en
:enabled

:di
:disabled

:ch
:checked

:fli
:first-line

:fle
:first-letter

:be
:before

:af
:after

:ln
:lang($1)

:nc
:nth-child($1)

:nlc
:nth-last-child($1)

:not
:nth-of-type($1)

:nlot
:nth-last-of-type($1)

:n
:not($1)

:s
::selection

:sm
::-moz-selection

## Special  • • • • • • • • • • • • • • • • • • • • • • • • • • • •

u
url($1)

e
expression($1)

fi
filter:$1;

!
!important

## Positioning  • • • • • • • • • • • • • • • • • • • • • • • • • •

### Position

pos
position:$1;

pos:s
position:static;

pos:a
position:absolute;

pos:r
position:relative;

pos:f
position:fixed;

### Top

t
top:${1:0};

t:a
top:auto;

### Right

r
right:${1:0};

r:a
right:auto;

### Bottom

b
bottom:${1:0};

b:a
bottom:auto;

### Left

l
left:${1:0};

l:a
left:auto;

### Z-Index

z
z-index:$1;

z:a
z-index:auto;

## Block  • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

### Float

fl
float:$1;

fl:n
float:none;

fl:l
float:left;

fl:r
float:right;

### Clear

cl
clear:$1;

cl:n
clear:none;

cl:l
clear:left;

cl:r
clear:right;

cl:b
clear:both;

### Display

d
display:$1;

d:n
display:none;

d:i
display:inline;

d:b
display:block;

d:ib
display:inline-block;

d:li
display:list-item;

d:ri
display:run-in;

d:c
display:compact;

d:f
display:flexbox;

d:if
display:inline-flexbox;

d:it
display:inline-table;

d:tca
display:table-caption;

d:tco
display:table-column;

d:tcg
display:table-column-group;

d:thg
display:table-header-group;

d:tfg
display:table-footer-group;

d:tr
display:table-row;

d:trg
display:table-row-group;

d:tc
display:table-cell;

### Visibility

v
visibility:$1;

v:v
visibility:visible;

v:h
visibility:hidden;

v:c
visibility:collapse;

### Overflow

ov
overflow:$1;

ov:v
overflow:visible;

ov:h
overflow:hidden;

ov:s
overflow:scroll;

ov:a
overflow:auto;

ovx
overflow-x:$1;

ovx:v
overflow-x:visible;

ovx:h
overflow-x:hidden;

ovx:s
overflow-x:scroll;

ovx:a
overflow-x:auto;

ovx:ms
-ms-overflow-x:$1;

ovy
overflow-y:$1;

ovy:v
overflow-y:visible;

ovy:h
overflow-y:hidden;

ovy:s
overflow-y:scroll;

ovy:a
overflow-y:auto;

ovy:ms
-ms-overflow-y:$1;

### Clip

cp
clip:$1;

cp:a
clip:auto;

cp:r
clip:rect(${1:0} ${2:0} ${3:0} ${4:0});

### Box-Sizing

bs
box-sizing:$1;

bs:cb
box-sizing:content-box;

bs:bb
box-sizing:border-box;

### Flex

fxd
flex-direction:$1;

fxd:lr
flex-direction:lr;

fxd:rl
flex-direction:rl;

fxd:tb
flex-direction:tb;

fxd:bt
flex-direction:bt;

fxd:i
flex-direction:inline;

fxd:ir
flex-direction:inline-reverse;

fxd:b
flex-direction:block;

fxd:br
flex-direction:block-reverse;

fxo
flex-order:$1;

fxp
flex-pack:$1;

fxp:s
flex-pack:start;

fxp:e
flex-pack:end;

fxp:c
flex-pack:center;

fxp:j
flex-pack:justify;

fxa
flex-align:$1;

fxa:a
flex-align:auto;

fxa:b
flex-align:baseline;

## Dimensions • • • • • • • • • • • • • • • • • • • • • • • • • • •

### Margin

m
margin:${1:0};

m:a
margin:auto;

m:2
margin:${1:0} ${2:0};

m:3
margin:${1:0} ${2:0} ${3:0};

m:4
margin:${1:0} ${2:0} ${3:0} ${4:0};

mt
margin-top:${1:0};

mt:a
margin-top:auto;

mr
margin-right:${1:0};

mr:a
margin-right:auto;

mb
margin-bottom:${1:0};

mb:a
margin-bottom:auto;

ml
margin-left:${1:0};

ml:a
margin-left:auto;

### Padding

p
padding:${1:0};

p:2
padding:${1:0} ${2:0};

p:3
padding:${1:0} ${2:0} ${3:0};

p:4
padding:${1:0} ${2:0} ${3:0} ${4:0};

pt
padding-top:${1:0};

pr
padding-right:${1:0};

pb
padding-bottom:${1:0};

pl
padding-left:${1:0};

### Min-Max

miw
min-width:${1:0};

mih
min-height:${1:0};

maw
max-width:${1:0};

maw:n
max-width:none;

mah
max-height:${1:0};

mah:n
max-height:none;

### Width-Height

w
width:${1:0};

w:a
width:auto;

w:dw
width:device-width;

h
height:${1:0};

h:a
height:auto;

h:dh
height:device-height;

## Colors • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

### Outline

o
outline:$1;

o:n
outline:none;

o+
outline:${1:1px} ${2:dotted} ${3:#000};

ow
outline-width:${1:1px};

os
outline-style:${1:dotted};

os:n
outline-style:none;

oc
outline-color:${1:#000};

oc:i
outline-color:invert;

oo
outline-offset:$1;

### Border

bd
border:$1;

bd:n
border:none;

bd+
border:${1:1px} ${2:solid} ${3:#000};

bdcl
border-collapse:$1;

bdcl:c
border-collapse:collapse;

bdcl:s
border-collapse:separate;

### Border-Width

bdw
border-width:${1:1px};

bdw:2
border-width:${1:1px} ${2:1px};

bdw:3
border-width:${1:1px} ${2:1px} ${3:1px};

bdw:4
border-width:${1:1px} ${2:1px} ${3:1px} ${4:1px};

### Border-Style

bds
border-style:$1;

bds:n
border-style:none;

bds:h
border-style:hidden;

bds:dt
border-style:dotted;

bds:ds
border-style:dashed;

bds:s
border-style:solid;

bds:db
border-style:double;

bds:g
border-style:groove;

bds:r
border-style:ridge;

bds:i
border-style:inset;

bds:o
border-style:outset;

### Border-Color

bdc
border-color:${1:#000};

### Border-Top

bdt
border-top:$1;

bdt:n
border-top:none;

bdt+
border-top:${1:1px} ${2:solid} ${3:#000};

bdtw
border-top-width:${1:1px};

bdts
border-top-style:${1:solid};

bdts:n
border-top-style:none;

bdtc
border-top-color:${1:#000};

### Border-Right

bdr
border-right:$1;

bdr:n
border-right:none;

bdr+
border-right:${1:1px} ${2:solid} ${3:#000};

bdrw
border-right-width:${1:1px};

bdrs
border-right-style:${1:solid};

bdrs:n
border-right-style:none;

bdrc
border-right-color:${1:#000};

### Border-Bottom

bdb
border-bottom:$1;

bdb:n
border-bottom:none;

bdb+
border-bottom:${1:1px} ${2:solid} ${3:#000};

bdbw
border-bottom-width:${1:1px};

bdbs
border-bottom-style:${1:solid};

bdbs:n
border-bottom-style:none;

bdbc
border-bottom-color:${1:#000};

### Border-Left

bdl
border-left:$1;

bdl:n
border-left:none;

bdl+
border-left:${1:1px} ${2:solid} ${3:#000};

bdlw
border-left-width:${1:1px};

bdls
border-left-style:${1:solid};

bdls:n
border-left-style:none;

bdlc
border-left-color:${1:#000};

### Border-Radius

bdrz
border-radius:$1;

bdrz=
-webkit-border-radius:$1;
-moz-border-radius:$1;
border-radius:$1;

bdtrrz
border-top-right-radius:$1;

bdbrrz
border-bottom-right-radius:$1;

bdblrz
border-bottom-left-radius:$1;

bdtlrz
border-top-left-radius:$1;

### Border-Image

bdi
border-image:$1;

bdi:n
border-image:none;

bdi+
border-image:url($1) ${2:0} ${3:repeat};

bdi=
-webkit-border-image:url($1) ${2:0} ${3:repeat};
-moz-border-image:url($1) $2 $3;
-o-border-image:url($1) $2 $3;
border-image:url($1) $2 $3;

### Border-Image-Source

bdisr
border-image-source:url($1);

bdisr:n
border-image-source:none;

### Border-Image-Slice

bdisl
border-image-slice:$1;

bdisl:0
border-image-slice:${1:0};

bdisl:2
border-image-slice:${1:0} ${2:0};

bdisl:3
border-image-slice:${1:0} ${2:0} ${3:0};

bdisl:4
border-image-slice:${1:0} ${2:0} ${3:0} ${4:0};

bdisl:f
border-image-slice:fill;

### Border-Image-Width

bdiw
border-image-width:${1:0};

bdiw:2
border-image-width:${1:0} ${2:0};

bdiw:3
border-image-width:${1:0} ${2:0} ${3:0};

bdiw:4
border-image-width:${1:0} ${2:0} ${3:0} ${4:0};

bdiw:a
border-image-width:auto;

### Border-Image-Outset

bdio
border-image-outset:$1;

bdio:0
border-image-outset:${1:0};

bdio:2
border-image-outset:${1:0} ${2:0};

bdio:3
border-image-outset:${1:0} ${2:0} ${3:0};

bdio:4
border-image-outset:${1:0} ${2:0} ${3:0} ${4:0};

### Border-Image-Repeat

bdir
border-image-repeat:$1;

bdir:st
border-image-repeat:stretch;

bdir:re
border-image-repeat:repeat;

bdir:ro
border-image-repeat:round;

bdir:sp
border-image-repeat:space;

### Background

bg
background:$1;

bg:n
background:none;

bg+
background:${1:#FFF} ${2:url($3)} ${4:0} ${5:0} ${6:no-repeat};

bg:ief
filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(src='$1', sizingMethod='${2:crop}');

### Bg-Color

bgc
background-color:${1:#FFF};

bgc:t
background-color:transparent;

### Bg-Image

bgi
background-image:url($1);

### Bg-Image-Gradients

bgi:lg
background-image:-webkit-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%});
background-image:-moz-linear-gradient($1, $2 $3, $4 $5);
background-image:-ms-linear-gradient($1, $2 $3, $4 $5);
background-image:-o-linear-gradient($1, $2 $3, $4 $5);
background-image:linear-gradient($1, $2 $3, $4 $5);

bgi:rlg
background-image:-webkit-repeating-linear-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%});
background-image:-moz-repeating-linear-gradient($1, $2 $3, $4 $5);
background-image:-ms-repeating-linear-gradient($1, $2 $3, $4 $5);
background-image:-o-repeating-linear-gradient($1, $2 $3, $4 $5);
background-image:repeating-linear-gradient($1, $2 $3, $4 $5);

bgi:rg
background-image:-webkit-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%});
background-image:-moz-radial-gradient($1, $2 $3, $4 $5);
background-image:-ms-radial-gradient($1, $2 $3, $4 $5);
background-image:-o-radial-gradient($1, $2 $3, $4 $5);
background-image:radial-gradient($1, $2 $3, $4 $5);

bgi:rrg
background-image:-webkit-repeating-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%});
background-image:-moz-repeating-radial-gradient($1, $2 $3, $4 $5);
background-image:-ms-repeating-radial-gradient($1, $2 $3, $4 $5);
background-image:-o-repeating-radial-gradient($1, $2 $3, $4 $5);
background-image:repeating-radial-gradient($1, $2 $3, $4 $5);

bgi:n
background-image:none;

### Bg-Repeat

bgr
background-repeat:$1;

bgr:r
background-repeat:repeat;

bgr:x
background-repeat:repeat-x;

bgr:y
background-repeat:repeat-y;

bgr:sp
background-repeat:space;

bgr:ro
background-repeat:round;

bgr:n
background-repeat:no-repeat;

### Bg-Attachment

bga
background-attachment:$1;

bga:f
background-attachment:fixed;

bga:l
background-attachment:local;

bga:s
background-attachment:scroll;

### Bg-Position

bgp
background-position:${1:0} ${2:0};

bgpx
background-position-x:$1;

bgpx:ms
-ms-background-position-x:$1;

bgpy
background-position-y:$1;

bgpy:ms
-ms-background-position-y:$1;

### Bg-Clip

bgcp
background-clip:$1;

bgcp:bb
background-clip:border-box;

bgcp:pb
background-clip:padding-box;

bgcp:cb
background-clip:content-box;

### Bg-Origin

bgo
background-origin:$1;

bgo:pb
background-origin:padding-box;

bgo:bb
background-origin:border-box;

bgo:cb
background-origin:content-box;

### Bg-Size

bgz
background-size:$1;

bgz:a
background-size:auto;

bgz:con
background-size:contain;

bgz:cov
background-size:cover;

### Box-Decoration

bdbr
box-decoration-break:$1;

bdbr:s
box-decoration-break:slice;

bdbr:c
box-decoration-break:clone;

### Box-Shadow

bsh
box-shadow:$1;

bsh:n
box-shadow:none;

bsh+
box-shadow:${1:0} ${2:0} ${3:0} ${4:#000};

bsh:i+
box-shadow:${1:0} ${2:0} ${3:0} ${4:#000} ${5:inset};

bsh=
-webkit-box-shadow:${1:0} ${2:0} ${3:0} ${4:#000};
-moz-box-shadow:$1 $2 $3 $4;
box-shadow:$1 $2 $3 $4;

bsh:i=
-webkit-box-shadow:${1:0} ${2:0} ${3:0} ${4:#000} ${5:inset};
-moz-box-shadow:$1 $2 $3 $4 $5;
box-shadow:$1 $2 $3 $4 $5;

### Linear-Gradient

lg
linear-gradient($1)

lg+
linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

lg:w
-webkit-linear-gradient($1)

lg:w+
-webkit-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

lg:m
-moz-linear-gradient($1)

lg:m+
-moz-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

lg:ms
-ms-linear-gradient($1)

lg:ms+
-ms-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

lg:o
-o-linear-gradient($1)

lg:o+
-o-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

lg:ief
filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=${1:#FF000000}, endColorstr=${2:#FFFFFFFF});

lg:msf
-ms-filter:'progid:DXImageTransform.Microsoft.gradient(startColorstr=${1:#FF000000}, endColorstr=${2:#FFFFFFFF});

### Repeating-Linear-Gradient

rlg
repeating-linear-gradient($1)

rlg+
repeating-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rlg:w
-webkit-repeating-linear-gradient($1)

rlg:w+
-webkit-repeating-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rlg:m
-moz-repeating-linear-gradient($1)

rlg:m+
-moz-repeating-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rlg:ms
-ms-repeating-linear-gradient($1)

rlg:ms+
-ms-repeating-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rlg:o
-o-repeating-linear-gradient($1)

rlg:o+
-o-repeating-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

### Radial-Gradient

rg
radial-gradient($1)

rg+
radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

rg:w
-webkit-radial-gradient($1)

rg:w+
-webkit-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

rg:m
-moz-radial-gradient($1)

rg:m+
-moz-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

rg:ms
-ms-radial-gradient($1)

rg:ms+
-ms-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

rg:o
-o-radial-gradient($1)

rg:o+
-o-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%})

### Repeating-Radial-Gradient

rrg
repeating-radial-gradient($1)

rrg+
repeating-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rrg:w
-webkit-repeating-radial-gradient($1)

rrg:w+
-webkit-repeating-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rrg:m
-moz-repeating-radial-gradient($1)

rrg:m+
-moz-repeating-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rrg:ms
-ms-repeating-radial-gradient($1)

rrg:ms+
-ms-repeating-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

rrg:o
-o-repeating-radial-gradient($1)

rrg:o+
-o-repeating-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%})

### Color

c
color:${1:#000};

rgb
rgb(${1:0} ${2:0} ${3:0})

rgba
rgba(${1:0} ${2:0} ${3:0} ${4:1})

hsl
hsl(${1:0} ${2:0} ${3:0})

hsla
hsla(${1:0} ${2:0} ${3:0} ${4:1})

## Content  • • • • • • • • • • • • • • • • • • • • • • • • • • • •

### Table

tl
table-layout:$1;

tl:a
table-layout:auto;

tl:f
table-layout:fixed;

cs
caption-side:$1;

cs:t
caption-side:top;

cs:b
caption-side:bottom;

ec
empty-cells:$1;

ec:s
empty-cells:show;

ec:h
empty-cells:hide;

### List

ls
list-style:$1;

ls:n
list-style:none;

lsp
list-style-position:$1;

lsp:i
list-style-position:inside;

lsp:o
list-style-position:outside;

lst
list-style-type:$1;

lst:n
list-style-type:none;

lst:d
list-style-type:disc;

lst:c
list-style-type:circle;

lst:s
list-style-type:square;

lst:dc
list-style-type:decimal;

lst:dclz
list-style-type:decimal-leading-zero;

lst:lr
list-style-type:lower-roman;

lst:ur
list-style-type:upper-roman;

lsi
list-style-image:url($1);

lsi:n
list-style-image:none;

### Quotes

q
quotes:$1;

q:n
quotes:none;

q:en
quotes:'\201C' '\201D' '\2018' '\2019';

q:ru
quotes:'\00AB' '\00BB' '\201E' '\201C';

### Content

ct
content:$1;

ct:n
content:normal;

ct:oq
content:open-quote;

ct:noq
content:no-open-quote;

ct:cq
content:close-quote;

ct:ncq
content:no-close-quote;

ct:a
content:attr($1);

ct:c
content:counter($1);

ct:cs
content:counters($1);

ct:i
content:icon;

coi
counter-increment:$1;

cor
counter-reset:$1;

## Text • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

wm:ms
-ms-writing-mode:$1;

### Vertical-Align

va
vertical-align:$1;

va:sup
vertical-align:super;

va:t
vertical-align:top;

va:tt
vertical-align:text-top;

va:m
vertical-align:middle;

va:ba
vertical-align:baseline;

va:bo
vertical-align:bottom;

va:tb
vertical-align:text-bottom;

va:sub
vertical-align:sub;

### Text-Align

ta
text-align:$1;

ta:l
text-align:left;

ta:c
text-align:center;

ta:r
text-align:right;

ta:j
text-align:justify;

ta:s
text-align:start;

ta:e
text-align:end;

tal
text-align-last:$1;

tal:a
text-align-last:auto;

tal:l
text-align-last:left;

tal:c
text-align-last:center;

tal:r
text-align-last:right;

tal:j
text-align-last:justify;

tal:ms
-ms-text-align-last:$1;

### Text-Decoration

td
text-decoration:$1;

td:n
text-decoration:none;

td:o
text-decoration:overline;

td:lt
text-decoration:line-through;

td:u
text-decoration:underline;

### Text-Emphasis

te
text-emphasis:$1;

tec
text-emphasis-color:${1:#C00};

tes
text-emphasis-style:$1;

tep
text-emphasis-position:$1;

### Text-Indent

ti
text-indent:$1;

ti:el
text-indent:each-line;

ti:h
text-indent:hanging;

ti:-
text-indent:-9999px;

### Text-Justify

tj
text-justify:$1;

tj:a
text-justify:auto;

tj:iw
text-justify:inter-word;

tj:ii
text-justify:inter-ideograph;

tj:ic
text-justify:inter-cluster;

tj:d
text-justify:distribute;

tj:dal
text-justify:distribute-all-lines;

tj:dcl
text-justify:distribute-center-last;

tj:k
text-justify:kashida;

tj:n
text-justify:newspaper;

tj:t
text-justify:tibetan;

tj:ms
-ms-text-justify:$1;

### Text-Outline

to
text-outline:$1;

to:n
text-outline:none;

to+
text-outline:${1:0} ${2:0} ${3:#000};

### Text-Transform

tt
text-transform:$1;

tt:n
text-transform:none;

tt:c
text-transform:capitalize;

tt:u
text-transform:uppercase;

tt:l
text-transform:lowercase;

tt:f
text-transform:fullwidth;

### Text-Wrap

tw
text-wrap:$1;

tw:n
text-wrap:normal;

tw:no
text-wrap:none;

tw:u
text-wrap:unrestricted;

tw:av
text-wrap:avoid;

### Text-Overflow

tov
text-overflow:$1;

tov:ms
-ms-text-overflow:$1;

tove
text-overflow-ellipsis:$1;

tovm
text-overflow-mode:$1;

tovm:c
text-overflow-mode:clip;

tovm:e
text-overflow-mode:ellipsis;

tovm:ew
text-overflow-mode:ellipsis-word;

### Text-Shadow

tsh
text-shadow:$1;

tsh:n
text-shadow:none;

tsh+
text-shadow:${1:0} ${2:0} ${3:0} ${4:#000};

### Line-Height

lh
line-height:${1:1};

lh:n
line-height:normal;

### White-Space

whs
white-space:$1;

whs:n
white-space:normal;

whs:p
white-space:pre;

whs:nw
white-space:nowrap;

whs:pw
white-space:pre-wrap;

whs:pl
white-space:pre-line;

### Word

wos
word-spacing:$1;

wos:n
word-spacing:normal;

wow
word-wrap:$1;

wow:n
word-wrap:normal;

wow:bw
word-wrap:break-word;

wow:ms
-ms-word-wrap:$1;

wob
word-break:$1;

wob:ms
-ms-word-break:$1;

### Tab

ts
tab-size:$1;

ts:m
-moz-tab-size:$1;

ts:o
-o-tab-size:$1;

### Letter

lts
letter-spacing:$1;

lts:n
letter-spacing:normal;

### Font

f
font:$1;

f+
font:1em Arial, sans-serif;

### Font-weight

fw
font-weight:$1;

fw:n
font-weight:normal;

fw:b
font-weight:bold;

fw:br
font-weight:bolder;

fw:lr
font-weight:lighter;

fw:1
font-weight:100;

fw:2
font-weight:200;

fw:3
font-weight:300;

fw:4
font-weight:400;

fw:5
font-weight:500;

fw:6
font-weight:600;

fw:7
font-weight:700;

fw:8
font-weight:800;

fw:9
font-weight:900;

### Font-Style

fs
font-style:$1;

fs:n
font-style:normal;

fs:i
font-style:italic;

fs:o
font-style:oblique;

### Font-Variant

fv
font-variant:$1;

fv:n
font-variant:normal;

fv:sc
font-variant:small-caps;

### Font-Size-Adjust

fza
font-size-adjust:$1;

fza:n
font-size-adjust:none;

fst
font-stretch:$1;

### Font-Stretch

fst:n
font-stretch:normal;

fst:uc
font-stretch:ultra-condensed;

fst:ec
font-stretch:extra-condensed;

fst:c
font-stretch:condensed;

fst:sc
font-stretch:semi-condensed;

fst:se
font-stretch:semi-expanded;

fst:e
font-stretch:expanded;

fst:ee
font-stretch:extra-expanded;

fst:ue
font-stretch:ultra-expanded;

### Font-Size

fz
font-size:$1;

### Font-Family

ff
font-family:$1;

ff:s
font-family:serif;

ff:ss
font-family:sans-serif;

ff:c
font-family:cursive;

ff:f
font-family:fantasy;

ff:m
font-family:monospace;

## Visual • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

### Opacity

op
opacity:$1;

op:ief
filter:progid:DXImageTransform.Microsoft.Alpha(Opacity=${1:100});

op:msf
-ms-filter:'progid:DXImageTransform.Microsoft.Alpha(Opacity=${1:100})';

### Interpolation-Mode

im:ms
-ms-interpolation-mode:$1;

im:msb
-ms-interpolation-mode:bicubic;

im:msn
-ms-interpolation-mode:nearest-neighbor;

### Resize

r
resize:$1;

r:n
resize:none;

r:b
resize:both;

r:h
resize:horizontal;

r:v
resize:vertical;

### Cursor

cu
cursor:$1;

cu:a
cursor:auto;

cu:d
cursor:default;

cu:n
cursor:none;

cu:cm
cursor:context-menu;

cu:h
cursor:help;

cu:p
cursor:pointer;

cu:pr
cursor:progress;

cu:w
cursor:wait;

cu:c
cursor:cell;

cu:cr
cursor:crosshair;

cu:t
cursor:text;

cu:vt
cursor:vertical-text;

cu:al
cursor:alias;

cu:cp
cursor:copy;

cu:mv
cursor:move;

cu:nd
cursor:no-drop;

cu:na
cursor:not-allowed;

cu:er
cursor:e-resize;

cu:nr
cursor:n-resize;

cu:ner
cursor:ne-resize;

cu:nwr
cursor:nw-resize;

cu:sr
cursor:s-resize;

cu:ser
cursor:se-resize;

cu:swr
cursor:sw-resize;

cu:wr
cursor:w-resize;

cu:ewr
cursor:ew-resize;

cu:nsr
cursor:ns-resize;

cu:neswr
cursor:nesw-resize;

cu:nwser
cursor:nwse-resize;

cu:cor
cursor:col-resize;

cu:ror
cursor:row-resize;

cu:als
cursor:all-scroll;

### Nav

ni
nav-index:$1;

ni:a
nav-index:auto;

nu
nav-up:$1;

nu:a
nav-up:auto;

nr
nav-right:$1;

nr:a
nav-right:auto;

nd
nav-down:$1;

nd:a
nav-down:auto;

nl
nav-left:$1;

nl:a
nav-left:auto;

### Transition

tr
transition:$1;

tr+
transition:${1:all} ${2:linear} ${3:1s};

tr=
-webkit-transition:${1:all} ${2:linear} ${3:1s};
-moz-transition:$1 $2 $3;
-ms-transition:$1 $2 $3;
-o-transition:$1 $2 $3;
transition:$1 $2 $3;

trde
transition-delay:${1:1s};

trde=
-webkit-transition-delay:${1:1s};
-moz-transition-delay:$1;
-ms-transition-delay:$1;
-o-transition-delay:$1;
transition-delay:$1;

trtf
transition-timing-function:$1;

trtf=
-webkit-transition-timing-function:$1;
-moz-transition-timing-function:$1;
-ms-transition-timing-function:$1;
-o-transition-timing-function:$1;
transition-timing-function:$1;

trtf:e
transition-timing-function:ease;

trtf:l
transition-timing-function:linear;

trtf:ei
transition-timing-function:ease-in;

trtf:eo
transition-timing-function:ease-out;

trtf:eio
transition-timing-function:ease-in-out;

trtf:cb
transition-timing-function:cubic-bezier(${1:0}, ${2:0}, ${3:0}, ${4:0});

trdu
transition-duration:${1:1s};

trdu=
-webkit-transition-duration:${1:1s};
-moz-transition-duration:$1;
-ms-transition-duration:$1;
-o-transition-duration:$1;
transition-duration:$1;

trp
transition-property:$1;

trp=
-webkit-transition-property:${1:1s};
-moz-transition-property:$1;
-ms-transition-property:$1;
-o-transition-property:$1;
transition-property:$1;

trp:a
transition-property:all;

trp:a=
-webkit-transition-property:all;
-moz-transition-property:all;
-ms-transition-property:all;
-o-transition-property:all;
transition-property:all;

trp:n
transition-property:none;

trp:n=
-webkit-transition-property:none;
-moz-transition-property:none;
-ms-transition-property:none;
-o-transition-property:none;
transition-property:none;

### Transform

tf
transform:$1;

tf=
-webkit-transform:$1;
-moz-transform:$1;
-ms-transform:$1;
-o-transform:$1;
transform:$1;

tf:mx
transform:matrix(${1:0}, ${2:0}, ${3:0}, ${4:0}, ${5:0}, ${6:0});

tf:mx=
-webkit-transform:matrix(${1:0}, ${2:0}, ${3:0}, ${4:0}, ${5:0}, ${6:0});
-moz-transform:matrix($1, $2, $3, $4, $5, $6);
-ms-transform:matrix($1, $2, $3, $4, $5, $6);
-o-transform:matrix($1, $2, $3, $4, $5, $6);
transform:matrix($1, $2, $3, $4, $5, $6);

tf:mx3
transform:matrix3d(${1:0}, ${2:0}, ${3:0}, ${4:0}, ${5:0}, ${6:0});

tf:mx3=
-webkit-transform:matrix3d(${1:0}, ${2:0}, ${3:0}, ${4:0}, ${5:0}, ${6:0});
-moz-transform:matrix3d($1, $2, $3, $4, $5, $6);
-ms-transform:matrix3d($1, $2, $3, $4, $5, $6);
-o-transform:matrix3d($1, $2, $3, $4, $5, $6);
transform:matrix3d($1, $2, $3, $4, $5, $6);

tf:per
transform:perspective(${1:0});

tf:per=
-webkit-transform:perspective(${1:0});
-moz-transform:perspective($1);
-ms-transform:perspective($1);
-o-transform:perspective($1);
transform:perspective($1);

tf:rt
transform:rotate(${1:45deg});

tf:rt=
-webkit-transform:rotate(${1:45deg});
-moz-transform:rotate($1);
-ms-transform:rotate($1);
-o-transform:rotate($1);
transform:rotate($1);

tf:rtx
transform:rotateX(${1:45deg});

tf:rtx=
-webkit-transform:rotateX(${1:45deg});
-moz-transform:rotateX($1);
-ms-transform:rotateX($1);
-o-transform:rotateX($1);
transform:rotateX($1);

tf:rty
transform:rotateY(${1:45deg});

tf:rty=
-webkit-transform:rotateY(${1:45deg});
-moz-transform:rotateY($1);
-ms-transform:rotateY($1);
-o-transform:rotateY($1);
transform:rotateY($1);

tf:rtz
transform:rotateZ(${1:45deg});

tf:rtz=
-webkit-transform:rotateZ(${1:45deg});
-moz-transform:rotateZ($1);
-ms-transform:rotateZ($1);
-o-transform:rotateZ($1);
transform:rotateZ($1);

tf:sc
transform:scale(${1:0});

tf:sc=
-webkit-transform:scale(${1:0});
-moz-transform:scale($1);
-ms-transform:scale($1);
-o-transform:scale($1);
transform:scale($1);

tf:scx
transform:scaleX(${1:0});

tf:scx=
-webkit-transform:scaleX(${1:0});
-moz-transform:scaleX($1);
-ms-transform:scaleX($1);
-o-transform:scaleX($1);
transform:scaleX($1);

tf:scy
transform:scaleY(${1:0});

tf:scy=
-webkit-transform:scaleY(${1:0});
-moz-transform:scaleY($1);
-ms-transform:scaleY($1);
-o-transform:scaleY($1);
transform:scaleY($1);

tf:scz
transform:scaleZ(${1:0});

tf:scz=
-webkit-transform:scaleZ(${1:0});
-moz-transform:scaleZ($1);
-ms-transform:scaleZ($1);
-o-transform:scaleZ($1);
transform:scaleZ($1);

tf:sk
transform:skew(${1:45deg});

tf:sk=
-webkit-transform:skew(${1:45deg});
-moz-transform:skew($1);
-ms-transform:skew($1);
-o-transform:skew($1);
transform:skew($1);

tf:skx
transform:skewX(${1:45deg});

tf:skx=
-webkit-transform:skewX(${1:45deg});
-moz-transform:skewX($1);
-ms-transform:skewX($1);
-o-transform:skewX($1);
transform:skewX($1);

tf:sky
transform:skewY(${1:45deg});

tf:sky=
-webkit-transform:skewY(${1:45deg});
-moz-transform:skewY($1);
-ms-transform:skewY($1);
-o-transform:skewY($1);
transform:skewY($1);

tf:tl
transform:translate(${1:0}, ${2:0});

tf:tl=
-webkit-transform:translate(${1:0}, ${2:0});
-moz-transform:translate($1, $2);
-ms-transform:translate($1, $2);
-o-transform:translate($1, $2);
transform:translate($1, $2);

tf:tlx
transform:translateX(${1:0});

tf:tlx=
-webkit-transform:translateX(${1:0});
-moz-transform:translateX($1);
-ms-transform:translateX($1);
-o-transform:translateX($1);
transform:translateX($1);

tf:tly
transform:translateY(${1:0});

tf:tly=
-webkit-transform:translateY(${1:0});
-moz-transform:translateY($1);
-ms-transform:translateY($1);
-o-transform:translateY($1);
transform:translateY($1);

tf:tlz
transform:translateZ(${1:0});

tf:tlz=
-webkit-transform:translateZ(${1:0});
-moz-transform:translateZ($1);
-ms-transform:translateZ($1);
-o-transform:translateZ($1);
transform:translateZ($1);

tf:tl3
transform:translate3d(${1:0});

tf:tl3=
-webkit-transform:translate3d(${1:0});
-moz-transform:translate3d($1);
-ms-transform:translate3d($1);
-o-transform:translate3d($1);
transform:translate3d($1);

tfo
transform-origin:${1:0} ${2:0};

tfo=
-webkit-transform-origin:${1:0} ${2:0};
-moz-transform-origin:$1 $2;
-ms-transform-origin:$1 $2;
-o-transform-origin:$1 $2;
transform-origin:$1 $2;

### Animation

an
animation:$1;

an=
-webkit-animation:$1;
-moz-animation:$1;
animation:$1;

ann
animation-name:$1;

ann=
-webkit-animation-name:$1;
-moz-animation-name:$1;
animation-name:$1;

ann:n
animation-name:none;

ann:n=
-webkit-animation-name:none;
-moz-animation-name:none;
animation-name:none;

andu
animation-duration:${1:1s};

andu=
-webkit-animation-duration:${1:1s};
-moz-animation-duration:$1;
animation-duration:$1;

anps
animation-play-state:$1;

anps=
-webkit-animation-play-state:$1;
-moz-animation-play-state:$1;
animation-play-state:$1;

anps:r
animation-play-state:running;

anps:r=
-webkit-animation-play-state:running;
-moz-animation-play-state:running;
animation-play-state:running;

anps:p
animation-play-state:paused;

anps:p=
-webkit-animation-play-state:paused;
-moz-animation-play-state:paused;
animation-play-state:paused;

antf
animation-timing-function:$1;

antf=
-webkit-animation-timing-function:$1;
-moz-animation-timing-function:$1;
animation-timing-function:$1;

ande
animation-delay:${1:1s};

ande=
-webkit-animation-delay:${1:1s};
-moz-animation-delay:$1;
animation-delay:$1;

anic
animation-iteration-count:$1;

anic=
-webkit-animation-iteration-count:$1;
-moz-animation-iteration-count:$1;
animation-iteration-count:$1;

anic:i
animation-iteration-count:infinite;

anic:i=
-webkit-animation-iteration-count:infinite;
-moz-animation-iteration-count:infinite;
animation-iteration-count:infinite;

andi
animation-direction:$1;

andi=
-webkit-animation-direction:$1;
-moz-animation-direction:$1;
animation-direction:$1;

andi:n
animation-direction:normal;

andi:n=
-webkit-animation-direction:normal;
-moz-animation-direction:normal;
animation-direction:normal;

andi:a
animation-direction:alternate;

andi:a=
-webkit-animation-direction:alternate;
-moz-animation-direction:alternate;
animation-direction:alternate;

## Layout • • • • • • • • • • • • • • • • • • • • • • • • • • • • •

### Unicode

ub
unicode-bidi:$1;

ub:n
unicode-bidi:normal;

ub:e
unicode-bidi:embed;

ub:bo
unicode-bidi:bidi-override;

### Direction

dir
direction:$1;

dir:l
direction:ltr;

dir:r
direction:rtl;

### Break

bra
break-after:$1;

bra:a
break-after:auto;

bra:al
break-after:always;

bra:av
break-after:avoid;

bra:l
break-after:left;

bra:r
break-after:right;

bra:p
break-after:page;

bra:c
break-after:column;

bra:avp
break-after:avoid-page;

bra:avc
break-after:avoid-column;

brb
break-before:$1;

brb:a
break-before:auto;

brb:al
break-before:always;

brb:av
break-before:avoid;

brb:l
break-before:left;

brb:r
break-before:right;

brb:p
break-before:page;

brb:c
break-before:column;

brb:avp
break-before:avoid-page;

brb:avc
break-before:avoid-column;

bri
break-inside:$1;

bri:a
break-inside:auto;

bri:av
break-inside:avoid;

bri:avp
break-inside:avoid-page;

bri:avc
break-inside:avoid-column;

### Columns

col
columns:$1 $2;

col=
-webkit-columns:${1:0} ${2:0};
-moz-columns:$1 $2;
columns:$1 $2;

cos
column-span:$1;

cos=
-webkit-column-span:$1;
-moz-column-span:$1;
column-span:$1;

cos:n
column-span:none;

cos:n=
-webkit-column-span:none;
-moz-column-span:none;
column-span:none;

cos:a
column-span:all;

cos:a=
-webkit-column-span:all;
-moz-column-span:all;
column-span:all;

cow
column-width:${1:100px};

cow=
-webkit-column-width:${1:100px};
-moz-column-width:$1;
column-width:$1;

cow:a
column-width:auto;

cow:a=
-webkit-column-width:auto;
-moz-column-width:auto;
column-width:auto;

coc
column-count:$1;

coc=
-webkit-column-count:$1;
-moz-column-count:$1;
column-count:$1;

coc:a
column-count:auto;

coc:a=
-webkit-column-count:auto;
-moz-column-count:auto;
column-count:auto;

cof
column-fill:$1;

cof=
-webkit-column-fill:$1;
-moz-column-fill:$1;
column-fill:$1;

cof:a
column-fill:auto;

cof:a=
-webkit-column-fill:auto;
-moz-column-fill:auto;
column-fill:auto;

cof:b
column-fill:balance;

cof:b=
-webkit-column-fill:balance;
-moz-column-fill:balance;
column-fill:balance;

cog
column-gap:$1;

cog=
-webkit-column-gap:$1;
-moz-column-gap:$1;
column-gap:$1;

cog:n
column-gap:normal;

cog:n=
-webkit-column-gap:normal;
-moz-column-gap:normal;
column-gap:normal;

cor
column-rule:$1;

cor+
column-rule:${1:1px} ${2:solid} ${3:#000};

cor=
-webkit-column-rule:${1:1px} ${2:solid} ${3:#000};
-moz-column-rule:$1 $2 $3;
column-rule:$1 $2 $3;

corc
column-rule-color:${1:#000};

corc=
-webkit-column-rule-color:${1:#000};
-moz-column-rule-color:$1;
column-rule-color:$1;

cors
column-rule-style:${1:solid};

cors=
-webkit-column-rule-style:${1:solid};
-moz-column-rule-style:$1;
column-rule-style:$1;

cors:n
column-rule-style:none;

cors:n=
-webkit-column-rule-style:none;
-moz-column-rule-style:none;
column-rule-style:none;

corw
column-rule-width:${1:1px};

corw=
-webkit-column-rule-width:${1:1px};
-moz-column-rule-width:$1;
column-rule-width:$1;

### Page

pbb
page-break-before:$1;

pbb:a
page-break-before:auto;

pbb:aw
page-break-before:always;

pbb:l
page-break-before:left;

pbb:r
page-break-before:right;

pbi
page-break-inside:$1;

pbi:a
page-break-inside:auto;

pbi:av
page-break-inside:avoid;

pba
page-break-after:$1;

pba:a
page-break-after:auto;

pba:aw
page-break-after:always;

pba:l
page-break-after:left;

pba:r
page-break-after:right;

### Special

orp
orphans:$1;

wid
widows:$1;

## Document • • • • • • • • • • • • • • • • • • • • • • • • • • • •

### Zoom

zo
zoom:$1;

zo:a
zoom:auto;

zo:ms
-ms-zoom:$1;

maz
max-zoom:$1;

maz:a
max-zoom:auto;

miz
min-zoom:$1;

miz:a
min-zoom:auto;

uz
user-zoom:$1;

uz:z
user-zoom:zoom;

uz:f
user-zoom:fixed;

### Orientation

or
orientation:$1;

or:a
orientation:auto;

or:p
orientation:portrait;

or:l
orientation:landscape;