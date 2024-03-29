

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called the _$j$-invariant_ is an invariant of [[cubic curves]] and hence of [[elliptic curves]], partly characterizing them. 

Over the [[complex numbers]] the _$j$-invariant_ is a [[modular function]] on the [[upper half plane]] which serves to characterize most of the properties of the [[moduli stack of elliptic curves]] in this case.

## Definition

### Over a general ring

With the Weierstrass parameterization discussed at _[elliptic curve -- Over general Rings -- As solution to the Weierstrass equation](elliptic%20curve#OverGeneralRingAsSolutionsToEquations)_, the $j$-invariant is the combination


$$
  j \coloneqq \frac{c_4^3}{\Delta}
  \,.
$$

In the case that 2 and 3 are invertible in the base ring, then this is equivalent to 

(...)

### Over the complex numbers

Over the [[complex numbers]],  with $G_{2k}$ the [[Eisenstein series]] and with 

$$
  g_2 \coloneqq 60 G_4
$$

$$
  g_3 \coloneqq 140 G_6
$$

and the [[discriminant]]

$$
  \Delta \coloneqq g_2^3 - 27 g_3^2
$$

then the _$j$-invariant_ is

$$
  j = 1728 \frac{g_2^3}{\Delta}
  \,.
$$

(Notice that $1728 = 12^3$.)

(e.g. [Miranda 88, def. I.2.1](#Miranda88)).

Notice the two special values

$$
  (j = 0 ) \Leftrightarrow (g_2 = 0)
$$

$$
  (j= 1728) \Leftrightarrow (g_3 = 0)
$$


### General

See at _[elliptic curve -- Definition for general rings -- j-invariant](elliptic+curve#WeierstrassCubicDiscriminantAndJInvariant)_.

## Properties

### Characterization of complex elliptic curves

Over the complex numbers, there are two [[elliptic curves]]
with special values

* the curve with $j = 0$, hence $g_2  = 0$, which is the one given by quotienting out an equilateral lattice; this has [[automorphism group]] $\mathbb{Z}/6\mathbb{Z}$;

* the curve with $j = 1728$, which corresponds to dividing out the lattice $(1,i)\mathbb{Z}$, this has automorphism group $\mathbb{Z}/4\mathbb{Z}$.

All other curves have automorphism $\mathbb{Z}/2\mathbb{Z}$, given by [[inversion involution]].

The case $j \to \infty$, hence $\Delta = 0 $ but $g_2 \neq 0$, corresponds to the [[nodal curve]] which is added in the [[Deligne-Mumford compactification]] of the [[moduli stack of elliptic curves]].


### As a branched cover of the complex plane 
 {#AsABranchedCoverOfTheComplexPlane}

Over the [[complex numbers]], the $j$-invariant is a map

$$
  j \;\colon \; \mathfrak{h} \longrightarrow \mathbb{C}
$$

from the [[upper half plane]] to the [[complex numbers]]. This is a [[branched cover]], with two branching points being $0,\;1728 \in \mathbb{C}$. 


The induced unramified covering

$$
  j \;\colon\; (\mathfrak{h}-j^{-1}(\{0,1728\})) \longrightarrow (\mathbb{C}-\{0,1728\})
$$

is a [[modular group]]($PSL_2(\mathbb{Z})$)-[[principal bundle]] and hence classified by a map

$$
  \mathbb{C} - \{0,1728\} \longrightarrow B PSL_2(\mathbb{C})
$$

from the [[plane]] with two points removed or equivalently 

$$
  \pi_1(\mathbb{C}-\{0,1728\}) \longrightarrow PSL_2(\mathbb{Z})
  \,.
$$

(e.g. [Miranda 88, section VI.3, p.65](#Miranda88))


## Related concepts

* [[moduli space of elliptic curves]]

* [[elliptic genus]]

* [[Moonshine]], [[Monster vertex algebra]]

## References

* Wikipedia _[j-invariant](http://en.wikipedia.org/wiki/J-invariant)_

* {#Miranda88} [[Rick Miranda]], _The basic theory of elliptic surfaces_, lecture notes 1988 ([pdf](http://www.math.colostate.edu/~miranda/BTES-Miranda.pdf))


[[!redirects j-invariants]]