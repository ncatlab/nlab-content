+-- {: .standout}
Every wiki needs a sandbox! Just test between the horizontal rules below (`***` in the source) and don't worry about messing things up.
=--


***

Click on the following links to jump to an anchor point.  Of course, the same syntax works when linking to different pages, just replace "Sandbox" with the name of that page.

* [jump to the first anchor point](/nlab/show/Sandbox#anchor1)

* [jump to the second anchor point](/nlab/show/Sandbox#anotheranchor)

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

This only works with anchors produced in definitions and similar.  So \ref{anotheranchor} doesn't work.  The converse, however, does work: we can use a link [like this](/nlab/show/Sandbox#catdef) to point to the above definition.  This also works from a different wiki page.

Now trying references to equations:

\[
\label{foo}
x^2 + y^2 = z^2
\]

We should be able to refer to equation \eqref{foo} explicitly, or to (eq:foo) if not.

But what if our equation is empty, like this?

\[\label{bar}\]

Can we still refer to it via \eqref{bar} or (eq:bar)?

Can we add anchors to pictures?

![n](n.png){#npic}

So we should now jump to [that pic](#npic)!

***

Here's a little experiment with the totally awesome all-new, all-singing, all-dancing WYSIWYG SVG editor from the totally awesome all-new, all-singing, all-dancing WYSIWIG Jacques Distler:

<svg width="359" height="83" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
  <marker viewBox="0 0 10 10" id="se_arrow_bk" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="2">
   <path d="m10,0l-10,5l10,5l-5,-5l5,-5z" fill="#000"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <line x1="31.449219" y1="31" x2="331.449219" y2="29" id="svg_1" stroke="#000000" stroke-width="5" fill="none" marker-end="url(#se_arrow_fw)"/>
  <line x1="325.449219" y1="32" x2="325.449219" y2="31" id="svg_2" stroke="#000000" stroke-width="5" fill="none"/>
  <text x="6.44922" y="50" id="svg_3" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve" transform="rotate(-13.0693, 6.94922, 41)">A</text>
  <text x="352.449" y="50" id="svg_4" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve" transform="rotate(12.0948, 351.949, 41)">B</text>
  <text x="171.449" y="83" id="svg_5" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve" transform="rotate(179.415, 170.949, 74)">F</text>
  <line x1="332.449219" y1="53" x2="32.449219" y2="53" id="svg_6" stroke="#000000" stroke-width="5" fill="none" marker-end="url(#se_arrow_fw)"/>
  <text x="171.449" y="18" id="svg_7" fill="#000000" stroke="#000000" stroke-width="0" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">G</text>
 </g>
</svg>

<img src="http://latex.codecogs.com/gif.latex?$$%20\xymatrix@R=23pt@C=12pt{%20%26E_\Sigma%20\ar[rr]^{E_\mathrm{out}}%20\ar[dd]_{E_\mathrm{in}}%20\ar[ddr]%20%26%26%20E_{\Sigma_{\mathrm{out}}}%20\ar[ddr]%20\\%20\\%20%26E_{\mathrm{in}}%20\ar[ddr]%20%26%20[\Sigma,X]%20\ar[dd]^{\mathrm{in}}%20\ar[rr]^{\mathrm{out}}%20\ar[ddrr]%20%26%26%20[\Sigma_{\mathrm{out}},X]%20\ar[dd]%20\ar@/^1pc/[rrdddd]^{\exp(S_\nabla)|_{\Sigma_\mathrm{out}}}%20\\%20\\%20%26%26%20[\Sigma_{\mathrm{in}},X]%20\ar[rr]%20\ar@/_1pc/[ddrrrr]_{\exp(S_\nabla)|_{\Sigma_\mathrm{in}}}%20%26%26%20\mathrm{Bord}(X)%20\ar[ddrr]|{\exp(S_\nabla)}%20\\%20\\%20%26%26%26%26%20%26%26%20V%20}%20$$" title="$$ \xymatrix@R=23pt@C=12pt{ &amp;E_\Sigma \ar[rr]^{E_\mathrm{out}} \ar[dd]_{E_\mathrm{in}} \ar[ddr] &amp;&amp; E_{\Sigma_{\mathrm{out}}} \ar[ddr] \\ \\ &amp;E_{\mathrm{in}} \ar[ddr] &amp; [\Sigma,X] \ar[dd]^{\mathrm{in}} \ar[rr]^{\mathrm{out}} \ar[ddrr] &amp;&amp; [\Sigma_{\mathrm{out}},X] \ar[dd] \ar@/^1pc/[rrdddd]^{\exp(S_\nabla)|_{\Sigma_\mathrm{out}}} \\ \\ &amp;&amp; [\Sigma_{\mathrm{in}},X] \ar[rr] \ar@/_1pc/[ddrrrr]_{\exp(S_\nabla)|_{\Sigma_\mathrm{in}}} &amp;&amp; \mathrm{Bord}(X) \ar[ddrr]|{\exp(S_\nabla)} \\ \\ &amp;&amp;&amp;&amp; &amp;&amp; V } $$" />

<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="10" markerWidth="10" markerUnits="strokeWidth" refY="5" id="se_arrow_fw" viewBox="0 0 10 10">
   <path fill="#000000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <foreignObject height="24" width="24" font-size="24" id="svg_1" y="61" x="53">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <msub>
     <mi>E</mi>
     <mi>&#931;</mi>
    </msub>
   </math>
  </foreignObject>
  <foreignObject height="24" width="48" font-size="24" id="svg_2" y="62" x="174.59999">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <msub>
     <mi>E</mi>
     <mrow>
      <msub>
       <mi>&#931;</mi>
       <mtext>out</mtext>
      </msub>
     </mrow>
    </msub>
   </math>
  </foreignObject>
  <foreignObject height="24" width="24" font-size="24" id="svg_3" y="161" x="58">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <msub>
     <mi>E</mi>
     <mtext>in</mtext>
    </msub>
   </math>
  </foreignObject>
  <foreignObject height="24" width="77" font-size="24" id="svg_4" y="145" x="112.625">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mo stretchy="false">[</mo>
    <mi>&#931;</mi>
    <mo>,</mo>
    <mi>X</mi>
    <mo stretchy="false">]</mo>
   </math>
  </foreignObject>
  <foreignObject height="24" width="88" font-size="24" id="svg_5" y="146" x="235.40069">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mo stretchy="false">[</mo>
    <msub>
     <mi>&#931;</mi>
     <mtext>out</mtext>
    </msub>
    <mo>,</mo>
    <mi>X</mi>
    <mo stretchy="false">]</mo>
   </math>
  </foreignObject>
  <foreignObject height="24" width="90" font-size="24" id="svg_6" y="246" x="112">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mo stretchy="false">[</mo>
    <msub>
     <mi>&#931;</mi>
     <mtext>in</mtext>
    </msub>
    <mo>,</mo>
    <mi>X</mi>
    <mo stretchy="false">]</mo>
   </math>
  </foreignObject>
  <foreignObject height="24" width="90" font-size="24" id="svg_7" y="250" x="247">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mo lspace="0em" rspace="thinmathspace">Bord</mo>
    <mo stretchy="false">(</mo>
    <mi>X</mi>
    <mo stretchy="false">)</mo>
   </math>
  </foreignObject>
  <foreignObject height="24" width="24" font-size="24" id="svg_8" y="349" x="400">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mo>V</mo>
   </math>
  </foreignObject>
 </g>
 <g>
  <title>Layer 2</title>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="93" y1="80" x2="171" y2="80" id="svg_24" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="67" y1="97" x2="67" y2="164" id="svg_25" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="81" y1="95" x2="128" y2="145" id="svg_26" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="188" y1="163" x2="230" y2="163" id="svg_27" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="150" y1="180" x2="150" y2="248" id="svg_28" fill="none"/>
  <line x1="184" y1="180" x2="246" y2="252" id="svg_29" fill="none" marker-end="url(#se_arrow_fw1)"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="281" y1="184" x2="281" y2="248" id="svg_30" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="199" y1="266" x2="244" y2="266" id="svg_31" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="87" y1="198" x2="119" y2="246" id="svg_32" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="224" y1="100" x2="264" y2="144" id="svg_33" fill="none"/>
  <line marker-end="url(#se_arrow_fw)" stroke="#000000" x1="314" y1="283" x2="396" y2="353" id="svg_34" fill="none"/>
  <path marker-end="url(#se_arrow_fw)" stroke="#000000" fill="none" d="m315,181c65,51 83,75 92,164" id="svg_35"/>
  <path marker-end="url(#se_arrow_fw)" stroke="#000000" fill="none" d="m162,281c67,70 143,83 230,83" id="svg_36"/>
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
[[!redirects שנה טובה]]