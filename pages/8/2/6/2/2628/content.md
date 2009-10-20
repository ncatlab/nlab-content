
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The _simplicial deRham complex_ of a [[simplicial object|simplicial]] [[manifold]] $X_\bullet$ is the analog of the [[deRham complex]] of [[differential form]]s of an ordinary [[manifold]]: it is the complex whose elements in degree $k$ may be thought of as $k$-[[differential form|form]]s on $X_\bullet$.

One useful conceptual way to think of this is to notice that a a [[simplicial object|simplicial]] [[manifold]] may be thought of as a degreewise [[representable functor|representable]] [[simplicial presheaf]] on [[Diff]]
and then to realize that by way of the standard [[model structure on simplicial presheaves]] such a simplicial presheaf presents an [[∞-stack]] on [[Diff]] which we may think of as a [[Lie ∞-groupoid]]. From that perspective we expect that 

+-- {: .standout}

**Slogan**. The simplicial deRham complex is the complex of differential forms on a [[Lie ∞-groupoid]] or differentiable [[∞-stack]].

=--

We shall discuss this in more detail below.

#Definition#

There are several definitions that are [[quasi-isomorphic]]. The first one we give is the conceptually most straightforward one. The second one we give is sometimes more useful in computations.

Let $X_\bullet : \Delta^{op} \to Diff$ be a [[simplicial object|simplicial]] [[manifold]]. 

+-- {: .un_defn}
###### Definition
**(simplicial deRahm complex, first version)**

Write $\mathcal{A}(X_\bullet)$ for the [[cochain complex]] that is the [[total complex]] of the [[double complex]] on the degreewise [[deRham complex]] with one differential the simplicial-degree-wise deRham differential and the other one the deRham-degree-wise alternating sum of pullback along the face maps

$$
  \array{
   \Omega^p(X_q) &\stackrel{\sum_i (-1)^i \delta_i^*}{\to}
    & \Omega^{p}(X_{q+1})
    \\
    \downarrow^{d_{dR}} && \downarrow^{d_{dR}}
    \\
    \Omega^{p+1}(X_q) 
     &\stackrel{\sum_i (-1)^i \delta_i^*}{\to}
    & \Omega^{p+1}(X_{q+1})
  }
  \,.
$$ 

=--


So an element $\omega \in \mathcal{A}(X_\bullet)$ in degree $n$ is a collection $(\omega^p_q \in \Omega^p(X_q))_{p+q = n}$ of ordinary differential forms.


+-- {: .un_defn}
###### Definition
**(simplicial deRahm complex, second version)**

Write $\Delta^n_{Diff}$ for the standard $n$-[[simplex]] in its standard incarnations as a smooth [[manifold]] (with boundary). These arrange in the obvious way into the [[cosimplicial object]] $\Delta_{Diff} : \Delta \to Diff$.

Say that a differential form $\omega^p_q \in \Omega^\bullet(\Delta^p_{Diff}\times X_q)$ is _compatible_ if for each face map $\delta_i$ we have

> (some condition, need to look something up...)

There is a decomposition 

$$
  \Omega^n(\Delta^p_{Diff} \times X_q)
  \simeq
  \oplus_{k+l=n} \Omega^k(\Delta^p_{Diff}) 
   \otimes_{C^\infty(\Delta^p_{Diff} \times X_q)}
   \Omega^l(X_q)
  \,.
$$

This defines a bidegree and $A(X_\bullet)$ is the obvious total complex of the obvious double complex here

> will polish this up later...

=--

The following proposition says that and how these two complexes are related.

+-- {: .un_prop}
###### Proposition
**(Dupont)**

Consider the map between the two [[double complex]]es involved above which integrates each element in degree $(p,q)$ over $\Delta^p_{Diff}$. This induces a map on the corresponding total complexes
$$
  \int_\Delta : A(X_\bullet) \to \mathcal{A}(X_\bullet)
  \,.
$$
This is a [[morphism]] of [[cochain complex]]es which is a [[quasi-isomorphism]].

=--

#Examples#

