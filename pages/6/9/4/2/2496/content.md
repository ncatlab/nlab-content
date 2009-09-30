[[!redirects higher order propositions]]

# Idea #

If functions of type $X \to \mathbb{B}$ are propositions about things in $X$, then functions of type $(X \to \mathbb{B}) \to \mathbb{B}$ are propositions about propositions about things in $X$, the first of a series of __higher order propositions__ about things in $X$.

# Higher order propositional expressions #

By way of equipping the discussion with a modicum of concrete material, let's begin with a consideration of higher order propositions and logical operators that stem from the ordinary propositions on 1 and 2 variables.

## Higher order propositions and logical operators $(n = 1)$ ##

A _higher order proposition_, also known as a _measure_ on propositions, is a proposition about propositions.  If the original order of propositions is a class of [[indicator functions]] $f : X \to \mathbb{B}$, then the next higher order of propositions consists of maps of the form $m : (X \to \mathbb{B}) \to \mathbb{B}$.

For example, consider the case where $X = \mathbb{B}$.  Then there are exactly four propositions $f : \mathbb{B} \to \mathbb{B}$, and exactly sixteen higher order propositions that are based on this set, all taking the form $m : (\mathbb{B} \to \mathbb{B}) \to \mathbb{B}$.

Table&#160;1 lists the 16 measures of the form $m : (\mathbb{B} \to \mathbb{B}) \to \mathbb{B}$.

<table align="center" border="1" cellpadding="4" cellspacing="0" markdown="1" style="background:white; color:black; text-align:center; width:90%">
<caption><font size="+2">$\text{Table 1.} \; \text{Higher Order Propositions} \; (n = 1)$</font></caption>

<tr style="background:ghostwhite">
<td align="right">$x:$</td>
<td>$1 \: 0$</td>
<td>$f$</td>
<td>$m_{0}$</td>
<td>$m_{1}$</td>
<td>$m_{2}$</td>
<td>$m_{3}$</td>
<td>$m_{4}$</td>
<td>$m_{5}$</td>
<td>$m_{6}$</td>
<td>$m_{7}$</td>
<td>$m_{8}$</td>
<td>$m_{9}$</td>
<td>$m_{10}$</td>
<td>$m_{11}$</td>
<td>$m_{12}$</td>
<td>$m_{13}$</td>
<td>$m_{14}$</td>
<td>$m_{15}$</td></tr>

<tr>
<td style="background:ghostwhite">$f_{0}$</td>
<td style="background:ghostwhite">$0 \: 0$</td>
<td style="background:ghostwhite">$\text{&#x2997; &#x2998;}$</td>
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
<td style="background:ghostwhite">$f_{1}$</td>
<td style="background:ghostwhite">$0 \: 1$</td>
<td style="background:ghostwhite">$\text{&#x2997;} x \text{&#x2998;}$</td>
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
<td style="background:ghostwhite">$f_{2}$</td>
<td style="background:ghostwhite">$1 \: 0$</td>
<td style="background:ghostwhite">$x$</td>
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
<td style="background:ghostwhite">$f_{3}$</td>
<td style="background:ghostwhite">$1 \: 1$</td>
<td style="background:ghostwhite">$\text{&#x2997;&#x2997; &#x2998;&#x2998;}$</td>
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

The contents of Table&nbsp;1 are organized as follows.  Columns&nbsp;1 and 2 form a truth table for the four propositions of the form $f : \mathbb{B} \to \mathbb{B}$, with the row leaders in Column&nbsp;1 displaying the names of the functions $f_i$ for $i$ = 0 to 3, while the entries in Column&nbsp;2 give the values of each function for the argument values that are listed in the corresponding column head.  Column&nbsp;3 displays a more or less canonical expression for the proposition in question.  The last sixteen columns are topped by a collection of conventional names for the measures $m_j$ as $j$ ranges from 0 to 15, where the entries in the body of the Table record the values that each $m_j$ assigns to each $f_i$.

## Higher order propositions and logical operators $(n = 2)$ ##

<div markdown="1"><font size="+3">$\ldots$</font></div>

# Functional conception of quantification theory #

Up till now quantification theory has been based on the assumption of individual variables ranging over universal collections of perfectly determinate elements.  Merely to write down quantified formulas like $\forall_{x \in X} f(x)$ and $\exists_{x \in X} f(x)$ involves a subscription to such notions, as shown by the membership relations invoked in their indices.  Reflected on pragmatic and constructive principles, these ideas begin to appear as problematic hypotheses whose warrants are not beyond question, projects of exhaustive determination that overreach the powers of finite information and control to manage.  Therefore, it is worth considering how we might shift the medium of quantification theory closer to familiar ground, toward the predicates themselves that represent our continuing acquaintance with phenomena.

# References and further reading #

* Quine, W.V. (1969/1981), "On the Limits of Decision", _Akten des XIV. Internationalen Kongresses f&#252;r Philosophie_, vol. 3 (1969).  Reprinted, pp. 156&ndash;163 in Quine (ed., 1981), _Theories and Things_, Harvard University Press, Cambridge, MA.

# External links #

* [Functional Logic : Quantification Theory](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Functional_Logic_:_Quantification_Theory)
