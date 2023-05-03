
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Suppose $M$ is a [[smooth manifold]].
Recall (e.g. from the article *[[Nijenhuis–Richardson bracket]]*) that any [[differential form|differential $(k+1)$-form]] $K\in\Omega^{k+1}(M,T M)$ valued in the [[tangent bundle]] of $M$ gives rise to a [[graded derivation|graded]] [[derivation]] $\iota_K$ of degree $k$ on the [[de Rham algebra]] of [[differential forms]] on $M$: on [[differential 1-form|1-forms]] we have $\iota_K \omega=\omega\circ K$ and on higher forms we extend using the [[Leibniz rule]].

Concretely,
$$
  \iota_K \omega(X_1,\ldots,X_{k+l})
  \;=\;
  \frac
    {1}
    {(k+1)!(l-1)!} 
  \sum_\sigma (-1)^\sigma
  \omega\big(
    K(Y_{\sigma(1)} ,\, \ldots ,\, Y_{\sigma(k+1)})
    ,\,
    Y_{\sigma(k+2)}
    ,\,\ldots
  \big)
  \,,
$$
where the [[sum]] is over all [[permutations]] $\sigma \in$ [[symmetric group|$Sym(k+l)$]] and where $(-1)^\sigma$ denotes the [[signature of a permutation|sign of the permutation]].

[[Cartan's magic formula]]
$$L_X=[\iota_X,d]$$
makes it natural to define the [[Lie derivative]] with respect to $K\in\Omega^k(M,\, T M)$:
$$L_K=[\iota_K,d].$$

The map $L$ defines an [[injective]] [[homomorphism]] of [[graded vector spaces]] from $\Omega(M,TM)$ to graded derivations of $\Omega(M)$.  Its image comprises precisely those derivations $D$ such that $[D,d]=0$ and is closed under the commutator operation.  Transferring the bracket to its source yields the __Frölicher–Nijenhuis bracket__:
$$L_{[K,L]} = [L_K,L_L]$$
for a uniquely defined $[K,L]\in\Omega^{k+l}(M,TM)$.

## Classification of graded derivations of differential forms

Taken together, the [[Frölicher–Nijenhuis bracket]] and the [[Nijenhuis–Richardson bracket]] allows us to fully classify the [[graded derivations]] of the [[de Rham algebra]] of [[differential forms]] on $M$:

A graded dervation $D$ of degree $k$ on $\Omega(M)$ has a unique presentation of the form
$$D=L_K + \iota_L,$$
where $K\in\Omega^k(M,TM)$, $L\in\Omega^{k+1}(M,TM)$.

We have $L=0$ if and only if $[D,d]=0$
and $K=0$ if and only if $D$ vanishes on 0-forms.

Finally, the graded commutator of graded derivations can be expressed in terms of the [[Frölicher–Nijenhuis bracket]] (for $K$) and the [[Nijenhuis–Richardson bracket]] (for $L$):
$$[L_K,L_L]=L_{[K,L]},$$
$$[\iota_K,\iota_L]=\iota_{[K,L]^\wedge},$$
$$[L_K,\iota_L]=\iota_{[K,L]}-(-1)^{k l}L_{\iota_L K},$$
$$[\iota_K,L_L]=L_{\iota_L K}+(-1)^k \iota_{[L,K]}.$$



## Explicit formula

Given a smooth manifold $M$ and differential forms $P\in\Omega^k(M,TM)$, $Q\in\Omega^l(M,TM)$
valued in the [[tangent bundle]] $TM$ of $M$,
their __Frölicher–Nijenhuis bracket__ is a [[differential form]]
$$[P,Q]\in\Omega^{k+l}(M,TM)$$
defined by the formula
$$
  \begin{array}{l}
  [P,Q](X_1,\ldots,X_{k+l})
  \;\coloneqq\;
  \frac{1}{k! l!} 
  \sum_\sigma (-1)^\sigma 
  \Big(
    &
    \big[
      P(Y_{\sigma(1)},\ldots, Y_{\sigma(k)}),
      \, 
      Q(Y_{\sigma(k+1)},\ldots,Y_{\sigma(k+l)})
    \big]
    \\
    &
    -l 
    \,
    Q\big(
      [P(Y_{\sigma(1)},\ldots,Y_{\sigma(k)})
      ,\,
      Y_{\sigma(k+1)}]
      ,\,Y_{\sigma(k+2)},
      \ldots
    \big)
    \\
    &
    +(-1)^{k l} k 
    \,
    P\big(
      [Q(Y_{\sigma(1)},\ldots,Y_{\sigma(k)})
      ,\,
      Y_{\sigma(k+1)}], Y_{\sigma(k+2)},\ldots\big)
    \\
    &
    + \frac{1}{2} (-1)^{k-1}  k l  
    \,
    Q\big(
      P([Y_{\sigma(1)},Y_{\sigma(2)}],Y_{\sigma(3)},
      \ldots),Y_{\sigma(k+2)},\ldots
    \big)
    \\
    &
    + \frac{1}{2} (-1)^{(k-1)l} k l
    \,
    P\big(
      Q([Y_{\sigma(1)},Y_{\sigma(2)}],Y_{\sigma(3)},\ldots),Y_{\sigma(k+2)}, \ldots
    \big) 
  \Big)
  \,,
  \end{array}
$$
and $(-1)^\sigma$ is the [[signature of a permutation|sign of the permutation]] $\sigma$.

## Applications

The [[Nijenhuis tensor]] of an [[almost complex structure]] $J\in\Omega^1(M,TM)$ is $[J,J]$.
The explicit formula yields
$$
  [J,J](X,Y)
  \;=\;
  2\big(
    [J X, J Y] - [X,Y] - J[X, J Y] - J[J X,Y]
  \big).
$$

## Related concepts

* [[Schouten–Nijenhuis bracket]]

* [[Nijenhuis–Richardson bracket]]

* [[Nijenhuis tensor]]

## References

Original definition:

* [[Alfred Frölicher]], [[Albert Nijenhuis]], _Theory of vector-valued differential forms.  Part I.  Derivations in the graded ring of differential forms_, Indagationes Mathematicae (Proceedings) 59 (1956), 338–350 and 351–359.  [doi:10.1016/s1385-7258(56)50046-7][1] and [doi:10.1016/s1385-7258(56)50047-9][2].

[1]: https://doi.org/10.1016/s1385-7258(56)50046-7
[2]: https://doi.org/10.1016/s1385-7258(56)50047-9

Refinements for [[almost complex structures]]:

* [[Alfred Frölicher]], [[Albert Nijenhuis]], _Theory of vector-valued differential forms.  Part II.  Almost-complex structures_, Indagationes Mathematicae (Proceedings) 61 (1958), 414–421 and 422-429.  [doi:10.1016/s1385-7258(58)50057-2][3] and [doi:10.1016/s1385-7258(58)50058-4][4].

[3]: https://doi.org/10.1016/s1385-7258(58)50057-2
[4]: https://doi.org/10.1016/s1385-7258(58)50058-4

Discussion as a [[natural operation]]:

* {#KolarMichorSlovak} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], p. 175 of: _[[Natural operations in differential geometry]]_, Springer (1993) &lbrack;[webpage](https://www.emis.de/monographs/KSM/), [doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3), [pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf)&rbrack;




[[!redirects Frölicher–Nijenhuis brackets]]
[[!redirects Frölicher-Nijenhuis brackets]]
[[!redirects Frölicher-Nijenhuis bracket]]
