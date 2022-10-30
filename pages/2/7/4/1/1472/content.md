<div class="rightHandSide toc">
[[!include physicscontents]]
***
[[!include category theory - contents]]
***
[[!include higher category theory - contents]]
</div>


This entry discusses [[physics]] from the [[nPOV]].

> well, this entry is hugely imperfect at the moment, at best a sketch of a sketch. But some nice entry of this topic should eventually be available.

#Contents#
* automatic table of contents goes here
{:toc}

## General considerations 

>[[Urs Schreiber|Urs]]: I inserted the following quick rough sketch just as a catalyst for further development/criticism/revision, without really taking or even having the time to do justice to this topic. I don't have the time and energy right now to run with this ball, but I thought I'd give it a kick anyway.

At this time, a systematic and comprehensive $n$-categorical formulation of fundamental physics, that was expected in one form or other for many years, is gradually beginning to take concrete shape in structures revolving around the concept of [[FQFT|extended quantum field theory]].

Given the current evidence there is some reason to expect that eventually [[higher category theory]] in general and [[(∞,n)-category]] theory in particular will find its role as the natural language for [[quantum field theory]] and all that entails in much the same way as, for instance, in the past

* [[differential geometry]] turned out to be the natural language for [[electromagnetic field|Maxwell theory]] and [[gravity|Einstein gravity]];

* [[symplectic geometry]] turned out to be the natural language for [[Hamiltonian mechanics]];

* etc.

For instance just recently with the [[cobordism hypothesis]] taking concrete shape we are seeing 

* [[geometric ∞-function theory]] in [[derived stack]] [[(∞,1)-topos]]es as a natural language for (at least topological) [[sigma-model]] quantum field theory.

also... blah ... blah

* [[AQFT]]/[[factorization algebra]] ...

.. blah...

If we take the presently available evidence of the picture that is emerging here, then it appears that all [[higher category theory|higher category theoretical]] phenomena in physics that have been identified already in the past may be fit into and organized according to the following pattern:

* **0th quantization: classical physics**: quantization is quantization of "[[action functional]]s". Action functionals in fundamental physics tend to arise in the form of holonomies of higher [[schreiber:Differential Nonabelian Cohomology|differential cocycles]]. For instance the Chern-Simons action functional is the 3-dimensional holonomy of a $U(1)$ 2-[[gerbe]], the Wess-Zumino model term the 2-dimensional holonomy of a 1-gerbe, and the gauge coupling term of the ordinary charged particle (an electron, or a quark) the ordinary holonomy of a bundle with connection. So  0th quantized physics is about [[parallel transport]] $n$-functors  in [[differential cohomology]] $\nabla$ that send "classical trajectories" to the "phases" assigned to them by the "gauge coupling". So 0th quantization is controled by $n$-functors of the form

  * classical action: target space $\to$ phases
 
    $\Pi(X) \to \infty Mod$

* **1st quantization: quantum mechanics**: it has become [[FQFT|clear]] that the quantum field theory that described the propagation of a fundamental $(n-1)$-brane (or "$n$-particle") is encoded in an $n$-functor from an [[(infinity,n)-category of cobordisms]] to some suitable codomain.  This sends "worldvolumes"  to "correlators". So first quantization is controled by $n$-functors of the form

  * quantum propagation: cobordisms/Feynman diagrams $\to$ correlators

    $$
      Bord_{(\infty,n)} \to \mathcal{C}
    $$



* **2nd quantization: quantum field theory**: quantum mechanical propagation functors as above that arise by quantizing classical data, i.e. that arise as [[sigma-model]]s typically compute the amplitude assigned to as a cobordism a sum of phases over classical trajectories. This pattern continues: in [[string theory|second quantization]] one constructs "$S$-matrix elements" by summing amplitudes over cobordisms/Feynman diagrams. This is by far the least developed bit, but it seems we want to say that the $n$-functor relevant for second quantized quantum field theory here is of the kind

  * scattering amplitude: reaction channel $\to$ $S$-matrix element

    $$
      \Pi(Bord) \to C
    $$

We will now list $n$-categorical physics ordered according to this rough pattern of successive quantization.


## Classical and Quantum Physics

### 0th quantized 

* the objects of interest in physics: [[space and quantity]]: [[motivation for sheaves, cohomology and higher stacks]]

* target spaces (spacetimes) and configuration spaces: **[[space]]** , [[generalized smooth space]], [[∞-stack]]/[[derived stack]], [[structured generalized space]]

* background [[gauge field]]s -- forces: 

  * integral description: [[schreiber:Differential Nonabelian Cohomology|higher gauge theory]]: the description of _background fields_: higher bundles with connection

  * differential description: [[rational homotopy theory]] -- [[Lie ∞-algebroid]]

