
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **sequential (co)limit** is a [[limit]]/[[colimit]] whose [[diagram]] category is a nonzero [[ordinal]] or its [[opposite poset|opposite]] (regarded as a [[poset]], regarded as a [[category]]). For instance over a [[tower diagram]]. 

 Sometimes the term is used even more specifically for a (co)limit over the ordinal $\omega$.

Thus, a sequential limit is a special case of a [[directed limit]]. See there for more details.

## Examples

Sequential limits i.e. the [[tower]]-diagram
$$
  \array{
     && && \lim_{\leftarrow_n} X(n) &&
     \\
     && &\swarrow& \downarrow & \searrow&
     \\
     \cdots & \to & X(2) & \to  & X(1) & \to & X(0)
  }
$$
are extremely common. Classical examples occur in the theory of [[Postnikov towers]] and also in the definition of the [[solenoids]], as well as [[projective limits]]. 

A [[ring]] $ K [ [ x ] ] $ of formal [[power series]] (for $K$ a [[field]]) is a sequential limit of the rings $K[x]/x^n$ (for $n$ a [[natural number]]). 

Similarly, a ring $\mathbf{Z}_p$ of $p$-[[adic integer]]s (for $p$ a [[prime number]]) is a sequential limit of the rings $\mathbf{Z}/p^n$.

A set of infinite [[sequences]] is a sequential limit of sets of [[list|finite sequences]] (which, at the level of [[sets]], includes the above examples).

The [[axiom of dependent choice]] states that given a [[family of sets]] $X_n$ and a family of [[surjections]] $f_n:X_{n + 1} \to X_n$ indexed by natural numbers $n \in \mathbb{N}$: 
$$
  \array{
     && && \lim_{\leftarrow_n} X_n &&
     \\
     && &\swarrow& \downarrow & \searrow&
     \\
     \cdots & \underset{f_2}\to & X_2 & \underset{f_1}\to  & X_1 & \underset{f_0}\to & X_0
  }
$$
the projection function to $X_0$ from the sequential limit $\underset{\leftarrow}\lim X_n$ of the above diagram is a surjection. 

## Related concepts

* [[tower of fibrations]]

* [[lim^1 and Milnor sequences]]

## References

Discussion of [[sequential colimits]] (in the generality of [[homotopy colimits]]) in [[homotopy type theory]]:

* [[Egbert Rijke]], *Sequential colimits* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/sequences.pdf)&rbrack;, Lecture 15 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

It could also be found in section 26 of the draft of the textbook:

* {#RijkeDraft22} [[Egbert Rijke]] (2022), *[[Introduction to Homotopy Type Theory]]*, draft. ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf))

[[!redirects sequential limit]]
[[!redirects sequential limits]]
[[!redirects cosequential limit]]
[[!redirects cosequential limits]]
[[!redirects sequential colimit]]
[[!redirects sequential colimits]]

[[!redirects sequential diagram]]
[[!redirects sequential diagrams]]