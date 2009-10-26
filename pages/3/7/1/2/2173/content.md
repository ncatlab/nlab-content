[[!redirects mno]]
[[!redirects minimal negation]]
[[!redirects minimal negations]]
[[!redirects Minimal Negation Operator]]
[[!redirects Minimal Negation Operators]]
[[!redirects minimal negation operators]]
[[!redirects minimal negation operation]]
[[!redirects minimal negation operations]]
[[!redirects logical boundary operator]]
[[!redirects logical boundary operators]]
[[!redirects logical boundary operation]]
[[!redirects logical boundary operations]]

* tic
{:toc}

# Definition #

The __minimal negation operator__ $\nu$ is a [[multigrade operator]] $(\nu_k)_{k \in \mathbb{N}}$ where each $\nu_k$ is a $k$-ary [[boolean function]] $\nu_k : \mathbb{B}^k \to \mathbb{B}$ defined in such a way that $\nu_k (x_1, \ldots, x_k) = 1$ in just those cases where exactly one of the $x_j$ is $0$.

In contexts where the initial letter $\nu$ is understood, the minimal negation operators may be indicated by argument lists in parentheses.  In the following text a distinctive typeface is used for logical expressions based on minimal negation operators, for example, $\text{&#10647;} x \text{&#65104;} y \text{&#65104;} z \text{&#10648;} = \nu (x, y, z)$.

The first four members of this family of operators are shown below, with paraphrases in a couple of other notations, where tildes and primes, respectively, indicate logical negation.

<font size="+1">
<table align="center" cellpadding="4" markdown="1" style="border:none; text-align:center; width:90%">

<tr>
<td style="border:none">$\text{&#x2997;} \text{&#x2998;}$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\nu_0$</td>
<td style="border:none">$=$</td>
<td style="border:none">$0$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\mathop{false}$</td></tr>

<tr>
<td style="border:none">$\text{&#x2997;} x \text{&#x2998;}$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\nu_1 (x)$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\tilde{x}$</td>
<td style="border:none">$=$</td>
<td style="border:none">$x'$</td></tr>

<tr>
<td style="border:none">$\text{&#x2997;} x \text{&#xFE50;} y \text{&#x2998;}$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\nu_2 (x, y)$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\tilde{x} y \; \vee \; x \tilde{y}$</td>
<td style="border:none">$=$</td>
<td style="border:none">$x' y \; \vee \; x y'$</td></tr>

<tr>
<td style="border:none">$\text{&#x2997;} x \text{&#xFE50;} y \text{&#xFE50;} z \text{&#x2998;}$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\nu_3 (x, y, z)$</td>
<td style="border:none">$=$</td>
<td style="border:none">$\tilde{x} y z \; \vee \; x \tilde{y} z \; \vee \; x y \tilde{z}$</td>
<td style="border:none">$=$</td>
<td style="border:none">$x' y z \; \vee \; x y' z \; \vee \; x y z'$</td></tr>

</table></font>

To express the general case of $\nu_k$ in terms of familiar operations, it helps to introduce an intermediary concept:

+-- {: .un_defn}
###### Definition
Let the function $\neg_j : \mathbb{B}^k \to \mathbb{B}$ be defined for each integer $j$ in the interval $[1, k]$ by the following equation:

\[ \neg_j (x_1, \ldots, x_j, \ldots, x_k)  =  x_1 \:\wedge\: \cdots \:\wedge\: x_{j-1} \:\wedge\: \neg x_j \:\wedge\: x_{j+1} \:\wedge\: \cdots \:\wedge\: x_k . \]

Then $\nu_k : \mathbb{B}^k \to \mathbb{B}$ is defined by the following equation:

\[ \nu_k (x_1, \ldots, x_k)  =  \neg_1 (x_1, \ldots, x_k) \:\vee\: \cdots \:\vee\: \neg_j (x_1, \ldots, x_k) \:\vee\: \cdots \:\vee\: \neg_k (x_1, \ldots, x_k) . \]
=--

If we think of the point $x = (x_1, \ldots, x_k) \in \mathbb{B}^k$ as indicated by the boolean product $x_1 \cdot \ldots \cdot x_k$ or the logical conjunction $x_1 \; \wedge \; \ldots \; \wedge \; x_k$, then the minimal negation $\text{&#x2997;} x_1 \text{&#xFE50;} \ldots \text{&#xFE50;} x_k \text{&#x2998;}$ indicates the set of points in $\mathbb{B}^k$ that differ from $x$ in exactly one coordinate.  This makes $\text{&#x2997;} x_1 \text{&#xFE50;} \ldots \text{&#xFE50;} x_k \text{&#x2998;}$ a discrete functional analogue of a _point omitted neighborhood_ in analysis, more exactly, a _point omitted distance one neighborhood_.  In this light, the minimal negation operator can be recognized as a particular type of differential construction, an observation that opens a very wide field.  It also serves to explain a variety of other names for the same concept, for example, _logical boundary operator_ and _least action operator_.  The rationale for these names is visible in the venn diagrams of the corresponding operations on sets.

The remainder of this discussion proceeds on the _algebraic boolean convention_ that the plus sign $(+)$ and the summation symbol $(\textstyle\sum)$ both refer to addition modulo 2.  Unless otherwise noted, the boolean domain $\mathbb{B} = \{ 0, 1 \}$ is interpreted so that $0 = \mathop{false}$ and $1 = \mathop{true}$.  This has the following consequences:

*  The operation $x + y$ is a function equivalent to the exclusive disjunction of $x$ and $y$, while its fiber of $1$ is the relation of inequality between $x$ and $y$.

*  The operation $\textstyle\sum_{j=1}^k x_j$ maps the bit sequence $(x_1, \ldots, x_k)$ to its _parity_.

The following properties of the minimal negation operators $\nu_k : \mathbb{B}^k \to \mathbb{B}$ may be noted:

*  The function $\text{&#x2997;} x \text{&#xFE50;} y \text{&#x2998;}$ is the same as that associated with the operation $x + y$ and the relation $x \ne y$.

*  In contrast, $\text{&#x2997;} x \text{&#xFE50;} y \text{&#xFE50;} z \text{&#x2998;}$ is not identical to $x + y + z$.

*  More generally, the function $\nu_k (x_1, \dots, x_k)$ for $k \gt 2$ is not identical to the boolean sum $\textstyle\sum_{j=1}^k x_j$.

*  The inclusive disjunctions indicated for the $\nu_k$ of more than one argument may be replaced with exclusive disjunctions without affecting the meaning, since the terms disjoined are already disjoint.

# Truth tables #

Table 1 is a truth table for the sixteen boolean functions of type $f : \mathbb{B}^3 \to \mathbb{B}$, each of which is either a boundary of a point in $\mathbb{B}^3$ or the complement of such a boundary.

<table align="center" border="1" cellpadding="4" markdown="1">

<caption><font size="+2">
$\text{Table 1.} \:\: \text{Logical Boundaries and Their Complements}$
</font></caption>

<td>
$\array{
\arrayopts{
\collines{solid}
\rowlines{none solid none none solid none none none none none none none solid none}}
\mathcal{L}_1
&amp; \mathcal{L}_2
&amp; \mathcal{L}_3
&amp; \mathcal{L}_4
\\
\text{Decimal Index}
&amp; \text{Binary Index}
&amp; \phantom{mmm} \text{Truth Table} \phantom{mmm}
&amp; \phantom{mmm} \text{Cactus Form} \phantom{mmm}
\\
&amp; \cellopts{\colalign{right}} p:
&amp; 1 \: 1 \: 1 \: 1 \: 0 \: 0 \: 0 \: 0
&amp;
\\
&amp; \cellopts{\colalign{right}} q:
&amp; 1 \: 1 \: 0 \: 0 \: 1 \: 1 \: 0 \: 0
&amp;
\\
&amp; \cellopts{\colalign{right}} r:
&amp; 1 \: 0 \: 1 \: 0 \: 1 \: 0 \: 1 \: 0
&amp;
\\
f_{104}
&amp; f_{01101000}
&amp; 0 \: 1 \: 1 \: 0 \: 1 \: 0 \: 0 \: 0
&amp; \text{&#x2997;} p \text{&#xFE50;} q \text{&#xFE50;} r \text{&#x2998;}
\\
f_{148}
&amp; f_{10010100}
&amp; 1 \: 0 \: 0 \: 1 \: 0 \: 1 \: 0 \: 0
&amp; \text{&#x2997;} p \text{&#xFE50;} q \text{&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;}
\\
f_{146}
&amp; f_{10010010}
&amp; 1 \: 0 \: 0 \: 1 \: 0 \: 0 \: 1 \: 0
&amp; \text{&#x2997;} p \text{&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;} r \text{&#x2998;}
\\
f_{97}
&amp; f_{01100001}
&amp; 0 \: 1 \: 1 \: 0 \: 0 \: 0 \: 0 \: 1
&amp; \text{&#x2997;} p \text{&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;}
\\
f_{134}
&amp; f_{10000110}
&amp; 1 \: 0 \: 0 \: 0 \: 0 \: 1 \: 1 \: 0
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;} q \text{&#xFE50;} r \text{&#x2998;}
\\
f_{73}
&amp; f_{01001001}
&amp; 0 \: 1 \: 0 \: 0 \: 1 \: 0 \: 0 \: 1
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;} q \text{&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;}
\\
f_{41}
&amp; f_{00101001}
&amp; 0 \: 0 \: 1 \: 0 \: 1 \: 0 \: 0 \: 1
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;} r \text{&#x2998;}
\\
f_{22}
&amp; f_{00010110}
&amp; 0 \: 0 \: 0 \: 1 \: 0 \: 1 \: 1 \: 0
&amp; \text{&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;}
\\
f_{233}
&amp; f_{11101001}
&amp; 1 \: 1 \: 1 \: 0 \: 1 \: 0 \: 0 \: 1
&amp; \text{&#x2997;&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;&#x2998;}
\\
f_{214}
&amp; f_{11010110}
&amp; 1 \: 1 \: 0 \: 1 \: 0 \: 1 \: 1 \: 0
&amp; \text{&#x2997;&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;} r \text{&#x2998;&#x2998;}
\\
f_{182}
&amp; f_{10110110}
&amp; 1 \: 0 \: 1 \: 1 \: 0 \: 1 \: 1 \: 0
&amp; \text{&#x2997;&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;} q \text{&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;&#x2998;}
\\
f_{121}
&amp; f_{01111001}
&amp; 0 \: 1 \: 1 \: 1 \: 1 \: 0 \: 0 \: 1
&amp; \text{&#x2997;&#x2997;&#x2997;} p \text{&#x2998;&#xFE50;} q \text{&#xFE50;} r \text{&#x2998;&#x2998;}
\\
f_{158}
&amp; f_{10011110}
&amp; 1 \: 0 \: 0 \: 1 \: 1 \: 1 \: 1 \: 0
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;&#x2998;}
\\
f_{109}
&amp; f_{01101101}
&amp; 0 \: 1 \: 1 \: 0 \: 1 \: 1 \: 0 \: 1
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;&#x2997;} q \text{&#x2998;&#xFE50;} r \text{&#x2998;&#x2998;}
\\
f_{107}
&amp; f_{01101011}
&amp; 0 \: 1 \: 1 \: 0 \: 1 \: 0 \: 1 \: 1
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} q \text{&#xFE50;&#x2997;} r \text{&#x2998;&#x2998;&#x2998;}
\\
f_{151}
&amp; f_{10010111}
&amp; 1 \: 0 \: 0 \: 1 \: 0 \: 1 \: 1 \: 1
&amp; \text{&#x2997;&#x2997;} p \text{&#xFE50;} q \text{&#xFE50;} r \text{&#x2998;&#x2998;}
}$

</td></table>

# Charts and graphs #

This Section focuses on visual representations of minimal negation operators.  A few bits of terminology are useful in describing the pictures, but the formal details are tedious reading, and may be familiar to many readers, so the full definitions of the terms marked in bold are relegated to a Glossary at the end of the article.

Two ways of visualizing the space $\mathbb{B}^k$ of $2^k$ points are the _hypercube_ picture and the _venn diagram_ picture.  The hypercube picture associates each point of $\mathbb{B}^k$ with a unique point of the $k$-dimensional hypercube (the $k$-[[cube]]).  The venn diagram picture associates each point of $\mathbb{B}^k$ with a unique "cell" of the venn diagram on $k$ "circles".

In addition, each point of $\mathbb{B}^k$ is the unique point in the __fiber of truth__ $[|s|]$ of a __singular proposition__ $s : \mathbb{B}^k \to \mathbb{B}$, and thus it is the unique point where a __singular conjunction__ of $k$ __literals__ is equal to 1.

For example, consider two cases at opposite vertices of the $k$-cube:

*  The point $(1, 1, \ldots, 1, 1)$ with all $1$s as coordinates is the point where the conjunction of all posited variables evaluates to 1, namely, the point where:

   : $x_1   x_2  \cdots  x_{k-1}   x_k  =  1$
*  The point $(0, 0, \ldots, 0, 0)$ with all $0$s as coordinates is the point where the conjunction of all negated variables evaluates to 1, namely, the point where:

   : `(`$x_1$`)(`$x_2$`)`$\cdots$`(`$x_{k-1}$`)(`$x_k$`)`$ =  1$

To pass from these limiting examples to the general case, observe that a singular proposition $s : \mathbb{B}^k \to \mathbb{B}$ can be given canonical expression as a conjunction of literals, $s = e_1   e_2  \cdots  e_{k-1}   e_k$.  Then the proposition $\nu(e_1, e_2, \ldots, e_{k-1}, e_k)$ is $1$ on the points adjacent to the point where $s$ is 1, and $0$ everywhere else on the cube.

For example, consider the case where $k = 3$.  Then the minimal negation operation $\nu(p, q, r)$ --- written more simply as `(p, q, r)` --- has the following venn diagram:

![Venn Diagram (p,q,r)](http://mywikibiz.com/images/1/11/Venn_Diagram_%28P%2CQ%2CR%29.jpg)

Figure 2.  `(p, q, r)`

For a contrasting example, the boolean function expressed by the form `((p),(q),(r))` has the following venn diagram:

![Venn Diagram ((p),(q),(r))](http://mywikibiz.com/images/a/a8/Venn_Diagram_%28%28P%29%2C%28Q%29%2C%28R%29%29.jpg)

Figure 3.  `((p),(q),(r))`

# Glossary of basic terms #

*  A __boolean domain__ $\mathbb{B}$ is a generic 2-element set, say, $\mathbb{B} = \{ 0, 1 \}$, whose elements are interpreted as logical values, usually but not invariably with $0$ = _false_ and $1$ = _true_.

*  A __boolean variable__ $x$ is a variable that takes its value from a boolean domain, as $x \in \mathbb{B}$.

*  In situations where boolean values are interpreted as logical values, a boolean-valued function $f : X \to \mathbb{B}$ or a boolean function $g : \mathbb{B}^k \to \mathbb{B}$ is frequently called a __proposition__.

*  Given a sequence of $k$ boolean variables, $x_1, \ldots, x_k$, each variable $x_j$ may be treated either as a basis element of the space $\mathbb{B}^k$ or as a coordinate projection $x_j : \mathbb{B}^k \to \mathbb{B}$.

*  This means that the $k$ objects $x_j$ for $j$ = $1$ to $k$ are just so many boolean functions $x_j : \mathbb{B}^k \to \mathbb{B}$, subject to logical interpretation as a set of _basic propositions_ that generate the complete set of $2^{2^k}$ propositions over $\mathbb{B}^k$.

*  A __literal__ is one of the $2k$ propositions $x_1, \ldots, x_k, $`(`$ x_1 $`)`$, \ldots, $`(`$ x_k $`)`, in other words, either a _posited_ basic proposition $x_j$ or a _negated_ basic proposition `(`$ x_j $`)`, for some $j$ = $1$ to $k$.

*  In mathematics generally, the __fiber__ of a point $y$ under a function $f : X \to Y$ is defined as the inverse image $f^{-1}(y)$.

*  In the case of a boolean-valued function $f : X \to \mathbb{B}$, there are just two fibers:
   *  The fiber of $0$ under $f$, defined as $f^{-1}(0)$, is the set of points where $f$ is 0.
   *  The fiber of $1$ under $f$, defined as $f^{-1}(1)$, is the set of points where $f$ is 1.

*  When $1$ is interpreted as the logical value _true_, then $f^{-1}(1)$ is called the __fiber of truth__ in the proposition $f$.  Frequent mention of this fiber makes it useful to have a shorter way of referring to it.  This leads to the definition of the notation $[|f|] = f^{-1}(1)$ for the fiber of truth in the proposition $f$.

*  A __singular boolean function__ $s : \mathbb{B}^k \to \mathbb{B}$ is a boolean function whose fiber of $1$ is a single point of $\mathbb{B}^k$.

*  In the interpretation where $1$ equals _true_, a singular boolean function is called a __singular proposition__.

*  Singular boolean functions and singular propositions serve as functional or logical representatives of the points in $\mathbb{B}^k$.

*  A __singular conjunction__ in $(\mathbb{B}^k \to \mathbb{B})$ is a conjunction of $k$ literals that includes just one conjunct of the pair $\{ x_j,   \nu(x_j) \}$ for each $j$ = $1$ to $k$.

*  A singular proposition $s : \mathbb{B}^k \to \mathbb{B}$ can be expressed as a singular conjunction:
   $$s = e_1 \, e_2 \, \cdots \, e_{k-1} \, e_k$$
   where $e_j = x_j$ or $e_j = \nu(x_j)$ for $j = 1$ to $k$

# External links #

* [Minimal Negation Operator @ MyWikiBiz](http://mywikibiz.com/Minimal_negation_operator)

* [Minimal Negation Operator @ PlanetMath](http://planetmath.org/encyclopedia/MinimalNegationOperator.html)

* [Minimal Negation Operator @ PlanetPhysics](http://planetphysics.org/encyclopedia/MinimalNegationOperator.html)

* [Minimal Negation Operator @ ProofWiki](http://www.proofwiki.org/wiki/Definition:Minimal_Negation_Operator)
