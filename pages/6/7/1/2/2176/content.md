[[!redirects Differential Logic]]

## Idea ##

__Differential logic__ is the component of [[logic]] whose object is the description of variation --- for example, the aspects of change, difference, distribution, and diversity --- in [[universes of discourse]] that are subject to logical description.  A definition that broad naturally incorporates any study of variation by way of mathematical models, but differential logic is especially charged with the qualitative aspects of variation that pervade or precede quantitative models.  To the extent that a logical inquiry makes use of a formal system, its differential component treats the principles that govern the use of a _differential logical calculus_, that is, a formal system with the expressive capacity to describe change and diversity in a logical universe of discourse.

A simple example of a differential logical calculus is furnished by a _[[differential propositional calculus]]_.  A differential propositional calculus is a [[propositional calculus]] extended by a set of terms for describing aspects of change and difference, for example, processes that take place in a universe of discourse or transformations that map a source universe into a target universe.  This augments ordinary propositional calculus in the same way that the differential calculus of Leibniz and Newton augments the analytic geometry of Descartes.

## Quick Overview ##

### Cactus Language for Propositional Logic ###

The development of differential logic is greatly facilitated by having a conceptually efficient calculus in place at the level of [[boolean-valued functions]] and elementary logical propositions.  A calculus that is very efficient from both conceptual and computational standpoints is based on just two types of logical connectives, both of variable $k$-ary scope.  The formulas of this calculus map into a species of graph-theoretical structures called _painted and rooted cacti_ (PARCs) that lend visual representation to their functional structure and smooth the path to efficient computation.

