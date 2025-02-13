
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _simplicial de Rham complex_ of a [[simplicial manifold]] $X_\bullet$ is the analog of the [[de Rham complex]] of [[differential form]]s of an ordinary [[manifold]]: it is the complex whose elements in degree $k$ may be thought of as $k$-[[differential form|form]]s on $X_\bullet$.

One useful conceptual way to think of this is to notice that a a [[simplicial object|simplicial]] [[manifold]] may be thought of as a degreewise [[representable functor|representable]] [[simplicial presheaf]] on [[Diff]]
and then to realize that by way of the standard [[model structure on simplicial presheaves]] such a simplicial presheaf presents an [[∞-stack]] on [[Diff]] which we may think of as a [[Lie ∞-groupoid]]. From that perspective we expect that 

+-- {: .standout}

**Slogan**. The simplicial de Rham complex is the complex of differential forms on a geometric [[∞-Lie groupoid]].

=--

We shall discuss this in more detail below.

## Definition

There are several definitions that are [[quasi-isomorphism|quasi-isomorphic]]. The first one we give is the conceptually most straightforward one. The second one we give is sometimes more useful in computations.

Let $X_\bullet : \Delta^{op} \to Diff$ be a [[simplicial object|simplicial]] [[manifold]]. 

+-- {: .num_defn}
###### Definition
**(simplicial de Rham complex, first version)**

Write 

$$
  \mathcal{A}(X_\bullet)
  :=
  Tot \Omega^\bullet(X_\bullet)
$$ 

for the [[cochain complex]] that is the [[total complex]] of the [[double complex]] on the degreewise [[de Rham complex]] with one differential the simplicial-degree-wise de Rham differential and the other one the de Rham-degree-wise alternating sum of pullback along the face maps

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


+-- {: .num_defn}
###### Definition
**(simplicial de Rham complex, second version)**

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

+-- {: .num_prop}
###### Proposition
**(Dupont)**

Consider the map between the two [[double complex]]es involved above which integrates each element in degree $(p,q)$ over $\Delta^p_{Diff}$. This induces a map on the corresponding total complexes
$$
  \int_\Delta : A(X_\bullet) \to \mathcal{A}(X_\bullet)
  \,.
$$
This is a [[morphism]] of [[cochain complex]]es which is a [[quasi-isomorphism]].

=--

## Examples

### Differential forms on $\mathbf{B}G$ 

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


## Reformulations in synthetic differential geometry 

+-- {: .query}

[[Urs Schreiber]]: This section is supposed to provide a useful reformulation of the simplicial de Rham complex in the context described at [[schreiber:∞-Lie theory]].

In the language uses there, the statement we establish is the following:

=--

+-- {: .num_prop}
###### Proposition

Let $C = $ [[CartSp]]${}_{th}$ and $\mathbf{H} = (sPSh(C)_{proj}^{loc})^\circ$ the [[(∞,1)-category of (∞,1)-sheaves]] on [[CartSp]], the [[(∞,1)-topos]] of [[Lie ∞-groupoid]]s. This is a [[locally contractible (∞,1)-topos]] (as discussed there). Accordinly we have its [[schreiber:path ∞-groupoid]] and [[schreiber:infinitesimal path ∞-groupoid]] $\mathbf{\Pi}_{inf}(-)$.

Then

* the [[schreiber:Chevalley-Eilenberg algebra]] of $\mathbf{\Pi}_{inf}(X)$ is [[quasi-isomorphism|quasi-isomorphic]] to the simplicial de Rham complex

  $$
    CE( \Pi^{inf}(X)) \simeq \mathcal{A}(X_\bullet)
    \,.
  $$

=--

The following discussion breaks this down and then describes the proof.

As a preparation, recall from the discussion at [[differential forms in synthetic differential geometry]] that if we pass from [[Diff]] to a [[smooth topos]] $(\mathcal{T},R)$ that models the axioms of [[synthetic differential geometry]], then for sufficiently well-behaved objects $X \in \mathcal{T}$ there is the [[infinitesimal singular simplicial complex]] $X^{(\Delta^\bullet_{inf})} : \Delta^{op} \to \mathcal{T}$, the [[simplicial object]] that in degree $k$ is the [[space]] of [[infinitesimal object|infinitesimal]] $k$-[[simplex|simplices]] in $X$.

As discussed there, this is such that under the [[Dold-Kan correspondence]] the [[cosimplicial algebra]] $Hom( X^{\Delta^\bullet_{inf}}, R )$ maps to the [[de Rham complex]] (and under the [[monoidal Dold-Kan correspondence]] to the full [[de Rham dg-algebra]]):

$$
  C_{Moore} : 
  C^\infty( X^{(\Delta^\bullet_{inf}}))
  \mapsto
  \Omega^\bullet(X)
  \,.
$$

It would be nice to have an analog of this statement for simplicial objects and the simplicial de Rham complex. I am thinking that the answer should be the following:

Let $X_\bullet : \Delta^{op} \to \mathcal{T}$ be a [[simplicial object]] that is degreewise of the sort such that the [[infinitesimal singular simplicial complex]] $(X_n)^{\Delta^\bullet_{inf}}$ exists. Use that $\mathcal{T}$ is canonically [[copower|tensored]] over $Set$ to find that simplicial objects in $\mathcal{T}$ are canonically tensored over [[simplicial set]]s. Then consider the _realization_

$$
  \mathbf{\Pi}_{inf}(X_\bullet) := \int^{[n] \in \Delta}
    \Delta[n] \cdot X_n^{(\Delta^{\bullet}_{inf})}
$$

where

* $\Delta[n]$ is the standard [[simplicial set|simplicial]] $n$-[[simplex]]

* the integrand is the tensor operatoin of simplicial objects by simplicial sets

