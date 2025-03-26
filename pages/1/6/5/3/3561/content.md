
# Partial equivalence relations
* table of contents
{: toc}

## Definitions

A __partial equivalence relation__ (sometimes abbreviated __PER__) is a [[binary relation]] satisfying the [[symmetric relation|symmetry]] and [[transitive relation|transitivity]] conditions of an [[equivalence relation]], but not necessarily the [[reflexive relation|reflexivity]] condition. That is, a partial equivalence relation on $X$ is a binary relation $R(x, y) \subseteq X^2$ such that for all $x$ and $y$ in $X$, $R(x, y)$ implies $R(y, x)$, and for all $x$, $y$, and $z$ in $X$, $R(x, y)$ and $R(y, z)$ together imply $R(x, z)$.

Just as [[unary relations]] on a set $X$ correspond to [[subsets]] of $X$ and equivalence relations on $X$ correspond to [[quotient set|quotients]] of $X$, so partial equivalence relations on $X$ correspond to [[subquotients]] of $X$.  That is, the elements satisfying $R(x, x)$ comprise a subset of $X$, on which the relation restricts to a total equivalence relation specifying a further quotient.


## Examples

Consider the set $X$ of all [[infinite sequences]] of [[rational numbers]].  Let such sequences $x$ and $y$ be related if
$$ \lim_{i,j\to \infty} {|x_i - y_j|} = 0 .$$
Then this defines a partial equivalence relation $R$ on $X$; the corresponding subquotient of $X$ is the set of [[Cauchy real numbers]].  Normally, this definition of real number is split into two parts: those sequences satsifying the reflexivity condition of $R$ are the [[Cauchy sequences]] of rational numbers (under the absolute-value metric), and then we impose a total equivalence relation on the Cauchy sequences.  But a single partial equivalence relation does all of the work.  (This example generalises in the usual ways.)

## Category of PERs and interpretation of the polymorphic lambda calculus

We can form [[category of PERs|categories of PERs]]. This is useful in various situations, including the construction of a [[topos]] from a [[tripos]]. A particular instance is as follows. 

Recall that a [[partial combinatory algebra]] is a model of combinatory logic (or, roughly speaking, the untyped lambda calculus). If $A$ is a partial combinatory algebra, then the partial equivalence relations on $A$ are the objects of the [[category of PERs]] over $A$, a [[locally cartesian closed category|locally cartesian closed]] [[Heyting category]] that is a [[full subcategory]] of the [[quasitopos]] of [[assemblies]], which is in turn a full subcategory of the [[realizability topos]] over $A$. Moreover, this interprets second-order lambda calculus, with [[impredicative polymorphism]].

In more detail, consider the following [[type theory#typeforming_rules|type forming rules]]:

$$ \sigma,\tau ::= X | \sigma\to \tau | \forall X.\sigma$$

where $X$ ranges over type variables. 

* Closed types $\tau$ (i.e. those with no free variables) are interpreted as PERs $\llbracket{\tau}\rrbracket$ over the fixed partial combinatory algebra $A$. The domain is thought of as the combinatory elements that inhabit the type.

* Open types $\tau$ with $n$ type variables are interpreted as assignments from $n$ PERs $R_1\dots R_n$ on $A$ to a PER $\llbracket{\tau}\rrbracket_{R_1\dots R_n}$ on $A$. 

* _[[function type|Function types]]:_ If the closed types $\sigma$ and $\tau$ are interpreted as PERs $\llbracket \sigma\rrbracket$ and $\llbracket \tau\rrbracket$, then the function type $\sigma\to\tau$ is interpreted as the PER $\llbracket \sigma\to\tau\rrbracket$, with domain 

$$\{a\in A | \forall b\in A.\ b\in\dom(\llbracket \sigma\rrbracket) \implies a\cdot b\in \dom(\llbracket \tau\rrbracket)\}$$

with $(a,a')\in \llbracket \sigma\to\tau\rrbracket$ if 
for all $(b,b')\in \llbracket \sigma\rrbracket$ we have 
$(a\cdot b,a'\cdot b')\in \llbracket \tau\rrbracket$. 

For open types, the definition is similar, just parameterize by the interpretation of the type variables.

* _Polymorphic types:_ If the type $\tau$ has one free type variable, $X$,
define second-order quantification as:
\[\llbracket \forall X.\tau\rrbracket = 
\bigcap_{R\ \text{ a PER}} \llbracket \tau\rrbracket_R
\]
For types with more free variables, the definition is similar, just parameterize by the interpretation of the type variables.



[[!redirects partial equivalence relation]]
[[!redirects partial equivalence relations]]
[[!redirects PER]]
[[!redirects PERs]]

