[[!redirects Differential Logic]]

## Idea ##

__Differential logic__ is the component of [[logic]] whose object is the description of variation --- for example, the aspects of change, difference, distribution, and diversity --- in [[universes of discourse]] that are subject to logical description.  A definition that broad naturally incorporates any study of variation by way of mathematical models, but differential logic is especially charged with the qualitative aspects of variation that pervade or precede quantitative models.  To the extent that a logical inquiry makes use of a formal system, its differential component treats the principles that govern the use of a _differential logical calculus_, that is, a formal system with the expressive capacity to describe change and diversity in a logical universe of discourse.

A simple example of a differential logical calculus is furnished by a _[[differential propositional calculus]]_.  A differential propositional calculus is a [[propositional calculus]] extended by a set of terms for describing aspects of change and difference, for example, processes that take place in a universe of discourse or transformations that map a source universe into a target universe.  This augments ordinary propositional calculus in the same way that the differential calculus of Leibniz and Newton augments the analytic geometry of Descartes.

## Quick Overview ##

### Cactus Language for Propositional Logic ###

The development of differential logic is greatly facilitated by having a conceptually efficient calculus in place at the level of [[boolean-valued functions]] and elementary logical propositions.  A calculus that is very efficient from both conceptual and computational standpoints is based on just two types of logical connectives, both of variable $k$-ary scope.  The formulas of this calculus map into a species of graph-theoretical structures called _painted and rooted cacti_ (PARCs) that lend visual representation to their functional structure and smooth the path to efficient computation.