* the integral sign denotes the [[coend]].

By the lemma _expression in terms of simplicial realization_ at [[schreiber:infinitesimal path ∞-groupoid]] this is the same as $\mathbf{\Pi}_{inf}(X)$.

The above proposition now reads in pedestrian terms:

+-- {: .num_prop}
###### Proposition

The [[Moore complex|Moore cochain complex]] of the [[cosimplicial algebra]] $C^\infty(\mathbf{\Pi}_{inf}(X_\bullet)) := Hom_{\mathcal{T}}(\mathbf{\Pi}_{inf}(X_\bullet),R)$ is [[quasi-isomorphism|quasi-isomorphic]] to the simplicial de Rham complex of $X_\bullet$.

=--


+-- {: .proof}
###### Proof

We use the cosimplicial and the simplicial version of the [[Eilenberg-Zilber theorem]] together with the fact that for a [[bisimplicial set]] the diagonal is given by the realization (as discussed there) $Diag F_{\bullet,\bullet} \simeq \int^{[n] \in \Delta} \Delta[n] \cdot F_{n,\bullet}$ to compute

$$
  \begin{aligned}
    C ( C^\infty(\mathbf{\Pi}_{inf}(X_\bullet)) )
    & :=
    C ( Hom( \int^{[n]} \Delta[n] \cdot X_n^{(\Delta^\bullet_{inf})}  
    , R))
    \\
    & \simeq
    C ( Hom( Diag X_\bullet^{(\Delta^\bullet_{inf})} , R))    
    \\
    & \simeq
    C Diag Hom( X_\bullet^{(\Delta^\bullet_{inf})} ,R)
    \\
    & \simeq_{q i}
    Tot C Hom( X_\bullet^{(\Delta^\bullet_{inf})} ,R)
    \\
    & \simeq 
    Tot \Omega^\bullet(X_\bullet)
    \,.
  \end{aligned}
$$

Here in the last step we used the following reasoning on the [[bisimplicial object]] $([p],[q]) \mapsto (X_p)^{(\Delta^q_{inf})}$.
We know that 

* for fixed $p$, the normalized [[Moore complex]] of the [[cosimplicial algebra]] $Hom((X_p)^{(\Delta^\bullet_{inf})},R)$ is the [[de Rham complex]] of $X_p$ -- this is the statement about combinatorial [[differential forms in synthetic differential geometry]].

* for fixed $q$ the [[Moore complex]] of the [[cosimplicial algebra]] $Hom((X_\bullet)^{((\Delta^q_{inf}))}, R)$ is the complex of functions on simplices whose differential is the alternating sum of pullbacks along face maps -- by the very definition of the [[Moore complex]].

This means that the simplicial de Rham complex is (quasi-isomorphic to) the total complex of the bi-cosimplicial algebra

$$
  \mathcal{A}(X_\bullet) \simeq
  Tot C(Hom((X_\bullet)^{(\Delta^\bullet_{inf})}, R))
  \,.
$$

So it remains to show that this total complex is also (quasi-isomorphic to) the [[Moore complex]] of $Hom(\mathbf{\Pi}_{inf}(X_\bullet),R)$. For this use [exercise 1.6 here](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) which says (transported from [[Set]] to $\mathcal{T}$) that this is the diagonal [[simplicial object]] of our [[bisimplicial object]]

$$
  d((X_\bullet)^{\Delta^\bullet_{inf}})
  \simeq
  \int^{[n]} \Delta^n \cdot (X_n)^{(\Delta^\bullet_{inf})}
  \,.
$$

This implies that the [[Moore complex]] of $Hom(\mathbf{\Pi}_{inf}(X_\bullet),R)$ is the Moore complex of the diagonal of the bisimplicial algebra $Hom(X_\bullet^{(\Delta^\bullet_{inf})}),R)$.

This way the desired statement recudes to the quasi-isomorphism 

$$
  diag (Hom(\mathbf{\Pi}_{inf}(X_\bullet),R)
  \simeq
  Tot (Hom(\mathbf{\Pi}_{inf}(X_\bullet),R)
  \,.
$$

But this (even their chain-homotopy equivalence) is the content of the generalized [[Eilenberg-Zilber theorem]].

=--


## References

Canonical references on simplicial de Rham cohomology are by [[Johan Louis Dupont]]. For instance

* [[Johan Louis Dupont]], _Simplicial de Rham Cohomology and characteristic classes of flat bundles_ Topology 15 (1976)

* [[Johan Louis Dupont]], _A dual simplicial de Rham complex_, Lecture notes in Mathematics 1318 (1988) ([journal](http://www.springerlink.com/content/65784420x146888h/))

* chaper 3 in _Curvature and Characteristic Classes_

>(I am still looking for the best survey reference...)

When restricted to low degree this is closely related to or synonymous to considerations of de Rham cohomology in the context of [[differentiable stack]]s.

> (need to dig out references)


A [[de Rham theorem]] for simplicial manifolds was proven in the classical

* {#BottShulmanStasheff76} [[Raoul Bott]], [[Herbert Shulman]], [[Jim Stasheff]], _On the de Rham theory of certain classifying spaces_, Advances in Mathematics, Volume 20, Issue 1, April 1976, Pages 43-56 (<a href="https://doi.org/10.1016/0001-8708(76)90169-9">doi:10.1016/0001-8708(76)90169-9</a>, [pdf](https://core.ac.uk/download/pdf/82496263.pdf))



In principle closely related is the discussion of a de Rham theorem for [[∞-stack]]s as discussed in

* [[nLab:Carlos Simpson|Carlos Simpson]], [[nLab:Constantin Teleman|Constantin Teleman]], _de Rham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

though a simplicial de Rham complex is only somewhat implicit in that article.



[[!redirects simplicial deRham complex]]