## differential forms on $\mathbf{B}G$ ##

A main application of this technology is to the simplicial manifold $\mathbf{B}G = (\cdots G \times G \stackrel{\stackrel{\to}{\to}}{\to} G \stackrel{\to}{\to} {*})$ that represents the smooth groupoid which is the [[delooping]] of a [[Lie group]] $G$.

Dupont exhibits a [[Chern-Weil homomorphism]]

$$
  I(G) \to A(\mathbf{B}G)
$$

and constructs a canonical [[connection on a bundle|connection]] on the [[generalized universal bundle|universal G-principal-bundle]]

$$
  \mathbf{E}G \to \mathbf{B}G
$$

(which, in traditional [[simplicial group]] notation, reads $W G \to \bar W G$ -- but recall that these are "Lie" simplicial groups here).


# Reformulations in synthetic differential geometry #

+-- {: .query}

[[Urs Schreiber]]: This section is supposed to provide a useful reformulation of the simplicial deRham complex in the context described at [[schreiber:∞-Lie theory]].

In the language uses there, the statement we establish is the following:

=--

+-- {: .un_prop}
###### Proposition

Let $(\mathcal{T} = Sh(C),R)$ be a [[Models for Smooth Infinitesimal Analysis|well adapted]] [[smooth topos]]. Regard the simplicial manifold $X_\bullet$ accordingly as an object $X$ in the corresponding [[schreiber:smooth (∞,1)-topos|smooth (∞,1)-topos]] $\mathbf{H}$. Let $\Pi^{inf}(X)$ be its [[schreiber:infinitesimal path ∞-groupoid|infinitesimal path ∞-groupoid]]. Then

* the [[schreiber:Chevalley-Eilenberg algebra|Chevalley-Eilenberg algebra]] of $\Pi^{inf}(X)$ is [[quasi-isomorphism|quasi-isomorphic]] to the simplicial deRham complex

  $$
    CE( \Pi^{inf}(X)) \simeq \mathcal{A}(X_\bullet)
    \,.
  $$

=--

The following discussion breaks this down and then describes the proof.

As a preparation, recall from the discussion at [[differential forms in synthetic differential geometry]] that if we pass from [[Diff]] to a [[smooth topos]] $(\mathcal{T},R)$ that models the axioms of [[synthetic differential geometry]], then for sufficiently well-behaved objects $X \in \mathcal{T}$ there is the [[infinitesimal singular simplicial complex]] $X^{\Delta^\bullet_{inf}} : \Delta^{op} \to \mathcal{T}$, the [[simplicial object]] that in degree $k$ is the [[space]] of [[infinitesimal object|infinitesimal]] $k$-[[simplex|simplices]] in $X$.

As discussed there, this is such that under the [[Dold-Kan correspondence]] the [[cosimplicial algebra]] $Hom( X^{\Delta^\bullet_{inf}}, R )$ maps to the [[deRham complex]] (and under the [[monoidal Dold-Kan correspondence]] to the full [[deRham dg-algebra]]):

$$
  C_{Moore} : 
  C^\infty( X^{\Delta^\bullet_{inf}})
  \mapsto
  \Omega^\bullet(X)
  \,.
$$

It would be nice to have an analog of this statement for simplicial objects and the simplicial deRham complex. I am thinking that the answer should be the following:

Let $X_\bullet : \Delta^{op} \to \mathcal{T}$ be a [[simplicial object]] that is degreewise of the sort such that the [[infinitesimal singular simplicial complex]] $(X_n)^{\Delta^\bullet_{inf}}$ exists. Use that $\mathcal{T}$ is canonically [[copower|tensored]] over $Set$ to find that simplicial objects in $\mathcal{T}$ are canonically tensored over [[simplicial set]]s. Then consider the _realization_

$$
  \Pi^{inf}(X_\bullet) := \int^{[n] \in \Delta}
    \Delta[n] \cdot X_n^{\Delta^{\bullet}_{inf}}
$$

where

* $\Delta[n]$ is the standard [[simplicial set|simplicial]] $n$-[[simplex]]

