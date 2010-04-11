
+-- {.standout}

  On the formalization of the process of [[quantization]] -- by [[category theory|abstract nonsense]] -- from classical [[∞-model]] data to the corresponding [[quantum field theory]] .

=--



#Contents#
* automatic table of contents goes here
{:toc}





## Background and motivation

The search is on for the abstract formalization of the process of _[[quantization]]_ -- the process that reads in a "[[classical field theory]]" -- for instance presented in form of a [[gauge theory]] or in form of a [[∞-model]] background field data -- and spits out the corresponding [[quantum field theory]].

+-- {.standout}

There is an open problem of mathematical (-[[physics]]) model building: 

* what is the true formalism behind [[quantization]]?  

One that is to quantization as, say, [[symplectic geometry]] is to [[Hamiltonian mechanics]]?

The formalism of [[FQFT]] clearly suggests that the fundamental description of [[quantization]] is some natural operation on higher functors.

=--



While for various aspects and facets of this question there are well-developed formalisms -- such as [[geometric quantization]] or [[deformation quantization]] or [[BV-BRST formalism]] -- a full answer is certainly still missing, not the least because the full formalization of the _question_ itself has still to be established.

Considerable progress on this formulation of the question has been achieved with the formalization and proof of the [[cobordism hypothesis]] in _[[On the Classification of Topological Field Theories]]_ by [[Jacob Lurie]]. This at least indicates what the _result_ of any full quantization procedure should be in that it clarifies what exactly a [[TQFT]] [[FQFT]] is: a morphism from the [[(∞,n)-category of cobordisms]] $Z : Bord_n \to C$.

In _[[On the Classification of Topological Field Theories]]_ Jacob Lurie indicates some first towards finding a similar formalization of "classical field theory" (in terms of his $(\infty,n)$-categories of "families") and a systematic procedure for turning the classical theory into the quantum theory. These thoughts were further developed in the article _[[Topological Quantum Field Theories from Compact Lie Groups]]_ . But for the moment, that, too, remains a bit sketchy.

For the purpose of the present entry this indication of a quantizaton proposal by Lurie et al. mainly serves as a reference for the idea itself that a formalization of something interesting is to be sought here, and of the kind of [[category theory|abstract nonsense]] answer one hopes to find. We will however discuss a somewhat different-looking approach. It may well be related to the Lurie-et al proposal in the end, but for the time being we shall not concentrate on that relation.

Rather, the approach for a formalization of the quantization procedure that shall be discussed at this entry here draws from a few different sources:

1. The observation that a classical background field that should serve as the input for a quantization of a $\sigma$-model that describes the dynamics of an object charged under this field is encoded by differential cocycles as as described at [[schreiber:differential cohomology in an (∞,1)-topos]].

1. The idea that by applying a pull-push quantization prescription a differential cocycle on a target space $X$ gives rise to a differential cocycle on a _parameter space_ $\Sigma$, which may be thought of as one of the bordisms appearing in the [[FQFT]]-description of quantum field theory. 

  The pull-push operation here is akin to that in [[geometric ∞-function theory]], where a [[quantum field theory]] is obtained from a [[∞-model]] target space object $X$ by homming [[extended cobordism]] [[cospan]]s $\Sigma_in \to \Sigma \leftarrow \Sigma_{out}$ into the target object and then pull-pushing [[geometric function object]]s through the resulting [[span]]s of configuration space objects $[\Sigma_{in},X] \leftarrow [\Sigma,X] \to [\Sigma_{out},X]$. 

   The main result of David Ben-Zvi et. al.'s work on this approach is that they point out that as soon as the [[geometric function object]] one uses satisfies the two [[geometric ∞-function theory|fundamental theorems of geometric infinity-function theory]], a considerable amount of rich structure that has in parts been known by itself gets unified into one coherent elegant story: the nature of partition functions (i.e. traces), of centers, of Hochschild (co)homology, Deligne-Kontsevich-statements, etc. all are understood by means of a suitable [[geometric function theory]] as induced from the underlying geometry of configuration space objects $[\Sigma,X]$ as well as the [[loop space object]]s of $X$.

  The resulting pull-push operation is an example or a generalization of what [[John Baez]] discusses under the term [[groupoidification]]. 

1. The observation that a differential coccycle on a [[Lorentzian manifold]] $\Sigma$ gives rise to a [[local net]] of observables, as used in the formalizaton of QFT known as [[AQTFT]]. (As described [here](http://ncatlab.org/schreiber/files/AQFTfromFQFT.pdf)).

   So the procedure discussed here regards differential cocycles on target space as classicai field theories, regards their quantization as a way to obtain a differential cocycle on Lorentzian parameter space, and identifies this as a quantum field theory by associating a local net of observables to it. 

  These local nets, in turn, are akin to [[factorization algebra]]s, which in the Euclidean (meaning non-Lorentzian setting) relate back to cobordism representations via the notion of [[topological chiral homology]]. However the -- physically crucial -- Lorentzian structure invoked here is not otherwise considered in these functorial axiomatization of quantum field theory.

## Classical background field

...

## The quantization

...

[[!redirects exercise in groupoidification -- the path integral]]


[[!redirects An Exercise in Groupoidification]]