* The first kind of propositional expression is a parenthesized sequence of propositional expressions, written as $\text{&#10647;} \; e_1 \text{&#65104;} e_2 \text{&#65104;} \ldots \text{&#65104;} e_{k-1} \text{&#65104;} e_k \; \text{&#10648;}$ and read to say that exactly one of the propositions $e_1, e_2, \ldots, e_{k-1}, e_k$ is false, in other words, that their [[minimal negation]] is true.  A clause of this form maps into a PARC structure called a _lobe_, in this case, one that is _painted_ with the colors $e_1, e_2, \ldots, e_{k-1}, e_k$ as shown below.

<center>
<img alt="Cactus Graph Lobe Connective" src="/nlab/files/Cactus_Graph_Lobe_Connective.jpg" width="500" />
</center>

* The second kind of propositional expression is a concatenated sequence of propositional expressions, written as $e_1 \; e_2 \; \ldots \; e_{k-1} \; e_k$ and read to say that all of the propositions $e_1, e_2, \ldots, e_{k-1}, e_k$ are true, in other words, that their logical conjunction is true.  A clause of this form maps into a PARC structure called a _node_, in this case, one that is _painted_ with the colors $e_1, e_2, \ldots, e_{k-1}, e_k$ as shown below.

<center>
<img alt="Cactus Graph Node Connective" src="/nlab/files/Cactus_Graph_Node_Connective.jpg" width="500" />
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
<td height="100px"><img alt="Rooted Edge" src="/nlab/files/Rooted_Edge.jpg" width="20" height="50" /></td>
<td><font size="+1">$\text{&#x2997;&nbsp;&#x2998;}$</font></td>
<td><font size="+1">$\mathop{false}$</font></td>
<td><font size="+1">$0$</font></td></tr>

<tr>
<td height="100px"><img alt="Cactus A Big" src="/nlab/files/Cactus_A_Big.jpg" width="20" height="40" /></td>
<td><font size="+1">$a$</font></td>
<td><font size="+1">$a$</font></td>
<td><font size="+1">$a$</font></td></tr>

<tr>
<td height="120px"><img alt="Cactus (A) Big" src="/nlab/files/Cactus_lAr_Big.jpg" width="20" height="80" /></td>
<td><font size="+1">$\text{&#x2997;} a \text{&#x2998;}$</font></td>
<td><font size="+1">$\mathop{not}\; a$</font></td>
<td><font size="+1">$\not a \quad \overset{-}{a} \quad \overset{~}{a} \quad a'$</font></td></tr>

<tr>
<td height="100px"><img alt="Cactus ABC Big" src="/nlab/files/Cactus_ABC_Big.jpg" width="50" height="40" /></td>
<td><font size="+1">$a \; b \; c$</font></td>
<td><font size="+1">$a \;\mathop{and}\; b \;\mathop{and}\; c$</font></td>
<td><font size="+1">$a \;\wedge\; b \;\wedge\; c$</font></td></tr>

<tr>
<td height="160px"><img alt="Cactus ((A)(B)(C)) Big" src="/nlab/files/Cactus_llArlBrlCrr_Big.jpg" width="65" height="120" /></td>
<td><font size="+1">$\text{&#x2997;&#x2997;} a \text{&#x2998;&#x2997;} b \text{&#x2998;&#x2997;} c \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$a \;\mathop{or}\; b \;\mathop{or}\; c$</font></td>
<td><font size="+1">$a \;\vee\; b \;\vee\; c$</font></td></tr>

<tr>
<td height="120px"><img alt="Cactus (A(B)) Big" src="/nlab/files/Cactus_lAlBrr_Big.jpg" width="60" height="80" /></td>
<td><font size="+1">$\text{&#x2997;} a \;\text{&#x2997;} b \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$\array{a \;\mathop{implies}\; b \\ \mathop{if}\; a \;\mathop{then}\; b}$</font></td>
<td><font size="+1">$a \Rightarrow b$</font></td></tr>

<tr>
<td height="120px"><img alt="Cactus (A,B) Big" src="/nlab/files/Cactus_lAcBr_Big.jpg" width="65" height="80" /></td>
<td><font size="+1">$\text{&#x2997;} a \text{&#xFE50;} b \text{&#x2998;}$</font></td>
<td><font size="+1">$\array{a \;\mathop{not equal to}\; b \\ a \;\mathop{exclusive or}\; b}$</font></td>
<td><font size="+1">$\array{a \ne b \\ a + b}$</font></td></tr>

<tr>
<td height="160px"><img alt="Cactus ((A,B)) Big" src="/nlab/files/Cactus_llAcBrr_Big.jpg" width="65" height="120" /></td>
<td><font size="+1">$\text{&#x2997;&#x2997;} a \text{&#xFE50;} b \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$\array{a \;\mathop{is equal to}\; b \\ a \;\mathop{if and only if}\; b}$</font></td>
<td><font size="+1">$\array{a = b \\ a \Leftrightarrow b}$</font></td></tr>

<tr>
<td height="120px"><img alt="Cactus (A,B,C) Big" src="/nlab/files/Cactus_lAcBcCr_Big.jpg" width="65" height="80" /></td>
<td><font size="+1">$\text{&#x2997;} a \text{&#xFE50;} b \text{&#xFE50;} c \text{&#x2998;}$</font></td>
<td><font size="+1">$\array{\mathop{just one of} \\ a, b, c \\ \mathop{is false}.}$</font></td>
<td><font size="+1">$\array{&amp; \overset{-}{a} \; b \; c \\ \vee &amp; a \; \overset{-}{b} \; c \\ \vee &amp; a \; b \; \overset{-}{c}}$</font></td></tr>

<tr>
<td height="160px"><img alt="Cactus ((A),(B),(C)) Big" src="/nlab/files/Cactus_llArclBrclCrr_Big.jpg" width="65" height="120" /></td>
<td><font size="+1">$\text{&#x2997;&#x2997;} a \text{&#x2998;&#xFE50;&#x2997;} b \text{&#x2998;&#xFE50;&#x2997;} c \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$\array{\mathop{just one of} \\ a, b, c \\ \mathop{is true}. \\ \\ \mathop{partition all} \\ \mathop{into}\; a, b, c.}$</font></td>
<td><font size="+1">$\array{&amp; a \; \overset{-}{b} \; \overset{-}{c} \\ \vee &amp; \overset{-}{a} \; b \; \overset{-}{c} \\ \vee &amp; \overset{-}{a} \; \overset{-}{b} \; c}$</font></td></tr>

<tr>
<td height="160px"><img alt="Cactus (A,(B,C)) Big" src="/nlab/files/Cactus_lAclBcCrr_Big.jpg" width="90" height="120" /></td>
<td><font size="+1">$\text{&#x2997;} a \text{&#xFE50;&#x2997;} b \text{&#xFE50;} c \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$\array{\mathop{oddly many of} \\ a, b, c \\ \mathop{are true}.}$</font></td>
<td><font size="+1">$\array{\cellopts{\colspan{2}} a + b + c \\ \\ &amp; a \; b \; c \\ \vee &amp; a \; \overset{-}{b} \; \overset{-}{c} \\ \vee &amp; \overset{-}{a} \; b \; \overset{-}{c} \\ \vee &amp; \overset{-}{a} \; \overset{-}{b} \; c}$</font></td></tr>

<tr>
<td><img alt="Cactus (X,(A),(B),(C)) Big" src="/nlab/files/Cactus_lXclArclBrclCrr_Big.jpg" width="90" height="120" /></td>
<td><font size="+1">$\text{&#x2997;} x \text{&#xFE50;&#x2997;} a \text{&#x2998;&#xFE50;&#x2997;} b \text{&#x2998;&#xFE50;&#x2997;} c \text{&#x2998;&#x2998;}$</font></td>
<td><font size="+1">$\array{\mathop{partition}\; x \\ \mathop{into}\; a, b, c. \\ \\ \mathop{genus}\; x \;\mathop{comprises} \\ \mathop{species}\; a, b, c.}$</font></td>
<td><font size="+1">$\array{&amp; \overset{-}{x} \; \overset{-}{a} \; \overset{-}{b} \; \overset{-}{c} \\ \vee &amp; x \; a \; \overset{-}{b} \; \overset{-}{c} \\ \vee &amp; x \; \overset{-}{a} \; b \; \overset{-}{c} \\ \vee &amp; x \; \overset{-}{a} \; \overset{-}{b} \; c}$</font></td></tr>

</table>

The simplest expression for logical truth is the empty word, usually denoted by $\varepsilon$ or $\lambda$ in formal languages, where it forms the identity element for concatenation.  To make it visible in context, it may be denoted by the equivalent expression &ldquo;$\text{&#x2997;&#x2997; &#x2998;&#x2998;}$&rdquo;, or, especially if operating in an algebraic context, by a simple &ldquo;$1$&rdquo;.  Also when working in an algebraic mode, the plus sign &ldquo;$+$&rdquo; may be used for exclusive disjunction.  For example, we have the following paraphrases of algebraic expressions by means of parenthesized expressions:

<div markdown="1"><font size="+1">
$$\array{a + b & = & \text{&#x2997;} a \text{&#xFE50;} b \text{&#x2998;}}$$

<br>

$$\array{
a + b + c
& = &
\text{&#x2997;} a \text{&#xFE50;&#x2997;} b \text{&#xFE50;} c \text{&#x2998;&#x2998;}
& = &
\text{&#x2997;&#x2997;} a \text{&#xFE50;} b \text{&#x2998;&#xFE50;} c \text{&#x2998;}
}$$
</font></div>

It is important to note that the last expressions are not equivalent to the 3-place parenthesis $\text{&#x2997;} a \text{&#xFE50;} b \text{&#xFE50;} c \text{&#x2998;}$.

The subject as it develops from this point on is a little like doing [[differential geometry]] over GF(2), but the logical aim puts a slightly different spin on the way we look at formulas.  For example, we think of a function $f : X \to \mathbb{B}$ as a device for drawing a distinction in the space $X$, relative to which distinction we frequently have call to indicate the contents on either side.  These two subsets of $X$ are the [[fibers]] $f^{-1}(0)$ and $f^{-1}(1)$ of the function $f$.  Picking sides as we usually do, $f^{-1}(1)$ is the _indicated_ or _intended_ fiber, leaving $f^{-1}(0)$ to be the _undicated_ or _untended_ fiber.  This makes it convenient to dedicate a more streamlined notation to the fiber of $1$, defining $\text{&#x301A;} f \text{&#x301B;} \;\text{:=}\; f^{-1}(1)$.  In this light, aside from the usual charge to compute the values of compound functions from information about the values of their components, we are especially charged to invert those functions and find the fibers of given end values.

## Differential Expansions of Propositions ##

### Bird's Eye View ###

An efficient calculus for the realm of logic represented by boolean functions and elementary propositions makes it feasible to compute the finite differences and differentials of those functions and propositions.

For example, consider a proposition of the form &ldquo;$p \;\mathop{and}\; q$&rdquo; that is graphed as two letters attached to a root node:

<center>
<img alt="Cactus Graph Existential P And Q" src="/nlab/files/Cactus_Graph_Existential_P_And_Q.jpg" width="500" />
</center>

Written as a string, this is just the concatenation $p \; q$.

The proposition $p \; q$ may be taken as a boolean function $f(p, q)$ having the abstract type $f : \mathbb{B} \;\times\; \mathbb{B} \to \mathbb{B}$, where $\mathbb{B} = \{ 0, 1 \}$ is read in such a way that $0$ means $\mathop{false}$ and $1$ means $\mathop{true}$.

Imagine yourself standing in a fixed cell of the corresponding venn diagram, say, the cell where the proposition $p \; q$ is true, as shown in the following Figure:

<center>
<img alt="Venn Diagram P And Q" src="/nlab/files/Venn_Diagram_P_And_Q.jpg" width="500" />
</center>

Now ask yourself:  What is the value of the proposition $p \; q$ at a distance of $\mathop{d}p$ and $\mathop{d}q$ from the cell $p \; q$ where you are standing?

Don't think about it --- just compute:

<center>
<img alt="Cactus Graph (P,dP)(Q,dQ)" src="/nlab/files/Cactus_Graph_lPcdPrlQcdQr.jpg" width="500" />
</center>

The cactus formula $\text{&#x2997;} p \text{&#xFE50;} \mathop{d}p \text{&#x2998;&#x2997;} q \text{&#xFE50;} \mathop{d}q \text{&#x2998;}$ and its corresponding graph arise by substituting $p + \mathop{d}p$ for $p$ and $q + \mathop{d}q$ for $q$ in the boolean product or logical conjunction $p \; q$ and writing the result in the two dialects of cactus syntax.  This follows from the fact that the boolean sum $p + \mathop{d}p$ is equivalent to the logical operation of exclusive disjunction, which parses to a cactus graph of the following form:

<center>
<img alt="Cactus Graph (P,dP)" src="/nlab/files/Cactus_Graph_lPcdPr.jpg" width="500" />
</center>

Next question:  What is the difference between the value of the proposition $p \; q$ over there, at a distance of $\mathop{d}p$ and $\mathop{d}q$, and the value of the proposition $p \; q$ where you are standing, all expressed in the form of a general formula, of course?  Here is the appropriate formulation:

<center>
<img alt="Cactus Graph ((P,dP)(Q,dQ),PQ)" src="/nlab/files/Cactus_Graph_llPcdPrlQcdQrcPQr.jpg" width="500" />
</center>

Last question, for now:  What is the value of this expression from your current standpoint, that is, evaluated at the point where $p \; q$ is true?  Well, substituting $1$ for $p$ and $1$ for $q$ in the graph amounts to erasing the labels $p$ and $q$, as shown here:

<center>
<img alt="Cactus Graph (( ,dP)( ,dQ), )" src="/nlab/files/Cactus_Graph_ll_cdPrl_cdQrc_r.jpg" width="500" />
</center>

And this is equivalent to the following graph:

<center>
<img alt="Cactus Graph ((dP)(dQ))" src="/nlab/files/Cactus_Graph_lldPrldQrr.jpg" width="500" />
</center>

We have just met with the fact that the logical difference of the __<font size="+1">and</font>__ is the __<font size="+1">or</font>__ of the logical differences.

<center>
<img alt="Cactus Graph PQ Diff ((dP)(dQ))" src="/nlab/files/Cactus_Graph_PQ_Diff_lldPrldQrr.jpg" width="500" />
</center>

It will be necessary to develop a more refined analysis of that statement directly, but that is roughly the nub of it.

If the form of the above statement reminds you of De&nbsp;Morgan's rule, it is no accident, as differentiation and negation turn out to be closely related operations.  Indeed, one can find discussions of logical difference calculus in the Boole&ndash;De&nbsp;Morgan correspondence and Peirce also made use of differential operators in a logical context, but the exploration of these ideas has been hampered by a number of factors, not the least of which has been the lack of a syntax that was adequate to handle the complexity of expressions that evolve.

### Worm's Eye View ###

Let us run through the initial example again, this time attempting to interpret the formulas that develop at each stage along the way.  We begin with a proposition or a boolean function $f(p, q) = p q$.

<table align="center" cellpadding="8" style="border:none">
<tr>
<td style="border:none">
<img alt="Venn Diagram F = P And Q" src="/nlab/files/Venn_Diagram_F_Equals_P_And_Q.jpg" width="500" /></td></tr>
<tr>
<td style="border:none">
<img alt="Cactus Graph F = P And Q" src="/nlab/files/Cactus_Graph_F_Equals_P_And_Q.jpg" width="500" /></td></tr>
</table>

A function like this has an abstract type and a concrete type.  The abstract type is what we invoke when we write things like $f : \mathbb{B} \; \times \; \mathbb{B} \to \mathbb{B}$ or $f : \mathbb{B}^2 \to \mathbb{B}$.  The concrete type takes into account the qualitative dimensions or the "units" of the case, which can be explained as follows.

## External links ##

* [Differential_Logic : Introduction](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Differential_Logic_:_Introduction)

* [Differential Propositional Calculus](http://planetmath.org/encyclopedia/DifferentialPropositionalCalculus.html)

* [Differential Logic and Dynamic Systems](http://www.mywikibiz.com/Directory:Jon_Awbrey/Papers/Differential_Logic_and_Dynamic_Systems_2.0)

## Gallery ##

__NB.__ I'll be using this area to test the remote images and upload the local images that I'll be inserting as the article develops.  ---[[JA]]

Templates ---

       [[mypic.jpg|alt text:pic]]

       ![alt text](/nlab/files/mypic.jpg)

       http://ncatlab.org/nlab/files/mypic.jpg

       <img alt="mytext" src="/nlab/files/mypic.jpg" width="500" />

Upload Queue ---

[[Venn_Diagram_P_Q_dP_dQ.jpg|Venn Diagram P Q dP dQ:pic]]

[[Cactus_Graph_Ef_eq_lPcdPrlQcdQr.jpg|Cactus Graph Ef = (P,dP)(Q,dQ):pic]]

[[Cactus_Graph_Df_eq_llPcdPrlQcdQrcPQr.jpg|Cactus Graph Df = ((P,dP)(Q,dQ),PQ):pic]]

[[Venn_Diagram_PQ_Difference_Conj_At_Conj.jpg|Venn Diagram PQ Difference Conj At Conj:pic]]

[[Cactus_Graph_PQ_Difference_Conj_At_Conj.jpg|Cactus Graph PQ Difference Conj At Conj:pic]]

[[Cactus_Graph_Df_eq_llPcdPrlQcdQrcPQr.jpg|Cactus Graph Df = ((P,dP)(Q,dQ),PQ):pic]]

[[Cactus_Graph_DfaPQ_eq_lldPrldQrr.jpg|Cactus Graph Df@PQ = ((dP)(dQ)):pic]]

[[Cactus_Graph_DfaPlQr_eq_ldPrdQ.jpg|Cactus Graph Df@P(Q) = (dP)dQ:pic]]

[[Cactus_Graph_DfalPrQ_eq_dPldQr.jpg|Cactus Graph Df@(P)Q = dP(dQ):pic]]

[[Cactus_Graph_DfalPrlQr_eq_dP_dQ.jpg|Cactus Graph Df@(P)(Q) = dP dQ:pic]]

[[Cactus_Graph_Lobe_Rule.jpg|Cactus Graph Lobe Rule:pic]]

[[Cactus_Graph_Spike_Rule.jpg|Cactus Graph Spike Rule:pic]]

[[Venn_Diagram_PQ_Difference_Conj.jpg|Venn Diagram PQ Difference Conj:pic]]

[[Directed_Graph_PQ_Difference_Conj.jpg|Directed Graph PQ Difference Conj:pic]]

[[Cactus_Graph_Ef_eq_lPcdPrlQcdQr.jpg|Cactus Graph Ef = (P,dP)(Q,dQ):pic]]

[[Cactus_Graph_EfaPQ_eq_ldPrldQr.jpg|Cactus Graph Ef@PQ = (dP)(dQ):pic]]

[[Cactus_Graph_EfaPlQr_eq_ldPrdQ.jpg|Cactus Graph Ef@P(Q) = (dP)dQ:pic]]

[[Cactus_Graph_EfalPrQ_eq_dPldQr.jpg|Cactus Graph Ef@(P)Q = dP(dQ):pic]]

[[Cactus_Graph_EfalPrlQr_eq_dP_dQ.jpg|Cactus Graph Ef@(P)(Q) = dP dQ:pic]]
