A **quasitopos** is a finitely complete, finitely cocomplete, locally cartesian closed category $E$ with an object $\Omega$ that classifies [[strong monomorphism|strong monomorphisms]]. In particular, this means 

* For each morphism $f: A \to B$, the pullback functor between slice toposes, 
$$f^*: E/B \to E/A,$$
admits a right adjoint; 
* There is a map $t: 1 \to \Omega$ such that every _strong_ monomorphism $i: A \to X$ occurs as the pullback of $t$ along some unique morphism $\chi_i: X \to \Omega$: 
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

## References ## 

Oswald Wyler, _Lecture Notes on Topoi and Quasitopoi_, World Scientific, 1991. 

Need to reference work by various combinations of authors including Baez, Dolan, Hoffnung, and others on diffeological spaces and simplicial complexes... 
