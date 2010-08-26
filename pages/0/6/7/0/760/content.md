
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

A **split monomorphism** in a [[category]] $C$ is a [[morphism]] $m: A \to B$ which has a [[retraction]], meaning a morphism $r: B \to A$ such that $r \circ m = 1_A$.

In such a situation one also says that $A$ is a [[retract]] of $B$, and that $A$ is a splitting of the [[idempotent]] $m \circ r: B \to B$.

The dual notion is that of [[split epimorphism]].

## Properties

Any split monomorphism is automatically a [[regular monomorphism]] (it is the [[equalizer]] of $m\circ r$ and $1_B$), and therefore also a [[strong monomorphism]], an [[extremal monomorphism]], and (of course) a [[monomorphism]].