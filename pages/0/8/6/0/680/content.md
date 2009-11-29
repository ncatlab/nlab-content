
#Contents#
* automatic toc
{:toc}

#Idea#

The _Dold--Kan correspondence_ asserts that the [[nerve and realization]] [[adjunction]] between abelian 
[[simplicial group]]s and [[chain complex]]es encodes
[[infinity-groupoid]]s with abelian group structure equivalently in terms of [[chain complex]]es of abelian groups. 

Analogous statement hold for the category of abelian groups replaces by any other [[abelian category]].

This allows one

* on the one hand to understand the true conceptual home of many constructions with [[chain complex]]es in [[homological algebra]];

* on the other to efficiently compute with certain higher categorical structures.

Compare this to the role played by [[rational homotopy theory]] as a tool for handling certain [[topological space]]s.

The classical Dold--Kan correspondence states the equivalence of

: [[simplicial group|simplicial abelian groups]] $\;\simeq\;$ non-negatively graded [[chain complex]]es of abelian groups.

Since every [[simplicial group]] is a [[Kan complex]], one can equivalently read this more suggestively as 

: $\infty$-groupoids with abelian group structure $\;\simeq\;$ chain complexes$_+$ internal to abelian groups.

The fact that this involves _[[abelian group|abelian]]_ groups is essential for the correspondence. However, a similar correspondence still holds in a slightly more nonabelian context.  This and various other generalizations are described further below.


#Details#

We now spell out technical details of the classical Dold--Kan correspondence.

+-- {: .num_theorem }
###### Theorem (Dold--Puppe)

For $A$ an [[abelian category]] 
there is an [[adjoint equivalence]]

$$
  N : [\Delta^{op},A] 
      \stackrel{\leftarrow}{\to} Ch_+(A) : \Xi
$$

between 

* the category $[\Delta^{op},A]$ of [[simplicial object]]s in $A$;

* the [[category of chain complexes]] in $A$ that are 0 in negative degree,

where

* $N$ is the normalized [[Moore complex]] functor, given by

  $$
    (N G)_n=\bigcap_{i=1}^{n}Ker\,d_i^n 
  $$

  with [[differential]] $\partial_n : N G_n \to N G_{n-1}$ given by $d_0^n$.

These functors respect the standard weak equivalences with respect to the standard [[model structure on simplicial sets]] [[model structure on chain complexes|and on chain complexes]] in that they induce isomorphisms between [[simplicial homotopy group]]s and [[homology]] groups.

=--

+-- {: .num_theorem }
###### Theorem (Kan)

For the case that $A$ is the category of abelian groups, the functors $N$ and $\Xi$ are [[nerve and realization]] with respect to the cosimplicial chain complex

$$
  Ch_\bullet := N F_\mathbb{Z}(-): \Delta \to Ch_+(Ab)
$$

that sends the standard $n$-[[simplex]] to the normalized [[Moore complex]] of the free simplicial abelian group $F_{\mathbb{Z}}(\Delta^n)$ on the [[simplicial set]] $\Delta^n$, i.e.

$$
    \Xi(V_\bullet)_n= Hom_{Ch_\bullet(Ab)}(C_\bullet(\Delta^n), V_\bullet)
    \,.
$$

=--

Before proving this, 
first briefly recall the definition of the (normalized) [[Moore complex]]:

+-- {: .un_defn}
###### Definition

For $A = (A_n)$ 
a simplicial abelian group, its **[[Moore complex]]** is

$$
  C_\bullet(A) = 
  \left(
    \cdots \to A_{n} 
     \stackrel{\partial_n :=  \sum_{i = 0}^{n} (-1)^i d_i}
     {\to} A_{n-1} \to \cdots
  \right)
  \,,
$$  

where the $d_i$ are the [[simplicial set|face maps]] of $A$.

The **degenerate Moore complex** $D_\bullet(A)$
of $A$ is the full subcomplex generated from [[simplicial set|degenerate elements]] 

$$
  D_n(A) := s(A_{n-1})
$$

=--

