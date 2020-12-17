
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# &#268;ech nerve
* table of contents
{:toc}

## Definition

### In category theory


+-- {: .num_defn}
###### Definition

In a [[category]] $C$ with [[pullbacks]] (possibly [[homotopy pullbacks]]), given a [[morphism]] $U \to X$ in $C$ its corresponding **&#268;ech nerve** $C(U)$ is the [[simplicial object]] in $C$ that in degree $k$ is given by the $(k+1)$-fold [[fiber product]] of $U$ over $X$ with itself :

$$
  C(U) \coloneqq
  \left(
    \cdots
    U \times_X U \times_X U 
   \overset{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}} U \times_X U \stackrel{\longrightarrow}{\longrightarrow} U
  \right)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is the [[internal nerve]] of the [[internal groupoid]] corresponding to the [[kernel pair]] of the morphism $U \to X$.

=--


### In $(\infty,1)$-category theory

The notion of &#268;ech nerve makes sense in any [[(∞,1)-category]] with [[limit in a quasi-category|(∞,1)-pullbacks]].

Consider a morphism $f: A \rightarrow B$  in an $(\infty,1)$-category $M$. The Cech nerve of that morphism is, by definition, the [[augmented simplicial object]] in $M$ obtained by the [[right Kan extension]] of that morphism (regarded as a functor from the obvious category into $M$) along the inclusion of the first two objects into the augmented simplicial category. See Lurie HTT 6.1.2.11. One can show that this gives a [[groupoid object]] in $M$. The Cech nerve is essentially unique by uniqueness of adjoint $\infty-$ functors.

See [[groupoid object in an (∞,1)-category]].


## Applications and occurences

* The [[cohomology]] theory obtained by mapping out of [[Čech covers]] instead of general [[hypercovers]] is [[Čech cohomology]].

* A [[groupoid object in an (infinity,1)-category]] that is a &#268;ech nerve $U \to X$ exhibits $X$ as a [[delooping]].

  * In an [[infinity-stack]] [[(infinity,1)-topos]] every [[groupoid object in an (infinity,1)-category]] is a &#268;ech nerve.


## Examples

+-- {: .num_example #FromACover}
###### Example

For $U = \coprod_i U_i$ the [[disjoint union]] of  a [[covering]] [[sieve]] $\{U_i \to X\}$ with respect to a [[coverage]], the objectwise [[simplicial homotopy group|connected components]] of the &#268;ech nerve is the [[subfunctor]] corresponding to the [[sieve]]

$$
  \Pi_0 C(U) = \bigcup_i hom(-,U_i)
  \,.
$$

This is described in more detail in the section "Interpretation in terms of higher descent and codescent" at [[sieve]]. This example is important in understanding the construction of the [[etale homotopy type]] of a scheme or more generally of objects in certain types of topos. 

=--

+-- {: .num_remark}
###### Remark (Historical and pedagogic note)

This example is more or less the way that [[Eduard Čech]] gave the original form of the construction that now carries his name. More on this can be found in the entry on [[&#268;ech methods]], and the discussion there of the **nerve of an open cover**. For the case of triangulable spaces (polyhedra), for the cover by open stars of vertices of a triangulation, one retrieves the simplicial complex used to triangulate the space. This is one of the strong roots of the modern theory of cohomology as nerves of open covers can be seen as analogues of triangulations, and then [[Čech cohomology]] is seen to extend simplicial cohomology to spaces that are locally nice. That is one of the first steps on the long route to [[Grothendieck]]'s definition of topos as a generalisation of space, expressly so as to define a cohomology further extending &#268;ech cohomology to the geometric objects studied in algebraic geometry.

=--


##Related entries

* [[Čech groupoid]]

* [[effective epimorphism]]

* [[nerve theorem]]

[[!redirects Cech nerve]]
[[!redirects Cech-nerve]]
[[!redirects Čech nerve]]
[[!redirects Čech-nerve]]
[[!redirects Čech nerve]]
[[!redirects Čech-nerve]]
[[!redirects Cech complex]]

[[!redirects Čech nerves]]
[[!redirects Cech nerves]]