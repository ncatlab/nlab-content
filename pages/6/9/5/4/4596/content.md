
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## In the snake lemma

... [[snake lemma]] ... [[five lemma]] ...

## For long exact sequences in (co)homology

For $0 \to A \to B \to C \to 0$ a [[short exact sequence]] of [[cochain complex]]es, the corresponding [[fiber sequence|long exact sequence]] in [[cochain cohomology]]

$$
  \cdots \to H^n(A) \to H^n(B) \to H^n(C) \stackrel{\delta}{\to} H^{n+1}(A) \to H^{n+1}(B) \to H^{n+1}(C) \to \cdots
$$

has in every third step a morphism $\delta$ that shifts cohomological degree. This is called a _connecting homomorphism_ . 

It may be constructed as follows:

for $[c]_C \in H^n(C)$ the class of a closed element $c$, by surjectivity of $B \to C$ there is an element $\hat c \in B$ mapping to it. This need not be closed anymore, but of course $d_B \hat c$ is. By the fact that $B \to C$ is a chain map we have that the image of $d_B \hat c$ in $B$ vanishes. Therefore by the exactness of the sequence the element $d_B \hat c$ may be regarded as a closed element of $A$. The cohomology class $[d_B \hat c]_A$ of this is what the connecting homomorphism assigns to $[c]_C$:

$$
  \delta : [c]_C \mapsto [d_B\hat c]_A
  \,.
$$

This is indeed well defined, in that it is independent of the choice of $\hat c$: for $\hat c'$ another choice, we have that the difference $\hat c - \hat c'$ is in the kernel of $B \to C$ hence is in $A$. Then $d_B \hat c' = d_B \hat C + d_A(\hat c - \hat c')$. Hence $[d_B \hat c]_A = [d_B \hat c']_A$.

[[!redirects connecting homomorphisms]]