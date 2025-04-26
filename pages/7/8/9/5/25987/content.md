## Idea

[[Grothendieck]] introduced spaces as locally representable [[sheaves]] over a fixed [[site]] whose objects are interpreted as local models. If local models are [[affine schemes]], then [[schemes]] and [[algebraic spaces]] can be considered as an example. 

## Schemes as presheaves

Given a [[commutative ring]] $R$, the correspondence 
$$Y\mapsto Spec(\Gamma_Y \mathcal{O}_Y)$$
extends to a [[functor]]
$$Scheme\to Aff.$$
A basic result, sometimes referred to as __fundamental theorem on morphisms of schemes__ says that there is a bijection  
$$CRing(R, \Gamma_Y\mathcal{O}_Y) \cong Scheme(Y, Spec R).$$

More precisely, for fixed [[scheme]] $Y$, and for varying $R$ there is a restricted functor  
$$Scheme(-,Y)|_{Aff^{op}} = h_Y|_{Aff^{op}} = h_Y|_{CRing} : CRing\to Set,$$ 
and the functor
$$Y\mapsto h_Y|_{CRing}$$
from schemes to presheaves on $Aff = CRing^{op}$ is [[fully faithful functor|fully faithful]].
Thus the general schemes if defined as ringed spaces, indeed form a full subcategory of the category of presheaves on $Aff$. 

In fact, the theorem is more general: instead of $Y$ being a scheme, we can take any locally ringed space. Thus the entire category of locally ringed spaces embeds into the category of presheaves on $Aff$.

## Schemes as locally representable sheaves

In fact, one can characterize the [[essential image]] of the category of [[schemes]] in the category of [[presheaves]] over the category of [[affine schemes]], as the [[full subcategory]] spanned by those [[small presheaves]] that are $\tau$-locally representable and are $\tau$-sheaves, where $\tau$ is the Zariski topology on the category of affine schemes. 

Here a presheaf $F$ is $\tau$-locally representable if there is a set-indexed [[covering family]]
$$f_i\colon X_i\to F,$$
where $X_i$ is an [[affine scheme]] and the morphisms $f_i$ are [[open immersions]].

Open immersions of presheaves are defined as follows.
A morphism of presheaves
$$F\to G$$
is an [[open immersion]] if for every presheaf $X$ represented by an [[affine scheme]] and every morphism
$$X\to G,$$
the [[base change]]
$$X\times_G F\to X$$
is an [[open immersion]].

See [Demazure–Gabriel](#DG) for the functorial approach to schemes and its relation to [[locally ringed spaces]].

## Noncommutative analogues

See [Rosenberg 1998](#R1998) for fundamental theorem on morphisms, and 1999 for the equivalence of two approaches)

## Derived analogues

...(Toen, Vezzosi etc.)


## References 

### Related entries in $n$Lab

* [[affine scheme]], [[algebraic scheme]]
* [[morphism of schemes]] 
* [[Yoneda embedding]], [[Isbell duality]]
* [[functorial geometry]]

### Literature

A standard reference to the functorial approach to schemes

* {#DG} [[Michel Demazure]], [[Pierre Gabriel]], _Groupes algebriques_, tome 1 (later volumes never appeared), Mason and Cie, Paris 1970;  English edition is Introduction to algebraic geometry and algebraic groups, North-Holland, Amsterdam 1980 (North-Holland)

The fundamental theorem of morphisms of schemes has been adapted to noncommutative schemes in

* {#R1998} [[Alexander Rosenberg]], _Noncommutative schemes_, Compos. Math. __112__ (1998) 93--125 [doi](https://doi.org/10.1023/A:1000479824211)

See also the [[MathOverflow]] answer:

* [[Zhen Lin Low]], [Answer to “What is a (Zariski-)locally representable (pre)sheaf?”](https://mathoverflow.net/questions/491623/what-is-a-zariski-locally-representable-presheaf/491645#491645).

For the fundamental theorem of morphisms of schemes in the language of [[locally ringed spaces]] see for example Theorem 2 in MIT 18-726 AG course notes

* [[Kiran Kedlaya]], _Algebraic Geometry_, Lectures 7–9 (Morphisms of Schemes), [PDF](https://ocw.mit.edu/courses/18-726-algebraic-geometry-spring-2009/resources/mit18_726s09_lec06_morphisms).

[[!redirects fundamental theorem on morphism of schemes]]
[[!redirects fundamental theorem of morphism of schemes]]