+-- {: .num_lemma #LeftCosetsDisjoint}
###### Lemma

This is indeed well defined in that
the boundary map satisfies 
$\partial \circ \partial = 0$ in $C_\bullet(A)$
and restricts to a boundary map on the degenerate subcomplex
$\partial : A_n|_{s(A_{n-1})} \to A_{n-1}|_{s(A_{n-2})}$.

=--

+-- {: .proof}
###### Proof

For the first statement one checks

$$
  \begin{aligned}
    \partial_n \partial_{n+1}
    & =
    \sum_{i, j} 
      (-1)^{i+j}
      d_i \circ d_{j}
    \\
    &=
    \sum_{i  \geq j} (-1)^{i+j} d_i \circ d_j 
    + 
    \sum_{i \lt j} (-1)^{i+j}
      d_i \circ d_j 
    \\
    &=
    \sum_{i  \geq j} (-1)^{i+j} d_i \circ d_j 
    + 
    \sum_{i \lt j} (-1)^{i+j}
      d_{j-1} \circ d_i 
    \\
    &=
    \sum_{i  \geq j} (-1)^{i+j} d_i \circ d_j 
    -
    \sum_{i \leq k} (-1)^{i+k}
      d_{k} \circ d_i 
    \\
    &=
    0
  \end{aligned}
$$

using the [[simplicial identities|simplicial identity]] $d_i \circ d_j = d_{j-1} \circ d_i$ for $i \lt j$.

Similarly, using the mixed [[simplicial identities]] we find that for $s_j(a) \in A_n$ a degenerate element, its boundary is

$$
  \begin{aligned}
     \sum_i (-1)^i d_i s_j(a)
     &=
     \sum_{i \lt j} (-1)^i  s_{j-1} d_i(a)
     +
     \sum_{i = j, j+1} (-1)^i  a
     +
     \sum_{i \gt j+1} (-1)^i s_j d_{i-1}(a)
     \\
     &=
     \sum_{i \lt j} (-1)^i  s_{j-1} d_i(a)
     +
     \sum_{i \gt j+1} (-1)^i s_j d_{i-1}(a)
  \end{aligned}
$$

which is again a combination of elements in the image of the degeneracy maps.

=--


+-- {: .num_lemma }
###### Lemma

The [[Moore complex]] splits as

$$
  C_\bullet(A) \simeq N_\bullet(A) \oplus D_\bullet(A)
$$

where the first summand is the [[Moore complex|normalized Moore complex]].

=--


+-- {: .num_theorem}
###### Theorem (Eilenberg--Mac Lane)

The inclusion 

$$
  N_\bullet(A) \hookrightarrow C_\bullet(A)
$$

is a [[model structure on chain complexes|homotopy equivalence]], i.e.
the complex $D_\bullet(X)$ is null-homotopic.

=--

+-- {: .proof}
###### Proof

Following the proof of what is 
[Theorem 2.1](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-3.dvi) in Goerss--Jardine we look for each $n \in \mathbb{N}$ and each $j \lt n$ at the  groups

$$
  N_n(A)_j :=  \cap_{i=0}^j ker (d_i) \subset A_n
$$

and similarly at

$$
  D_n(A)_j = \{s_{i}\}_{i \leq j}(A_{n-1}) \subset A_n
  \,,
$$ 

the subgroup generated by the first $j$ degeneracies.

For $j= n-1$ these coincide with $N_n(A)$ and with $D_n(A)$, respectively.  We show by induction on $j$ that the composite

$$
  N_n(A)_j \hookrightarrow A_n \stackrel{}{\to} A_n/D_n(A)_j
$$

is an isomorphism of all $j \lt n$. For $j = n-1$ this is then the desired result.

...  


=--

Now consider the free chain complex on $\Delta^n$...

# Generalizations and enhancements #

There are various generalizations and enhancements of the
Dold--Kan correspondence.

## Monoidal version ##

Both the category of simplicial abelian groups as well as the category of nonnegatively graded [[category of chain complexes|chain complexes]] of abelian groups carry a standard structure of a [[monoidal category]].  For simplicial abelian groups this is the levelwise or 'pointwise' tensor product
$$  (A \otimes B)_n = A_n \otimes B_n $$
For chain complexes of abelian groups the tensor product is given by
$$  (C \otimes D)_n = \sum_{i,j : i+j = n} C_i \otimes D_j $$
The same is true if we replace abelian groups by $R$-modules for any commutative ring $R$.

This means that one may ask whether the normalized Moore complex functor
$$
  N : [\Delta^{op},R-Mod] \to Ch_+(R-Mod) 
$$
and its adjoint
$$
  \Xi:  
       Ch_+(R-Mod) \to [\Delta^{op},R-Mod] 
$$
respect these monoidal structures.  A partial answer is:

+-- {: .num_theorem }
###### Theorem 

If $R$ is any commutative ring, the functor
$$
  N : [\Delta^{op},R-Mod] \to Ch_+(R-Mod) 
$$

is [[lax monoidal functor|lax monoidal]] with respect to the [[Eilenberg Zilber map|Eilenberg-Zilber map]]

$$
    EZ :  N(A \otimes B) \to N(A) \otimes N(B) 
$$

and [[oplax monoidal functor|oplax monoidal]] with respect to the [[Alexander Whitney map|Alexander-Whitney map]] 

$$ 
AW :  N(A) \otimes N(B) \to N(A \otimes B)
$$

The Alexander--Whitney map is left inverse to the Eilenberg--Zilber map:

$$  
 AW \circ EZ = 1 
$$

However, the Alexander--Whitney map is not right inverse to the Eilenberg--Zilber map:

$$  
 EZ \circ AW \ne 1 
$$

Instead there is a chain homotopy 

$$ 
EZ \circ AW \simeq 1  
$$

Similarly, the adjoint to the normalized Moore complex functor

$$
  \Xi : Ch_+(Ab) \to [\Delta^{op},Ab]
$$

is lax monoidal with respect to the Alexander--Whitney map and oplax monoidal with respect to the Eilenberg--Zilber map.

=--

+-- {: .proof}
###### Proof
Apparently this result appears in Mac Lane's _Homology_.  It was proved by Eilenberg and Mac Lane in their 1954 Annals paper "On the groups $H(\pi, n)$. II".

=--

As a consequence, both $N$ and $\Xi$ send [[monoid|monoids]] to monoids and [[comonoid|comonoids]] to comonoids.   In other words: 

* if $A$ is a monoid internal to simplicial $R$-modules, $N(A)$ is a [[differential graded algebra]] over $R$;

* if $A$ is a comonoid internal to simplicial $R$-modules, $N(A)$ is a differential graded coalgebra over $R$;

* if $C$ is a differential graded algebra over $R$, $\Xi(C)$ is a monoid internal to simplicial $R$-modules.

* if $C$ is a differential graded coalgebra over $R$, $\Xi(C)$ is a comonoid internal to simplicial $R$-modules.

For more details, see:

* [[monoidal Dold–Kan correspondence]]

These [remarks by Kathryn Hess](http://golem.ph.utexas.edu/category/2009/11/doldkan_question.html#c029668) are also very useful, and should be integrated into the story here.  She uses "lax comonoidal functor" to mean what above is called an "[[oplax monoidal functor]]".

>The normalized chains functor from simplicial sets to chain complexes (with any coefficients) is both lax monoidal and lax comonoidal.  The Eilenberg-Zilber equivalence, from the tensor product of the chains on X and on Y to the chains on the cartesian product of X and Y, provides the natural transformation that shows that the chain functor is lax monoidal. The Alexander-Whitney equivalence goes in the opposite direction and shows that the chain functor is lax comonoidal.

>Since the chain functor is lax comonoidal, the normalized chains on any simplicial set is a dg coalgebra, where the comultiplication is given by the composite of the chain functor applied to the diagonal map, followed be the Alexadnder-Whitney transformation.  It turns out that the Eilenberg-Zilber equivalence is actually itself a morphism of coalgebras with respect to this comultiplication.  On the other hand, the Alexander-Whitney map is a morphism of coalgebras up to strong homotopy.

>The A-W/E-Z equivalences for the normalized chains functor are a special case of the strong deformation retract of chain complexes that was constructed by Eilenberg and MacLane in their 1954 Annals paper "On the groups H(pi, n). II".  For any commutative ring R, they defined chain equivalences between the tensor product of the normalized chains on two simplicial R-modules and the normalized chains on their levelwise tensor product.

>Steve Lack and I observed recently that the normalized chains functor is actually even Frobenius monoidal.  We then discovered that Aguiar and Mahajan already had a proof of this fact in their recent monograph&#8230; :-)

>As to the Hopf algebra/bialgebra question, I admit I've often been guilty of referring to loop space homology as a "graded Hopf algebra", without any mention of antipode.  I was happy to learn a few years ago that connected graded bialgebras admit a unique antipode, as Mike has already pointed out.  On the chain level, if the simplicial group you're considering is reduced (i.e., has a unique 0-simplex), then its normalized chain complex is a connected dg bialgebra and therefore a dg Hopf algebra.


## Dual Dold--Kan correspondence ##

There is a version relating [[cochain complex]]es in non-negative degree to cosimplicial abelian groups.  Indeed,
replacing the abelian category $A$ by its [[opposite category]] $A^{op}$ in the Dold--Puppe theorem above, we instantly see:

+-- {: .num_theorem }
###### Theorem (dual Dold--Puppe)

For $A$ an [[abelian category]] 
there is an [[adjoint equivalence]] between 

* the category $[\Delta,A]$ of [[cosimplicial object|cosimplicial objects]] in $A$;

and 

* the [[category of cochain complexes]] in $A$ that are 0 in negative degree.
=--

More concretely, let us take the case where $A$ is the category of abelian groups, and construct an explicit equivalence.

If $G$ is a cosimplicial abelian group, the dual Moore complex $C^\bullet$ is formally defined just as the ordinary [[Moore complex]] with

$$
  C^k := G^k
$$

by taking the the alternating sum of the [[simplicial identities|face maps]] $\partial_i$. 

$$
  d : \sum_{i = 0}^{k} (-1) \partial_i : C^k \to C^{k+1}
  \,.
$$

Notice that since we have now a cosimplicial object this differential indeed increases degree, as befits a [[cochain complex]].

It is in the definition of the _normalized_ dual Moore complex $N^\bullet G$ that the role of face maps $d_i$ and boundary maps $s_i$ is interchanged as compared to the ordinary normalized complex. We have

$$
  N^k G := G^n/\sum{i=0}^n d_i G^n
  \simeq
  \cap_{i=0}^{n-1} ker(s_i)
  \,.
$$

This statement is reviewed and various further references are given in [section 4](http://arxiv.org/PS_cache/math/pdf/0306/0306289v3.pdf#page=5) of 

* J.L. Castiglioni, G. Corti&#241;as, 
Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence, J. Pure Appl. Algebra  191  (2004),  no. 1-2, 119--142, [arXiv:math.KT/0306289](http://arxiv.org/abs/math/0306289).


## Nonabelian versions ##

In a series of articles by Brown and Higgins, based on old work by Whitehead, the above was generalized to

: strict $\infty$-groupoids $\;\simeq\;$ crossed complexes.

Here on the left we have [[strict omega-groupoid]]s and on the right [[crossed complex]]es, a non-abelian generalization of chain complexes of groups.

: crossed complexes $\supset$ chain complexes$_+$ internal of abelian groups

There is a discussion of some of these and extensions to them to the non-abelian case, in the entry on [[Moore complex]].


Perhaps the 'ultimate' form of a 'classical' Dold--Kan result is by Pilar Carrasco, who identified the extra structure on chain complexes of groups in order that they be [[Moore complex|Moore complexes]] of simplicial groups.  Dominique Bourn has a general form of this result for his [[semi-abelian category|semi-abelian categories]]. His results provide a neat categorical gloss on the theorem.

Dominique Bourn's formulation is very pretty. The Moore complex functor is [[monad|monadic]] when the basic category is semi-Abelian (Th. 1.4. p.113 in _Bourn2007_ below). Of course for simplicial _groups_, the  monad on chain complexes of groups gives the [[hypercrossed complex]]es of Carrasco and Cegarra, but here they fall out from the theory.  On the down side there is apparently no 
full analysis as yet of the actual form of this monad.




## Version for Lie algebras ## 

In rational homotopy theory, Quillen proved and used an analogous statement for Lie algebras: Quillen equivalence between the reduced rational dg Lie algebras and reduced rational simplicial Lie algebras:

* D. G. Quillen, Rational homotopy theory, Ann. Math. 90 (1969), 204--265.



## Parameterized version ##

The statement of the Dold--Kan correspondence generalizes to
[[sheaf|sheaves]] with values in the respective categories and this way from [[Infinity-Grpd]] to more general [[(infinity,1)-topos|(infinity,1)-topoi]]:

For $X$ be a [[site]], let $Sh(X, sAb)$ be the category of 
_simplicial abelian sheaves_ -- i.e. [[simplicial presheaf|simplicial sheaves]] which take values
in simplicial abelian groups -- and let $Sh(X, Ch_+(Ab))$
be the category of [[sheaf|sheaves]] on $S$ with values in
non-negatively graded [[chain complex]]es of abelian groups.
The normalized chain complex extends objectwise to a functor
$$
  Sh(X,sAb) \stackrel{\simeq}{\to} Sh(X, Ch_+(Ab))
$$
which is an [[equivalence]] of categories. Moreover, 
both these categories are naturally 
[[category with weak equivalences|categories with weak equivalences]]:
the weak equivalences in $Sh(X, sAb)$ are the stalkwise
[[model structure on simplicial sets|weak equivalences of simplicial sets]]
and the weak equivalences in $Sh(X, Ch_+(Ab))$ are the
[[quasi-isomorphism]]s. The normalized chain complex functor
preserves these weak equivalences.
This sheaf version of the Dold--Kan correspondence 
allows to understand [[abelian sheaf cohomology]]
as a special case of [[nonabelian cohomology]].

See page 9,10 of 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

## $(\infinity,1)$-Version ##

There is a version of the Dold--Kan correspondence in the context of [[(infinity,1)-category|(infinity,1)-categories]]:

let $C$ be a [[stable (infinity,1)-category]]. Then the $(\infty,1)$-categories of [[complex]]es in $C$ is equivalent to the $(\infty,1)$-category of [[simplicial object]]s in $C$

$$
  Fun(N(\mathbb{Z}_{\geq 0}), C)
  \simeq
  Fun(N(\Delta)^{op}, C)  
  \,.
$$

This is [theorem 12.8, p. 50](http://math.mit.edu/~lurie/topoibook/DAGI.pdf) of 

* [[Jacob Lurie]], [[Stable Infinity-Categories]] 

## Dendroidal version ##

There is a version of the Dold--Kan correspondence with [[simplicial set]]s generalized to [[dendroidal set]]s. This is described in

* [[Javier Gutiérrez]], [[Andor Lukacs]], [[Ittay Weiss]], _Dold-Kan correspondence for dendroidal abelian groups_ ([arXiv](http://arxiv.org/abs/0909.3995))

## Related nerve constructions ## 

This gives a pattern for constructing simplicial structures, often called the _simplicial [[nerve]]_,  from algebraic structures. 

For example the nerve of a groupoid $G$ may be defined as the simplicial set which is $Ob(G)$ in dimension 0 and is given in dimension $n\gt 0$ by 

$$Nerve(G)_n= Gpd(\pi_1(\Delta^n,\Delta^n_0) , G).$$

where $\Delta^n_0$ denotes the set of vertices of $\Delta^n$. 

A [[filtered space]] $X_*$ has a fundamental crossed complex $\Pi X_*$, and a geometric simplex $\Delta^n$ has a filtration $\Delta^n_*$ by skeleta. The nerve of a [[crossed complex]] $C$ is then the simplicial set given in dimension $n$ by 

$$Nerve(C)_n= Crs(\Pi(\Delta^n_*, C).$$

This includes the case when $C$ is a [[crossed module]] (of groupoids) regarded as a crossed complex of length 2. The geometric realisation of this simplicial set gives the [[classifying space]] $BC$ of the crossed complex $C$. This space is filtered by the length of truncations of $C$ to give a filtered space $(BC)_*$ and it is a theorem that $\Pi(BC)_* \cong C$. 


An obvious analogue gives cubical or globular nerves. 



#References#

Historical references for the Dold--Kan correspondence are

* A. Dold, _Homology of symmetric products and other functors of complexes_ 
([jstor](http://www.jstor.org/stable/1970043))

which considers the correspondence for categories of [[module]]s, and

* A. Dold, D. Puppe, _Homologie nicht-additiver Funktoren. Anwendugen_ ([numdam](http://www.numdam.org/item?id=aif_1961__11__201_0))

that generalizes the result to arbitrary [[abelian category|abelian categories]].

The expression of the correspondence in terms of [[nerve]]s is due to

* [[Daniel Kan]], _Functors involving c.s.s complexes_, Transactions of the American Mathematical Society, Vol. 87, No. 2 (Mar., 1958), pp. 330--346 ([jstor](http://www.jstor.org/stable/1993103)).


A standard modern textbook reference for the ordinary Dold--Kan correspondence is [chapter III.2](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-3.dvi) of 

* Goerss, Jardine, _Simplicial Homotopy Theory_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

The monoidal structure on the Dold--Kan correspondence functors is discussed in


The relation between [[strict omega-groupoid]]s and [[crossed complex]]es is in

* R. Brown, P. Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 371-386  ([pdf](http://archive.numdam.org/article/CTGDC_1981__22_4_371_0.pdf))

The discussion of Dold--Kan in the general context of [[semi-abelian category|semi-abelian categories]] is in

* **Bourn2007** D. Bourn, _Moore normalisation and Dold--Kan theorem for semi-Abelian categories_, in 
Categories in algebra, geometry and mathematical physics , volume 431 of Contemp. Math., 
105--124, Amer. Math. Soc., Providence, RI. (2007)



[[!redirects Dold--Kan correspondence]]
[[!redirects Dold–Kan correspondence]]
[[!redirects Dold-Kan theorem]]
[[!redirects Dold--Kan theorem]]
[[!redirects Dold–Kan theorem]]
[[!redirects dual Dold--Kan correspondence]]
[[!redirects dual Dold–Kan correspondence]]
[[!redirects dual Dold-Kan theorem]]
[[!redirects dual Dold--Kan theorem]]
[[!redirects dual Dold–Kan theorem]]
