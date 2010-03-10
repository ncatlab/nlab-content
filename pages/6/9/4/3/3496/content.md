
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[geometric morphism]] $f : E \to F$ between [[topos]]es is a [[functor]] of the underlying categories that is consistent with the interpretation of $E$ and $F$ as generalized [[topological space]]s. 

A geometric morphism is **essential** if in addition $f$ behaves as if...

+--{: .query}
[[Mike Shulman]]: Interesting ellipsis.  I'm not sure that "essentiality" has any real intuitive meaning; it's kind of "like being locally connected" except not quite right if $F$ isn't $Set$.

[[Urs Schreiber]]: shouldn't it be right to say that $f$ behaves as if the fibers of $f$ are locally connected spaces?

[[Mike Shulman]]: No, that would be a [[locally connected geometric morphism]].  Not every essential geometric morphism is locally connected.

=--


## Definition

Given a geometric morphism $(f^* \dashv f_*) : E \to F$, it is an **essential geometric morphism** if the [[inverse image]] functor $f^*$ has not only the [[right adjoint]] $f_*$, but also a [[left adjoint]] $f_!$:

$$
  (f_! \dashv f^* \dashv f_*) \;\;\; : \;\;\;
  E
    \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
  F
  \,.
$$

## Properties

+-- {: .un_prop}
###### Proposition

For every $\phi : X \to f^* f_* A$ in $E$ the diagram

$$
  \array{
    X &\stackrel{\phi}{\to}& f^* f_* A
    \\
    \downarrow && \downarrow
    \\
    f^* f_! X &\stackrel{}{\to}& A
  }
$$

commutes, where the vertical morphisms are unit and counit, respectively, and where the bottom horizontal morphism is the [[adjunct]] of $\phi$ under the composite adjunction $(f^* f_! \dashv f^* f_*)$.

=--

+-- {: .proof}
###### Proof

The morphism $\phi : X \to f^* f_* A$ is the component of a natural transformation

$$
  \array{
    *&&\overset{X}{\to}&& E
    \\
    {}^{\mathllap{A}}\downarrow
    &\Downarrow^\phi&& {}^{\mathllap{f^*}}\nearrow 
    \\
    E &\underset{f_*}{\to}&F
  }
  \,.
$$

The composite $X \stackrel{\phi}{\to}  f^* f_ A \to A$ is the component of this composed with the counit $f^* f_* \Rightarrow Id$.

We may insert the 2-identity given by the zig-zag law

$$
  \cdots \;\;\; = \;\;\;
  \array{
    *&&\overset{X}{\to}&& E && = && E
    \\
    {}^{\mathllap{A}}\downarrow
    &\Downarrow^\phi&& {}^{\mathllap{f^*}}\nearrow &\Downarrow& \searrow^{f_!} 
    &\Downarrow& \nearrow_{\mathrlap{f^*}}
    \\
    E &\underset{f_*}{\to}&F &&=&& F   
  }
  \,.
$$

Composing this with the counit $f^* f_* \Rightarrow Id$ produces the transformation whose component is manifestly the morphism $X \to f^* f_! X \to A$.

=--


## Examples

For any morphism $f\colon A\to B$ in a topos $E$, the induced geometric morphism $f\colon E/A \to E/B$ is essential.

A [[locally connected topos]] $E$ is one where the [[global section]] [[geometric morphism]] $\Gamma : E \to Set$ is essential. 

$$
  (f_! \dashv f^* \dashv f_*) \;\;\; : \;\;\;
  E
    \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
  \,.
$$

In this case, the functor $\Gamma_! = \Pi_0 : E \to Set$ sends each object to its set of connected components.  More on this situation is at [[homotopy groups in an (∞,1)-topos]].  

Note, though that if $p\colon E\to S$ is an arbitrary geometric morphism through which we regard $E$ as an $S$-topos, i.e. a topos "in the world of $S$," the condition for $E$ to be locally connected as an $S$-topos is not just that $p$ is essential, but that the left adjoint $p_!$ can be made into an $S$-[[indexed functor]] (which is automatically true for $p^*$ and $p_*$).  This is automatically the case for $Set$-toposes (at least, when our [[foundation]] is [[material set theory]]---and if our foundation is [[structural set theory]], then our large categories and functors all need to be assumed to be $Set$-indexing anyway).


## References

The definition appears before Lemma A.4.1.5 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ 
