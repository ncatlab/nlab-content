* tic
{:toc}

# Rosetta Stone #

## Tablets from the Unicode Data Bank ##

__Ref.__ [Unicode Data Bank](http://www.sql-und-xml.de/unicode-database/) --- [Online Integer:Hex:Character Conversion Tool](http://www.sql-und-xml.de/unicode-database/online-tools/)

1.  [Math Symbols](http://www.sql-und-xml.de/unicode-database/sm.html)
1.  [Math Operators](http://www.sql-und-xml.de/unicode-database/mathematical-operators.html)
1.  [Math Miscellaneous A](http://www.sql-und-xml.de/unicode-database/miscellaneous-mathematical-symbols-a.html)
1.  [Math Miscellaneous B](http://www.sql-und-xml.de/unicode-database/miscellaneous-mathematical-symbols-b.html)
1.  [Letterlike Symbols](http://www.sql-und-xml.de/unicode-database/letterlike-symbols.html)
1.  [Miscellaneous Symbols](http://www.sql-und-xml.de/unicode-database/miscellaneous-symbols.html)
1.  [General Punctuation](http://www.sql-und-xml.de/unicode-database/general-punctuation.html)
1.  [Open Punctuation](http://www.sql-und-xml.de/unicode-database/ps.html)
1.  [Other Punctuation](http://www.sql-und-xml.de/unicode-database/po.html)
1.  [Close Punctuation](http://www.sql-und-xml.de/unicode-database/pe.html)
1.  [Geometric Shapes](http://www.sql-und-xml.de/unicode-database/geometric-shapes.html)
1.  [Other Symbols](http://www.sql-und-xml.de/unicode-database/so.html)
1.  [Dingbats](http://www.sql-und-xml.de/unicode-database/dingbats.html)

# $\partial$Construction Zone #

## Symbol String Renderings ##

<table align="center" cellpadding="4" cellspacing="0" markdown="1" width="100%">

<caption><font size="+2">$\text{Symbol String Renderings in Various Environments}$</font></caption>

<tr>
<td align="center" style="border-bottom:2px solid black">$\text{Input Symbol String}$</td>

<td align="center" style="border-bottom:2px solid black">$\text{Local Rendering}$</td>

<td align="center" style="border-bottom:2px solid black">
$\array{\text{The Way It Looks In} \\ \text{Windows} \\ \text{Firefox 3.5.4} \\ \text{STIX}}$</td>

<td align="center" style="border-bottom:2px solid black">
$\array{\text{The Way It Looks In} \\ \text{System 2} \\ \text{Browser 2} \\ \text{Fontset 2}}$</td></tr>

<tr>
<td>`A \;\text{:=}\; B`</td>
<td>$A \;\text{:=}\; B$</td>
<td>acceptable</td>
<td>$\ldots$</td></tr>

<tr>
<td>`A \coloneqq B`</td>
<td>$A \coloneqq B$</td>
<td>acceptable</td>
<td>$\ldots$</td></tr>

<tr>
<td>`A \mathrel{:=} B`</td>
<td>$A \mathrel{:=} B$</td>
<td>acceptable</td>
<td>Crappy vertical alignment
<br>using U+003A.</td></tr>

<tr>
<td>`A \mathrel{&#8758;=} B`</td>
<td>$A \mathrel{&#8758;=} B$</td>
<td>kinda cute &mdash;
<br>looks like a planarian</td>
<td>Correct vertical alignment
<br>(too loose horiz. spacing?)
<br>using U+2236.</td></tr>

<tr>
<td>`A \;\text{-\lt}\; B`</td>
<td>$A \;\text{-\lt}\; B$</td>
<td>`A -\lt B`</td>
<td>$\ldots$</td></tr>

<tr>
<td>`A \mathrel{-\lt} B`</td>
<td>$A \mathrel{-\lt} B$</td>
<td>`A -\lt B`</td>
<td>$\ldots$</td></tr>

<tr>
<td>`A \;\text{&amp;#8722;&amp;#60;}\; B`</td>
<td>$A \;\text{&#8722;&#60;}\; B$</td>
<td>not rendering ???</td>
<td>$\ldots$</td></tr>

<tr>
<td>`A \mathrel{&amp;#8722;&amp;#60;} B`</td>
<td>$A \mathrel{&#8722;&#60;} B$</td>
<td>not rendering ???</td>
<td>$\ldots$</td></tr>

<tr>
<td>`A \;\text{&amp;#x2212;&amp;#x003C;}\; B`</td>
<td>$A \;\text{&#x2212;&#x003C;}\; B$</td>
<td>not rendering ???</td>
<td>$\ldots$</td></tr>

<tr>
<td>`A \mathrel{&amp;#x2212;&amp;#x003C;} B`</td>
<td>$A \mathrel{&#x2212;&#x003C;} B$</td>
<td>not rendering ???</td>
<td>$\ldots$</td></tr>

</table>

In my e-POV, the last formulas in the above table are not converting to TeX at all.  I did type that stuff really late last night, but still can't see what's wrong.

Is the HTML context inhibiting something?

Try them in a TeX array ---

$\array{\arrayopts{\colalign{left left}}
`A \:\text{&amp;#8722;&amp;#60;}\: B`
&
A \:\text{&#8722;&#60;}\: B
\\
`A \mathrel{&amp;#8722;&amp;#60;} B`
&
A \mathrel{&#8722;&#60;} B
\\
`A \:\text{&amp;#x2212;&amp;#x003C;}\: B`
&
A \:\text{&#x2212;&#x003C;}\: B
\\
`A \mathrel{&amp;#x2212;&amp;#x003C;} B`
&
A \mathrel{&#x2212;&#x003C;} B
}$

Quotation not working.  Talk about non-reflective!

Try ---

$\array{\arrayopts{\colalign{left left}}
\text{A \:\text{&amp;#8722;&amp;#60;}\: B}
&
A \:\text{&#8722;&#60;}\: B
\\
\text{A \mathrel{&amp;#8722;&amp;#60;} B}
&
A \mathrel{&#8722;&#60;} B
\\
\text{A \:\text{&amp;#x2212;&amp;#x003C;}\: B)
&
A \:\text{&#x2212;&#x003C;}\: B
\\
\text{A \mathrel{&amp;#x2212;&amp;#x003C;} B}
&
A \mathrel{&#x2212;&#x003C;} B
}$

Screw this &hellip;


## Residual Problems with Mathcal ##

* $\mathcal{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
: Firefox 3.5+ with STIX fonts shows only {B, E, F, H, I, L, M, R}
: same with IE and MathPlayer

* $\mathcal{abcdefghijklmnopqrstuvwxyz}$
: Firefox 3.5+ with STIX fonts shows only {e, g, o}
: same with IE and MathPlayer

You don't have the STIX fonts installed correctly --- they are not being used by your browser(s).

I installed what looks like a big list of STIX and also CODE2000 in my fonts folder, and these show up in Character Map.  It looks like I get only the chars in the Unicode 0000 to FFFF range, which things like \mathcal{A} = $\mathcal{A}$ = 01D49C evidently are not.  Does anyone know which STIX file exactly the Mathcal is supposed to be in?  ---[[JA]]

Try getting rid of the Code2000 Fonts. Also see [here](http://golem.ph.utexas.edu/wiki/instiki/show/Browsers)