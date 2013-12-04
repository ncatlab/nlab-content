
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Wirthm&#252;ller context_ is a pair of two [[symmetric monoidal categories]] $(\mathcal{X}, \otimes_X, 1_{X})$, $(\mathcal{Y}, \otimes_Y, 1_Y)$ which are connected by an [[adjoint triple]] of [[functors]] such that the middle one is a [[closed monoidal functor]].

This is the variant/special case of the [[yoga of six operations]] with two [[adjoint pairs]] $(f_! \dashv f^!)$ and $(f^\ast \dashv f_\ast)$ for $f^! \simeq f^\ast$. 

$$
  f_! \dashv (f^! = f^\ast) \dashv f_\ast
  \;\colon\;
  \mathcal{X}
    \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^! = f^\ast }{\leftarrow}}{\underset{f_\ast}{\longrightarrow}}}
  \mathcal{Y}
  \,.
$$

(The other specialization of the [[six operations]] where $f_\ast \simeq f_!$ is called the _[[Grothendieck context]]_).

Often one is interested in the case that there is an [[object]] $C \in \mathcal{Y}$ and an [[equivalence]]

$$
  f_\ast 1_{\mathcal{X}} \simeq f_! C
  \,.
$$

If this induces a [[natural equivalence]]

There is then a canonincal [[natural transformation]]

$$
  f_\ast A  \simeq f_!(A \otimes_X C)
$$

for $A \in \mathcal{X}$, then one says this is a _Wirthm&#252;ller isomorphism_, following ([Wirthmueller 74](#Wirthmueller74)).

Specifically, there always is a canonical [[natural transformation]] 

$$
  f_\ast A  \longrightarrow f_!(A \otimes_X C)
$$

and one can ask this to be an equivalence, hence a Wirthm&#252;ller isomorphism ([May 05](#May05)).


## Examples

### In $E_\infty$-geometry

In [[E-∞ geometry]] left adjoints

$$
  f_! \;\colon\; QCoh(X) \longrightarrow QCo
$$

to the canonical [[inverse image]] map along a morphism of [[E-∞ geometry|E-∞ algebraic spaces]] is discussed in ([Lurie, prop. 3.3.23](#Lurie)).

The existence of [[dualizing modules]] $K$

$$
  D X = [X,K]
$$ 

([[Verdier duality]]) is in ([[Representability theorems|Lurie, Representability theorems, section 4.2]].)

## References

The construction goes back to and is named afzer

* Klaus Wirthm&#252;ller, _Equivariant homology and duality_. Manuscripta Math. 11(1974), 373-390
 {#Wirthmueller74}

A clear discussion of axioms of [[six operations]] and their consequences, with emphasis on the Wirthm&#252;ller isomorphisms, is in 

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_ ([pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))
 {#May05}

Discussion of the Wirthm&#252;ller isomorphism in [[equivariant stable homotopy theory]], based on this, is in

* [[Peter May]], _The Wirthm&#252;ller isomorphism revisited_ ([pdf](http://www.math.uiuc.edu/K-theory/0574/WirthRev.pdf))

Discussion in [[E-∞ geometry]] is in

* [[Jacob Lurie]], section 3.3. of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_
 {#Lurie}

* [[Jacob Lurie]], section 4.2 of _[[Representability theorems]]_


[[!redirects Wirthmüller contexts]]

[[!redirects Wirthmueller context]]
[[!redirects Wirthmueller contexts]]

[[!redirects Wirthmuller context]]
[[!redirects Wirthmuller contexts]]


[[!redirects Wirthmüller isomorphism]]
[[!redirects Wirthmüller isomorphisms]]

[[!redirects Wirthmueller isomorphism]]
[[!redirects Wirthmueller isomorphisms]]

[[!redirects Wirthmuller isomorphism]]
[[!redirects Wirthmuller isomorphisms]]

