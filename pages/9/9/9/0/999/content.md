<div class="rightHandSide toc">
[[!include compact object - contents]]
</div>


#Contents 
* automatic table of contents goes here
{:toc}

## Idea

An [[object]] of a [[category]] is often called *compact* if it is "finite" or "small" in some precise sense.


## Definition 

Let $C$ be a [[locally small category]] that admits [[filtered colimits]]. Then an [[object]] $X \in C$ is **compact** (or sometimes called **[[locally finitely presentable category|finitely presented]]**) if the [[representable functor|corepresentable functor]]

$$
  Hom_C(X,-) : C \to Set
$$

commutes with these [[filtered colimits]].

So if for every [[filtered category]] $D$ and every functor $F : D \to C$ the canonical morphism

$$
  colim C(X,F(-)) \stackrel{\simeq}{\to} 
  C(X, colim F)
$$

is an [[isomorphism]].

### Small objects 

There is a slight variant of this definition.

If $\kappa$ is a [[cardinal number|regular cardinal]], then objects $X$ such that $C(X,-)$ commutes with such $\kappa$-[[filtered colimits]] are also called **$\kappa$-compact objects**. An object which is $\kappa$-compact for some regular $\kappa$ is called a [[small object]].


## Examples 

### In $Set$

In $C = $ [[Set]] an object is compact precisely if it is a (Kuratowski) [[finite set]].

### In $Grp$ 

In $C = $ [[Grp]] an object is compact precisely if it is finitely presented as a group.

### In a topos 

For $C$ a [[topos]], $X$ is compact if it is 
$K$-[[finite object|finite]]. 


### In $Top$

Let $X$ be a [[topological space]] and let $C = Op(X)$ be the [[category of open subsets]] of $X$. The an open subset $U \in C$ is a compact object in $C$ precisely if it is a [[compact space|compact topological space]].



See the discussion below for variations of this theme.

## Generalizations 

This definition has an obvious generalization to [[compact object in an (infinity,1)-category]].


## Subtleties and different meanings 

One has to be careful about the following variations on this theme


### Compactness in additive categories 

When $C$ is an [[additive category]] (often a [[triangulated category]]), an object $x$ in $C$ is called **compact** if for every set $S$ of objects of $C$ such that the coproduct $\coprod_{s\in S} s$ exists, the canonical map
$$
\coprod_{s\in S} C(x,s)\to C(x,\coprod_{s\in S}s)
$$
is an [[isomorphism]] of [[set]]s (a [[bijection]]).

Here is an application of this concept to characterize which abelian categories are categories of modules of some ring:

+-- {: .un_theorem}
###### Theorem

Let $C$ be an abelian category.  If $C$ has all [[small category|small]] [[coproducts]] and has a compact [[projective object| projective]] [[generator]], then $C \simeq R Mod$ for some ring $R$.  In fact, in this situation we can take $R = C(x,x)^{op}$ where $x$ is any compact projective generator.   Conversely, if $C \simeq R Mod$, then $C$ has all small coproducts and $x = R$ is a compact projective generator.
=--

+-- {: .proof}
###### Proof

This theorem, minus the explicit description of $R$, can be found as Exercise F on page 103 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=132).
The first part of this theorem can also be found as Prop. 2.1.7. of Victor Ginzburg's [Lectures on noncommutative geometry](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=4).  Conversely, it is easy to see that $R$ is a compact projective generator of $R Mod$. 
=--

+--{.query}
Zoran: While Ginzburg's reference is surely a worthy to look at, it would be better not to give false impression that this [[reconstruction theorem]] is due Ginzburg or at all new. It is rather a classical and well know fact probably from early 1960s, essentially small strengthening of a variant of a circle of abelian reconstruction theorems including the [Gabriel-Popescu theorem](http://myyn.org/m/article/gabriel-popescu-theorem-for-ab5-categories)(probably our variant could be read off from classical algera book by Faith for example, or Popescu's book on abelian categories, in any case it is well known in [[noncommutative algebraic geometry]]). In fact for this fact, if I think better, the reconstruction belongs usually to expositions which treat classical Morita theory for rings. 
=--

