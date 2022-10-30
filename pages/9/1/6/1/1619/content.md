+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

# Contents #
* table of contents
{:toc}

A _string structure_ on a [[manifold]] is a higher version of a [[spin structure]]. A string structure on a [[manifold]]  with [[spin structure]] given by a [[Spin group]]-[[principal bundle]] to which the [[tangent bundle]] is [[associated bundle|associated]] is a lift $\hat g$ of the classifying map $g : X \to \mathcal{B} Spin(n)$ through the  third nontrivial step $\mathcal{B}String(n) \to \mathcal{B}Spin(n)$ in the [[Whitehead tower]] of $BO(n)$ to a [[String group]]-[[principal bundle]]:

$$
  \array{
    && \mathcal{B}String(n)
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathcal{B}Spin(n)
  }
$$

A lift one further step through the Whitehead tower is a [[Fivebrane structure]].

This has generalizations to the smooth context, where instead of the topological String-group one uses the [[String Lie 2-group]].

Let $X$ be an $n$-dimensional [[topological manifold]]. 

Its tangent [[bundle]] is canonically associated to a $O(n)$-principal bundle, which is in turn classified by a [[continuous function]]

$$
  X \to B O(n)
$$

from $X$ to the [[classifying space]] of the [[orthogonal group]] $O(n)$.

* A **String structure** on $X$ is the choice of a lift of this map a few steps through the [[Whitehead tower]] of $BO(n)$.

* The manifold "is string" if such a lift exists.

This means the following:

