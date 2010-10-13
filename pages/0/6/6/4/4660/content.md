
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

_Lie group cohomology_ generalizes the notion of [[group cohomology]] from bare [[group]]s to [[Lie group]]s.

From the [[nPOV]] on [[cohomology]], a natural definition is that for $G$ a Lie group, its cohomology is the intrinsic cohomology of its [[delooping]] [[Lie groupoid]] $\mathbf{B}G$ in the [[(∞,1)-topos]] $\mathbf{H} =$ [[?LieGrpd]].

In the literature one finds a sequence of definitions that approach this intrisic topos-theoretic definition. This is discussed below. For a detailed discussion of the relation of this to the intrinsic topos-theoretic definition see the section <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#CohomologyOfLieGroups">Cohomology of Lie groups</a> at [[∞-Lie groupoid]].


### Structured group cohomology

If the groups in question are not [[group object]]s internal to [[Set]] but groups with extra structure, such as [[topological group]]s or [[Lie group]]s, then their cohomology has to be understood in the corresponding natural context.

In parts of the literature cohomology of structured groups $G$ is defined in direct generalization of the formulas above as homotopy classes of morphisms from the simplicial object

$$
  \left(
    \cdots G \times G\stackrel{\to}{\stackrel{\to}{\to}}G \stackrel{\to}{\to} *
  \right)
$$

to a simplicial object $N (\mathbf{B}^n A)$.

This is what is described above. But this does **not** in general give the right answer for structured groups:

namely [[cohomology]] is really about homotopy classes of maps in the suitable ambient [[(∞,1)-topos]]. For plain groups as in the above entry, we are working in the $(\infty,1)$-topos [[∞Grpd]]. That may be modeled by the standard [[model structure on simplicial sets]]. In that model structure, all objects a cofibrant and [[Kan complex]]es are fibrant. That means all objects we are dealing with here are both cofibrant and fibrant, and hence the simplicial set of maps between them is the cofrrect [[derived hom-space]] between these objects.

But this changes as we consider groups with extra structure. For a [[Lie group]] $G$, the object

$$
  \left(
    \cdots G \times G\stackrel{\to}{\stackrel{\to}{\to}}G \stackrel{\to}{\to} *
  \right)
$$

has to be considered as an [[Lie ∞-groupoid]]: an object in the [[model structure on simplicial presheaves]] over a [[site]] such as [[Diff]] or [[CartSp]]. As such it is in general **not** both cofibrant and fibrant. To that extent plain morphisms out of this object do **not** compute the correct [[derived hom-space]]s. Instead, the right definition of structured group cohomology uses the correct fibrant and cofibrant replacements.

### Topological group cohomology

In

* [[Jim Stasheff]], _Continuous cohomology of groups and classifying spaces_  Bull. Amer. Math. Soc. Volume 84, Number 4 (1978), 513-530 ([web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183540920))

$n$-cocycles on a topological group $G$ with valzues in a topological abelian group $A$ are considered as continuous maps $G^{\times n}\to A$ (p. 3 ).

A definition in terms of [[derived functor|Ext-functor]]s and comparison with the naive definition is in 

* David Wigner, _Algebraic cohomology of topological groups_ Transactions of the American Mathematical Society, volume 178 (1973)([pdf](http://egg.epfl.ch/~nmonod/bonn/Wigner_1973.pdf))

A classical reference that considers the cohomology of Lie groups as topological spaces is

* [[Armand Borel]], _Homology and cohomology of compact connected Lie groups_ ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1063923/pdf/pnas01596-0040.pdf))

A corrected definition of topological group cohomology has been given by Segal

