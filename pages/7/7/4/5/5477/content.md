
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[site]] being _locally and globally $\infty$-connected_ means that it satisfies sufficient conditions such that the [[(∞,1)-category of (∞,1)-sheaves]] over it is a [[locally ∞-connected (∞,1)-topos]] and a [[∞-connected (∞,1)-topos]].


## Definition

+-- {: .un_def}
###### Definition

A a [[site]] is **locally and globally $\infty$-connected** over [[∞Grpd]] 
if

* it has a [[terminal object]] *

* for every [[covering]] family $\{U_i \to U\}$ in $C$ 

  1. the [[Cech nerve]] $C(\{U_i\}) \in [C^{op}, sSet]$ is degreewise 
       a [[coproduct]] of [[representable functor|representables]];

  1. the [[simplicial set]] obtained by replacing each copy of 
     a representable by a point is [[contractible]], equivalently
     the [[colimit]] $\lim_\to : [C^{op}, sSet] \to sSet$ 
     of $C(\{U_i\})$ has a [[weak homotopy equivalence]] to the point

     $$
       \lim_\to C(\{U\}) \stackrel{\simeq}{\to} *
       \,.
     $$
  
=--

## Properties

+-- {: .un_theorem}
###### Theorem

The [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(C)$ over locally and globally $\infty$-conneted site $C$, regarded as an [[(∞,1)-site]], is a ([[n-localic (∞,1)-topos|1-localic]]) [[locally ∞-connected (∞,1)-topos]] and [[∞-connected (∞,1)-topos]], in that it comes with a triple of [[adjoint (∞,1)-functor]]s

$$
  (\Pi \dashv \Delta \dashv \Gamma) :
  Sh_{(\infty,1)}(C)
  \stackrel{\stackrel{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
$$

such that $\Pi$ preserves the [[terminal object]].

=--

To prove this, we we use the [[model structure on simplicial presheaves]] to [[locally presentable (∞,1)-category|present]] $Sh_{(\infty,1)}(C)$. 

Write $[C^{op}, sSet]_{proj}$ for the projective global model structure and $[C^{op}, sSet]_{proj,loc}$ for its [[Bousfield localization of model categories|left Bousfield localization]] at the set of morphisms $C(\{U_i\}) \to U$ out of the [[Cech nerve]] for each covering family $\{U_i \to U\}$, and $[C^{op}, sSet]_{proj,loc}^\circ$ for the [[Kan complex]]-[[enriched category]] on the fibrant-cofibrant objects. By the discussion at [[model structure on simplicial presheaves]] we have

$$
  Sh_{(\infty,1)}(C) \simeq [C^{op}, sSet]_{proj, loc}^\circ
$$

and the [[adjoint (∞,1)-functor]]s on the left are presented by [[simplicial Quillen adjunction]]s on the right. 

To establish these, we proceed by a sequence of lemmas.


+-- {: .un_lemma}
###### Standard fact

The model categories

* standard [[model structure on simplicial sets]] $sSet_{Quillen}$;

*  global [[model structure on simplicial presheaves]]  $[C^{op}, sSet]_{proj,loc}$;


*  local [[model structure on simplicial presheaves]]  $[C^{op}, sSet]_{proj,loc}$

are all  [[left proper model categories]].

=--

+-- {: .proof}
###### Proof

The first since all objects are cofibrant. The second by general statements about the global [[model structure on functors]], the third because [[Bousfield localization of model categories|left Bousfield localization]] preserves left propernes.

=--

+-- {: .un_lemma}
###### Lemma

For $\{U_i \to U\}$ a [[covering]] family in the $\infty$-connected site $C$, the [[Cech nerve]]
$C(\{U_i\}) \in [C^{op}, sSet]$ is a cofibrant [[resolution]] of $U$ both in the projective model structure $[C^{op}, sSet]_{proj}$ as well as in the Cech local model structure $[C^{op}, sSet]_{proj,loc}$.

=--

+-- {: .proof}
###### Proof

By assumption on $C$ we have that $C(\{U_i\})$ is a [[split hypercover]]. By <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects">Dugger's theorem on cofibrant objects</a> in the projective model structure this implies that $C(U)$ is cofibrant in the global model structure. By general properties of left [[Bousfield localization of model categories|Bousfield localization]] we have that the cofibrations in the local model structure as the same as in the global one. Finally that $C(\{U_i\}) \to U$ is a weak equivalence in the local model structure holds effectively by definition (since we are localizing at these morphisms).

=--

+-- {: .un_prop}
###### Proposition

On a locally and globally $\infty$-connected site $C$ 
the [[global section]] [[(∞,1)-geometric morphism]]

$$  
  (\Delta \dashv \Gamma) : Sh_{(\infty,1)}(C) 
  \stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

is [[presentable (∞,1)-category|presented]] by the 
[[simplicial Quillen adjunction]]

$$
  (Const \dashv \Gamma) :  [C^{op}, sSet]_{proj,loc}
  \stackrel{\leftarrow}{\to}
  sSet_{Quillen}
  \,,
$$

where $\Gamma$ is the functor that evaluates on the point, $\Gamma X = X(*)$, and $Const$ is the functor that sends a simplicial set $S$ to the presheaf constant on that value, $Const S : U \mapsto S$.

=--

+-- {: .proof}
###### Proof

We use (as described there) that [[adjoint (∞,1)-functor]]s are modeled by [[simplicial Quillen adjunction]]s between the [[simplicial model categories]] that model the $(\infty,1)$-categories in question.

That we have an [[adjunction]] $(Const \dashv \Gamma)$ follows for instance by observing that since $C$ has a [[terminal object]] we may think of $\Gamma$ as being the functor $\Gamma = \lim_\leftarrow$ that takes the [[limit]]. 

To see that we have a [[Quillen adjunction]] first notice that we have a Quillen adjunction

$$
  (Const \dashv \Gamma) :  
  [C^{op}, sSet]_{proj}
  \stackrel{\leftarrow}{\to}
  sSet_{Quillen}
$$

on the global model structure, since $\Gamma$ manifestly preserves fibrations and acyclic fibrations there. Since $[C^{op}, sSet]_{proj,loc}$ is [[proper model category|left proper]] and has the same cofibrations as the global model structure, it follows with [[Higher Topos Theory|HTT, corollary A.3.7.2]] (see the discussion of <a href="http://ncatlab.org/nlab/show/Quillen+adjunction#sSet">sSet-Quillen adjunctions</a>) that for 
this to descend to a Quillen adjunction on the local model structure it is sufficient that $\Gamma$ preserves fibrant objects. But every fibrant object in the local structure is in particular fibrant in the global structure, hence in particular fibrant over the terminal object of $C$.

The left [[derived functor]] of $Const : sSet_{Quillen} \to [C^{op},sSet]_{proj}$ preserves [[homotopy limit]]s (because [[(∞,1)-limit]]s in an [[(∞,1)-category of (∞,1)-presheaves]] are computed objectwise), and [[∞-stackification]], the left derived functor of $Id : [C^{op}, sSet]_{proj} \to [C^{op}, sSet]_{proj,loc}$ is a left [[exact (∞,1)-functor]], therefore the left derived functor of $Const : sSet_{Quillen} \to [C^{op}, sSet]_{proj,loc}$ preserves finite homotopy limits.

This means that our Quillen adjunction does model a [[(∞,1)-geometric morphism]] $Sh_{(\infty,1)}(C) \to \infty Grpd$. By the discussion at [[global section]] the space of these geometric morphisms to [[∞Grpd]] is [[contractible]], hence this is indeed a representative of the terminal geometric morphism as claimed.

=--

+-- {: .proof}
###### Proof of the theorem

By general abstract facts the [[sSet]]-functor $Const : sSet \to [C^{op}, sSet]$ given on $S \in sSet$ by $Const_S : U \mapsto S$ for all $U \in C$ has an  [[sSet]]-[[left adjoint]] 

$$
  \Pi : X \mapsto \int^U X(U) = \lim_\to X
$$ 

naturally in $X$ and $S$, given by the [[colimit]] operation. Notice that since [[sSet]] is itself a [[category of presheaves]] (on the [[simplex category]]), these colimits are degreewise colimits in [[Set]]. Also notice that the colimit over a [[representable functor]] is the point (by a simple [[Yoneda lemma]]-style argument).

Regarded as a functor  $sSet_{Quillen} \to [C^{op}, sSet]_{proj}$ the functor $Const$ manifestly preserves fibrations and acyclic fibrations and hence

$$
  (\Pi \dashv Const) : [C^{op}, sSet]_{proj} 
      \stackrel{\overset{\lim_\to}{\to}}{\underset{Const}{\leftarrow}}
    sSet_{Quillen} 
$$

is a [[Quillen adjunction]], in particular $\Pi : [C^{op},sSet]_{proj} \to sSet_{Quillen}$ preserves cofibrations. Since by general properties of left [[Bousfield localization of model categories]] the cofibrations of $[C^{op},sSet]_{proj,loc}$ are the same, also $\Pi : [C^{op}, sSet]_{proj,loc} \to sSet_{Quillen}$ preserves cofibrations. 

Since $sSet_{Quillen}$ is a [[left proper model category]] it follows as before with [[Higher Topos Theory|HTT, corollary A.3.7.2]] (see the discussion of <a href="http://ncatlab.org/nlab/show/Quillen+adjunction#sSet">sSet-Quillen adjunctions</a>) that for 

$$
  (\Pi \dashv Const) : [C^{op}, sSet]_{proj,loc}
   \stackrel{\overset{\lim_\to}{\to}}{\underset{Const}{\leftarrow}}
   sSet_{Quillen}
$$

to be a [[Quillen adjunction]], it suffices to show that $Const$ preserves fibrant objects. That means that constant simplicial presheaves satisfy [[descent]] along [[covering]] families in the $\infty$-cohesive site $C$: for every covering family $\{U_i \to U\}$ in $C$ and every simplicial set $S$ it must be true that

$$
  [C^{op}, sSet](U, Const S) \to [C^{op}, sSet](C(U), Const S)
$$

is a [[homotopy equivalence]] of [[Kan complexes]]. (Here we use that $U$, being a [[representable functor|representable]], is cofibrant, that $C(U)$ is cofibrant by the above lemma and that $Const S$ is fibrant in the projective structure by the assumption that $S$ is fibrant. So the simplicial hom-complexes in the above equaltion really are the correct [[derived hom-space]]s.)

But that this is the case follows by the condition on the $\infty$-cohesive site $C$ by which $\lim_\to C(U) \simeq *$: using this it follows that

$$
  [C^{op}, sSet](C(U), Const S) = sSet(\lim_\to C(U), S) \simeq sSet(*, S) = S
  \,.
$$

So we have established that also

$$
  (\Pi \dashv Const) : [C^{op}, sSet]_{proj,loc} \stackrel{\overset{\lim_\to}{\to}}{\underset{Const}{\leftarrow}}
  sSet_{Quillen}
$$

is a [[Quillen adjunction]].

It is clear that the left [[derived functor]] of $\Pi$ preserves the terminal object: since that is representable by assumption on $C$, it is cofibrant in $[C^{op}, sSet]_{proj,loc}$, hence $\mathbb{L} \lim_\to * = \lim_\to * = *$.


=--


## Examples


+-- {: .un_prop}
###### Proposition

The sites

* [[CartSp]], [[ThCartSp]].

are locally and globally $\infty$-connected and in fact [[∞-cohesive site|∞-cohesive]].

=--

This implies that [[∞LieGrpd]] is a [[cohesive (∞,1)-topos]]. See there for details.




## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected (∞,1)-site]]

  * [[connected site]] / **∞-connected (∞,1)-site**

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]], [[∞-cohesive site]]


[[!redirects ∞-connected site]]
[[!redirects infinity-connected site]]

[[!redirects ∞-connected sites]]
[[!redirects infinity-connected sites]]


[[!redirects ∞-connected (∞,1)-site]]
[[!redirects ∞-connected (∞,1)-sites]]
