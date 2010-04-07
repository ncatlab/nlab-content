
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of adjunction between two [[(∞,1)-functors]] generalizes the notion of [[adjoint functors]] from [[category theory]] to [[(infinity,1)-category|(∞,1)-category theory]].


There are many equivalent definitions of the ordinary notion of [[adjoint functor]]. Some of them have more evident generalizations to some parts of [[higher category theory]] than others. 

* One definition of ordinary adjoint functors says that a pair of functors $C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ is an adjunction if there is a [[natural transformation|natural isomorphism]]

  $$
    Hom_C(L(-),(-) \simeq Hom_D(-,R(-))
    \,.
  $$

  The analog of this definition makes sense very generally in [[(∞,1)-category theory]], where $Hom_C(-,-) : C^{op} \times C \to \infty Grpd$ is the $(\infty,1)$-categorical hom-object.

* One other characterization of adjoint functors  in terms of their [[cograph of a functor|cographs]]: the [[Cartesian fibration]]s to which the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-Grothendieck+construction#FibsOverInterval">functor is associated</a>. At [[cograph of a functor]] it is discussed how two functors $L : C \to D$ and $R : D \to C$ are adjoint precisely if the cograph of $L$ coincides with the cograph of $R$ up to the obvious reversal of arrows

$$
  (L \dashv R) \Leftrightarrow
  (cograph(L) \simeq cograph(R^{op})^{op})
  \,.
$$

Using the [[(∞,1)-Grothendieck construction]] the notion of cograph of a functor has an evident generalization to $(\infty,1)$-categories.



## Definition 

### In terms of hom-equivalences

+-- {: .un_defn}
###### Definition
**(in terms of hom equivalence induced by unit map)**

A pair of [[(∞,1)-functors]] 

$$ 
  C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} 
  D
$$

is an adjunction, if there exists a _unit transformation_ 
$\epsilon : Id_C \to R \circ L$ -- a morphism in the [[(∞,1)-category of (∞,1)-functors]] $Func(C,C)$ -- such that for all $c \in C$ and $d \in D$ the induced morphism

$$
  Hom_C(L(c),d)
   \stackrel{R_{L(c), d}}{\to}  
  Hom_D(R(L(c)), R(d))
  \stackrel{Hom_D(\epsilon, R(d))}{\to}
  Hom_D(c,R(d))
$$

is an equivalence of [[∞-groupoids]].

=--

In terms of the concrete incarnation of the notion of $(\infty,1)$-category by the notion of [[quasi-category]], we have that $Hom_(C)(L(c),d)$ and $Hom_D(c,R(d))$ are incarnated as [[hom-object in a quasi-category|hom-objects in quasi-categories]], which are [[Kan complexes]], and the above equivalence is a [[homotopy equivalence]] of Kan complexes.

In this form this definition appears as [[Higher Topos Theory|HTT, def. 5.2.2.7]].

### In terms of cographs

We make use here of the explicit realization of the [[(∞,1)-Grothendieck construction]] in its incarnation for [[quasi-categories]]: here an [[(∞,1)-functors]] $L : D \to C$ may be regarded as a map $\Delta[1]^{op} \to $ [[(∞,1)Cat]], which corresponds under the Grothendieck construction to a [[Cartesian fibration]] of [[simplicial sets]] $coGraph(L) \to \Delta[1]$. 

+-- {: .un_defn}
###### Definition
**(in terms of Cartesian/coCartesian fibrations)**

Let $C$ and $D$ be [[quasi-categories]]. An **adjunction** between $C$ and $D$ is 

* a morphism $K \to \Delta[1]$ of [[simplicial sets]], which is both a [[Cartesian fibration]] as well as a coCartesian fibration.

* together with [[equivalence of quasi-categories]] $C \stackrel{\simeq}{\to} K_{\{0\}}$ and $D \stackrel{\simeq}{\to} K_{\{1\}}$.

Two [[(∞,1)-functors]] $L : C \to D$ and $R : D \to C$ are called **adjoint** -- with $L$ _left adjoint_ to $R$ and $R$ _right adjoint_ to $L$ if

* there exists an adjunction $K \to I$ in the above sense

* and $L$ and $K$ are the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-Grothendieck+construction#FibsOverInterval">associated functors to</a> the Cartesian fibation $p : K to \Delta[1]$ and the Cartesian fibration $p^{op} : K^{op} \to \Delta[1]^{op}$, respectively. 

=--


## Properties

The two diferent definition above are indeed equivalent:

+-- {: .un_prop}
###### Proposition

For $C$ and $D$ [[quasi-categories]], the two definitions of adjunction, in terms of Hom-equivalence induced by unit maps and in terms of Cartesian/coCartesian fibrations are equivalent.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.2.8]].

=--

### Uniqueness of adjoints

The adjoint of a functor is, if it exists, essentially unique:

+-- {: .un_prop}
###### Proposition

If the $(\infty,1)$-functor between quasi-categoris $L : D \to C$ admits a right adjoint $R : C \to D$, then this is unique up to homotopy.