* [[Graeme Segal]], _Cohomology of topological groups_ In Symposia Mathematica, Vol. IV (INDAM, Rome, 1968/69), pages 377{387. Academic Press, London, (1970).

* [[Graeme Segal]], _A classifying space of a topological group in the sense of Gel'fand-Fuks. Funkcional. Anal. i Prilozen.,
9(2):48{50, (1975).





## Definition

For $G$ a [[Lie group]] and $A$ an abelian Lie group, write

$$
  H_{naive}^n(G,A) = \{smooth G^{\times n } \to A\}/_\sim
$$

for the naive notion of cohomology on $G$.

A refined definition of Lie group cohomology, denoted $H^n_{diff}(G,A)$, was given in ([Brylinski](#Brylinski)) following ([Blanc](#Blanc)) and effectively rediscovers Segal's definition. See section 4 of ([Schommer-Pries](#Shommer-Pries)) for a review and applications.

+-- {: .un_defn}
###### Definition
**(Brylinski)**

Let $G$ be a [[Lie group]] ([[paracompact space|paracompact]]) and $A$ an abelian Lie group.

For eack $k \in \mathbb{N}$ we can pick a [[good open cover]] $\{U^{k}_{i} \to G^{\times_k}| i \in I_k\}$ such that

* the index sets arrange themselves into a [[simplicial set]]
  $I : [k] \mapsto I_k$;

* and for $d_j(U^k_i)$ and $s_j(U^k_i)$ the images of the
  face and degeneracy maps of $G^{\times\bullet}$ we have

  $$
    d_j(U^k_i) \subset U^{k-1}_{d_j(i)}
  $$ 

  and

  $$
    s_j(U^k_i) \subset U^{k+1}_{s_j(i)}
    \,.
  $$

Then the **differentiable group cohomology** of $G$ with coefficients in 
$A$ is the cohomology of the total complex of the [[Cech cohomology|Cech]]
double complex $C^\infty( U^{\bullet}_{i_0, \cdots, i_\bullet} , A)$
whose differentials are the alternating sums of the face maps 
of $G^{\times_\bullet}$ and of the [[Cech nerve]]s, respectively:

$$
  H^n_{diff}(G,A) := H^n Tot C^\infty( U^{\bullet}_{i_0, \cdots, i_\bullet} , A)
$$


=--



This is definition 1.1 in 

* [[Jean-Luc Brylinski]], _Differentiable cohomology of gauge groups_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf)).

As discussed there, this is equivalent to other definitions, notably to a definition given earlier by Segal. 

There is an evident morphism

$$
  H^n_{naive}(G,A) \to H^n_{diff}(G,A)
$$

obtained by pulling back a globally defined smooth cocycle to a cover.

At [[∞-Lie groupoid]] it is discussed that there is a further refinement

$$
  H^n_{diff}(G,A) \to H^n(\mathbf{B}G,A)
  \,,
$$

where on the right we have the [[cohomology|intrinsic cohomology]] of [[∞-Lie groupoid]]s.

## Properties

### General

From now on, for definiteness by a _Lie group_ $G$ we mean (following [Bry, page3](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf#page=3)) a [[paracompact space|paracompact]] [[Frechet manifold]] equipped with a group structure such that the product and the inverse maps are smooth, and there is an everywhere defined exponential map $exp : \mathfrak{g} \to G$ where $\mathfrak{g}$ is the [[Lie algebra]] of $G$.
 

+-- {: .un_prop }
###### Proposition

If the coefficient Lie group $A$ is a [[topological vector space]], then the naive group cohomology $H^n(G,A) = \{smooth G^{\times n} \to A\}/_\sim$ coincides with the correct Lie group cohomology

$$
  (A top.\;vect.\;space) \Rightarrow 
  (H^n_{naive}(G,A) \stackrel{\simeq}{\to} H^n_{diff}(G,A) )
  \,.
$$

If the coefficient Lie group $A$ is discrete, then Lie group cohomology coindices with the topological cohomology of the [[classifying space]] $\mathcal{B}G$

$$
  (A discrete) \Rightarrow 
  (H^n(G,A) \simeq H^n(\mathcal{B}G), A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is [Bry, prop. 1.3](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf#page=4) and [Bry, lemma 1.5](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf#page=5).


=--


+-- {: .un_prop }
###### Proposition

$H^2_{diff}(G,A)$ classifies central [[group extension|extensions of Lie groups]]

$$
   A \to \hat G \stackrel{\pi}{\to} G
$$

such that $\pi : \hat G \to G$ is a locally trivial smooth [[principal bundle|principal]] $A$-fibration.

The image of $H^2_{naive}(G,A) \to H^2_{diff}(G,A)$ consists of those central extensions for which is bundle is trivial.

=--

+-- {: .proof}
###### Proof

This is [Bry, prop. 1.6](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf#page=4) and [Bry, lemma 1.5](http://arxiv.org/PS_cache/math/pdf/0011/0011069v1.pdf#page=5).


=--

### Long sequence in differential cohomology {#SequenceDiffCohomology}

For the purpose of this section we specifically conceive Lie group cohomology inside the [[(∞,1)-topos]] [[?LieGrpd]] of [[∞-Lie groupoid]]s, as described there.

This is a [[local (∞,1)-topos]], hence in particular an [[∞-connected (∞,1)-topos]] and therefore it admits [[schreiber:differential cohomology in an (∞,1)-topos]]. By the theorem about the <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#DiffCohWithGroupalCoeffs">differential fiber sequence</a>
we have for $G$ a [[Lie group]], $\mathbf{B}G$ its [[delooping]], $\mathbf{B}^{n} U(1)$ the [[∞-Lie groupoid|circle n+1-group]] a long sequence in cohomology

$$
  \cdots \to H^n_{diff}(G, (1))\to H^n_G(G,U(1)) \to H_{dR, G}^{n+1}(G) \to 
  \cdots
  \,,
$$

where $H_G(G,-)$ denotes $G$-equivariant cohomology, in that

$$
  H^n_G(G,A) := \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n A)
$$

and so on.

The point to note is that we may identify [[Lie algebra cohomology]] inside $H^n_{dR,G}(G)$ and may therefore regard the map

$$
  H^n_G(G,U(1)) \to H_{dR, G}^{n+1}(G)
$$

as the differentiation map that take a smooth group cocycle to a Lie algebra cocycle. This morphism operates by putting constructing a [[circle n-bundle with connection]] over $\mathbf{B}G$ and then computing its [[curvature]] forms.

**Example** 

For $\mathfrak{g}$ a [[semisimple Lie algebra]],$G$ its simply connected Lie group,  let $\mathbf{B}G \to \mathbf{B}^3 U(1)$ be the group cocycle that classifies the [[string 2-group]]. Its image in $H^3_{dR,G}(G)$ is the curvature of the [[Chern-Simons circle 3-bundle]] over $\mathbf{B}G$. This is represented by a simplicial differential form consisting of two pieces

* on $G$ the form $\langle \theta\wedge \theta \wedge \theta \rangle$ obtained by feeding the [[Maurer-Cartan form]] on $G$ into the canoical Lie algebra cocycle that is [[Chern-Simons element|in transtression]] with the [[Killing form]] [[invariant polynomial]];

* on $G \times G$ something like $\langle \theta_1 \wedge \theta_2\rangle$.

(...)

## Related entries

* [[group cohomology]]

  * [[nonabelian group cohomology]], [[groupoid cohomology]]

* [[group extension]]

* **Lie group cohomology** 

  * [[∞-Lie groupoid cohomology]]



## References

The definition of the refined Lie group cohomology in terms of sheaves on simplicial spaces was given by Segal and later rediscovered in

* [[Jean-Luc Brylinski]], _Differentiable Cohomology of Gauge Groups_ ([arXiv](http://arxiv.org/abs/math/0011069))
{#Brylinski}

following

* P. Blanc, _Cohomologie diff&eacute;rentiable et changement de groupes, Ast&eacute;risque vol. 124-125 (1985), pp. 113-130
{#Blanc}

Relevant background on the theory of abelian sheaf cohomology on simplicial spaces is at the beginning of 

* [[Pierre Deligne]], _Th&eacute;orie de Hodge: III_  Publication math&eacute;tematique de l'I.H.E.S, tome 44 (1974), p. 5-77 ([numdam](http://www.numdam.org/item?id=PMIHES_1974__44__5_0))

More discussion of Lie group cohomology along these lines is in

* [[Chris Schommer-Pries]], _A finite-dimensional String 2-group_ ([arXiv:0911.2483](http://arxiv.org/abs/0911.2483))
{#Schommer-Pries}

A discussion of the relation between _local_ Lie group cohomology and [[Lie algebra cohomology]] is in

* S. &#346;wierczkowski, _Cohomology of group germs and Lie algebras_ Pacific Journal of Mathematics, Volume 39, Number 2 (1971), 471-482.  ([pdf](http://projecteuclid.org/DPubS/Repository/1.0/Disseminate?view=body&id=pdf_1&handle=euclid.pjm/1102969572))