* tools for handling $\infty$-categorical action functionals

  * [[BV theory]]

  * [[AKSZ theory]]


### 1st quantized 

* [[FQFT]]

  * [[cobordism hypothesis]]

  * [[(∞,n)-category of cobordisms]]

* $\infty$-[[sigma-model]]s

  * [[geometric infinity-function theory]]


* [[AQFT]]: [[sheaf|sheaves]] of operator algebra, [[nonabelian cohomology]]

* [[factorization algebra]]

#### The path integral

The [[path integral]] is becoming expected to have a formalization in
terms of higher category theory as a suitable "push-forward  of a classical theory to a point".

* a proposal for how to think of this is in _[[Topological Quantum Field Theories from Compact Lie Groups]]_



#### linear $(\infty,1)$-categorical QFT 

> the following a stub obtained from copy-and-pasting material that [[David Ben-Zvi]] mentioned [here](http://golem.ph.utexas.edu/category/2009/07/a_prehistory_of_ncategorical_p_1.html#c025075)

Kontsevich's 1994 ICM article, is one of the seminal papers of the 1990s. This paper invented the categorical side of mirror symmetry (homological mirror symmetry), discovered D-[[brane]]s (before physicists realized their role --- and directly inspiring many physicists) and the fact that they naturally form [[dg-category|dg-categories]] and $A_\infty$-[[A-infinity-category|category]], and thus led to a deluge of papers involving [[category theory]] and [[higher category theory]] in close relation with mathematical physics.

In particular the Moore--Segal paper should be seen in the light of this development. On a similar note, roughly contemporary with Moore--Segal (which is [arXiv:math/0609042](http://www.arxiv.org/abs/math/0609042) though developed earlier) are the works of Costello ([arXiv:math/0412149](http://www.arxiv.org/abs/math/0412149)) and Kontsevich--Soibelman ([arXiv:math/0606241](http://www.arxiv.org/abs/math/0606241) --- some of the results were lectured on in various places by Kontsevich in 2003 and in particular helped inspire Costello) proving a much stronger result, which is the TCFT (or equivalently differential graded or $A_\infty$-) version of the classification of open-closed 2d [[TQFT]]s. These papers were directly motivated by homological mirror symmetry and [[topological string theory|topological]] [[string theory]], and have greatly influenced work in areas such as [[string topology]] which you mention and the [[cobordism hypothesis]] ([[On the Classification of Topological Field Theories|Hopkins-Lurie]] started from Costello's paper and abstracted the argument, before the general argument in n-dimensions came around). 


### 2nd quantized 


* [[Hopf-algebraic renormalization]]



## Further topics

* Discrete Differential Geometry
* Lattice Gauge Theory

>[[Urs Schreiber|Urs]]: not sure which $n$-categorical aspect of these two subjects we might want to discuss. As soon as I know, I would try to move it into the above pattern, but for the moment I am not sure.

... 

## References

A historical introduction to some aspects of $n$-categories in physics can be found here:

* [[John Baez]] and [[Aaron Lauda]], _A prehistory of $n$-categorical physics_ ([pdf](http://math.ucr.edu/home/baez/history.pdf)), to appear in _Deep Beauty: Mathematical Innovation and the Search for an Underlying Intelligibility of the Quantum World_, ed. Hans Halvorson.

For blog discussion of this paper see:

* _A prehistory of $n$-categorical physics_, ([n-Category Cafe](http://golem.ph.utexas.edu/category/2009/05/a_prehistory_of_ncategorical_p.html))

* _A prehistory of $n$-categorical physics II_, ([n-Category Cafe](http://golem.ph.utexas.edu/category/2009/07/a_prehistory_of_ncategorical_p_1.html))

[[Jim Stasheff]] is also writing a historical introduction to cohomological physics:

* [[Jim Stasheff]], [[A Survey of Cohomological Physics]] 

The following book-to-be aims to give picture of the present state of the art of describing the [[category theory|general abstract nonsense]] structure of the universe, as far as fundamental physics is concerned

* [[Hisham Sati]], [[Urs Schreiber]], [[Branislav Jurco]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_

### On the quantization procedure

First sketches of the idea that [[path integral]] [[quantization]] may have a formalization in terms of [[higher category theory]] appeared in

* [[Dan Freed]], _Higher Algebraic Structures and Quantization_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115))

and its companing (coming? companion?) paper

* [[Dan Freed]], ...

More formal aspects along these lines appear in

* [[Simon Willerton]] _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv:math/0503266](http://arxiv.org/abs/math.QA/0503266))

An indication of a full formalization of what that may mean for discrete QFTs such as [[Dijkgraaf-Witten theory]] is in

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]] _[[Topological Quantum Field Theories from Compact Lie Groups]]_

based on work in 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

[[!redirects n-categorical physics]]
