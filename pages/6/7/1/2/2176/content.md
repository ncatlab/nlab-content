[[!redirects Differential Logic]]

## Idea ##

__Differential logic__ is the component of [[logic]] whose object is the description of variation --- for example, the aspects of change, difference, distribution, and diversity --- in [[universes of discourse]] that are subject to logical description.  A definition that broad naturally incorporates any study of variation by way of mathematical models, but differential logic is especially charged with the qualitative aspects of variation that pervade or precede quantitative models.  To the extent that a logical inquiry makes use of a formal system, its differential component treats the principles that govern the use of a _differential logical calculus_, that is, a formal system with the expressive capacity to describe change and diversity in a logical universe of discourse.

A simple example of a differential logical calculus is furnished by a _[[differential propositional calculus]]_.  A differential propositional calculus is a [[propositional calculus]] extended by a set of terms for describing aspects of change and difference, for example, processes that take place in a universe of discourse or transformations that map a source universe into a target universe.  This augments ordinary propositional calculus in the same way that the differential calculus of Leibniz and Newton augments the analytic geometry of Descartes.

## Quick Overview ##

### Cactus Language for Propositional Logic ###

The development of differential logic is greatly facilitated by having a conceptually efficient calculus in place at the level of [[boolean-valued functions]] and elementary logical propositions.  A calculus that is very efficient from both conceptual and computational standpoints is based on just two types of logical connectives, both of variable $k$-ary scope.  The formulas of this calculus map into a species of graph-theoretical structures called _painted and rooted cacti_ (PARCs) that lend visual representation to their functional structure and smooth the path to efficient computation.

* The first kind of propositional expression is a parenthesized sequence of propositional expressions, written as $\text{&#10647;} \: e_1 \text{&#65104;} e_2 \text{&#65104;} \ldots \text{&#65104;} e_{k-1} \text{&#65104;} e_k \: \text{&#10648;}$ and read to say that exactly one of the propositions $e_1, e_2, \ldots, e_{k-1}, e_k$ is false, in other words, that their [[minimal negation]] is true.  A clause of this form maps into a PARC structure called a _lobe_, in this case, one that is _painted_ with the _colors_ $e_1, e_2, \ldots, e_{k-1}, e_k$ as shown below.

<center>
<img src="http://mywikibiz.com/images/5/5e/Cactus_Graph_Lobe_Connective.jpg" width="500"/>
</center>

* The second kind of propositional expression is a concatenated sequence of propositional expressions, written as $e_1 \: e_2 \: \ldots \: e_{k-1} \: e_k$ and read to say that all of the propositions $e_1, e_2, \ldots, e_{k-1}, e_k$ are true, in other words, that their logical conjunction is true.  A clause of this form maps into a PARC structure called a _node_, in this case, one that is _painted_ with the _colors_ $e_1, e_2, \ldots, e_{k-1}, e_k$ as shown below.

<center>
<img src="http://mywikibiz.com/images/9/98/Cactus_Graph_Node_Connective.jpg" width="500"/>
</center>

All other propositional connectives can be obtained through combinations of these two forms.  Strictly speaking, the parenthesized form is sufficient to define the concatenated form, making the latter formally dispensable, but it is convenient to maintain it as a concise way of expressing more complicated combinations of parenthesized forms.  While working with expressions solely in propositional calculus, it is easiest to use plain parentheses for logical connectives.  In contexts where ordinary parentheses are needed for other purposes an alternate typeface $\text{&#10647;} \text{&#65104;} \text{&#10648;}$ may be used for logical operators.

Table&nbsp;1 collects a sample of basic propositional forms as expressed in terms of cactus connectives.

<table align="center" border="1" cellpadding="8" cellspacing="0" style="text-align:center; width:90%">
<caption> <img class='tex' src="http://mywikibiz.com/images/math/4/b/7/4b714e121dcb7e880367b3c348294e1f.png" alt="\text{Table 1.}~~\text{Syntax and Semantics of a Calculus for Propositional Logic}" />
</caption>

<tr style="background:#f0f0ff">
<td> <img class='tex' src="http://mywikibiz.com/images/math/c/f/8/cf8355a1bf9b6821ed2c15658060d349.png" alt="\text{Graph}\!" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/0/2/b/02ba04972afebb8d123c4e920909b8fb.png" alt="\text{Expression}\!" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/a/8/6/a8654d8844fc34a58809af813c22919a.png" alt="\text{Interpretation}\!" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/5/3/f/53f0ee60a3ccd002629b474070df9e53.png" alt="\text{Other Notations}\!" />
</td></tr>

<tr>
<td height="100px"><img alt="Rooted Node" src="/nlab/files/Rooted_Node.jpg" width="20" height="10" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/4/c/7/4c761f170e016836ff84498202b99827.png" alt="~" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/a/9/8/a98f0f208c522b8d25f88110dfa5be3a.png" alt="\operatorname{true}" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/3/3/f/33f7ec109298779a887aff2887ff9c7c.png" alt="1\!" />
</td></tr>

<tr>
<td height="100px"><img alt="Rooted Edge" src="/nlab/files/Rooted_Edge.jpg" width="20" height="51" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/3/7/f/37f1dfde729312575b502e8b80c4f1b1.png" alt="\texttt{(~)}" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/8/5/5/855c491bdfa6847adb8adea57c8a78f4.png" alt="\operatorname{false}" />
</td><td> <img class='tex' src="http://mywikibiz.com/images/math/f/7/4/f7496913e3e61d6a5227c611eb355e93.png" alt="0\!" />
</td></tr>
</table>

__NB.__ Still working on this --- can probably trim away the remote content over time. ---[[JA]]

## External links ##

* [Differential_Logic : Introduction](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Differential_Logic_:_Introduction)

* [Differential Propositional Calculus](http://planetmath.org/encyclopedia/DifferentialPropositionalCalculus.html)

* [Differential Logic and Dynamic Systems](http://www.mywikibiz.com/Directory:Jon_Awbrey/Papers/Differential_Logic_and_Dynamic_Systems_2.0)
