##Idea##

A _quantum heap_ is a dual version of a notion of a [[heap]] internalized to the [[monoidal category]] $k$-[[Vect]], with usual tensor product over $k$. A quantum heap is to a [[Hopf algebra]] what a heap is to a [[group]]. 


##Definition##

A __quantum heap__ is an [[associative unital algebra]] $(H,\mu,\eta)$ 
together with a ternary algebra cooperation
\[ \tau : H \rightarrow H \otimes H_{op} \otimes H,\]
satisfying the following properties

$$(\id  \otimes \id \otimes \tau) \tau 
= (\tau \otimes \id \otimes \id) \tau $$

$$(\id \otimes \mu) \tau = \id \otimes 1_H$$

$$(\mu \otimes \id) \tau = 1_H \otimes \id$$

Moreover, $\tau$ is required to be algebra homomorphism from $H$ into
$H \otimes H_{op} \otimes H$, where  $H_{op}$ has the opposite
algebra structure and the tensor product has the usual algebra structure.
We use heap analogue of the Sweedler notation:
\[ \tau(h) = \sum h^{(1)} \otimes h^{(2)} \otimes h^{(3)},\]
and because of the first of the above identities,
it is justified to extend it to any odd number $\geq 3$ factors, e.g.
\[ (\id \otimes \id \otimes \tau) \tau(h) =
 \sum h^{(1)} \otimes h^{(2)} \otimes h^{(3)} 
\otimes h^{(4)} \otimes h^{(5)}. \]


##Versions and references##

The algebra of functions on an affine variety with a structure of an algebraic [[heap]] is an example of a commutative heap. This has been used explicitly in 

* M. Kontsevich, _Operads and motives in deformation quantization_, Lett. Math. Phys. 48 1 (1999) 35--72 

The noncommutative case has been first introduced and studied in chapter 9 of 

* Zoran &#352;koda, _Cosets for quantum groups_, Ph. D. thesis, University of Wisconsin, defended January 17, 2002

Choosing a character of a quantum heap one obtains a __copointed quantum heap__. According to the main theorem in that chapter, the category of copointed quantum heap is equivalent to the category of Hopf algebras. 
An updated version of that chapter 9 has been published only much later in 

* Z. &#352;koda, _Quantum heaps, cops and heapy categories_, Mathematical Communications 12, No. 1, pp. 1--9 (2007) [math.QA/0701749](http://arxiv.org/abs/math.QA/0701749)

where also a notion of "heapy category", sort of monoidal-category like categorification of a heap is proposed. 

Independently, a relative version (that is over commutative $k$-algebra $A$ instead over $k$) of a quantum heap has been proposed in 2002 under the name "quantum torsor" by 

* C. Grunspan, _Quantum torsors_, [math.QA/0204280](http://arXiv.org/abs/math.QA/0204280)

where the list has an additional unnecessary and superfluous axiom, later removed by 

* P. Schauenburg, _Quantum torsors and Hopf-Galois objects_, [math.QA/0208047](http://arXiv.org/abs/math.QA/0208047)

An interesting notion in Grunspan's work are the left and right automorphism Hopf algebras of a quantum heap which are analogues of the automorphism group of a [[heap]]; in addition he has exhibited a counterexample showing that the left and right automorphism Hopf algebra do not need to be isomorphic.  

A recent related article is

* G. B&#246;hm, T. Brzezi&#324;ski, _Pre-torsors and equivalences_,  J. Algebra 317 544--580 (2007) ([math.QA/0607529](http://arxiv.org/abs/math.QA/0607529)), Corrigendum: J Algebra 319 1339-1340 (2008) 

and generalizations with emphasis on noncommutative base are studied in 

* Tomasz Brzezi&#324;ski, Joost Vercruysse, _Bimodule herds_, J. Algebra __321__:9, (2009) 2670-2704 [arXiv:0805.2510](http://arXiv.org/abs/0805.2510) [doi](https://doi.org/10.1016/j.jalgebra.2009.01.020)

See also

* Thomas Booker, Ross Street, _Torsors, herds and flocks_, J. Algebra 330:1 (2011) 346–374 [arxiv/0912.4551](http://arxiv.org/abs/0912.4551) [doi](http://dx.doi.org/10.1016/j.jalgebra.2010.12.009)


[[!redirects quantum heaps]]