* the integrand is the tensor operatoin of simplicial objects by simplicial sets

* the integral sign denotes the [[coend]].

By the lemma _expression in terms of simplicial realization_ at [[schreiber:infinitesimal path ∞-groupoid]] this is the same as $\Pi^{inf}(X)$.

The above proposition now reads in pedestrian terms:

+-- {: .un_prop}
###### Proposition

The [[Moore complex|Moore cochain complex]] of the [[cosimplicial algebra]] $C^\infty(\Pi^{inf}(X_\bullet)) := Hom_{\mathcal{T}}(\Pi^{inf}(X_\bullet),R)$ is [[quasi-isomorphism|quasi-isomorphic]] to the simplicial deRham complex of $X_\bullet$.

=--


+-- {: .proof}
###### Proof

The problem is entirely controlled by the [[bisimplicial object]] $([p],[q]) \mapsto (X_p)^{\Delta^q_{inf}}$.
We know that 

* for fixed $p$, the normalized [[Moore complex]] of the [[cosimplicial algebra]] $Hom((X_p)^{\Delta^\bullet_{inf}},R)$ is the [[deRham complex]] of $X_p$ -- this is the statement about combinatorial [[differential forms in synthetic differential geometry]].

* for fixed $q$ the [[Moore complex]] of the [[cosimplicial algebra]] $Hom((X_\bullet)^{\Delta^q_{inf}}, R)$ is the complex of functions on simplices whose differential is the alternating sum of pullbacks along face maps -- by the very definition of the [[Moore complex]].

This means that the simplicial deRham complex is (quasi-isomorphic to) the total complex of the bi-cosimplicial algebra

$$
  \mathcal{A}(X_\bullet) \simeq
  Tot(Hom((X_\bullet)^{\Delta^\bullet_{inf}}, R))
  \,.
$$

So it remains to show that this total complex is also (quasi-isomorphic to) the [[Moore complex]] of $Hom(\Pi^{inf}(X_\bullet),R)$. For this use [exercise 1.6 here](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) which says (transported from [[Set]] to $\mathcal{T}$) that this is the diagonal [[simplicial object]] of our [[bisimplicial object]]

$$
  d((X_\bullet)^{\Delta^\bullet_{inf}})
  \simeq
  \int^{[n]} \Delta^n \cdot (X_n)^{\Delta^\bullet_{inf}}
  \,.
$$

This implies that the [[Moore complex]] of $Hom(\Pi^{inf}(X_\bullet),R)$ is the Moore complex of the diagonal of the bisimplicial algebra $Hom(\Pi^{inf}(X_\bullet),R)$.

This way the desired statement recudes to the quasi-isomorphism 

$$
  diag (Hom(\Pi^{inf}(X_\bullet),R)
  \simeq
  Tot (Hom(\Pi^{inf}(X_\bullet),R)
  \,.
$$

But this (even their chain-homotopy equivalence) is the content of the generalized [[Eilenberg-Zilber theorem]].

=--


#References#

Canonical references on simplicial deRham cohomology are by [[Jean-Luc Dupont]]. For instance

* J. L Dupont, _Simplicial deRham Cohomology and characteristic classes of flat bundles_ Topology 15 (1976)

* J. L- Dupont, _A dual simplicial de Rham complex_, Lecture notes in Mathematics 1318 (1988) ([journal](http://www.springerlink.com/content/65784420x146888h/))

* chaper 3 in _Curvature and Characteristic Classes_

>(I am still looking for the best survey reference...)

When restricted to low degree this is closely related to or synonymous to considerations of deRham cohomology in the context of [[differentiable stack]]s.

> (need to dig out references)


In principle closely related is the discussion of a deRham theorem for [[∞-stack]]s as discussed in

* [[nLab:Carlos Simpson|Carlos Simpson]], [[nLab:Constantin Teleman|Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

though a simplicial deRham complex is only somewhat implicit in that article.

> A related discussion is at [[schreiber:deRham theorem for ∞-Lie groupoids]]s