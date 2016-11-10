
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents 
* table of contents 
{: toc}

## Idea 

### General

Traditionally, a compactification of a [[topological space]] $X$ is a [[compact space]] $C$ together with an [[embedding]] $i \colon X \to C$ as a [[dense subspace]]. Well known is for instance the _[[one-point compactification]]_ of a [[locally compact Hausdorff space]] which for instance sends the real [[line]] to the [[circle]] by adding a point at infinity.

In some cases, the terminology 'compactification' is applied to generalizations where $i$ is not a dense embedding (does not map [[homeomorphism|homeomorphically]] to an image that is dense). For example, the one-point compactification of an already [[compact Hausdorff space]] adds an *isolated* point at infinity, and so is not a dense subspace. Or, if $X$ is not a Tychonoff space, then the universal map to its [[Stone-Cech compactification]] is not an embedding.  

If the space has further geometric structure, the compactification is 
usually required to has such a structure and embedding has to preserve it.
Many [[moduli space]]s in algebraic and differential geometry have their
natural compactifications. They are often useful because they carry natural integration which is useful in defining various invariants. 

A useful intuition throughout is that a 'compactification' is a process of adding "ideal points at infinity" in some way to "complete" a space. (Compact [[regular space|regular]] spaces $X$ themselves being "complete" in a technical sense: there is a unique [[uniform space|uniform structure]] whose uniform topology is the topology on $X$, and $X$ is complete with respect to this uniformity.) 


### Fiberwise

Often a space can be viewed as a total space of a bundle over some base.
We may want to embed the space into a bigger bundle, such that the induced
embedding of each fiber into the new fiber is a compactification.

This is roughly the case in most __compactifications in physics__. In most cases the space is equipped with a [[Riemannian metric]] and additional quantities for defining physics, like a [[Lagrangian density]], which possibly depend on the metric.

Then one requires that the compactified fiber is finite but small compared to some reference scale (or even viewed in a limit when the Riemannian volume tends to zero), see at _[[Kaluza-Klein mechanism]]_. Often one does not even consider a noncompact case to start with but by compactification in physics means only passing to the limit of small (Riemannian volume of) fibers. 

## Definition

+-- {: .num_defn #Compactification}
###### Definition

A _compactification_ of a [[topological space]] $X$
is a [[compact topological space|compact]] [[Hausdorff topological space]]
$Y$ equipped with an [[embedding]] $X \hookrightarrow Y$
such that the [[closure]] of $X$ in $Y$ is the compact space:
$\overline{X} = Y$.

An [[equivalence]] of two compactifications $Y_1$, $Y_2$ of $X$
is a [[homeomorphism]] $h \;\colon\; Y_1 \longrightarrow Y_2$
that preserves the inclusion of $X$.

=--

## Properties



### Uniqueness

In some sense the [[one-point compactification]] is the smallest 
possible compactification, while the [[Stone-Cech compactification]]
is the largest. The following gives conditions that
all notions of compactification agree.

+-- {: .num_prop #UniqueCompactificationOfAlmostCompactSpaces}
###### Proposition

For $X$ a [[Tychonoff space]] the following are equivalent:

1. There is a unique (up to equivalence) compactification, def. \ref{Compactification}. 

1. $X$ is already [[compact topological space|compact]] or its [[Stone-Cech compactification]] $\beta X$ adds a single point $\vert \beta X \backslash X\vert = 1$.

1. If two [[closed subsets]] of $X$ are completeley separated, then one of them is a [[compactum]].

=--

One place where this appears is ([Hewitt 47](#Hewitt47)).

+-- {: .num_remark}
###### Remark

The topological spaces satisfying the conditions of
prop. \ref{UniqueCompactificationOfAlmostCompactSpaces}
are also called [[almost compact topological space|almost compact topological spaces]].

=--


## Examples 

### In topology

* [[One-point compactification]]

* [[Stone–Cech compactification]]

* [[end compactification|End compactification]]

* [[Bohr compactification]]

### In geometry

* [[wonderful compactification]] 

* [[Deligne-Mumford compactification]].

* [[Kaluza-Klein compactification]]

  * [[Freund-Rubin compactification]]

* [[conformal compactification]]
* [[projective compactification]]

## References


* Edwin Hewitt, _Certain generalizations of the Weierstrass approximation theorem_,  Duke Math. J. Volume 14, Number 2 (1947), 419-427. ([Euclid](http://projecteuclid.org/euclid.dmj/1077474139))
  {#Hewitt47}


[[!redirects compactification]]
[[!redirects compactifications]]
