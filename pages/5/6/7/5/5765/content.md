
# Affine morphisms
* table of contents
{: toc}

## Idea and definition

An affine morphism of [[schemes]] is a relative version of an [[affine scheme]]: given a scheme $X$, the canonical morphism $X \to Spec \mathbb{Z}$ is affine iff $X$ is an affine scheme. By the basics of [[spectrum|spectra]], every morphism of affine schemes $Spec S \to Spec R$ corresponds to a morphism $f^\circ\colon R \to S$ of [[rings]]. The affine morphisms of general schemes are defined as the ones which are locally of that form: 

* a morphism $f\colon X\to Y$ of (general) schemes is **affine** if there is a [[cover]] of $Y$ (as a [[ringed space]]) by affines $U_\alpha$ such that $f^{-1} U_\alpha$ is an affine subscheme of $X$. 

A seemingly stronger, but in fact equivalent, characterization follows: $f\colon X\to Y$ is affine iff for every affine $U \subset Y$, the [[inverse image]] $f^{-1}(U)$ is affine. 


## Relative spectra and affine schemes

[[Grothendieck]] constructed a spectrum of a (commutative unital) [[commutative algebra|algebra]] in the category of quasicoherent $\mathcal{O}X$-modules. The result is a scheme over $X$; [[relative point of view|relative]] schemes of that form are called __relative affine schemes__. 


## Functorial point of view

Now notice that a map of (associative) rings, possibly noncommutative (and possibly nonunital), induces an [[adjoint triple]] of functors $f^*\dashv f_*\dashv f^!$ among the categories of (say left) modules where $f^*$ is the extension of scalars, $f_*$ the restriction of scalars and $f^!\colon M \mapsto Hom_R(S,M)$ where the latter is an $R$-module via $(r x) (s) = x (s r)$. In particular, $f_*$ is exact. 

In fact, if $f\colon X\to Y$ is a [[quasicompact morphism]] of schemes and $X$ is [[separated scheme|separated]], then $f$ is affine iff it is cohomologically affine, that is, the direct image $f_*$ is exact ([[Serre's criterion of affineness]], cf. EGA II 5.2.2, EGA IV 1.7.17). 

An [[affine localization]] is a localization functor among categories of quasicoherent $\mathcal{O}$-modules which is also the inverse image functor of an affine morphism; or an abstraction of this situation.  

See also [[monad in algebraic geometry]]. 


## Extensions

One can extend the notion of an affine morphism to [[algebraic spaces]], the noncommutative schemes of Rosenberg, Durov's generalized schemes, algebraic stacks and so on. The affinity is a local property so for algebraic stacks and the like one looks at the pullback to affine charts and checks if the resulting morphism is affine; for Durov's and Rosenberg's schemes one is basically generalizing the functorial criterium by definition. (more on this later)


## Literature 

Some of the material is extracted from MathOverflow &lt;http://mathoverflow.net/questions/15291/affine-morphisms-in-different-settings-coincide/58486>.

* R. Hartshorne, _Algebraic geometry_, exercise II.5.17

* [[A. L. Rosenberg]], _Noncommutative schemes_, Compositio Math. __112__ (1998) 93--125, [MR99h:14002](http://www.ams.org/mathscinet-getitem?mr=1622759), [doi](http://dx.doi.org/10.1023/A:1000479824211)

category: algebraic geometry, noncommutative geometry
[[!redirects affine morphism]]
[[!redirects affine morphisms]]
[[!redirects affine morphism of schemes]]
[[!redirects affine morphisms of schemes]]
