
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Algebraic topology_ refers to the application of methods of [[algebra]] to problems in [[topology]]. More specifically,
the method of algebraic topology is to assign [[homeomorphism]]/[[homotopy]]-[[invariants]] to [[topological spaces]], or more systematically, to the construction  and applications of [[functors]] from some [[category]] of topological objects  (e.g. [[Hausdorff spaces]], topological [[fibre bundles]]) to some algebraic category (e.g. [[abelian groups]],
[[modules]] over the [[Steenrod algebra]]). Landing in an algebraic category aids to the computability, 
but typically loses some information (say getting from 
a topological spaces with a continuum or more points 
to rather discrete algebraic structures).


### The idea of functorial invariants

The basic idea of the functorial method for the problem of existence of morphisms is the following: 
If $F:A\to B$ is a [[functor]] 
(we present here a general statement, but in the above context 
$A$ is a category of topological objects
and $B$ some category of algebraic objects) 
and $d:D\to A$ a [[diagram]] in $A$ then
$F\circ d$ is a diagram in $B$. 
If one can fill certain additional
arrow $f$ in the diagram $d$ making the extended diagram commutative,
then $F(f)$ is a morphism between the corresponding vertices in $B$ extending $F\circ d$ to a commutative diagram.
Thus if we prove that there is no morphism extending $F\circ d$ then
there was no morphism extending $d$ in the first place. 
Therefore, the functorial method is very suitable to prove 
_negative_ existence for morphisms. Sometimes,
however, there is a theorem showing that some set of invariants
completely characterizes a problem hence being able to show
positive existence or uniqueness for maps or spaces.
For the uniqueness for morphisms, it is enough to show that $F$ is
faithful and that there is at most one solution for the existence
problem in the target category. 
Faithful functors in this context are rare, 
but it is sufficient for $F$ to be faithful on some subcategory $A_p$
of $A$ containing at least all morphisms which are 
the possible candidates for the solution of 
the particular existence problem for morphisms.

## Overview of methods

The archetypical example is the classification of [[surfaces]] via their [[Euler characteristic]]. But as this example already shows, algebraic topology tends to be less about [[topological spaces]] themselves as rather about the [[homotopy types]] which they [[homotopy hypothesis|present]]. Therefore the topological invariants in question
are typically homotopy invariants of spaces with some exceptions, like the [[shape theory|shape invariants]] for spaces with bad local behaviour.   

Hence modern algebraic topology is to a large extent the application of algebraic methods to [[homotopy theory]]. 

A general and powerful such method is the assignment of [[homology]] and [[cohomology]] [[groups]] to topological spaces, such that these [[abelian groups]] depend only on the [[homotopy type]]. The simplest such are [[ordinary homology]] and [[ordinary cohomology]] groups, given by [[singular simplicial complexes]]. This way algebraic topology makes use of tools of [[homological algebra]]. 

The [[axiom|axiomatization]] of the properties of such [[cohomology]] group assignments is what led to the formulation of the trinity of concepts of _[[category]]_, _[[functor]]_ and _[[natural transformations]]_, and algebraic topology has come to make intensive use of [[category theory]].

In particular this leads to the formulation of  [[generalized (Eilenberg-Steenrod) cohomology]] theories which detect more information about classes of homotopy types. By the [[Brown representability theorem]] such are represented by [[spectra]] (generalizing [[chain complexes]]), hence [[stable homotopy types]], and this way algebraic topology comes to use and be about [[stable homotopy theory]]. 

Still finer invariants of [[homotopy types]] are detected by further refinements of these "algebraic" structures, for instance to [[multiplicative cohomology theories]], to  [[equivariant homotopy theory]]/[[equivariant stable homotopy theory]] and so forth. The construction and analysis of these requires the intimate combination of algebra and homotopy theory to [[higher category theory]] and [[higher algebra]], notably embodied in the [[universal algebra|universal]] higher algebra of [[operads]].

The central tool for breaking down all this [[higher algebra|higher algebraic]] data into computable pieces are [[spectral sequences]], which are maybe the main heavy-lifting workhorses of algebraic topology.

## Related entries

*  [[topology]], [[differential topology]]
*  [[homotopy theory]], [[shape theory]], [[nonabelian algebraic topology]], [[rational homotopy theory]]
*  [[homotopy lifting property]], [[Hurewicz fibration]], [[Hurewicz connection]], [[Serre fibration]]
*  [[homotopy extension property]], [[Hurewicz cofibration]], [[deformation retract]]
*  [[suspension]], [[loop space]], [[mapping cylinder]], [[mapping cone]], [[mapping cocylinder]]
*  [[cohomology]], [[spectrum]], [[Brown representability theorem]]
*  [[fundamental group]], [[fundamental groupoid]] 
*  [[homotopy group]], [[Eckmann-Hilton duality]], [[H-space]], [[Whitehead product]]
*  [[topological K-theory]], [[complex cobordism]], [[elliptic cohomology]], [[tmf]]
*  [[CW complex]], [[CW approximation]], [[simplicial complex]], [[simplicial set]]  
*  [[model category]], [[model structure on topological spaces]], [[homotopy category]]
*  [[fibration sequence]], [[cofibration sequence]] 
*  [[Freudenthal suspension theorem]], [[Whitehead theorem]] 


## References
 {#References}


[[!include homotopy theory and algebraic topology -- references]]


