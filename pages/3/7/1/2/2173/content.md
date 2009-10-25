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

The __minimal negation operator__ $\nu$ is a [[multigrade operator]] $(\nu_k)_{k \in \mathbb{N}}$ where each $\nu_k$ is a $k$-ary [[boolean function]] defined in such a way that $\nu_k (x_1, \ldots, x_k) = 1$ in just those cases where exactly one of the arguments $x_j$ is $0$.

In contexts where the initial letter $\nu$ is understood, the minimal negation operators can be indicated by argument lists in parentheses.  In the following text a distinctive typeface will be used for logical expressions based on minimal negation operators, for example, `(x, y, z)` = $\nu (x, y, z)$.

The first four members of this family of operators are shown below, with paraphrases in a couple of other notations, where tildes and primes, respectively, indicate logical negation.

*  `()` $= \nu_0 = 0 = false$

*  `(x)` $= \nu_1 (x) = \tilde{x} = x'$

*  `(x, y)` $= \nu_2 (x, y) = \tilde{x} y \:\vee\: x \tilde{y} = x' y \:\vee\: x y'$

*  `(x, y, z)` $= \nu_3 (x, y, z) = \tilde{x} y z \:\vee\: x \tilde{y} z \:\vee\: x y \tilde{z} = x' y z \:\vee\: x y' z \:\vee\: x y z'$

To express the general case of $\nu_k$ in terms of familiar operations, it helps to introduce an intermediary concept:

+-- {: .un_defn}
###### Definition
Let the function $\neg_j : \mathbb{B}^k \to \mathbb{B}$ be defined for each integer $j$ in the interval $[1, k]$ by the following equation:

\[ \neg_j (x_1, \ldots, x_j, \ldots, x_k)  =  x_1 \:\wedge\: \cdots \:\wedge\: x_{j-1} \:\wedge\: \neg x_j \:\wedge\: x_{j+1} \:\wedge\: \cdots \:\wedge\: x_k . \]

Then $\nu_k : \mathbb{B}^k \to \mathbb{B}$ is defined by the following equation:

\[ \nu_k (x_1, \ldots, x_k)  =  \neg_1 (x_1, \ldots, x_k) \:\vee\: \cdots \:\vee\: \neg_j (x_1, \ldots, x_k) \:\vee\: \cdots \:\vee\: \neg_k (x_1, \ldots, x_k) . \]
=--

If we think of the point $x = (x_1, \ldots, x_k) \in \mathbb{B}^k$ as indicated by the boolean product $x_1 \cdot \cdots \cdot x_k$ or the logical conjunction $x_1 \:\wedge\: \cdots \:\wedge\: x_k$, then the minimal negation `(`$ x_1, \ldots, x_k $`)` indicates the set of points in $\mathbb{B}^k$ that differ from $x$ in exactly one coordinate.  This makes `(`$ x_1, \ldots, x_k $`)` a discrete functional analogue of a _point omitted neighborhood_ in analysis, more exactly, a _point omitted distance one neighborhood_.  In this light, the minimal negation operator can be recognized as a differential construction, an observation that opens a very wide field.  It also serves to explain a variety of other names for the same concept, for example, _logical boundary operator_, _limen operator_, _least action operator_, or _hedge operator_, to name but a few.  The rationale for these names is visible in the venn diagrams of the corresponding operations on sets.

The remainder of this discussion proceeds on the _algebraic boolean convention_ that the plus sign $(+)$ and the summation symbol $(\textstyle\sum)$ both refer to addition modulo 2.  Unless otherwise noted, the boolean domain $\mathbb{B} = \{ 0, 1 \}$ is interpreted so that $0 = false$ and $1 = true$.  This has the following consequences:

*  The operation $x + y$ is a function equivalent to the exclusive disjunction of $x$ and $y$, while its fiber of $1$ is the relation of inequality between $x$ and $y$.

*  The operation $\textstyle\sum_{j=1}^k x_j$ maps the bit sequence $(x_1, \ldots, x_k)$ to its _parity_.

The following properties of the minimal negation operators $\nu_k : \mathbb{B}^k \to \mathbb{B}$ may be noted:

