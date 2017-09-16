[[!include physicscontents]]


This entry lists and discusses applications and occurences of [[higher category theory]] in [[physics]].

# General considerations #

>[[Urs Schreiber|Urs]]: I inserted the following quick rough sketch just as a catalyst for further development/criticism/revision, without really taking or even having the time to do justice to this topic. I don't have the time and energy right now to run with this ball, but I thought I'd give it a kick anyway.

At this time, a systematic and comprehensive $n$-categorical formulation of fundamental physics, that was expected in one form or other for many years, is gradually beginning to take concrete shape in structures revolving around the concept of [[FQFT|extended quantum field theory]].

Given the current evidence there is some reason to expect that eventually [[higher category theory]] in general and [[(infinity,n)-category]] theory in particular will find its role as the natural language for [[quantum field theory]] and all that entails in much the same way as, for instance, in the past

* [[differential geometry]] turned out to be the natural language for [[Maxwell theory]] and [[Einstein gravity]];

* [[symplectic geometry]] turned out to be the natural language for [[Hamiltonian mechanics]];

* etc.

For instance just recently with the [[generalized tangle hypothesis]] taking concrete shape we are seeing 

* [[geometric infinity-function theory]] as a natural language for (at least topological) [[sigma-model]] quantum field theory.

If we take the presently available evidence of the picture that is emerging here, then it appears that all $n$-categorical phenomena in physics that have been identified already in the past may be fit into and organized according to the following pattern:

* **0th quantization: classical physics**: quantization is quantization of "action functionals". Action functionals in fundamental physics tend to arise in the form of holonomies of higher [[schreiber:Differential Nonabelian Cohomology|differential cocycles]]. For instance the Chern-Simons action functional is the 3-dimensional holonomy of a $U(1)$ 2-gerbe, the Wess-Zumino model term the 2-dimensional holonomy of a 1-gerbe, and the gauge coupling term of the ordinary charged particle (an electron, or a quark) the ordinary holonomy of a bundle with connection. So  0th quantized physics is about parallel transport $n$-functors $\nabla$ that send "classical trajectories" to the "phases" assigned to them by the "gauge coupling". So 0th quantization is controled by $n$-functors of the form

  * classical action: target space $\to$ phases

* **1st quantization: quantum mechanics**: it has become [[FQFT|clear]] that the quantum field theory that described the propagation of a fundamental $(n-1)$-brane (or "$n$-particle") is encoded in an $n$-functor from an [[(infinity,n)-category of cobordisms]] to some suitable codomain.  This sends "worldvolumes"  to "correlators". So first quantization is controled by $n$-functors of the form

  * quantum propagation: cobordisms/Feynman diagrams $\to$ correlators

* **2nd quantization: quantum field theory**: quantum mechanical propagation functors as above that arise by quantizing classical data, i.e. that arise as [[sigma-model]]s typically compute the amplitude assigned to as a cobordism a sum of phases over classical trajectories. This pattern continues: in [[string theory|second quantization]] one constructs "$S$-matrix elements" by summing amplitudes over cobordisms/Feynman diagrams. This is by far the least developed bit, but it seems we want to say that the $n$-functor relevant for second quantized quantum field theory here is of the kind

  * scattering amplitude: reaction channel $\to$ $S$-matrix element

We will now list $n$-categorical physics ordered according to this rough pattern of successive quantization.


#0th quantized $n$-categorical physics#

* the objects of interest in physics: [[space and quantity]]: [[motivation for sheaves, cohomology and higher stacks]]

* target spaces (spacetimes) and configuration spaces: [[generalized smooth space]], [[infinity-stack]], [[structured generalized space]]

* background fields -- forces: 

  * integral description: [[schreiber:Differential Nonabelian Cohomology|higher gauge theory]]: the description of _background fields_: higher bundles with connection


  * differential description: [[rational homotopy theory]] -- [[Lie infinity-algebroid]]

* tools for handling $\infty$-categorical action functionals

  * [[BV theory]]

  * [[AKSZ theory]]


#1st quantized $n$-categorical physics#

* [[FQFT]]

  * [[generalized tangle hypothesis]]

  * [[(infinity,n)-category of cobordisms]]

* $\infty$-[[sigma-model]]s

  * [[geometric infinity-function theory]]


* [[AQFT]]: [[sheaf|sheaves]] of operator algebra, [[nonabelian cohomology]]



#2nd quantized $n$-categorical physics#



* [[Hopf algebraic renormalization]]



#Further topics#

* Discrete Differential Geometry
* Lattice Gauge Theory

>[[Urs Schreiber|Urs]]: not sure which $n$-categorical aspect of these two subjects we might want to discuss. As soon as I know, I would try to move it into the above pattern, but for the moment I am not sure.

... 

#References#

Two sets of developing notes sketching a "history" of $n$-categorical and homotopical physics exist:

* [[Jim Stasheff]], _A survey of cohomological physics_ ([pdf](http://www.math.unc.edu/Faculty/jds/survey.pdf))

* [[John Baez]] and Aaron Lauda, _A prehistory of $n$-categorical physics_ ([pdf](http://math.ucr.edu/home/baez/history.pdf)) 

This comes with its blog discussion:

* _A prehistory of $n$-categorical physics_ ([blog](http://golem.ph.utexas.edu/category/2009/05/a_prehistory_of_ncategorical_p.html))