A quasitopos is a particular kind of [[category]] that is not quite a [[topos]].  Instead of the usual [[subobject classifier]], it has a classifier only for *[[strong monomorphism|strong]]* [[subobject]]s.

## Definition

A **quasitopos** is a [[finitely complete category|finitely complete]], [[finitely cocomplete category|finitely cocomplete]], [[locally cartesian closed category]] $E$ with an object $\Omega$ that classifies [[strong monomorphism|strong monomorphisms]]. In particular, this means 

* Every finite [[limit]] and [[colimit]] exists;
* For each morphism $f: A \to B$, the [[base change|pullback functor]] between [[over category|slice quasitoposes]], 
$$f^*: E/B \to E/A,$$
admits a [[adjoint functor|right adjoint]]; 
* There is a map $t: 1 \to \Omega$ such that every _strong_ monomorphism $i: A \to X$ occurs as the [[pullback]] of $t$ along some unique morphism $\chi_i: X \to \Omega$: 
$$\array{
A & \to & 1\\
i \downarrow & & \downarrow t\\
X & \overset{\chi_i}{\to} & \Omega
}$$

## Examples ##

* Any [[topos]] is a quasitopos. 
* The category of [[separated presheaf|separated presheaves]] with respect to a [[site]] is a quasitopos. 
* The category of [[simplicial complex]]es is a quasitopos. 
* The category of [[diffeological space]]s is a quasitopos. 
* Any [[Heyting algebra]] is a quasitopos.
* The category of [[pseudotopological spaces]] is a quasitopos, as is the category of [[subsequential spaces]].  The category of [[topological spaces]] fails only to be locally cartesian closed.

## References ## 

*  Oswald Wyler, _Lecture Notes on Topoi and Quasitopoi_, World Scientific, 1991. 

Need to reference work by various combinations of authors including Baez, Dolan, Hoffnung, and others on diffeological spaces and simplicial complexes... 
