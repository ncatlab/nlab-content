
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea


Let $\mathcal{C}$ be a [[closed monoidal category]] with [[tensor product]] and [[internal hom]] denoted by

\begin{tikzcd}[row sep=4pt]
  \mathcal{C} \times \mathcal{C} 
  \ar[r, "{ (\mbox{-})\otimes (\mbox{-})}"]
  &
  \mathcal{C}
  \\
  \mathcal{C}^{\mathrm{op}} \times \mathcal{C} 
  \ar[r, "{ [\mbox{-},\,\mbox{-}]}"]
  &
  \mathcal{C}
  \mathrlap{\,,}
\end{tikzcd}
 
respectively, and consider a [[monoid object|monoid]] [[internalization|internal]] to $\mathcal{C}$:

$$
  A \,\in\, Mon\big(\mathcal{C}\big)
  \,.
$$ 


Recall that the "$A$-[[action monad]]" induced by $A$ -- often called the "$A$-[[writer monad]]" when considered as a [[monad in computer science]] -- is the [[endofunctor]] of forming the [[tensor product]] with $A$

$$
  A \otimes (\text{-})
  \;\colon\;
  \mathcal{C} \to \mathcal{C}
$$

equipped with unit and multiplication structure morphisms induced, under the tensor product, from the unit and multiplication on $A$, respectively.

The analogous construction but with the tensor product replaced by the [[internal hom]]

$$
  [A,\, \text{-}]
  \;\colon\;
  \mathcal{C} \to \mathcal{C}
$$

which in [[computer science]]/[[type theory]] tends to be written

$$
  (A \to \text{-})
  \;\colon\;
  \mathcal{C} \to \mathcal{C}
  \,,
$$

gives a [[comonad]] which hence deserves to be called the *coaction comonad* or *cowriter comonad* induced by $A$.

Alternatively, one might think to [[formal duality|dualize]] the notion of the [[writer monad]] by considering a [[comonoid]]-object

$$
  B \,\in\, CoMon(\mathcal{C})
$$

and the induced comonad structure on $B \otimes (\text{-})$.

But if $\mathcal{C}$ is in fact a [[compact closed category]], then these two notions agree: In this case the [[internal hom]] out of the [[monoid object]] $A$ is the [[tensor product]] with the [[dual object|dual]] [[comonoid object]]

$$
  [A,\,\text{-}]
  \;\simeq\;
  A^\ast \otimes (\text{-})
  \,.
$$

Finally, if $A$ carries both [[monoid]]- and [[comonoid]]-[[structure]] in a compatible way to make a [[Frobenius monoid]], then the induced (co)writer (co)monad structures are compatible to make a [[Frobenius monad]].


## Related concepts

[[!include reader-writer (co)monads -- table]]



## References

The terminology "cowriter comonad" is used for instance in:

* {#AhmanUustalu17} [[Danel Ahman]], [[Tarmo Uustalu]], p. 5 of: *Taking updates seriously*, Proceedings of the Sixth International Workshop on [Bidirectional Transformations (Bx 2017)](https://ceur-ws.org/Vol-1827/), CEUR Workshop Proceedings **1827** (2017) &lbrack;[pdf](http://ceur-ws.org/Vol-1827/paper11.pdf)&rbrack;


* {#Uustalu21} [[Tarmo Uustalu]], lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021):

  {#Uustalu21Lecture3} p. 21 of: *Monads and Interaction Lecture 3* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs3.pdf), [[Uustalu-Monads3.pdf:file]]&rbrack;

In [[Haskell]], the comonad $[A, -]$ for a monoid $A$ is called [Traced](https://hackage.haskell.org/package/comonad-5.0.9/docs/Control-Comonad-Traced.html), although there is also [an instance](https://hackage.haskell.org/package/comonad-5.0.9/docs/Control-Comonad.html) for the function type.

[[!redirects cowriter comonads]]


[[!redirects traced comonad]]








