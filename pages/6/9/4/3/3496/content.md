
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[geometric morphism]] $f : E \to F$ between [[topos]]es is a [[functor]] of the underlying categories that is consistent with the interpretation of $E$ and $F$ as generalized [[topological space]]s. 

A geometric morphism is **essential** if in addition $f$ behaves as if...


## Definition

Given a geometric morphism $(f^* \dashv f_*) : E \to F$, it is an **essential geometric morphism** if the [[inverse image]] functor $f^*$ has not only the [[right adjoint]] $f_*$, but also a [[left adjoint]] $f_!$:

$$
  (f_! \dashv f^* \dashv f_*) \;\;\; : \;\;\;
  E
    \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\overset{f_*}{\to}}}
  F
  \,.
$$

## Examples

A [[locally connected topos]] $E$ is one where the [[global section]] [[geometric morphism]] $\Gamma : E \to Set$ is essential. 


$$
  (f_! \dashv f^* \dashv f_*) \;\;\; : \;\;\;
  E
    \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  Set
  \,.
$$

The functor $\Gamma_! = \Pi_0 : E \to Set$ sends each object to its set of connected components.

More on this situation is at [[homotopy groups in an (∞,1)-topos]].

## References

The definition appears before Lemma A.4.1.5 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ 