*  The function `(x, y)` is the same as that associated with the operation $x + y$ and the relation $x \ne y$.

*  In contrast, `(x, y, z)` is not identical to $x + y + z$.

*  More generally, the function $\nu_k (x_1, \dots, x_k)$ for $k \gt 2$ is not identical to the boolean sum $\textstyle\sum_{j=1}^k x_j$.

*  The inclusive disjunctions indicated for the $\nu_k$ of more than one argument may be replaced with exclusive disjunctions without affecting the meaning, since the terms disjoined are already disjoint.

# Truth tables #

Table 1 is a truth table for the sixteen boolean functions of type $f : \mathbb{B}^3 \to \mathbb{B}$, each of which is either a boundary of a point in $\mathbb{B}^3$ or the complement of such a boundary.

Table 1.  Logical Boundaries and Their Complements

|           |                |      |                 |                   |
|:---------:|:--------------:| ----:|:---------------:|:-----------------:|
| $L_1$     | $L_2$          |      | $L_3$           | $L_4$             |
| Decimal   | Binary         |      | Sequential      | Parenthetical     |
|           |                |      |                 |                   |
|           |                | $p:$ | 1 1 1 1 0 0 0 0 |                   |
|           |                | $q:$ | 1 1 0 0 1 1 0 0 |                   |
|           |                | $r:$ | 1 0 1 0 1 0 1 0 |                   |
|           |                |      |                 |                   |
| $f_{104}$ | $f_{01101000}$ |      | 0 1 1 0 1 0 0 0 | `( p , q , r )`   |
| $f_{148}$ | $f_{10010100}$ |      | 1 0 0 1 0 1 0 0 | `( p , q ,(r))`   |
| $f_{146}$ | $f_{10010010}$ |      | 1 0 0 1 0 0 1 0 | `( p ,(q), r )`   |
| $f_{97}$  | $f_{01100001}$ |      | 0 1 1 0 0 0 0 1 | `( p ,(q),(r))`   |
| $f_{134}$ | $f_{10000110}$ |      | 1 0 0 0 0 1 1 0 | `((p), q , r )`   |
| $f_{73}$  | $f_{01001001}$ |      | 0 1 0 0 1 0 0 1 | `((p), q ,(r))`   |
| $f_{41}$  | $f_{00101001}$ |      | 0 0 1 0 1 0 0 1 | `((p),(q), r )`   |
| $f_{22}$  | $f_{00010110}$ |      | 0 0 0 1 0 1 1 0 | `((p),(q),(r))`   |
|           |                |      |                 |                   |
| $f_{233}$ | $f_{11101001}$ |      | 1 1 1 0 1 0 0 1 | `(((p),(q),(r)))` |
| $f_{214}$ | $f_{11010110}$ |      | 1 1 0 1 0 1 1 0 | `(((p),(q), r ))` |
| $f_{182}$ | $f_{10110110}$ |      | 1 0 1 1 0 1 1 0 | `(((p), q ,(r)))` |
| $f_{121}$ | $f_{01111001}$ |      | 0 1 1 1 1 0 0 1 | `(((p), q , r ))` |
| $f_{158}$ | $f_{10011110}$ |      | 1 0 0 1 1 1 1 0 | `(( p ,(q),(r)))` |
| $f_{109}$ | $f_{01101101}$ |      | 0 1 1 0 1 1 0 1 | `(( p ,(q), r ))` |
| $f_{107}$ | $f_{01101011}$ |      | 0 1 1 0 1 0 1 1 | `(( p , q ,(r)))` |
| $f_{151}$ | $f_{10010111}$ |      | 1 0 0 1 0 1 1 1 | `(( p , q , r ))` |

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

# Links #

* [Minimal Negation Operator @ MyWikiBiz](http://mywikibiz.com/Minimal_negation_operator)

* [Minimal Negation Operator @ PlanetMath](http://planetmath.org/encyclopedia/MinimalNegationOperator.html)

* [Minimal Negation Operator @ PlanetPhysics](http://planetphysics.org/encyclopedia/MinimalNegationOperator.html)

* [Minimal Negation Operator @ ProofWiki](http://www.proofwiki.org/wiki/Definition:Minimal_Negation_Operator)
