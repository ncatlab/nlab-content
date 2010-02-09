+-- {: .standout}
Every wiki needs a sandbox! Just test between the horizontal rules below (`***` in the source) and don't worry about messing things up.
=--


***

Click on the following links to jump to an anchor point.

* [jump to the first anchor point](http://ncatlab.org/nlab/show/Sandbox#anchor1)

* [jump to the second anchor point](http://ncatlab.org/nlab/show/Sandbox#anotheranchor)

Linking to theorems and so forth is even easier.  Make sure you use the **numbered** versions and give each one a label.  For example:

~~~
+-- {: .num_defn #catdef}
###### Definition
A **category** has **objects** and **arrows** subject to some boring rules that I can never be bothered to remember.
=--
~~~

produces:

+-- {: .num_defn #catdef}
###### Definition
A **category** has **objects** and **arrows** subject to some boring rules that I can never be bothered to remember.
=--

The key bit here is the `#catdef`.  That produces the anchor just as in Urs' examples.  We can refer back to this definition using:

~~~
Definition \ref{catdef} is clearly missing something.
~~~

Definition \ref{catdef} is clearly missing something.

One caveat: if you want to use references to numbered definitions and theorems and so forth then **every** _numbered_ definition (etc) has to have a label, even if you don't intend referring back to it.  So if we have Definition 1 and Definition 2, and only intend referring back to Definition 2 then Definition 1 still has to have a label.

This only works with anchors produced in definitions and similar.  So \ref{anotheranchor} doesn't work.

Linking to anchors in other pages is something that maybe ought to go in the HowTo, but perhaps not in [this section](HowTo#svgedit).

***

Here's a little experiment with the totally awesome all-new, all-singing, all-dancing WYSIWYG SVG editor from the totally awesome all-new, all-singing, all-dancing WYSIWIG Jacques Distler:

<svg width="640" height="480" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
  <marker refX="2" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_bk" viewBox="0 0 10 10">
   <path fill="#000" d="m10,0l-10,5l10,5l-5,-5l5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <line marker-end="url(#se_arrow_fw)" fill="none" stroke-width="5" stroke="#000000" id="svg_1" y2="96" x2="366" y1="98" x1="66"/>
  <line fill="none" stroke-width="5" stroke="#000000" id="svg_2" y2="98" x2="360" y1="99" x1="360"/>
  <text transform="rotate(-13.0693, 41.5, 108)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_3" y="117" x="41">A</text>
  <text transform="rotate(12.0948, 386.5, 108)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_4" y="117" x="387">B</text>
  <text transform="rotate(179.415, 205.5, 141)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_5" y="150" x="206">F</text>
  <line marker-end="url(#se_arrow_fw)" fill="none" stroke-width="5" stroke="#000000" id="svg_6" y2="120" x2="67" y1="120" x1="367"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_7" y="85" x="206">G</text>
 </g>
</svg>
***

## XYPic diagrams using CodeCogs

This code here

      <img src="http://latex.codecogs.com/gif.latex?\xymatrix{(f/g)\ar[r]\ar[d]%26A\ar[d]^f\ar[dl]^\alpha\\B\ar[r]_g%26C}"/>

produces this xypic diagram picture:

<center>
<img src="http://latex.codecogs.com/gif.latex?\xymatrix{(f/g)\ar[r]\ar[d]%26A\ar[d]^f\ar[dl]^\alpha\\B\ar[r]_g%26C}" />
</center>


Notice that all the ampersand symbols

      &

that you have in ordinary xypic code have to be replaced (unfortunately) by the symbols


      %26

otherwise the $n$Lab parser gets mixed up.


Another diagram using `\array`:

$$\array{
X&\cong&S^{\Delta^1}_f &\to &Y^{\Delta^1}&\to& S^{\Delta^1}&
\\ &\searrow&\downarrow &Pb &\downarrow&Pb&\downarrow
\\ L_f&\cong &S_{t'} & \to &L'&\to& L & \to & S^{\{1\}} &
\\ &&\downarrow &Pb&\downarrow&Pb&\downarrow&Pb&\downarrow p
\\ &&\Delta^{0} & \to &(\Delta^1)^{\Delta^1} &\to& T^{\Delta^1} & \to & T^{\{1\}}
\\ &&&id&&(f)^{\Delta^1}&&d_1}$$


***

### Fonts

* $\mathcal{A}$


{#anchor1} Here is anchor point number 1!

a

a

a

a

a

a

a

a

a

a

a

a

a

a

a

a

a

a

a


{#anotheranchor} Here is the second anchor point.

b

b

b

b

b

b

b

b

b

b

b
category: meta

[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects &#1513;&#1504;&#1492; &#1496;&#1493;&#1489;&#1492;]