* there is a canonical map $w_1 : B O(n) \to B\mathbb{Z}_2$ from the [[classifying space]] of $O(n)$ to that of $\mathbb{Z}_2 = \mathbb{Z}/2\mathbb{Z}$ that represents the generator of the cohomology $H^1(B O(n), \mathbb{Z}_2)$. The classifying space of the group $SO(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B SO(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B O(n) &\stackrel{w_1}{\to}& \mathbb{B}\mathbb{Z}_2
   }
  $$

  Namely using the [[homotopy hypothesis]] (which is a theorem, recall), we may identify $B O(n)$ with the one object [[groupoid]] whose space of morphisms is $O(n)$ and similarly for $ B \mathbb{Z}_2$. Then the map in question is the one induced from the group homomorphism that sends orientation preserving elements in $O(n)$ to the identity and orientation reversing elements to the nontrivial element in $\mathbb{Z}_2$.

  * an **[[orientation]]** on $X$ is a choice of lift of the structure group through $B SO(n) \to B O(n)$
  $$
   \array{
    && B SO(n)
    \\
    & {}^{orientation}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B O(n)
   }
   \,.
  $$

* there is a canonical map $w_2 : B SO(n) \to B^2 \mathbb{Z}_2$ representing the generator of $H^2(B SO(n), \mathbb{Z}_2)$. The classifying space of the group $Spin(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B Spin(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B SO(n) &\stackrel{w_2}{\to}& \mathbb{B}^2\mathbb{Z}_2
   }
  $$

  * a **[[spin structure]]** on an oriented manifold $X$ is a choice of lift of the structure group through $B Spin(n) \to B SO(n)$
  $$
   \array{
    && B Spin(n)
    \\
    & {}^{spin structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B SO(n)
   }
   \,.
  $$

* there is a canonical map $B Spin(n) \to B^3 U(1)$ The classifying space of the group $String(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B String(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B Spin(n) &\stackrel{\frac{1}{2}p_1}{\to}& \mathbb{B}^3 U(1)
   }
  $$

  * a **string structure** on an oriented manifold $X$ is a choice of lift of the structure group through $B String(n) \to B Spin(n)$
  $$
   \array{
    && B String(n)
    \\
    & {}^{string structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B Spin(n)
   }
   \,.
  $$

* there is a canonical map $B String(n) \to B^7 U(1)$ The classifying space of the group $Fivebrane(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B Fivebrane(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B String(n) &\stackrel{\frac{1}{6}p_2}{\to}& \mathbb{B}^7 U(1)
   }
  $$

  * a **[[fivebrane structure]]** on an string manifold $X$ is a choice of lift of the structure group through $B Fivebrane(n) \to B String(n)$
  $$
   \array{
    && B Fivebrane(n)
    \\
    & {}^{fivebrane structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B String(n)
   }
   \,.
  $$


## Definition ##

### Topological and smooth string structures

Let the ambient [[(∞,1)-topos]] by $\mathbf{H} = $ [[ETop∞Grpd]] or [[Smooth∞Grpd]]. Write $X$ for a [[topological manifold]] or [[smooth manifold]] of [[dimension]] $n$, respectively. 

Write $String(n)$ for the [[string 2-group]], a [[1-truncated]] [[∞-group]] object in $\mathbf{H}$.


+-- {: .num_defn #PlainStringStructures}
###### Definition

The [[2-groupoid]] of (topological or smooth) **string structures** on $X$ is 
the hom-space of [[cocycle]]s $X \to \mathbf{B}String(n)$, or equivalently that of (topological or smooth) $String(n)$-[[principal 2-bundle]]s:

$$
  String(X) := String(n) Bund(X) \simeq \mathbf{X}(X,\mathbf{B}String)
  \,.
$$ 


=--

Write $\frac{1}{2} \mathbf{p}_1 : \mathbf{B} Spin(n) \to \mathbf{B}^3 U(1)$ in $\mathbf{H}$ for the topological or smooth refinement of the first fractional Pontryagin class (see [[differential string structure]] for details on this).


+-- {: .num_prop #StringStructuresAsObstructions}
###### Observation

The [[2-groupoid]] of string structure on $X$ is the [[homotopy fiber]] of $\frac{1}{2}\mathbf{p}_1^X$: the [[(∞,1)-pullback]]

$$
  \array{
    String(X) &\to& * 
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{H}(X, \mathbf{B}Spin(n))
     &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}&
    \mathbf{H}(X, \mathbf{B}^3 U(1))
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition of the [[string 2-group]] we have the [[fiber sequence]] $\mathbf{B} String \to \mathbf{B}Spin \stackrel{\frac{1}{2}} \mathbf{p_1}{\to} \mathbf{B}^3 U(1)$. The [[hom-functor]] $\mathbf{H}(X,-)$ preserves every [[(∞,1)-limit]], hence preserves this [[fiber sequence]].

=--

+-- {: .num_defn #FiberOverSpinStructure}
###### Definition

Given a [[spin structure]] $S : X \to \mathbf{B} Spin(n)$ we say that the **string structures extending this spin-structure** is the [[homotopy fiber]] $String_S(X)$ of the projection $String(X) \to Spin(X)$ from observation \ref{StringStructuresAsObstructions}:


=--

### Twisted and differential string structures

(...)

The [[2-groupoid]] of string structures is the [[homotopy fiber]] of 

$$
  \frac{1}{2}p_1 : Top(X, \mathcal{B}Spin) \to Top(X, \mathcal{B}^4 \mathbb{Z})
$$

over the trivial cocycle. Followowing the general logic of [[twisted cohomology]] the 2-groupoids over a nontrivial cocycle $c : X \to \mathcal{B}^4 \mathbb{Z}$ may be thought of as that of _twisted_ string structures.

The [[Pontryagin class]] $\frac{1}{2}p_1$ refines to the [[smooth first fractional Pontryagin class]] $\frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)$. That leads to [[differential string structure]]s.

(...)




## Properties

### Choices of string structures

+-- {: .num_prop #ChoicesOfSpinStructures}
###### Observation

The space of choices of string structures extending a given spin structure $S$ are as follows

* if $[\frac{1}{2}\mathbf{p}_1(S)] \neq 0$ it is empty: $String_S(X) \simeq \emptyset$;

* if $[\frac{1}{2}\mathbf{p}_1(S)] = 0$ it is $String_S(X) \simeq \mathbf{H}(X, \mathbf{B}^2 U(1))$.

  In particular the set of [[equivalence class]]es of string structures lifting $S$ is the [[cohomology]] set 

  $$
    \pi_0 String_S(X) \simeq H^3(X, \mathbb{Z})
    \,.
  $$

=--

+-- {: .proof}
###### Proof

Apply the [[pasting law]] for [[(∞,1)-pullback]]s on the [[diagram]]

$$
  \array{  
    String_S(X) &\to& String(X) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    * &\stackrel{S}{\to}& \mathbf{H}(X, \mathbf{B} Spin(n))
    &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}&
    \mathbf{H}(X, \mathbf{B}^3 U(1))
  }
  \,.
$$

The outer diagram defines the [[loop space object]] of $\mathbf{H}(X, \mathbf{B}^3 U(1))$. Since $\mathbf{H}(X,-)$ commutes with forming loop space objects (see [[fiber sequence]] for details) we have

$$
  String_S(X) \simeq \Omega \mathbf{H}(X, \mathbf{B}^3 U(1))
   \simeq
  \mathbf{H}(X, \mathbf{B}^2 U(1))
  \,.
$$

=--


### String structures by gerbes on a bundle 
 {#ClassesOnTotalSpace}

One can reformulate an

* [[orientation]]-
 
* [[spin structure|Spin]]-

* [[string structure|String]]-

* [[fivebrane structure|Fivebrane]]-

structure in terms of the existence of a certain class in abelian cohomolgy on the total space of the given [[principal bundle]]. This decomposition is a special case of th general [[Whitehead principle of nonabelian cohomology]].



+-- {: .num_defn #StringStrucDefinitionByTotalSpace}
###### Definition

Let $X$ be a manifolds with [[spin structure]] $S : X \to \mathbf{B}Spin$. Write $P \to X$ for the corresponding [[spin group]]-principal bundle. 

Then a **string structure** lifting $S$ is a cohomology class $H^3(P,\mathbb{Z})$ such that the restriction of the class to any fiber $\simeq Spin(n)$ is a generator of $H^3(Spin(n), \mathbb{Z}) \simeq \mathbb{Z}$.

=--

This kind of definition appears in ([Redden, def. 6.4.2](#Redden)).

+-- {: .num_prop #DirectStringStructureImpliesIndirectOne}
###### Proposition

Every string structure in the sense of def. \ref{FiberOverSpinStructure} induces a string structure in the sense of def. \ref{StringStrucDefinitionByTotalSpace}.

=--

+-- {: .proof}
###### Proof


Consider the [[pasting]] diagram of  [[(∞,1)-pullback]]s

$$
  \array{
    String &\to& \hat P &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Spin &\to& P &\to&  B^2 U(1) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& X &\to& B String(n) &\to& B Spin(n)
  }
$$

This uses repeatedly the [[pasting law]] for $(\infty,1)$-pullbacks. The map $P \to B^2 U(1)$ appears by decomposing the homotopy pullback of the point along $X \to B Spin(n)$ into a homotopy pullback first along $B String(n) \to B Spin(n)$ and then along $X \to B String(n)$ using the given String structure. This is the [[cocycle]] for a $\mathbf{B}U(1)$-[[principal 2-bundle]] on the total space $P$ of the $Spin$-principal bundle: a [[bundle gerbe]].

The rest of the diagram is constructed in order to prove the following:

* The class in $H^3(P, \mathbb{Z})$ of this bundle gerbe, represented by $P \to B^2 U(1)$ has the property that restricted to the fibers of the $Spin(n)$-principal bundle $P$ it becomes the generating class in $H^3(Spin(n), \mathbb{Z})$.

=--

## Examples

* On a 3-[[dimension|dimensional]] [[orientation|oriented]] [[manifold]] string structures are equivalently [[2-framings]].

## Related entries

* [[orientation]]

* [[spin structure]], [[twisted spin structure]]

* [[p1-structure]], [[Atiyah 2-framing]]

* **string structure**, [[differential string structure]]

* [[fivebrane structure]], [[differential fivebrane structure]]

[[!include higher spin structure - table]]


## References ##

The relevance of String structures (like that of Spin structures half a century before) was recognized in the physics of spinning strings, therefore the name.

The article

* Killingback, _World-sheet anomalies and loop geometry_ Nuclear Physics B Volume 288, 1987, Pages 578-588

was (it seems) the first to derive the Green-Schwarz anomaly cancellation condition of the effective background theory as the [[quantum anomaly]] cancellation condition for the worldsheet theory of the heterotic string's [[sigma-model]] by direct generalization of the way the condition of a [[spin structure]] may be deduced from anomaly cancellation for the superparticle.

String stuctures had at that time been discussed in terms of their transgressions to loop spaces

* [[Edward Witten]], _The Index of the Dirac Operator in Loop Space_ Proc. of Conf. on Elliptic Curves and Modular Forms in Algebraic Topology, Princeton, N.J., Sep 1986.
{#WittenIndexLoopSpace}

* [[Edward Witten]], _Elliptic Genera and Quantum Field Theory_
Commun.Math.Phys.109:525,1987
{#WittenElliptic}

later it was reformulated in terms of the classes down on base space just mentioned in

* [[Stefan Stolz]], [[Peter Teichner]], [What is an elliptic object](http://math.ucr.edu/home/baez/qg-winter2007/Oxford.pdf).

The relation between the two pictures is analyzed for instance in

* A. Asada, _Characteristic classes of loop group bundles and generalized string classes_ , Differential geometry and its applications (Eger, 1989), 33--66, Colloq. Math. Soc. J&#225;nos Bolyai, 56, North-Holland, Amsterdam, 1992. ([[Asada.pdf:file]])

A precise formulation of Killingbacks original argument in [[differential K-theory]] appeared in 

* [[Ulrich Bunke]], _String structures and trivialisations of a Pfaffian line bundle_, Commun. Math. Phys. (2011) 307: 675 ([arXiv:0909.0846](http://arxiv.org/abs/0909.0846), [doi:10.1007/s00220-011-1348-0](https://doi.org/10.1007/s00220-011-1348-0))

A review of that is in 

* [[Konrad Waldorf]], _Geometric string structure and supersymmetric sigma-models_ ([pdf](http://www.konradwaldorf.de/docs/cardiff.pdf))

The definition of string structures by degree-3 classes on the total space of the spin bundle is used in

* [[Corbett Redden]], _Canonical metric connections associated to string structures_ PhD Thesis, (2006)([pdf](https://www.math.sunysb.edu/~redden/Thesis.pdf))

For discussion of String-structures using 3-classes on total spaces see for instance the work by Corbett Redden and Konrad Waldorf described at 

* [[Oberwolfach Workshop, June 2009 -- Friday, June 12]]

Discussion of the [[moduli stack]] of [[twisted differential string structures]] is in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_, Communications in Mathematical Physics, October 2012, Volume 315, Issue 1, pp 169-213 ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001))

An explicit cocycle construction of the essentially unique [[string 2-group]]-[[principal 2-bundle]] lift of the [[tangent bundle]] of the [[sphere|5-sphere]] is given in 

* {#Roberts14} [[David Roberts]], _Explicit string bundles_, talk at _[Workshop on Higher Gauge Theory and Higher Quantization](http://www.christiansaemann.de/higherworkshop2014/index.html)_ 2014 ([[RobertsStringS5.pdf:file]])

Discussion for indefinite (Lorentzian) signature is in

* Hyung Bo Shim, _Indefinite string structure_, thesis 2013 ([web](http://d-scholarship.pitt.edu/19620/))

More discussion of relation to spin structures on loop spaces is in 

* Alessandra Capotosti, _[[From String structures to Spin structures on loop spaces]]_, Ph.D. thesis, Universit&#224; degli Studi Roma Tre, Rome, April 2016




[[!redirects String structure]]
[[!redirects String-structure]]
[[!redirects string-structure]]

[[!redirects string structures]]
[[!redirects String structures]]