A triangulated category is __compactly generated__ if it is generated (see [[generator]]) by a _set_ of compact objects.

The notion can be modified for categories [[enriched category|enriched]] over a [[closed monoidal category]] (compare to the notions of finite and/or rigid objects in various contexts).

Compact objects in the derived categories of quasicoherent sheaves over a scheme are called perfect complexes. Any compact object in the category of modules over a perfect ring is finitely generated as a module.  Lurie uses $\kappa$-compact objects in the setup of $(\infty,1)$-categories.

### Compactness in non-additive categories

In non-additive contexts, the above definition is not right.  For instance, with this definition a [[topological space]] would be compact iff it is [[connected space|connected]]. In general one should expect to preserve _filtered colimits_ (see below for discussion). For $C$ any category and $X \in C$, the condition that $C(X,-) : C \to C$ preserves [[filtered colimits]] imposes  some kind of finiteness condition on $X$. For instance 




#### Compact objects in Top 

Recall the above example of [[compact space|compact topological spaces]]. Notice that the statement which one might expect, that a topological space $X$ is [[compact space|compact]] if it is a compact object in [[Top]] is not quite right in general.

A counterexample is given for instance on page 49 of Hovey's Model Categories, which itself was corrected by Don Stanley (see the errata of that book).
See also the blog discussion 
[here](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_3.html#c023790).

Namely, the two-element set with the indiscrete topology is a compact space $X$ for which 
 \[
 Hom(X, -): Top \rightarrow Top
\]
doesn't preserve filtered colimits, in fact not even colimits of sequences (functors out of the ordered set of natural numbers). 

For example, consider the sequence of spaces 
 \[
 X_n=[n,\infty) \times \{0,1\}
\]
where the open sets are of the form 
\[
 [n, \infty]\cup [m,\infty) \times \{1\}
\]
(where $m \geq n$), plus the empty set. Define $X_n \rightarrow X_{n+1}$ so that it sends a pair $(k, \epsilon)$ to itself if $k \gt n$, and $(n,\epsilon)$ to $(n+1,\epsilon)$. This defines a functor 
\[
F: \mathbb{N} \rightarrow Top 
\]
The colimit $X_\infty$ of this sequence is the two-element set $\{0,1\}$ with the indiscrete topology. However, the identity map on this space does not factor through any of the canonical maps $X_n \rightarrow X_\infty$. It follows that 
the comparison map 
\[
 colim_n Hom(X_\infty, X_n) \rightarrow Hom(X_\infty, X_\infty)
\]
is not surjective, and therefore not an isomorphism. 

+--{.query}
_[[Todd Trimble|Todd]]_ (posted from n-category cafe): I don't know if the story is any different for $X$ compact _Hausdorff_, but it could be worth considering. 
=--

But with a bit care on the assumptions, similar results do hold:

If $Y$ is compact, then 
$hom(Y,-)$ preserves colimits of functors mapping out of limit ordinals, provided that the arrows of the cocone diagram, 
 \[
 X_\alpha \rightarrow X_\beta,
\]
are closed inclusions of $T_1$ spaces. (This applies for example to the sequence of inclusions of n-skeleta in a CW-complex. Taking $Y=S_k$, this has obvious desirable consequences for the functor $\pi_k$.) 

This example is discussed on page 50 of Hovey's book. 

Hovey wants this result in view of a small object argument on the way to proving that $Top$ is a model category. 




## References

For the pages quoted in the context of the discussion of compact objects in [[Top]] see

* Mark Hovey, _Model categories_.

For the general definition with an eye towards the definition of [[compact object in an (infinity,1)-category]]  see section A.1.1 section 5.3.4 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]


[[!redirects compact object"]]