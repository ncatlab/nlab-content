[[!redirects higher order propositions]]

* tic
{:toc}

# Idea #

If functions of type $X \to \mathbb{B}$ are propositions about things in $X$, then functions of type $(X \to \mathbb{B}) \to \mathbb{B}$ are propositions about propositions about things in $X$, the first of a series of __higher order propositions__ based on $X$.

# Higher order propositional expressions #

By way of equipping the discussion with a modicum of concrete material, let's begin with a consideration of higher order propositions and logical operators that stem from the ordinary propositions on 1 and 2 variables.

## Higher order propositions and logical operators $(n = 1)$ ##

A _higher order proposition_ is a proposition about propositions.  If the original order of propositions consists of maps of the form $f : X \to \mathbb{B}$, then the next higher order of propositions consists of maps of the form $m : (X \to \mathbb{B}) \to \mathbb{B}$.  It is often useful to think of a higher order proposition as a _measure_ on propositions.

For example, consider the case where $X = \mathbb{B}$.  Then there are exactly four propositions $f : \mathbb{B} \to \mathbb{B}$, and exactly sixteen higher order propositions that are based on this set, all taking the form $m : (\mathbb{B} \to \mathbb{B}) \to \mathbb{B}$.

Table&#160;1 lists the 16 measures of the form $m : (\mathbb{B} \to \mathbb{B}) \to \mathbb{B}$.

<table align="center" cellpadding="4" cellspacing="0" markdown="1" style="background:white; color:black; text-align:center; width:90%">

<caption><font size="+2">$\text{Table 1.} \:\: \text{Higher Order Propositions} \: (n = 1)$</font></caption>

<tr>
<td style="border-bottom:2px solid black" align="right">$x:$</td>
<td style="border-bottom:2px solid black">$1 \: 0$</td>
<td style="border-bottom:2px solid black; border-right:2px solid black">$f$</td>
<td style="border-bottom:2px solid black">$m_{0}$</td>
<td style="border-bottom:2px solid black">$m_{1}$</td>
<td style="border-bottom:2px solid black">$m_{2}$</td>
<td style="border-bottom:2px solid black">$m_{3}$</td>
<td style="border-bottom:2px solid black">$m_{4}$</td>
<td style="border-bottom:2px solid black">$m_{5}$</td>
<td style="border-bottom:2px solid black">$m_{6}$</td>
<td style="border-bottom:2px solid black">$m_{7}$</td>
<td style="border-bottom:2px solid black">$m_{8}$</td>
<td style="border-bottom:2px solid black">$m_{9}$</td>
<td style="border-bottom:2px solid black">$m_{10}$</td>
<td style="border-bottom:2px solid black">$m_{11}$</td>
<td style="border-bottom:2px solid black">$m_{12}$</td>
<td style="border-bottom:2px solid black">$m_{13}$</td>
<td style="border-bottom:2px solid black">$m_{14}$</td>
<td style="border-bottom:2px solid black">$m_{15}$</td></tr>

