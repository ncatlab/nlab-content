

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #RegularValue}
###### Definition
**([[regular value]])**

For 

$$
  f 
    \;\colon\;
  X
    \longrightarrow
  Y
$$

a [[differentiable function]] between [[differentiable manifolds]] (e.g. a [[smooth function]] between [[smooth manifolds]]) a [[point]] $q \in f(X) \subset Y$ in the [[image]] of $f$ is called a _regular value_ of $f$ if at all points $p \in f^{-1}(\{q\})$ in its [[preimage]], the [[differential]]

$$
  d f_p \;\colon\; T_p X \longrightarrow T_{f(x)} Y = T_{q}Y
$$

is a [[surjective function]] between the corresponding [[tangent spaces]].



A function all whose values are regular values is called a _[[submersion]]_.

=--

(e.g. [Kosinski 93, II (2.4)](#Kosinski93))

+-- {: .num_remark #RelationToTransversality}
###### Remark
**(relation to [[transversal map|transversality]])**

That $q \in Y$ is a [[regular value]] (Def. \ref{RegularValue}) of $f \colon X \to Y$ means equivalently that $f$ is a [[transverse map]] to the [[submanifold]]-inclusion $\ast \overset{q}{\hookrightarrow} Y$.

In this sense [[transversal map|transversality]] generalizes the concept of [[regular values]].

=--

## Properties

### Inverse image

The [[inverse function theorem]] implies that:

+-- {: .num_prop }
###### Proposition

The [[inverse image]] $f^{-1}(q) \subset X$ of a [[smooth function]] $f \colon X \to Y$ at a [[regular value]] $q \in Y$ is a [[smooth manifold]] of $X$.

=--

Together with the [[Thom's transversality theorem]], this is the key to the [[proof]] of the [[Pontryagin-Thom isomorphism]].


## Related concepts

* [[immersion]], [[submersion]]

* [[transverse map]]

* [[Thom's transversality theorem]]

* [[Pontryagin-Thom isomorphism]]


## References

* {#Kosinski93} [[Antoni Kosinski]], _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))


[[!redirects regular values]]

