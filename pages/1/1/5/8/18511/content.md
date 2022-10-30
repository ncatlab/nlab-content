
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Fedosov's method ([Fedosov 94](#Fedosov94)) is a prescription for constructing [[formal deformation quantizations]] of the [[algebra of functions|algebra of]] [[smooth functions]] on any [[symplectic manifold]] $(X,\omega)$.

In particular this establishes the existence of formal deformation quantizations of all [[symplectic manifolds]]. While [Kontsevich 97](deformation+quantization#Kontsevich97) more generally proves the existence of deformation quantization of all [[Poisson manifolds]] of finite dimension, Fedosov's method, in a variant applicable to [[almost Kähler structures]] ([Karabegov-Schlichenmaier 01](#KarabegovSchlichenmaier01)) generalizes to infinite-dimensional symplectic manifolds as they appear in [[local field theory]], where it yields the quantization to [[perturbative quantum field theory]] equivalent to the method of [[causal perturbation theory]] ([Collini 16](#Collini16)). (Kontsevich's deformation quantization is however not compatible with field theory ([Hawkins-Rejzner 16, section 5.3.2](#HawkinsRejzner16)).) For more on this see at _[[locally covariant perturbative quantum field theory]]_.

Fedosov's method proceeds by the following steps:

1. For each point $x \in X$ regard the [[tangent space]] $T_x X$ as a [[symplectic vector space]] $(T_x X, \omega_x)$ and consider its [[Moyal deformation quantization]] $\mathcal{W}_x \coloneqq A_{Moy}(T_x X, \omega_x)$. In the context of [[local field theory]] these Moyal algebras are the [[Wick algebras]] of the underlying [[free field theory]].

   The union of these yelds an [[associative algebra]]-[[fiber bundle]] $\mathcal{W} \to X$. From the fiber-wise product in $A_{Moy}(T_x X, \omega_x)$ the [[space of sections]] $\Gamma_X(\mathcal{W})$ inherits itself the structure of an [[associative algebra]].

1. Find a [[flat connection]] $\nabla_{Fed}$ on $\mathcal{W}$ which respects the associative algebra structure, and such that there is a [[linear isomorphism]]

   $$
     \Gamma_X(\mathcal{W}) \supset  ker(\nabla_{Fed}) \simeq C^\infty(X) [ [ \hbar ] ] 
   $$ 

   between the [[covariantly constant sections]] of the algebra bundle and the algebra of  smooth functions on $X$ with a [[formal power series|formal variable]] $\hbar$ adjoined.

   Such $\nabla_{Fed}$ exists, (non-uniquely), it is called a _Fedosov connection_. 

1. By this linear isomorphism the algebra structure on $\Gamma_X(\mathcal{W})$ induces an [[associative algebra]] structure on $C^\infty(X)[ [ \hbar ] ]$, and this turns out to be a [[formal deformation quantization]] of $(X,\omega)$.

   In the context of [[local field theory]], this deformation quantization is equivalent to the result of quantization via [[causal perturbation theory]] ([Collini 16](#Collini16)).




## References

The method is due to

* {#Fedosov94} [[Boris Fedosov]], _A simple geometrical construction of deformation quantization_ Journal of Differential Geometry, 40(2):213&#8211;238, 1994 ([Euclid](https://projecteuclid.org/euclid.jdg/1214455536))

Its generalization to [[almost Kähler structures]] is due to

* {#KarabegovSchlichenmaier01} V. Karabegov, M. Schlichenmaier,  _Almost-K&#228;hler deformation quantization_, Letters in Mathematical Physics, 57(2):135&#8211;148, 2001 ([proceedings pdf](http://www.atlantis-press.com/php/download_paper.php?id=540))

The observation that the construction of [[perturbative quantum field theory]] via [[causal perturbation theory]] is equivalent to Fedosov quantization is due to 

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

Discussion showing that this generalization to field theory is not given by Kontsevich deformation quantization is in  

* {#HawkinsRejzner16} [[Eli Hawkins]], [[Kasia Rejzner]], section 5.3.2 of _The Star Product in Interacting Quantum Field Theory_ ([arXiv:1612.09157](https://arxiv.org/abs/1612.09157))


[[!redirects Fedosov deformation quantization]]
[[!redirects Fedosov deformation quantizations]]


[[!redirects Fedosov quantization]]
[[!redirects Fedosov quantizations]]
