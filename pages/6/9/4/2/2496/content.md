[[!redirects higher order propositions]]

# Idea #

If functions of type $X \to \mathbb{B}$ are propositions about things in $X$, then functions of type $(X \to \mathbb{B}) \to \mathbb{B}$ are propositions about propositions about things in $X$, the first of a series of __higher order propositions__ based on $X$.

# Higher order propositional expressions #

By way of equipping the discussion with a modicum of concrete material, let's begin with a consideration of higher order propositions and logical operators that stem from the ordinary propositions on 1 and 2 variables.

## Higher order propositions and logical operators $(n = 1)$ ##

A _higher order proposition_ is a proposition about propositions.  If the original order of propositions consists of maps of the form $f : X \to \mathbb{B}$, then the next higher order of propositions consists of maps of the form $m : (X \to \mathbb{B}) \to \mathbb{B}$.  It is often useful to think of a higher order proposition as a boolean-valued _measure_ on propositions.

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

Table&nbsp;2 presents a sample of _interpretive categories_ for higher order propositions of type $(\mathbb{B}^1 \to \mathbb{B}) \to \mathbb{B}$, but it's best to put off discussing this Table further until we get beyond the 1-dimensional case.  These lower dimensional cases tend to be extremely _condensed_ or _degenerate_ in their structures, and the pattern of what's going on here can be set in higher relief as soon as we have even two logical variables to play off each other.

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

<div markdown="1"><font size="+3">$\ldots$</font></div>

# Functional conception of quantification theory #

Up till now quantification theory has been based on the assumption of individual variables ranging over universal collections of perfectly determinate elements.  Merely to write down quantified formulas like $\forall_{x \in X} f(x)$ and $\exists_{x \in X} f(x)$ involves a subscription to such notions, as shown by the membership relations invoked in their indices.  Reflected on pragmatic and constructive principles, these ideas begin to appear as problematic hypotheses whose warrants are not beyond question, projects of exhaustive determination that overreach the powers of finite information and control to manage.  Therefore, it is worth considering how we might shift the medium of quantification theory closer to familiar ground, toward the predicates themselves that represent our continuing acquaintance with phenomena.

# References and further reading #

* Quine, W.V. (1969/1981), "On the Limits of Decision", _Akten des XIV. Internationalen Kongresses f&#252;r Philosophie_, vol. 3 (1969).  Reprinted, pp. 156&ndash;163 in Quine (ed., 1981), _Theories and Things_, Harvard University Press, Cambridge, MA.

# External links #

* [Functional Logic : Quantification Theory](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Functional_Logic_:_Quantification_Theory)