Moreover, even the choice of homotopy is unique, up to ever higher homotopy, i.e. the collection of all right adjoints to $L$ forms a [[contractible]] [[∞-groupoid]], in the following sense:

Let $Func^L(C,D), Func^R(C,D) \subset Func(C,D)$ be the full sub-quasi-categories on the [[(∞,1)-category of (∞,1)-functors]] between $C$ and $D$ on those functors that are left adjoint and those that are right adjoints, respectively. Then there is a canonical [[equivalence of quasi-categories]] 
$$
  Func^L(C,D) \stackrel{\simeq}{\to}
  Func^R(C,D)^{op}
$$

(to the [[opposite quasi-category]]), which takes every left adjoint functor to a corresponding right adjoint.

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.1.3]] (also remark 5.2.2.2), and [[Higher Topos Theory|HTT, prop. 5.2.6.2]].

=--

### Preservation of limits and colimits {#PresOfLims}

Recall that for $(L \dashv R)$ an ordinary pair of [[adjoint functor]]s, the fact that $L$ preserves [[colimit]]s (and that $R$ preserves [[limit]]s) is a formal consequence of 

1. the hom-isomorphism $Hom_C(L(-),-) \simeq Hom_D(-,R(-))$;

1. the fact that $Hom_C(-,-) : C^{op} \times C \to Set$ preserves all limits in both arguments;

1. the [[Yoneda lemma]], which says that two objects are isomorphic if all homs out of (into them) are.

Using this one computes for all $c \in C$ and diagram $d : I \to D$

$$
\begin{aligned}
  Hom_C(L(\lim_{\to} d_i), c) & \simeq 
  Hom_D(\lim_\to d_i, R(c))
  \\
  & \simeq 
  \lim_{\leftarrow} Hom_D(d_i, R(c))
  \\
  & \simeq \lim_{\leftarrow} Hom_C(L(d_i), c)
  \\
  & \simeq Hom_C(\lim_{\to} L(d_i), c)
  \,,
\end{aligned}
$$

which implies that $L(\lim_\to d_i) \simeq \lim_\to L(d_i)$.

Now to see this in $(\infty,1)$-category theory...


### Adjunctions on homotopy categories {#OnHomotopyCat}


+-- {: .un_prop}
###### Proposition

For $(L \dashv R) : C \stackrel{\leftarrow}{\to} D$ an $(\infty,1)$-adjunction, its image under decategorifying to [[homotopy category of an (infinity,1)-category|homotopy categories]] is a pair of ordinary [[adjoint functor]]s 

$$
  (Ho(L) \dashv Ho(R)) : Ho(C) \stackrel{\leftarrow}{\to} Ho(D)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.2.9]].

This follows from that fact that for $\epsilon : Id_C \to R \circ L$ a unit of the $(\infty,1)$-adjunction, its image $Ho(\epsilon)$ is a unit for an ordinary adjunction.

=--


+-- {: .un_remark}
###### Remark

The converse statement is in general false. 

One way to find  that an ordinary adjunction of homotopy categories lifts to an $(\infty,1)$-adjunction is to exhibit it as a [[Quillen adjunction]] between [[simplicial model category]]-structures. This is discussed in the Examples-section [Simplicial and derived adjunction](#SimplicialAndDerived) below.

=--


## Examples

### Simplicial and derived adjunctions {#SimplicialAndDerived}

A large class of examples arises from adjunctions in [[sSet]]-[[enriched category theory]], and in particular from enriched [[Quillen adjunctions]] between [[simplicial model category|simplicial model categories]].

+-- {: .un_prop}
###### Proposition

For $C$ and $D$ [[sSet]]-[[enriched categories]] whose hom-objects are all [[Kan complexes]], the image 

$$
  N(A) \stackrel{\overset{N(L)}{\leftarrow}}{\underset{N(R)}{\to}}
  N(B)
$$

under the [[homotopy coherent nerve]] of an [[sSet]]-enriched adjunction between $sSet$-[[enriched categories]]

$$
  A \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  B
$$

is an adjunction of [[quasi-categories]].

Moreover, if $A$ and $B$ are equipped with the structure of a [[simplicial model category]] then the quasi-categorically [[derived functors]] 

$$
  N(A^\circ) \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  N(B^\circ)
$$

form an adjunction of quasi-categories.


=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, cor.  5.2.4.5]] and
[[Higher Topos Theory|HTT, prop. 5.2.4.6]].

=--

### Localizations


A pair of adjoint $(\infty,1)$-functors $(L \dashv R) : C \stackrel{\leftarrow}{\hookrightarrow} D$ where $R$ is a [[full and faithful (∞,1)-functor]] exhibits $C$ as a [[reflective (∞,1)-subcategory]] of $D$. This subcategory and the composite $R \circ L : D \to D$ are a [[localization of an (∞,1)-category|localization]] of $D$.

## References

Section 5.2 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

[[!redirects adjoint (∞,1)-functor]]
[[!redirects adjoint (infinity,1)-functors]]
[[!redirects adjoint (∞,1)-functors]]