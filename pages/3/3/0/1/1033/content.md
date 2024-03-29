
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


+-- {: .num_defn}
###### Definition

In a [[category]] with a [[terminal object]] $1$, the **cokernel** of a [[morphism]] $f : A \to B$ is the [[pushout]] 

$$
  coker(f)
    \;\coloneqq\; 
  1 \underset{A}{\sqcup} B
  \phantom{AAAAAA}
  \array{
    A &\stackrel{\phantom{A}f\phantom{A}}{\longrightarrow}& B
    \\
    \big\downarrow &{}^{(po)}& \big\downarrow
    \\
    1 
      &\longrightarrow& 
    coker(f)
  }
$$

=--

+-- {: .num_remark}
###### Remark

In the case when the terminal object is in fact [[zero object]], one can, more explicitly, characterize the object $coker(f)$ as [[generalized the|the]] object (unique up to unique [[isomorphism]]) that satisfies the following [[universal property]]:

for every object $C$ and every morphism $h \colon B \longrightarrow C$ such that $h \circ f = 0$ is the [[zero morphism]], there is a unique morphism $\phi \colon coker(f) \to C$ such that $h = \phi \circ i$.

=--


+-- {: .num_remark}
###### Remark

The notion of cokernel is [[duality|dual]] to that of _[[kernel]]_. A **cokernel** in a [[category]] $\mathcal{C}$ is a [[kernel]] in the [[opposite category]] $\mathcal{C}^{op}$.

=--

## Properties

### Exactness properties

* Taking cokernels is a [[right exact functor]] on arrow-categories.

## Examples

+-- {: .num_example}
###### Example

In the category [[Ab]] of [[abelian groups]] the cokernel of a morphism $f : A \to B$ is the [[quotient]] of $B$ by the [[image]] (of the underlying morphism of [[sets]]) of $f$.

=--

+-- {: .num_example}
###### Example

More generally, for $R$ any [[ring]], this is true in the category $R$[[Mod]] of [[modules]]: the cokernel of a morphism is the quotient by its set-theoretic image.

=--

+-- {: .num_example}
###### Example

In the category [[Grp]] of general (not necessarily abelian) groups, the cokernel is instead the [[quotient group]] by the [[normal closure]] of the image.

=--

The following example is by the very definition of _[[abelian category]]_.

+-- {: .num_example}
###### Example

In an [[abelian category]] the [[coimage]] of any morphism $f$ is the cokernel of its [[kernel]]

$$
  coim(f) = coker(ker(f))
  \,.
$$

=--

## Related concepts


* [[kernel]]

* [[cocone]]

* [[cofiber]], [[homotopy cofiber]]

[[!redirects cokernels]]