* The first kind of propositional expression is a parenthesized sequence of propositional expressions, written as $\text{&#10647;} \: e_1 \text{&#65104;} e_2 \text{&#65104;} \ldots \text{&#65104;} e_{k-1} \text{&#65104;} e_k \: \text{&#10648;}$ and read to say that exactly one of the propositions $e_1, e_2, \ldots, e_{k-1}, e_k$ is false, in other words, that their [[minimal negation]] is true.  A clause of this form maps into a PARC structure called a _lobe_, in this case, one that is _painted_ with the colors $e_1, e_2, \ldots, e_{k-1}, e_k$ as shown below.

<center>
<img src="http://mywikibiz.com/images/5/5e/Cactus_Graph_Lobe_Connective.jpg" width="500"/>
</center>

* The second kind of propositional expression is a concatenated sequence of propositional expressions, written as $e_1 \: e_2 \: \ldots \: e_{k-1} \: e_k$ and read to say that all of the propositions $e_1, e_2, \ldots, e_{k-1}, e_k$ are true, in other words, that their logical conjunction is true.  A clause of this form maps into a PARC structure called a _node_, in this case, one that is _painted_ with the colors $e_1, e_2, \ldots, e_{k-1}, e_k$ as shown below.

<center>
<img src="http://mywikibiz.com/images/9/98/Cactus_Graph_Node_Connective.jpg" width="500"/>
</center>

All other propositional connectives can be obtained through combinations of these two forms.  Strictly speaking, the parenthesized form is sufficient to define the concatenated form, making the latter formally dispensable, but it is convenient to maintain it as a concise way of expressing more complicated combinations of parenthesized forms.  While working with expressions solely in propositional calculus, it is easiest to use plain parentheses for logical connectives.  In contexts where ordinary parentheses are needed for other purposes an alternate typeface --- e.g. $\text{&#x2997;} \text{&#xFE50;} \text{
&#x2998;}$ --- may be used for logical operators.

Table&nbsp;1 collects a sample of basic propositional forms as expressed in terms of cactus connectives.

<table align="center" border="1" cellpadding="8" cellspacing="0" markdown="1" style="text-align:center; width:90%">

<caption><font size="+2">$\text{Table 1.  Syntax and Semantics of a Calculus for Propositional Logic}$</font></caption>

<tr style="background:#f0f0ff">
<td><font size="+2">$\text{Graph}$</font></td>
<td><font size="+2">$\text{Expression}$</font></td>
<td><font size="+2">$\text{Interpretation}$</font></td>
<td><font size="+2">$\text{Other Notations}$</font></td></tr>

<tr>
<td height="100px"><img alt="Rooted Node" src="/nlab/files/Rooted_Node.jpg" width="20" height="10" /></td>
<td>&nbsp;</td>
<td><font size="+1">$\mathop{true}$</font></td>
<td><font size="+1">$1$</font></td></tr>

<tr>
<td height="100px"><img alt="Rooted Edge" src="/nlab/files/Rooted_Edge.jpg" width="20" height="51" /></td>
<td><font size="+1">$\text{&#x2997;&nbsp;&#x2998;}$</font></td>
<td><font size="+1">$\mathop{false}$</font></td>
<td><font size="+1">$0$</font></td></tr>

<tr>
<td height="100px"><img alt="Cactus A Big" src="/nlab/files/Cactus_A_Big.jpg" width="20" height="38" /></td>
<td><font size="+1">$a$</font></td>
<td><font size="+1">$a$</font></td>
<td><font size="+1">$a$</font></td></tr>

<tr>
<td height="120px"><img alt="Cactus (A) Big" src="/nlab/files/Cactus_lAr_Big.jpg" width="20" height="79" /></td>
<td><font size="+1">$\text{&#x2997;} a \text{&#x2998;}$</font></td>
<td><font size="+1">$\mathop{not}\: a$</font></td>
<td><font size="+1">$\not a \quad \widebar{a} \quad \overset{\mathop{~}}{a} \quad a'$</font></td></tr>

<tr>
<td height="100px"><img alt="Cactus ABC Big" src="/nlab/files/Cactus_ABC_Big.jpg" width="50" height="38" /></td>
<td><font size="+1">$a \: b \: c$</font></td>
<td><font size="+1">$a \;\mathop{and}\; b \;\mathop{and}\; c$</font></td>
<td><font size="+1">$a \:\wedge\: b \:\wedge\: c$</font></td></tr>

<tr>
<td height="160px"><img alt="Cactus ((A)(B)(C)) Big" src="/nlab/files/Cactus_llArlBrlCrr_Big.jpg" width="65" height="118" /></td>
<td><font size="+1">$\text{&#x2997;&#x2997;} a \text{&#x2998;&#x2997;} b \text{&#x2998;&#x2997;} c \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$a \;\mathop{or}\; b \;\mathop{or}\; c$</font></td>
<td><font size="+1">$a \:\vee\: b \:\vee\: c$</font></td></tr>

<tr>
<td height="120px"><img alt="Cactus (A(B)) Big" src="/nlab/files/Cactus_lAlBrr_Big.jpg" width="60" height="80" /></td>
<td><font size="+1">$\text{&#x2997;} a \:\text{&#x2997;} b \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$\array{a \;\mathop{implies}\; b \\ \mathop{if}\; a \;\mathop{then}\; b}$</font></td>
<td><font size="+1">$a \Rightarrow b$</font></td></tr>

<tr>
<td height="120px"><img alt="Cactus (A,B) Big" src="/nlab/files/Cactus_lAcBr_Big.jpg" width="65" height="78" /></td>
<td><font size="+1">$\text{&#x2997;} a \text{&#xFE50;} b \text{&#x2998;}$</font></td>
<td><font size="+1">$\array{a \;\mathop{not equal to}\; b \\ a \;\mathop{exclusive or}\; b}$</font></td>
<td><font size="+1">$\array{a \ne b \\ a + b}$</font></td></tr>

</table>

__NB.__ Still working on this &hellip; [[JA]]

<img alt="Rooted Node" src="/nlab/files/Rooted_Node.jpg" width="20" height="10" />
<img alt="Rooted Edge" src="/nlab/files/Rooted_Edge.jpg" width="20" height="51" />
<img alt="Cactus A Big" src="/nlab/files/Cactus_A_Big.jpg" width="20" height="38" />
<img alt="Cactus (A) Big" src="/nlab/files/Cactus_lAr_Big.jpg" width="20" height="79" />
<img alt="Cactus ABC Big" src="/nlab/files/Cactus_ABC_Big.jpg" width="50" height="38" />
<img alt="Cactus ((A)(B)(C)) Big" src="/nlab/files/Cactus_llArlBrlCrr_Big.jpg" width="65" height="118" />
<img alt="Cactus (A(B)) Big" src="/nlab/files/Cactus_lAlBrr_Big.jpg" width="60" height="80" />
<img alt="Cactus (A,B) Big" src="/nlab/files/Cactus_lAcBr_Big.jpg" width="65" height="78" />
<img alt="Cactus ((A,B)) Big" src="/nlab/files/Cactus_llAcBrr_Big.jpg" width="65" height="118" />
<img alt="Cactus (A,B,C) Big" src="/nlab/files/Cactus_lAcBcCr_Big.jpg" width="65" height="78" />
<img alt="Cactus ((A),(B),(C)) Big" src="/nlab/files/Cactus_llArclBrclCrr_Big.jpg" width="65" height="118" />

## External links ##

* [Differential_Logic : Introduction](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Differential_Logic_:_Introduction)

* [Differential Propositional Calculus](http://planetmath.org/encyclopedia/DifferentialPropositionalCalculus.html)

* [Differential Logic and Dynamic Systems](http://www.mywikibiz.com/Directory:Jon_Awbrey/Papers/Differential_Logic_and_Dynamic_Systems_2.0)
