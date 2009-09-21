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

All other propositional connectives can be obtained through combinations of these two forms.  Strictly speaking, the parenthesized form is sufficient to define the concatenated form, making the latter formally dispensable, but it is convenient to maintain it as a concise way of expressing more complicated combinations of parenthesized forms.  While working with expressions solely in propositional calculus, it is easiest to use plain parentheses for logical connectives.  In contexts where ordinary parentheses are needed for other purposes an alternate typeface --- e.g. $\text{&#x2997;} \text{&#xFE50;} \text{&#x2998;}$ --- may be used for logical operators.

Table&nbsp;1 collects a sample of basic propositional forms as expressed in terms of cactus connectives.

<table align="center" border="1" cellpadding="8" cellspacing="0" markdown="1" style="text-align:center; width:90%">

<caption><font size="+2">
$\text{Table 1.} \quad \text{Syntax and Semantics of a Calculus for Propositional Logic}$
</font></caption>

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
&amp; = &amp;
\text{&#x2997;} a \text{&#xFE50;&#x2997;} b \text{&#xFE50;} c \text{&#x2998;&#x2998;}
&amp; = &amp;
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

A function like this has an abstract type and a concrete type.  The abstract type is what we invoke when we write things like $f : \mathbb{B} \;\times\; \mathbb{B} \to \mathbb{B}$ or $f : \mathbb{B}^2 \to \mathbb{B}$.  The concrete type takes into account the qualitative dimensions or the "units" of the case, which can be explained as follows.

* Let $P$ be the set of values $\{ \text{&#x2997;} p \text{&#x2998;}, \; p \} \;=\; \{ \not p, \; p \} \;\cong\; \mathbb{B}$.

* Let $Q$ be the set of values $\{ \text{&#x2997;} q \text{&#x2998;}, \; q \} \;=\; \{ \not q, \; q \} \;\cong\; \mathbb{B}$.

Then interpret the usual propositions about $p, q$ as functions of the concrete type $f : P \;\times\; Q \to \mathbb{B}$.

We are going to consider various _operators_ on these functions.  Here, an operator $\mathop{F}$ is a function that takes one function $f$ into another function $\mathop{F}f$.

The first couple of operators that we need to consider are logical analogues of the pair that play a founding role in the classical finite difference calculus, namely:

* The _difference operator_ $\mathop{&Delta;}$, written here as $\mathop{D}$.

* The _enlargement operator_ $\mathop{&Epsilon;}$, written here as $\mathop{E}$.

These days, $\mathop{E}$ is more often called the _shift operator_.

In order to describe the universe in which these operators operate, it is necessary to enlarge the original universe of discourse.  Starting from the initial space $X = P \;\times\; Q$, its _(first order) differential extension_ $\mathop{E}X$ is constructed according to the following specifications:

<div markdown="1"><font size="+1">
$$\array{\arrayopts{\colalign{right center center}}
\mathop{E}X &amp; = &amp; X \;\times\; \mathop{d}X
}$$
</font></div>

where:

<div markdown="1"><font size="+1">
$$\array{
\arrayopts{\colalign{right center center}}
X &amp; = &amp; P \;\times\; Q
\\
\mathop{d}X &amp; = &amp; \mathop{d}P \;\times\; \mathop{d}Q
\\
\mathop{d}P &amp; = &amp; \{ \text{&#x2997;} \mathop{d}p \text{&#x2998;}, \; \mathop{d}p \}
\\
\mathop{d}Q &amp; = &amp; \{ \text{&#x2997;} \mathop{d}q \text{&#x2998;}, \; \mathop{d}q \}
}$$
</font></div>

The interpretations of these new symbols can be diverse, but the easiest option for now is just to say that $\mathop{d}p$ means &ldquo;$\mathop{change}\; p$&rdquo; and $\mathop{d}q$ means &ldquo;$\mathop{change}\; q$&rdquo;.

Drawing a venn diagram for the differential extension $\mathop{E}X = X \;\times\; \mathop{d}X$ requires four logical dimensions, $P, Q, \mathop{d}P, \mathop{d}Q$, but it is possible to project a suggestion of what the differential features $\mathop{d}p$ and $\mathop{d}q$ are about on the 2-dimensional base space $X = P \;\times\; Q$ by drawing arrows that cross the boundaries of the basic circles in the venn diagram for $X$, reading an arrow as $\mathop{d}p$ if it crosses the boundary between $p$ and $\text{&#x2997;} p \text{&#x2998;}$ in either direction and reading an arrow as $\mathop{d}q$ if it crosses the boundary between $q$ and $\text{&#x2997;} q \text{&#x2998;}$ in either direction.

<center>
<img alt="Venn Diagram P Q dP dQ" src="/nlab/files/Venn_Diagram_P_Q_dP_dQ.jpg" width="500" />
</center>

Propositions are formed on differential variables, or any combination of ordinary logical variables and differential logical variables, in the same ways that propositions are formed on ordinary logical variables alone.  For example, the proposition $\text{&#x2997;} \mathop{d}p \; \text{&#x2997;} \mathop{d}q \text{&#x2998;&#x2998;}$ says the same thing as  $\mathop{d}p \Rightarrow \mathop{d}q$, in other words, that there is no change in $p$ without a change in $q$.

Given the proposition $f(p, q)$ over the space $X = P \;\times\; Q$, the _(first order) enlargement_ of $f$ is the proposition $\mathop{E}f$ over the differential extension $\mathop{E}X$ that is defined by the
following formula:

<table align="center" cellpadding="8" markdown="1" style="border:none">

<td style="border:none"><font size="+1">
$
\mathop{E}f(p, q, \mathop{d}p, \mathop{d}q)
\; = \;
f(p + \mathop{d}p, \; q + \mathop{d}q)
\; = \;
f( \; \text{&#x2997;} p, \mathop{d}p \text{&#x2998;}, \; \text{&#x2997;} q, \mathop{d}q \text{&#x2998;} \; )
$
</font></td>

</table>

In the example $f(p, q) = p q$, the enlargement $\mathop{E}f$ is computed as follows:

<table align="center" cellpadding="8" markdown="1" style="border:none">

<tr>
<td style="border:none"><font size="+1">
$
\mathop{E}f(p, q, \mathop{d}p, \mathop{d}q)
\quad = \quad
(p + \mathop{d}p)(q + \mathop{d}q)
\quad = \quad
\text{&#x2997;} p, \mathop{d}p \text{&#x2998;&#x2997;} q, \mathop{d}q \text{&#x2998;}
$
</font></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Ef = (P,dP)(Q,dQ)" src="/nlab/files/Cactus_Graph_Ef_eq_lPcdPrlQcdQr.jpg" width="500" /></td></tr>

</table>

Given the proposition $f(p, q)$ over $X = P \;\times\; Q$, the _(first order) difference_ of $f$ is the proposition $\mathop{D}f$ over $\mathop{E}X$ that is defined by the formula $\mathop{D}f = \mathop{E}f - f$, or, written out in full:

<table align="center" cellpadding="8" markdown="1" style="border:none"><font size="+1">
<td style="border:none">
$\mathop{D}f(p, q, \mathop{d}p, \mathop{d}q)
\; = \;
f(p + \mathop{d}p, \; q + \mathop{d}q) - f(p, q)
\; = \;
\text{&#x2997;} f( \; \text{&#x2997;} p, \mathop{d}p \text{&#x2998;}, \; \text{&#x2997;} q, \mathop{d}q \text{&#x2998;} \; ), \; f(p, q) \text{&#x2998;}$</td>
</font></table>

In the example $f(p, q) = p q$, the difference $\mathop{D}f$ is computed as follows:

<table align="center" cellpadding="8" markdown="1" style="border:none">

<tr>
<td style="border:none"><font size="+1">
$
\mathop{D}f(p, q, \mathop{d}p, \mathop{d}q)
\; = \;
(p + \mathop{d}p)(q + \mathop{d}q) - p q
\; = \;
\text{&#x2997;&#x2997;} p, \mathop{d}p \text{&#x2998;&#x2997;} q, \mathop{d}q \text{&#x2998;}, p q \text{&#x2998;}
$
</font></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Df = ((P,dP)(Q,dQ),PQ)" src="/nlab/files/Cactus_Graph_Df_eq_llPcdPrlQcdQrcPQr.jpg" width="500" /></td></tr>

</table>

We did not yet go through the trouble to interpret this (first order) _difference of conjunction_ fully, but were happy simply to evaluate it with respect to a single location in the universe of discourse, namely, at the point picked out by the singular proposition $p q$, that is, at the place where $p = 1$ and $q = 1$.  This evaluation is written in the form $\mathop{D}f|_{p q}$ or $\mathop{D}f|_{(1, 1)}$, and we arrived at the locally applicable law that is stated and illustrated as follows:

<table align="center" cellpadding="8" markdown="1" style="border:none; text-align:center">

<tr>
<td style="border:none"><font size="+1">
$\array{
f(p, q)
&amp; = &amp;
p q
&amp; = &amp;
p \;\mathop{and}\; q
\\
&amp; &amp; \Downarrow
\\
\mathop{D}f|{p q}
&amp; = &amp;
\text{&#x2997;&#x2997;} \mathop{d}p \text{&#x2998;&#x2997;} \mathop{d}q \text{&#x2998;&#x2998;}
&amp; = &amp;
\mathop{d}p \;\mathop{or}\; \mathop{d}q
}$
</font></td></tr>

<tr>
<td style="border:none">
<img alt="Venn Diagram PQ Difference Conj At Conj" src="/nlab/files/Venn_Diagram_PQ_Difference_Conj_At_Conj.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph PQ Difference Conj At Conj" src="/nlab/files/Cactus_Graph_PQ_Difference_Conj_At_Conj.jpg" width="500" /></td></tr>

</table>

The venn diagram shows the analysis of the inclusive disjunction $\text{&#x2997;&#x2997;} \mathop{d}p \text{&#x2998;&#x2997;} \mathop{d}q \text{&#x2998;&#x2998;}$ into the following exclusive disjunction:

<div markdown="1"><font size="+1">
$$
\mathop{d}p \; \text{&#x2997;} \mathop{d}q \text{&#x2998;}
\quad + \quad
\text{&#x2997;} \mathop{d}p \text{&#x2998;} \; \mathop{d}q
\quad + \quad
\mathop{d}p \; \mathop{d}q
$$
</font></div>

The differential proposition that results may be interpreted to say "change $p$ or change $q$ or both".  And this can be recognized as just what you need to do if you happen to find yourself in the center cell and require a complete and detailed description of ways to escape it.

We have just computed what is variously called the _difference map_, the _difference proposition_, or the _local proposition_ $\mathop{D}f_x$ of the proposition $f(p, q) = p q$ at the point $x$ where $p = 1$ and $q = 1$.

In the universe $X = P \;\times\; Q$, the four propositions $p q, \; p \text{&#x2997;} q \text{&#x2998;}, \; \text{&#x2997;} p \text{&#x2998;} q, \; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}$ that indicate the "cells", or the smallest regions of the venn diagram, are called ''singular propositions''.  These serve as an alternative notation for naming the points $(1, 1), \; (1, 0), \; (0, 1), \; (0, 0)$, respectively.

Thus we can write $\mathop{D}f_x = \mathop{D}f|x = \mathop{D}f|(1, 1) = \mathop{D}f|p q$, so long as we know the frame of reference in force.

In the example $f(p, q) = p q$, the value of the difference proposition $\mathop{D}f_x$ at each of the four points in $x \in X$ may be computed in graphical fashion as shown below:

<table align="center" cellpadding="8" style="border:none">

<tr>
<td style="border:none">
<img alt="Cactus Graph Df = ((P,dP)(Q,dQ),PQ)" src="/nlab/files/Cactus_Graph_Df_eq_llPcdPrlQcdQrcPQr.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Df@PQ = ((dP)(dQ))" src="/nlab/files/Cactus_Graph_DfaPQ_eq_lldPrldQrr.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Df@P(Q) = (dP)dQ" src="/nlab/files/Cactus_Graph_DfaPlQr_eq_ldPrdQ.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Df@(P)Q = dP(dQ)" src="/nlab/files/Cactus_Graph_DfalPrQ_eq_dPldQr.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Df@(P)(Q) = dP dQ" src="/nlab/files/Cactus_Graph_DfalPrlQr_eq_dP_dQ.jpg" width="500" /></td></tr>

</table>

The easy way to visualize the values of these graphical expressions is just to notice the following equivalents:

<table align="center" cellpadding="8" style="border:none">

<tr>
<td style="border:none">
<img alt="Cactus Graph Lobe Rule" src="/nlab/files/Cactus_Graph_Lobe_Rule.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Spike Rule" src="/nlab/files/Cactus_Graph_Spike_Rule.jpg" width="500" /></td></tr>

</table>

Laying out the arrows on the augmented venn diagram, one gets a picture of a _differential vector field_.

<center>
<img alt="Venn Diagram PQ Difference Conj" src="/nlab/files/Venn_Diagram_PQ_Difference_Conj.jpg" width="500" />
</center>

The Figure shows the points of the extended universe $\mathop{E}X = P \;\times\; Q \;\times\; \mathop{d}P \;\times\; \mathop{d}Q$ that are indicated by the difference map $\mathop{D}f : \mathop{E}X \to \mathbb{B}$, namely, the following six points or singular propositions:

<div markdown="1"><font size="+1">
$$\array{
\arrayopts{\colalign{right center}}
1. &amp;
p &amp; q &amp; \mathop{d}p &amp; \mathop{d}q
\\
2. &amp;
p &amp; q &amp; \mathop{d}p &amp; \text{&#x2997;} \mathop{d}q \text{&#x2998;}
\\
3. &amp;
p &amp; q &amp; \text{&#x2997;} \mathop{d}p \text{&#x2998;} &amp; \mathop{d}q
\\
4. &amp;
p &amp; \text{&#x2997;} q \text{&#x2998;} &amp; \text{&#x2997;} \mathop{d}p \text{&#x2998;} &amp; \mathop{d}q
\\
5. &amp;
\text{&#x2997;} p \text{&#x2998;} &amp; q &amp; \mathop{d}p &amp; \text{&#x2997;} \mathop{d}q \text{&#x2998;}
\\
6. &amp;
\text{&#x2997;} p \text{&#x2998;} &amp; \text{&#x2997;} q \text{&#x2998;} &amp; \mathop{d}p &amp; \mathop{d}q
}$$
</font></div>

The information borne by $\mathop{D}f$ should be clear enough from a survey of these six points --- they tell you what you have to do from each point of $X$ in order to change the value borne by $f(p, q)$, that is, the move you have to make in order to reach a point where the value of the proposition $f(p, q)$ is different from what it is where you started.

We have been studying the action of the difference operator $\mathop{D}$ on propositions of the form $f : P \;\times\; Q \to \mathbb{B}$, as illustrated by the example $f(p, q) = p q$ that is known in logic as the conjunction of $p$ and $q$.  The resulting difference map $\mathop{D}f$ is a (first order) differential proposition, that is, a proposition of the form $\mathop{D}f : P \;\times\; Q \;\times\; \mathop{d}P \;\times\; \mathop{d}Q \to \mathbb{B}$.

Abstracting from the augmented venn diagram that shows how the _models_ or _satisfying interpretations_ of $\mathop{D}f$ distribute over the extended universe of discourse $\mathop{E}X = P \;\times\; Q \;\times\; \mathop{d}P \;\times\; \mathop{d}Q$, the difference map $\mathop{D}f$ can be represented in the form of a _digraph_ or _directed graph_, one whose points are labeled with the elements of $X =  P \;\times\; Q$ and whose arcs are labeled with the elements of $\mathop{d}X = \mathop{d}P \;\times\; \mathop{d}Q$, as shown in the following Figure.

<table align="center" cellpadding="8" markdown="1" style="border:none; text-align:center">

<tr>
<td style="border:none">
<img alt="Directed Graph PQ Difference Conj" src="/nlab/files/Directed_Graph_PQ_Difference_Conj.jpg" width="500" /></td></tr>

<tr>
<td style="border:none"><font size="+1">
$\array{\arrayopts{\colalign{right center}}
f &amp; = &amp; p &amp; \cdot &amp; q
\\
\mathop{D}f
&amp; = &amp;
p
&amp; \cdot &amp;
q
&amp; \cdot &amp;
\text{&#x2997;&#x2997;} \mathop{d}p \text{&#x2998;&#x2997;} \mathop{d}q \text{&#x2998;&#x2998;}
\\
&amp; + &amp;
p
&amp; \cdot &amp;
\text{&#x2997;} q \text{&#x2998;}
&amp; \cdot &amp;
\; \text{&#x2997;} \mathop{d}p \text{&#x2998;} \; \mathop{d}q \;\;
\\
&amp; + &amp;
\text{&#x2997;} p \text{&#x2998;}
&amp; \cdot &amp;
q
&amp; \cdot &amp;
\;\; \mathop{d}p \; \text{&#x2997;} \mathop{d}q \text{&#x2998;} \;
\\
&amp; + &amp;
\text{&#x2997;} p \text{&#x2998;}
&amp; \cdot &amp;
\text{&#x2997;} q \text{&#x2998;}
&amp; \cdot &amp;
\;\; \mathop{d}p \;\; \mathop{d}q \;
}$
</font></td></tr>

</table>

Any proposition worth its salt can be analyzed from many different points of view, any one of which has the potential to reveal an unsuspected aspect of the proposition's meaning.  We will encounter more and more of these alternative readings as we go.

The _enlargement_ or _shift_ operator $\mathop{E}$ exhibits a wealth of interesting and useful properties in its own right, so it pays to examine a few of the more salient features that play out on the surface of our initial example, $f(p, q) = p q$.

A suitably generic definition of the extended universe of discourse is afforded by the following set-up:

<table align="center" cellpadding="8" markdown="1" style="border:none; width:90%">
<td style="border:none"><font size="+1">
$\array{
\arrayopts{\colalign{left center center left}}
\text{Let}
&amp; X
&amp; = &amp; X_1 \;\times\; \ldots \;\times\; X_k.
\\
\text{Let}
&amp; \mathop{d}X
&amp; = &amp; \mathop{d}X_1 \;\times\; \ldots \;\times\; \mathop{d}X_k.
\\
\text{Then}
&amp; \mathop{E}X
&amp; = &amp; X \;\times\; \mathop{d}X
\\
&amp;
&amp; = &amp;
X_1 \;\times\; \ldots \;\times\; X_k \;\times\; \mathop{d}X_1 \;\times\; \ldots \;\times\; \mathop{d}X_k.
}$
</font></td>
</table>

For a proposition of the form $f : X_1 \;\times\; \ldots \;\times\; X_k \to \mathbb{B}$, the _(first order) enlargement_ of $f$ is the proposition $\mathop{E}f : \mathop{E}X \to \mathbb{B}$ that is defined by the following equation:

<table align="center" cellpadding="8" markdown="1" style="border:none; width:90%">
<td style="border:none"><font size="+1">
$\array{
\arrayopts{\colalign{left}}
\mathop{E}f(x_1, \ldots, x_k, \mathop{d}x_1, \ldots, \mathop{d}x_k)
\\
= \quad f(x_1 + \mathop{d}x_1, \ldots, x_k + \mathop{d}x_k)
\\
= \quad f( \; \text{&#x2997;} x_1, \mathop{d}x_1 \text{&#x2998;}, \ldots, \text{&#x2997;} x_k, \mathop{d}x_k \text{&#x2998;} \; )
}$
</font></td>
</table>

The _differential variables_ $\mathop{d}x_j$ are boolean variables of the same basic type as the ordinary variables $x_j$.  Although it is conventional to distinguish the (first order) differential variables with the operative prefix &ldquo;$\mathop{d}$&rdquo; this way of notating differential variables is entirely optional.  It is their existence in particular relations to the initial variables, not their names, that defines them as differential variables.

In the example of logical conjunction, $f(p, q) = p q$, the enlargement $\mathop{E}f$ is formulated as follows:

<div markdown="1"><font size="+1">
$$
\mathop{E}f(p, q, \mathop{d}p, \mathop{d}q)
\quad = \quad
(p + \mathop{d}p)(q + \mathop{d}q)
\quad = \quad
\text{&#x2997;} p \text{&#xFE50;} \mathop{d}p \text{&#x2998;}
\text{&#x2997;} q \text{&#xFE50;} \mathop{d}q \text{&#x2998;}
$$
</font></div>

Given that this expression uses nothing more than the boolean ring operations of addition and multiplication, it is permissible to "multiply things out" in the usual manner to arrive at the following result:

<div markdown="1"><font size="+1">
$$
\mathop{E}f(p, q, \mathop{d}p, \mathop{d}q)
\quad = \quad
p \: q
\quad + \quad
p \: \mathop{d}q
\quad + \quad
q \: \mathop{d}p
\quad + \quad
\mathop{d}p \: \mathop{d}q
$$
</font></div>

To understand what the _enlarged_ or _shifted_ proposition means in logical terms, it serves to go back and analyze the above expression for $\mathop{E}f$ in the same way that we did for $\mathop{D}f$.  Toward that end, the value of $\mathop{E}f_x$ at each $x \in X$ may be computed in graphical fashion as shown below:

<table align="center" cellpadding="8" style="border:none">

<tr>
<td style="border:none">
<img alt="Cactus Graph Ef = (P,dP)(Q,dQ)" src="/nlab/files/Cactus_Graph_Ef_eq_lPcdPrlQcdQr.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Ef@PQ = (dP)(dQ)" src="/nlab/files/Cactus_Graph_EfaPQ_eq_ldPrldQr.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Ef@P(Q) = (dP)dQ" src="/nlab/files/Cactus_Graph_EfaPlQr_eq_ldPrdQ.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Ef@(P)Q = dP(dQ)" src="/nlab/files/Cactus_Graph_EfalPrQ_eq_dPldQr.jpg" width="500" /></td></tr>

<tr>
<td style="border:none">
<img alt="Cactus Graph Ef@(P)(Q) = dP dQ" src="/nlab/files/Cactus_Graph_EfalPrlQr_eq_dP_dQ.jpg" width="500" /></td></tr>

</table>

Given the data that develops in this form of analysis, the disjoined ingredients can now be folded back into a _boolean expansion_ or a _disjunctive normal form_ (DNF) that is equivalent to the enlarged proposition $\mathop{E}f$.

<div markdown="1"><font size="+1">
$$
\mathop{E}f
\quad = \quad
p q \cdot \mathop{E}f_{p q}
\quad + \quad
p \text{&#x2997;} q \text{&#x2998;} \cdot \mathop{E}f_{p \text{&#x2997;} q \text{&#x2998;}}
\quad + \quad
\text{&#x2997;} p \text{&#x2998;} q \cdot \mathop{E}f_{\text{&#x2997;} p \text{&#x2998;} q}
\quad + \quad
\text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;} \cdot
\mathop{E}f_{\text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}}
$$
</font></div>

Here is a summary of the result, illustrated by means of a digraph picture, where the "no change" element $\text{&#x2997;} \mathop{d}p \text{&#x2998;&#x2997;} \mathop{d}q \text{&#x2998;}$ is drawn as a loop at the point $p \; q$.

<table align="center" cellpadding="8" markdown="1" style="border:none; text-align:center">

<tr>
<td style="border:none">
<img alt="Directed Graph PQ Enlargement Conj" src="/nlab/files/Directed_Graph_PQ_Enlargement_Conj.jpg" width="500" /></td></tr>

<tr>
<td style="border:none"><font size="+1">
$\array{\arrayopts{\colalign{right center}}
f &amp; = &amp; p &amp; \cdot &amp; q
\\
\mathop{E}f
&amp; = &amp;
p
&amp; \cdot &amp;
q
&amp; \cdot &amp;
\text{&#x2997;} \mathop{d}p \text{&#x2998;&#x2997;} \mathop{d}q \text{&#x2998;}
\\
&amp; + &amp;
p
&amp; \cdot &amp;
\text{&#x2997;} q \text{&#x2998;}
&amp; \cdot &amp;
\text{&#x2997;} \mathop{d}p \text{&#x2998;} \; \mathop{d}q \;
\\
&amp; + &amp;
\text{&#x2997;} p \text{&#x2998;}
&amp; \cdot &amp;
q
&amp; \cdot &amp;
\; \mathop{d}p \; \text{&#x2997;} \mathop{d}q \text{&#x2998;}
\\
&amp; + &amp;
\text{&#x2997;} p \text{&#x2998;}
&amp; \cdot &amp;
\text{&#x2997;} q \text{&#x2998;}
&amp; \cdot &amp;
\; \mathop{d}p \;\; \mathop{d}q \;
}$
</font></td></tr>

</table>

We may understand the enlarged proposition $\mathop{E}f$ as telling us all the different ways to reach a model of the proposition $f$ from each point of the universe $X$.

## Propositional Forms on Two Variables ##

To broaden our experience with simple examples, let us examine the sixteen functions of concrete type $P \;\times\; Q \to \mathbb{B}$ and abstract type $\mathbb{B} \;\times\; \mathbb{B} \to \mathbb{B}$.  A few Tables are set here that detail the actions of $\mathop{E}$ and $\mathop{D}$ on each of these functions, allowing us to view the results in several different ways.

Tables&nbsp;A1 and A2 show two ways of arranging the 16 boolean functions on two variables, giving equivalent expressions for each function in several different systems of notation.

<table align="center" border="1" cellpadding="0" cellspacing="0" markdown="1">
<caption><font size="+2">
$\text{Table A1.} \quad \text{Propositional Forms on Two Variables}$
</font></caption>
<td>
$\array{
\arrayopts{
\collines{solid}
\rowlines{none solid none solid
none none none none none none none solid none}}
\mathcal{L}_1 &amp; \mathcal{L}_2 &amp; \mathcal{L}_3 &amp;
\mathcal{L}_4 &amp; \mathcal{L}_5 &amp; \mathcal{L}_6
\\
\text{Decimal Index} &amp; \text{Binary Index} &amp;
\text{Truth Table} &amp; \text{Cactus Expression} &amp;
\text{English Paraphrase} &amp; \text{Conventional Notation}
\\
&amp; \cellopts{\colalign{right}} p: &amp; 1\:1\:0\:0 &amp; &amp; &amp;
\\
&amp; \cellopts{\colalign{right}} q: &amp; 1\:0\:1\:0 &amp; &amp; &amp;
\\
f_{0}
&amp; f_{0000}
&amp; 0\:0\:0\:0
&amp; \text{&#x2997;} \: \text{&#x2998;}
&amp; \mathop{false}
&amp; 0
\\
f_{1}
&amp; f_{0001}
&amp; 0\:0\:0\:1
&amp; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}
&amp; \mathop{neither}\: p \:\mathop{nor}\: q
&amp; \not p \:\wedge\: \not q
\\
f_{2}
&amp; f_{0010}
&amp; 0\:0\:1\:0
&amp; \text{&#x2997;} p\text{&#x2998;} \: q
&amp; q \:\mathop{without}\: p
&amp; \not p \:\wedge\: q
\\
f_{3}
&amp; f_{0011}
&amp; 0\:0\:1\:1
&amp; \text{&#x2997;} p \text{&#x2998;}
&amp; \mathop{not}\: p
&amp; \not p
\\
f_{4}
&amp; f_{0100}
&amp; 0\:1\:0\:0
&amp; p \: \text{&#x2997;} q \text{&#x2998;}
&amp; p \:\mathop{without}\: q
&amp; p \:\wedge\: \not q
\\
f_{5}
&amp; f_{0101}
&amp; 0\:1\:0\:1
&amp; \text{&#x2997;} q \text{&#x2998;}
&amp; \mathop{not}\: q
&amp; \not q
\\
f_{6}
&amp; f_{0110}
&amp; 0\:1\:1\:0
&amp; \text{&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;}
&amp; p \:\mathop{not equal to}\: q
&amp; p \ne q
\\
f_{7}
&amp; f_{0111}
&amp; 0\:1\:1\:1
&amp; \text{&#x2997;} p \: q \text{&#x2998;}
&amp; \mathop{not both}\: p \:\mathop{and}\: q
&amp; \not p \:\vee\: \not q
\\
f_{8}
&amp; f_{1000}
&amp; 1\:0\:0\:0
&amp; p \: q
&amp; p \:\mathop{and}\: q
&amp; p \:\wedge\: q
\\
f_{9}
&amp; f_{1001}
&amp; 1\:0\:0\:1
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;&#x2998;}
&amp; p \:\mathop{equal to}\: q
&amp; p = q
\\
f_{10}
&amp; f_{1010}
&amp; 1\:0\:1\:0
&amp; q
&amp; q
&amp; q
\\
f_{11}
&amp; f_{1011}
&amp; 1\:0\:1\:1
&amp; \text{&#x2997;} p \: \text{&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \mathop{not}\: p \:\mathop{without}\: q
&amp; p \Rightarrow q
\\
f_{12}
&amp; f_{1100}
&amp; 1\:1\:0\:0
&amp; p
&amp; p
&amp; p
\\
f_{13}
&amp; f_{1101}
&amp; 1\:1\:0\:1
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;} \: q \text{&#x2998;}
&amp; \mathop{not}\: q \:\mathop{without}\: p
&amp; p \Leftarrow q
\\
f_{14}
&amp; f_{1110}
&amp; 1\:1\:1\:0
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;&#x2998;}
&amp; p \:\mathop{or}\: q
&amp; p \:\vee\: q
\\
f_{15}
&amp; f_{1111}
&amp; 1\:1\:1\:1
&amp; \text{&#x2997;&#x2997;} \: \text{&#x2998;&#x2998;}
&amp; \mathop{true}
&amp; 1
}$
</td>
</table>

<br>

<table align="center" border="1" cellpadding="0" cellspacing="0" markdown="1">
<caption><font size="+2">
$\text{Table A2.} \quad \text{Propositional Forms on Two Variables by Group Orbits}$
</font></caption>
<td>
$\array{
\arrayopts{
\collines{solid}
\rowlines{none solid none solid
solid none none none solid none solid none solid none solid none none none solid}}
\mathcal{L}_1 &amp; \mathcal{L}_2 &amp; \mathcal{L}_3 &amp;
\mathcal{L}_4 &amp; \mathcal{L}_5 &amp; \mathcal{L}_6
\\
\text{Decimal Index} &amp; \text{Binary Index} &amp;
\text{Truth Table} &amp; \text{Cactus Expression} &amp;
\text{English Paraphrase} &amp; \text{Conventional Notation}
\\
&amp; \cellopts{\colalign{right}} p: &amp; 1\:1\:0\:0 &amp; &amp; &amp;
\\
&amp; \cellopts{\colalign{right}} q: &amp; 1\:0\:1\:0 &amp; &amp; &amp;
\\
f_{0}
&amp; f_{0000}
&amp; 0\:0\:0\:0
&amp; \text{&#x2997;} \: \text{&#x2998;}
&amp; \mathop{false}
&amp; 0
\\
f_{1}
&amp; f_{0001}
&amp; 0\:0\:0\:1
&amp; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}
&amp; \mathop{neither}\: p \:\mathop{nor}\: q
&amp; \not p \:\wedge\: \not q
\\
f_{2}
&amp; f_{0010}
&amp; 0\:0\:1\:0
&amp; \text{&#x2997;} p\text{&#x2998;} \: q
&amp; q \:\mathop{without}\: p
&amp; \not p \:\wedge\: q
\\
f_{4}
&amp; f_{0100}
&amp; 0\:1\:0\:0
&amp; p \: \text{&#x2997;} q \text{&#x2998;}
&amp; p \:\mathop{without}\: q
&amp; p \:\wedge\: \not q
\\
f_{8}
&amp; f_{1000}
&amp; 1\:0\:0\:0
&amp; p \: q
&amp; p \:\mathop{and}\: q
&amp; p \:\wedge\: q
\\
f_{3}
&amp; f_{0011}
&amp; 0\:0\:1\:1
&amp; \text{&#x2997;} p \text{&#x2998;}
&amp; \mathop{not}\: p
&amp; \not p
\\
f_{12}
&amp; f_{1100}
&amp; 1\:1\:0\:0
&amp; p
&amp; p
&amp; p
\\
f_{6}
&amp; f_{0110}
&amp; 0\:1\:1\:0
&amp; \text{&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;}
&amp; p \:\mathop{not equal to}\: q
&amp; p \ne q
\\
f_{9}
&amp; f_{1001}
&amp; 1\:0\:0\:1
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;&#x2998;}
&amp; p \:\mathop{equal to}\: q
&amp; p = q
\\
f_{5}
&amp; f_{0101}
&amp; 0\:1\:0\:1
&amp; \text{&#x2997;} q \text{&#x2998;}
&amp; \mathop{not}\: q
&amp; \not q
\\
f_{10}
&amp; f_{1010}
&amp; 1\:0\:1\:0
&amp; q
&amp; q
&amp; q
\\
f_{7}
&amp; f_{0111}
&amp; 0\:1\:1\:1
&amp; \text{&#x2997;} p \: q \text{&#x2998;}
&amp; \mathop{not both}\: p \:\mathop{and}\: q
&amp; \not p \:\vee\: \not q
\\
f_{11}
&amp; f_{1011}
&amp; 1\:0\:1\:1
&amp; \text{&#x2997;} p \: \text{&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \mathop{not}\: p \:\mathop{without}\: q
&amp; p \Rightarrow q
\\
f_{13}
&amp; f_{1101}
&amp; 1\:1\:0\:1
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;} \: q \text{&#x2998;}
&amp; \mathop{not}\: q \:\mathop{without}\: p
&amp; p \Leftarrow q
\\
f_{14}
&amp; f_{1110}
&amp; 1\:1\:1\:0
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;&#x2998;}
&amp; p \:\mathop{or}\: q
&amp; p \:\vee\: q
\\
f_{15}
&amp; f_{1111}
&amp; 1\:1\:1\:1
&amp; \text{&#x2997;&#x2997;} \: \text{&#x2998;&#x2998;}
&amp; \mathop{true}
&amp; 1
}$
</td>
</table>

## Transforms Expanded over Differential Features ##

The next four Tables expand the expressions of $\mathop{E}f$ and $\mathop{D}f$ in two different ways, for each of the sixteen functions $f : \mathbb{B} \:\times\: \mathbb{B} \to \mathbb{B}$.  Notice that the functions are arranged by their $G$-orbits under the action of the group $G = \{ \mathop{T}_{00}, \mathop{T}_{01}, \mathop{T}_{10}, \mathop{T}_{11} \} \cong V_4$.

<table align="center" border="1" cellpadding="0" cellspacing="0" markdown="1" style="text-align:center">
<caption><font size="+2">
$\text{Table A3.} \quad \mathop{E}f \:\text{Expanded Over Differential Features}\: \{ \mathop{d}p, \mathop{d}q \}$
</font></caption>
<td>
$\array{
\arrayopts{
\collines{solid}
\rowlines{solid solid none none none solid none solid none solid none solid none none none solid}}
&amp;
\phantom{xxxx} f \phantom{xxxx}
&amp;
\phantom{xxxx}
\array{\mathop{T}_{11} f \\ \mathop{E} f|_{\mathop{d}p \: \mathop{d}q} }
\phantom{xxxx}
&amp;
\phantom{xxxx}
\array{\mathop{T}_{10} f \\ \mathop{E} f|_{\mathop{d}p \: \text{&#x2997;} \mathop{d}q \text{&#x2998;}} }
\phantom{xxxx}
&amp;
\phantom{xxxx}
\array{\mathop{T}_{01} f \\ \mathop{E} f|_{\text{&#x2997;} \mathop{d}p \text{&#x2998;} \: \mathop{d}q} }
\phantom{xxxx}
&amp;
\phantom{xxxx}
\array{\mathop{T}_{00} f \\ \mathop{E} f|_{\text{&#x2997;} \mathop{d}p \text{&#x2998;&#x2997;} \mathop{d}q \text{&#x2998;}} }
\phantom{xxxx}
\\
f_{0}
&amp; \text{&#x2997;} \: \text{&#x2998;}
&amp; \text{&#x2997;} \: \text{&#x2998;}
&amp; \text{&#x2997;} \: \text{&#x2998;}
&amp; \text{&#x2997;} \: \text{&#x2998;}
&amp; \text{&#x2997;} \: \text{&#x2998;}
\\
f_{1}
&amp; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}
&amp; p \: q
&amp; p \: \text{&#x2997;} q \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#x2998;} \: q
&amp; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}
\\
f_{2}
&amp; \text{&#x2997;} p \text{&#x2998;} \: q
&amp; p \: \text{&#x2997;} q \text{&#x2998;}
&amp; p \: q
&amp; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#x2998;} \: q
\\
f_{4}
&amp; p \: \text{&#x2997;} q \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#x2998;} \: q
&amp; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}
&amp; p \: q
&amp; p \: \text{&#x2997;} q \text{&#x2998;}
\\
f_{8}
&amp; p \: q
&amp; \text{&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#x2998;} q
&amp; p \text{&#x2997;} q \text{&#x2998;}
&amp; p \: q
\\
f_{3}
&amp; \text{&#x2997;} p \text{&#x2998;}
&amp; p
&amp; p
&amp; \text{&#x2997;} p \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#x2998;}
\\
f_{12}
&amp; p
&amp; \text{&#x2997;} p \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#x2998;}
&amp; p
&amp; p
\\
f_{6}
&amp; \text{&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;}
\\
f_{9}
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;}
&amp; \text{&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} \: q \text{&#x2998;&#x2998;}
\\
f_{5}
&amp; \text{&#x2997;} q \text{&#x2998;}
&amp; q
&amp; \text{&#x2997;} q \text{&#x2998;}
&amp; q
&amp; \text{&#x2997;} q \text{&#x2998;}
\\
f_{10}
&amp; q
&amp; \text{&#x2997;} q \text{&#x2998;}
&amp; q
&amp; \text{&#x2997;} q \text{&#x2998;}
&amp; q
\\
f_{7}
&amp; \text{&#x2997;} p \: q \text{&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;} \: q \text{&#x2998;}
&amp; \text{&#x2997;} p \: \text{&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;} p \: q \text{&#x2998;}
\\
f_{11}
&amp; \text{&#x2997;} p \: \text{&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;} \: q \text{&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;} p \: q \text{&#x2998;}
&amp; \text{&#x2997;} p \: \text{&#x2997;} q \text{&#x2998;&#x2998;}
\\
f_{13}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;} \: q \text{&#x2998;}
&amp; \text{&#x2997;} p \: \text{&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;} p \: q \text{&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;} \: q \text{&#x2998;}
\\
f_{14}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;} p \: q \text{&#x2998;}
&amp; \text{&#x2997;} p \: \text{&#x2997;} q \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;} \: q \text{&#x2998;}
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#x2997;} q \text{&#x2998;&#x2998;}
\\
f_{15}
&amp; \text{&#x2997;&#x2997;} \: \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} \: \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} \: \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} \: \text{&#x2998;&#x2998;}
&amp; \text{&#x2997;&#x2997;} \: \text{&#x2998;&#x2998;}
\\
\cellopts{\colspan{2}} \text{Fixed Point Total}
&amp;  4
&amp;  4
&amp;  4
&amp; 16
}$
</td>
</table>

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

: $\varnothing$
