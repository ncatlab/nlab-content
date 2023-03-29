
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



# Globular sets
* table of contents
{: toc}


## Idea

Globular sets are to [[simplicial sets]] as [[globes]] are to simplices.

Much like [[simplicial sets]] underly common [[geometric definitions of higher categories]], so globular sets underly some [[algebraic definitions of higher categories]], see [below](#AsShapesForHigherCategories).



## Definition

### Basic definition

+-- {: .num_defn}
###### Definition

The **[[globe category]]** $\mathbb{G}$ is the [[category]] whose [[objects]] are the [[natural numbers]], denoted here $[n] \in \mathbb{N}$ (N.B. not to be confused with ordinals in any structural sense) and whose morphisms are [[generators and relations|generated]] from

$$
  \sigma_n : [n] \to [n+1]
$$
$$
  \tau_n : [n] \to [n+1]
$$

for all $n \in \mathbb{N}$ subject to the relations (dropping obvious subscripts)

$$
  \sigma\circ \sigma = \tau \circ \sigma
$$
$$
  \sigma\circ \tau = \tau \circ \tau
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

A _globular set_, also called an *$\omega$-[[graph]]*, is a [[presheaf]] on $\mathbb{G}$. The [[category]] of globular sets is the [[category of presheaves]]

$$
  gSet \coloneqq PSh(\mathbb{G})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This means that a globular set $X \in gSet$ is given by a collection of sets $\{X_n\}_{n \in \mathbb{N}}$ (the **set of $n$-[[globes]]**) equipped with [[functions]]

$$
  \{s_n,t_n \colon X_{n+1} \to X_n\}_{n \in \mathbb{N}}
$$

called the **$n$-source** and **$n$-target** maps (or similar), such that the **globular identities** hold: for all $n \in \mathbb{N}$

* $s_n \circ s_{n+1} = s_n \circ t_{n+1} $

* $t_n \circ s_{n+1} = t_n \circ t_{n+1} $.

=--

+-- {: .num_remark}
###### Remark

The globular identities ensure that two sequences of boundary maps

$$
  f_n \circ \cdots \circ f_{n+m-1} \circ f_{n+m} :
  S_{n+m+1} \to S_n
$$

with $n,m \in \mathbb{N}$ and for $f_k, \in \{s_k, t_k\}$ are
equal if and only if their last term $f_n$ coincides; 
for all $n,m \in \mathbb{N}$ we have

$$
    s_n \cdots s_{n+1} \circ \cdots \circ
    s_{n+m} \circ i_{n+m} \circ \cdots \circ i_{n+1} \circ i_n
    =
    \mathrm{Id}
$$
$$
    t_n \cdots t_{n+1} \circ \cdots \circ
    t_{n+m} \circ i_{n+m} \circ \cdots \circ i_{n+1} \circ i_n
    =
    \mathrm{Id}
    \,.
$$

For $S$ a globular set we may therefore write unambiguously

$$
  s_n, t_n : S_{n+m+1} \to S_n
$$
$$
  i_n : S_n \to S_{n+m+1}  
$$

with $i_n, s_n, t_m$ the sequence of $m$ consecutive identity-assigning, source or target maps, respectively.

=--



+-- {: .num_remark}
###### Remark

The presheaf definition can understood from the point of view of [[space and quantity]]: a _globular set_ is a space characterized by the fact that and how it may be _probed_ by mapping standard globes into it: the set $S_n$ assigned by a globular set to the standard $n$-globe $[n]$ is the set of $n$-globes in this space, hence the way of mapping a standard $n$-globe into this spaces.
=--

More generally:

+-- {: .num_defn}
###### Definition

A **globular object** $X$ [[internalization|in]] a [[category]] $\mathcal{C}$ is a [[functor]] $X : \mathbb{G}^{\mathrm{op}} \to \mathcal{C}$.  

=--



### Reflexive globular sets {#ReflexiveGlobularSets}

If to the globe category we add additional generating morphisms

$$
  \iota_n : [n+1] \to [n]
$$

satisfying the relations

$$
  \iota \circ \sigma = \mathrm{Id}
$$
$$
  \iota \circ \tau = \mathrm{Id}
$$

we obtain the **reflexive globe category**, a presheaf on which is a
**reflexive globular set**.  In this case the morphism

$$
  i_n := S(\iota_n) : S_{n} \to S_{n+1}
$$

is called the $n$th **identity assigning map**; it satisfies the globular identities:

$$
  s \circ i = \mathrm{Id}
$$
$$
  t \circ i = \mathrm{Id}
$$


### $n$-globular sets

A presheaf on the full subcategory of the globe category containing only the integers $[0]$ through $[n]$ is called an **$n$-globular set** or an **$n$-graph**.  An $n$-globular set may be identified with an $\infty$-globular set which is empty above dimension $n$.

Note that a $1$-globular set is just a [[directed graph]], and a $0$-globular set is just a [[set]].



## Examples

* Any [[strict 2-category]] or [[bicategory]] has an underlying 2-globular set.  Likewise, any [[tricategory]] has an underlying 3-globular set.  Globular sets can be used as underlying data for [[n-categories]] as well; see for instance [[Batanin ∞-category]].

* A _[[strict omega-category]]_ is a globular set $C$ equipped in each degree with the structure of a [[category]] such that for every pair $k_1 \lt k_2 \in \mathbb{N}$ the induced structure on the 2-graph $C_{k_2} \stackrel{\to}{\to} C_{k_1} \stackrel{\to}{\to} C_0$ is that of a [[strict 2-category]].

* The **globular $n$-globe** $G_n$ is the globular set represented by $n$, i.e. $G_n(-) := Hom_G(-,n)$.

## Properties

### Grothendieck homotopy theory

The category of [[globes]] is not a [[weak test category]] according
to Scholium 8.4.14 in [Cisinski 06](#Cisinski06).

However, if we construct the free [[strict monoidal category]]
on the category of [[globes]], while ensuring that the terminal object becomes the monoidal unit,
then the resulting category of polyglobes is a [[test category]].


### As shapes for higher categories
 {#AsShapesForHigherCategories}

Globular sets may be used as a [[geometric shape for higher structures|geometric shape]] for [[algebraic definitions of higher categories]]:

* Equipped with strictly compatible [[composition]] [[structure]] on cells in any dimension, globular sets model *[[strict ∞-categories]]* (originally often: "[[omega-category|omega-categories]]", see also at *[[complicial sets]]*), historically one of the earliest notions of [[higher category theory]] but too restrictive to be useful for most purposes (in their further restriction to [[strict omega-groupoids]] they [are equivalent](strict+omega-groupoid#RelationToCrossedComplexes) just to [[crossed complexes]]). 

* A more general ([[semi-strict infinity-category|semi-strict]]) notion of [[n-categories|$n$-categories]] modeled on globular sets are known as *[[associative n-category|associative $n$-categories]]*, see there for more, and see a corresponding [[proof assistant]]: *[[homotopy.io]]* (previously: *[[Globular]]*).



## Related concepts

* [[graph]]

* [[directed graph]]

  * **directed $n$-graph**

  * [[directed (n,r)-graph|directed $(n,r)$-graph]]

* [[ribbon graph]]

* [[Theta category]], 

* [[globular theory]], [[globular operad]]

* Also related is the notion of [[computad]], which is similar to a globular set in some ways, but allows "formal composites" of $n$-cells to appear in the sources and targets of $(n+1)$-cells.

* [[simplicial object]]

  * [[simplicial set]]

  * [[simplicial object in an (∞,1)-category]]

* [[semi-simplicial object]]

  * [[semisimplicial set]]

* [[strict infinity-category]], [[strict omega-groupoid]]

* [[associative n-category]], [[Globular]]


## References



The definition is reviewed around def. 1.4.5, p. 49 of 

* [[Tom Leinster]]: _Higher operads, higher categories_ ([arXiv:math/0305049](http://arxiv.org/abs/math/0305049))

See also

* [[Sjoerd Crans]], _On combinatorial models for higher dimensional homotopies_ ([web](https://web.archive.org/web/20130514164856/http://home.tiscali.nl/secrans/papers/comb.html))

* [[R. Street]], _The petit topos of globular sets_ , JPAA **154** (2000) pp.299-315.

* {#Cisinski06} [[Denis-Charles Cisinski]], *Les préfaisceaux comme types d'homotopie*, Astérisque **308** Soc. Math. France (2006), 392 pages &lbrack;[numdam:AST_2006__308__R1_0](http://www.numdam.org/item/?id=AST_2006__308__R1_0) [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf)&rbrack;

The definition of globular set, without using that term, is in 2.2 and 2.3 of the following paper: 

* [[Ronnie Brown]], [[Philip J. Higgins]], *The equivalence of $\infty$-groupoids and crossed  complexes*,  Cah. Top. G\'eom. Diff. 22 (1981) 371-386.


[[!redirects globular set]]
[[!redirects globular sets]]
[[!redirects reflexive globular set]]
[[!redirects reflexive globular sets]]
[[!redirects n-globular set]]
[[!redirects n-globular sets]]
[[!redirects reflexive n-globular set]]
[[!redirects reflexive n-globular sets]]
[[!redirects omega-graph]]
[[!redirects omega-graphs]]
[[!redirects ∞-graph]]
[[!redirects ∞-graphs]]
[[!redirects infinity-graph]]
[[!redirects infinity-graphs]]
[[!redirects ∞-graph]]
[[!redirects ∞-graphs]]
[[!redirects n-graph]]
[[!redirects n-graphs]]
[[!redirects omega-quiver]]
[[!redirects omega-quivers]]
[[!redirects ∞-quiver]]
[[!redirects ∞-quivers]]
[[!redirects infinity-quiver]]
[[!redirects infinity-quivers]]
[[!redirects ∞-quiver]]
[[!redirects ∞-quivers]]
[[!redirects n-quiver]]
[[!redirects n-quivers]]
[[!redirects directed omega-graph]]
[[!redirects directed omega-graphs]]
[[!redirects directed ∞-graph]]
[[!redirects directed ∞-graphs]]
[[!redirects directed infinity-graph]]
[[!redirects directed infinity-graphs]]
[[!redirects directed ∞-graph]]
[[!redirects directed ∞-graphs]]
[[!redirects directed n-graph]]
[[!redirects directed n-graphs]]
[[!redirects omega-directed graph]]
[[!redirects omega-directed graphs]]
[[!redirects ∞-directed graph]]
[[!redirects ∞-directed graphs]]
[[!redirects infinity-directed graph]]
[[!redirects infinity-directed graphs]]
[[!redirects ∞-directed graph]]
[[!redirects ∞-directed graphs]]
[[!redirects n-directed graph]]
[[!redirects n-directed graphs]]
[[!redirects reflexive omega-graph]]
[[!redirects reflexive omega-graphs]]
[[!redirects reflexive ∞-graph]]
[[!redirects reflexive ∞-graphs]]
[[!redirects reflexive infinity-graph]]
[[!redirects reflexive infinity-graphs]]
[[!redirects reflexive ∞-graph]]
[[!redirects reflexive ∞-graphs]]
[[!redirects reflexive n-graph]]
[[!redirects reflexive n-graphs]]
[[!redirects reflexive omega-quiver]]
[[!redirects reflexive omega-quivers]]
[[!redirects reflexive ∞-quiver]]
[[!redirects reflexive ∞-quivers]]
[[!redirects reflexive infinity-quiver]]
[[!redirects reflexive infinity-quivers]]
[[!redirects reflexive ∞-quiver]]
[[!redirects reflexive ∞-quivers]]
[[!redirects reflexive n-quiver]]
[[!redirects reflexive n-quivers]]
[[!redirects reflexive directed omega-graph]]
[[!redirects reflexive directed omega-graphs]]
[[!redirects reflexive directed ∞-graph]]
[[!redirects reflexive directed ∞-graphs]]
[[!redirects reflexive directed infinity-graph]]
[[!redirects reflexive directed infinity-graphs]]
[[!redirects reflexive directed ∞-graph]]
[[!redirects reflexive directed ∞-graphs]]
[[!redirects reflexive directed n-graph]]
[[!redirects reflexive directed n-graphs]]
[[!redirects reflexive omega-directed graph]]
[[!redirects reflexive omega-directed graphs]]
[[!redirects reflexive ∞-directed graph]]
[[!redirects reflexive ∞-directed graphs]]
[[!redirects reflexive infinity-directed graph]]
[[!redirects reflexive infinity-directed graphs]]
[[!redirects reflexive ∞-directed graph]]
[[!redirects reflexive ∞-directed graphs]]
[[!redirects reflexive n-directed graph]]
[[!redirects reflexive n-directed graphs]]