<tr>
<td>$f_{0}$</td>
<td>$0 \: 0$</td>
<td style="border-right:2px solid black">$\text{&#x2997; &#x2998;}$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{1}$</td>
<td>$0 \: 1$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} x \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{2}$</td>
<td>$1 \: 0$</td>
<td style="border-right:2px solid black">$x$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{3}$</td>
<td>$1 \: 1$</td>
<td style="border-right:2px solid black">$\text{&#x2997;&#x2997; &#x2998;&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td></tr>

</table>

The contents of Table&nbsp;1 are organized as follows.  Columns&nbsp;1 and 2 form a truth table for the four propositions of the form $f : \mathbb{B} \to \mathbb{B}$, with the row leaders in Column&nbsp;1 displaying the names of the functions $f_i$ for $i$ = 0 to 3, while the entries in Column&nbsp;2 give the values of each function for the argument values that are listed in the corresponding column head.  Column&nbsp;3 displays a more or less canonical expression for the proposition in question.  The last sixteen columns are topped by a collection of conventional names for the measures $m_j$ as $j$ ranges from 0 to 15, where the entries in the body of the Table record the values assigned to each $f_i$ by each $m_j$.

Table&nbsp;2 presents a sample of _interpretive categories_ for higher order propositions of type $(\mathbb{B}^1 \to \mathbb{B}) \to \mathbb{B}$, but it's best to put off discussing this Table further until we get beyond the 1-dimensional case.  These lower dimensional cases tend to be extremely _condensed_ or _degenerate_ in their structures, and the pattern of what's going on here can be set in higher relief as soon as we get even two logical variables to play off each other.

<table align="center" cellpadding="4" cellspacing="0" markdown="1" style="text-align:center; width:90%">

<caption><font size="+2">$\text{Table 2.} \:\: \text{Interpretive Categories for Higher Order Propositions} \: (n = 1)$</font></caption>

<tr>
<td style="border-bottom:2px solid black; border-right:2px solid black">Measure</td>
<td style="border-bottom:2px solid black">Happening</td>
<td style="border-bottom:2px solid black">Exactness</td>
<td style="border-bottom:2px solid black">Existence</td>
<td style="border-bottom:2px solid black">Linearity</td>
<td style="border-bottom:2px solid black">Uniformity</td>
<td style="border-bottom:2px solid black">Information</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{0}$</td>
<td>Nothing happens</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{1}$</td>
<td>&nbsp;</td>
<td>Just false</td>
<td>Nothing exists</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{2}$</td>
<td>&nbsp;</td>
<td>Just not $x$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{3}$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>Nothing is $x$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{4}$</td>
<td>&nbsp;</td>
<td>Just $x$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{5}$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>Everything is $x$</td>
<td>$f$ is linear</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{6}$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>$f$ is not uniform</td>
<td>$f$ is informed</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{7}$</td>
<td>&nbsp;</td>
<td>Not just true</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{8}$</td>
<td>&nbsp;</td>
<td>Just true</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{9}$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>$f$ is uniform</td>
<td>$f$ is not informed</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{10}$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>Something is not $x$</td>
<td>$f$ is not linear</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{11}$</td>
<td>&nbsp;</td>
<td>Not just $x$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{12}$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>Something is $x$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{13}$</td>
<td>&nbsp;</td>
<td>Not just not $x$</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{14}$</td>
<td>&nbsp;</td>
<td>Not just false</td>
<td>Something exists</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

<tr>
<td style="border-right:2px solid black">$m_{15}$</td>
<td>Anything happens</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td></tr>

</table>

## Higher order propositions and logical operators $(n = 2)$ ##

By way of reviewing notation and preparing to extend it to higher order universes of discourse, let's first consider the universe of discourse $X^\circ = \left[ x_1, x_2 \right] = \left[ u, v \right]$ that is based on just two logical features or boolean variables $u$ and $v$.

The universe of discourse $X^\circ$ consists of two parts, a set of _points_ and a set of _propositions_.

The points of $X^\circ$ form a space notated as follows:

<div markdown="1"><font size="+1">
$$\array{
X
&amp; = &amp;
\lang u, v \rang
&amp; = &amp;
\{ (u, v) \}
&amp; \cong &amp;
\mathbb{B}^2
}$$
</font></div>

Each point in $X$ may be indicated by means of a _singular proposition_, that is, a proposition that describes it uniquely.  This form of representation leads to the following enumeration of points:

<div markdown="1"><font size="+1">
$$\array{
X
&amp; = &amp;
\{ &amp;
\text{&#x2997;} u \text{&#x2998;&#x2997;} v \text{&#x2998;}
&amp; , &amp;
\text{&#x2997;} u \text{&#x2998;} \: v
&amp; , &amp;
u \: \text{&#x2997;} v \text{&#x2998;}
&amp; , &amp;
u \: v
&amp; \}
&amp; \cong &amp;
\mathbb{B}^2
}$$
</font></div>

Each point in $X$ may also be described by means of its _coordinates_, that is, by the ordered pair of values in $\mathbb{B}$ that the coordinate propositions $u$ and $v$ take on that point.  This form of representation leads to the following enumeration of points:

<div markdown="1"><font size="+1">
$$\array{
X
&amp; = &amp;
\{ &amp;
(0, 0)
&amp; , &amp;
(0, 1)
&amp; , &amp;
(1, 0)
&amp; , &amp;
(1, 1)
&amp; \}
&amp; \cong &amp;
\mathbb{B}^2
}$$
</font></div>

The propositions of $X^\circ$ form a space notated as follows:

<div markdown="1"><font size="+1">
$$\array{
X^\uparrow
&amp; = &amp;
(X \to \mathbb{B})
&amp; = &amp;
\{ f : X \to \mathbb{B} \}
&amp; \cong &amp;
(\mathbb{B}^2 \to \mathbb{B})
}$$
</font></div>

As always, it is convenient to overlook the finer marks of distinction between isomorphic structures, so long as one is aware of their presence and knows when it is critical to call on them again.

The next higher order universe of discourse that is built on $X^\circ$ is $X^{\circ 2} = \left[ X^\circ \right] = \left[\left[ u, v \right]\right]$, which may be developed in the following way.  The propositions of $X^\circ$ become the points of $X^{\circ 2}$, and the mappings of the type $m : (X \to \mathbb{B}) \to \mathbb{B}$ become the propositions of $X^{\circ 2}$.  In addition, it is convenient to equip the discussion with a selected set of higher order operators on propositions, all of which have the form $w : (\mathbb{B}^2 \to \mathbb{B})^k \to \mathbb{B}$.

To save a few words in the remainder of this discussion, let us use the terms _measure_ and _qualifier_ to refer to all types of higher order propositions and operators.  To describe the present setting in picturesque terms, the propositions of $\left[ u, v \right]$ may be regarded as a gallery of sixteen venn diagrams, while the measures $m : (X \to \mathbb{B}) \to \mathbb{B}$ are analogous to a body of judges or a panel of critical viewers, each of whom evaluates each of the pictures as a whole and reports the ones that find favor or not.  In this way, each judge $m_j$ partitions the gallery of pictures into two aesthetic portions, the pictures $m_j^{-1}(0)$ that $m_j$ dislikes and the pictures $m_j^{-1}(1)$ that $m_j$ likes.

There are $2^{16} = 65536$ measures of the form $m : (\mathbb{B}^2 \to \mathbb{B}) \to \mathbb{B}$.  Table&nbsp;3 shows the first 24 of these measures in the same style of higher order truth table used above.  The column headed $m_j$ shows the values of the measure $m_j$ on each of the propositions $f_i : \mathbb{B}^2 \to \mathbb{B}$ for $i$ = 0 to 15, with blank entries in the Table being optional for values of zero.  Let us refer to the arrangement of measures that continues according to this plan as their _standard ordering_.  In this scheme of things, the index $j$ of the measure $m_j$ is the decimal equivalent of the bit string in the corresponding column of the Table, reading the binary digits in order from bottom to top.

<table align="center" cellpadding="1" cellspacing="0" markdown="1" style="background:white; color:black; text-align:center; width:90%">

<caption><font size="+2">$\text{Table 3.} \:\: \text{Higher Order Propositions} \: (n = 2)$</font></caption>

<tr>
<td style="border-bottom:2px solid black" align="right">$u:$<br>$v:$</td>
<td style="border-bottom:2px solid black">$1100$<br>$1010$</td>
<td style="border-bottom:2px solid black; border-right:2px solid black">$f$</td>
<td style="border-bottom:2px solid black">$m_{0}$</td>
<td style="border-bottom:2px solid black">$m_{1}$</td>
<td style="border-bottom:2px solid black">$m_{2}$</td>
<td style="border-bottom:2px solid black">$m_{3}$</td>
<td style="border-bottom:2px solid black">$m_{4}$</td>
<td style="border-bottom:2px solid black">$m_{5}$</td>
<td style="border-bottom:2px solid black">$m_{6}$</td>
<td style="border-bottom:2px solid black">$m_{7}$</td>
<td style="border-bottom:2px solid black">$m_{8}$</td>
<td style="border-bottom:2px solid black">$m_{9}$</td>
<td style="border-bottom:2px solid black">$m_{10}$</td>
<td style="border-bottom:2px solid black">$m_{11}$</td>
<td style="border-bottom:2px solid black">$m_{12}$</td>
<td style="border-bottom:2px solid black">$m_{13}$</td>
<td style="border-bottom:2px solid black">$m_{14}$</td>
<td style="border-bottom:2px solid black">$m_{15}$</td>
<td style="border-bottom:2px solid black">$m_{16}$</td>
<td style="border-bottom:2px solid black">$m_{17}$</td>
<td style="border-bottom:2px solid black">$m_{18}$</td>
<td style="border-bottom:2px solid black">$m_{19}$</td>
<td style="border-bottom:2px solid black">$m_{20}$</td>
<td style="border-bottom:2px solid black">$m_{21}$</td>
<td style="border-bottom:2px solid black">$m_{22}$</td>
<td style="border-bottom:2px solid black">$m_{23}$</td></tr>

<tr>
<td>$f_{0}$</td>
<td>$0000$</td>
<td style="border-right:2px solid black">$\text{&#x2997; &#x2998;}$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{1}$</td>
<td>$0001$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} u \text{&#x2998;&#x2997;} v \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{2}$</td>
<td>$0010$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} u\text{&#x2998;} \: v$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{3}$</td>
<td>$0011$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} u \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{4}$</td>
<td>$0100$</td>
<td style="border-right:2px solid black">$u \: \text{&#x2997;} v \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{5}$</td>
<td>$0101$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} v \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{6}$</td>
<td>$0110$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} u \text{&#xFE50;} v \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{7}$</td>
<td>$0111$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} u \: v \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{8}$</td>
<td>$1000$</td>
<td style="border-right:2px solid black">$u \: v$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{9}$</td>
<td>$1001$</td>
<td style="border-right:2px solid black">$\text{&#x2997;&#x2997;} u \text{&#xFE50;} v \text{&#x2998;&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{10}$</td>
<td>$1010$</td>
<td style="border-right:2px solid black">$v$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{11}$</td>
<td>$1011$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} u \: \text{&#x2997;} v \text{&#x2998;&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{12}$</td>
<td>$1100$</td>
<td style="border-right:2px solid black">$u$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{13}$</td>
<td>$1101$</td>
<td style="border-right:2px solid black">$\text{&#x2997;&#x2997;} u \text{&#x2998;} \: v \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{14}$</td>
<td>$1110$</td>
<td style="border-right:2px solid black">$\text{&#x2997;&#x2997;} u \text{&#x2998;&#x2997;} v \text{&#x2998;&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

<tr>
<td>$f_{15}$</td>
<td>$1111$</td>
<td style="border-right:2px solid black">$\text{&#x2997;&#x2997; &#x2998;&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td></tr>

</table>

# Umpire operators #

We now examine measures at the high end of the standard ordering.  Instrumental to this purpose we define a couple of higher order operators, $\Upsilon : (\lang u, v \rang \to \mathbb{B})^2 \to \mathbb{B}$ and $\Upsilon_1 : (\lang u, v \rang \to \mathbb{B}) \to \mathbb{B}$, referred to as the relative and absolute _umpire operators_, respectively.  If either of these operators is defined in terms of more primitive notions then the remaining operator can be defined in terms of the one first established.

Given an ordered pair of propositions $e, f : \lang u, v \rang \to \mathbb{B}$ as arguments, the relative umpire operator reports the value $1$ if the first implies the second, otherwise $0$.

<div markdown="1"><font size="+1">
$$
\Upsilon (e, f) = 1
\qquad \mathop{if and only if} \qquad
e \Rightarrow f
$$
</font></div>

Expressing it another way:

<div markdown="1"><font size="+1">
$$
\Upsilon (e, f) = 1
\qquad \iff \qquad
\text{&#x2997;} e \text{&#x2997;} f \text{&#x2998;&#x2998;} = \mathbf{1}
$$
</font></div>

In writing this, however, it is important to notice that the $1$'s appearing on the left and right have different meanings.  Filling in the details, we have:

<div markdown="1"><font size="+1">
$$
\Upsilon (e, f) = 1 \in \mathbb{B}
\qquad \iff \qquad
\text{&#x2997;} e \text{&#x2997;} f \text{&#x2998;&#x2998;} = 1 : \lang u, v \rang \to \mathbb{B}
$$
</font></div>

Writing types as subscripts and using the fact that $X = \lang u, v \rang$, it is possible to express this a little more succinctly as follows:

<div markdown="1"><font size="+1">
$$
\Upsilon (e, f) = 1_\mathbb{B}
\qquad \iff \qquad
\text{&#x2997;} e \text{&#x2997;} f \text{&#x2998;&#x2998;} = 1_{X \to \mathbb{B}}
$$
</font></div>

Finally, it is often convenient to write the first argument as a subscript, hence $\Upsilon_e (f) = \Upsilon (e, f)$.

As a special application of the relative umpire operator, we next define the absolute umpire operator, also known as the _umpire measure_.  In the present setting this is a higher order proposition $\Upsilon_1 : (\mathbb{B}^2 \to \mathbb{B}) \to \mathbb{B}$ that is defined by the equation $\Upsilon_1 (f) = \Upsilon (1, f)$.  Here, the subscript 1 on the left and the argument 1 on the right both refer to the constant proposition $1 : \mathbb{B}^2 \to \mathbb{B}$.  In most contexts where $\Upsilon_1$ is actually applied the subscript 1 is safely omitted, since the number of arguments indicates which type of operator is intended.  Thus, we have the following identities and equivalents:

<div markdown="1"><font size="+1">
$$
\Upsilon f = \Upsilon_1 (f) = 1_\mathbb{B}
\qquad \iff \qquad
\text{&#x2997;} 1 \text{&#x2997;} f \text{&#x2998;&#x2998;} = \mathbf{1}
\qquad \iff \qquad
f = 1_{\mathbb{B}^2 \to \mathbb{B}}
$$
</font></div>

The umpire measure is defined at the level of [[boolean functions]], but can also be understood in terms of its implied judgments at the syntactic level.  Interpreted this way, $\Upsilon_1$ recognizes theorems of the propositional calculus over $\left[ u, v \right]$, giving a score of "1" to tautologies and a score of "0" to everything else, regarding all contingent statements as no better than falsehoods.

One remark in passing for those who might prefer an alternative definition.  If we had originally taken $\Upsilon$ to mean the absolute measure, then the relative version could have been defined as $\Upsilon_e f = \Upsilon \text{&#x2997;} e \text{&#x2997;} f \text{&#x2998;&#x2998;}$.

# Measure for measure #

Define two families of measures:

<div markdown="1"><font size="+1">
$$\alpha_i, \beta_i : (\mathbb{B}^2 \to \mathbb{B}) \to \mathbb{B}, i = 0 \ldots 15,$$
</font></div>

by means of the following equations:

<div markdown="1"><font size="+1">
$$\array{
\alpha_i f &amp; = &amp; \Upsilon (f_i, f) &amp; = &amp; \Upsilon (f_i \Rightarrow f),
\\
\beta_i f  &amp; = &amp; \Upsilon (f, f_i) &amp; = &amp; \Upsilon (f \Rightarrow f_i).
}$$
</font></div>

The values of the sixteen $\alpha_i$ on each of the sixteen boolean functions $f : \mathbb{B}^2 \to \mathbb{B}$ are shown in Table&nbsp;4.  Expressed in terms of the implication ordering on the sixteen functions, $\alpha_i f = 1$ says that $f$ is _above or identical to_ $f_i$ in the implication lattice, that is, $\ge f_i$ in the implication ordering.

<table align="center" cellpadding="1" cellspacing="0" markdown="1" style="background:white; color:black; text-align:center; width:90%">

<caption><font size="+2">$\text{Table 4.} \:\: \text{Qualifiers of the Implication Ordering:} \: \alpha_{i} f = \Upsilon (f_{i}, f) = \Upsilon (f_{i} \Rightarrow f)$</font></caption>

<tr>
<td style="border-bottom:2px solid black" align="right">$u:$<br>$v:$</td>
<td style="border-bottom:2px solid black">$1100$<br>$1010$</td>
<td style="border-bottom:2px solid black; border-right:2px solid black">$f$</td>
<td style="border-bottom:2px solid black">$\alpha_{15}$</td>
<td style="border-bottom:2px solid black">$\alpha_{14}$</td>
<td style="border-bottom:2px solid black">$\alpha_{13}$</td>
<td style="border-bottom:2px solid black">$\alpha_{12}$</td>
<td style="border-bottom:2px solid black">$\alpha_{11}$</td>
<td style="border-bottom:2px solid black">$\alpha_{10}$</td>
<td style="border-bottom:2px solid black">$\alpha_{9}$</td>
<td style="border-bottom:2px solid black">$\alpha_{8}$</td>
<td style="border-bottom:2px solid black">$\alpha_{7}$</td>
<td style="border-bottom:2px solid black">$\alpha_{6}$</td>
<td style="border-bottom:2px solid black">$\alpha_{5}$</td>
<td style="border-bottom:2px solid black">$\alpha_{4}$</td>
<td style="border-bottom:2px solid black">$\alpha_{3}$</td>
<td style="border-bottom:2px solid black">$\alpha_{2}$</td>
<td style="border-bottom:2px solid black">$\alpha_{1}$</td>
<td style="border-bottom:2px solid black">$\alpha_{0}$</td></tr>

<tr>
<td>$f_{0}$</td>
<td>$0000$</td>
<td style="border-right:2px solid black">$\text{&#x2997; &#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td></tr>

<tr>
<td>$f_{1}$</td>
<td>$0001$</td>
<td style="border-right:2px solid black">$\text{&#x2997;} u \text{&#x2998;&#x2997;} v \text{&#x2998;}$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td>$0$</td><td>$0$</td><td>$0$</td><td>$0$</td>
<td style="background:black; color:white">$1$</td>
<td style="background:black; color:white">$1$</td></tr>

</table>

<div markdown="1"><font size="+3">$\ldots$</font></div>

# Functional conception of quantification theory #

Up till now quantification theory has been based on the assumption of individual variables ranging over universal collections of perfectly determinate elements.  Merely to write down quantified formulas like $\forall_{x \in X} f(x)$ and $\exists_{x \in X} f(x)$ involves a subscription to such notions, as shown by the membership relations invoked in their indices.  Reflected on pragmatic and constructive principles, these ideas begin to appear as problematic hypotheses whose warrants are not beyond question, projects of exhaustive determination that overreach the powers of finite information and control to manage.  Therefore, it is worth considering how we might shift the medium of quantification theory closer to familiar ground, toward the predicates themselves that represent our continuing acquaintance with phenomena.

# References and further reading #

* Quine, W.V. (1969/1981), "On the Limits of Decision", _Akten des XIV. Internationalen Kongresses f&#252;r Philosophie_, vol. 3 (1969).  Reprinted, pp. 156&ndash;163 in Quine (ed., 1981), _Theories and Things_, Harvard University Press, Cambridge, MA.

# External links #

* [Functional Logic : Quantification Theory](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Functional_Logic_:_Quantification_Theory)
