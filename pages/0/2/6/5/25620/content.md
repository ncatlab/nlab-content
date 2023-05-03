## Definition

Suppose $M$ is a [[smooth manifold]].
Recall (from the article [[Nijenhuis–Richardson bracket]]) that any differential $(k+1)$-form $K\in\Omega^{k+1}(M,TM)$ valued in the [[tangent bundle]] of $M$ gives rise to a [[graded derivation]] $\iota_K$ of degree $k$ on the algebra of [[differential forms]] on $M$: on 1-forms we have $\iota_K \omega=\omega\circ K$ and on higher forms we extend using the Leibniz identity.

Concretely,
$$\iota_K \omega(X_1,\ldots,X_{k+l})=1/((k+1)!(l-1)!)\sum_\sigma (-1)^\sigma \omega(K(Y_1,\ldots,Y_{k+1}),Y_{k+2},\ldots),$$
where $Y_i=X_{\sigma(i)}$.

[[Cartan's magic formula]]
$$L_X=[\iota_X,d]$$
makes it natural to define the [[Lie derivative]] with respect to $K\in\Omega^k(M,TM)$:
$$L_K=[\iota_K,d].$$

The map $L$ defines an injective homomorphism of [[graded vector spaces]] from $\Omega(M,TM)$ to graded derivations of $\Omega(M)$.  Its image comprises precisely those derivations $D$ such that $[D,d]=0$ and is closed under the commutator operation.  Transferring the bracket to its source yields the __Frölicher–Nijenhuis bracket__:
$$L_{[K,L]} = [L_K,L_L]$$
for a uniquely defined $[K,L]\in\Omega^{k+l}(M,TM)$.

## Classification of graded derivations of differential forms

Taken together, the [[Frölicher–Nijenhuis bracket]] and the [[Nijenhuis–Richardson bracket]] allows us to fully classify the graded derivations of the algebra of [[differential forms]] on $M$:

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
$$[P,Q](X_1,\ldots,X_{k+l})=1/(k!l!) \sum_\sigma (-1)^\sigma 
\left(
[P(Y_1,\ldots,Y_k),Q(Y_{k+1},\ldots,Y_{k+l})]
-l Q([P(Y_1,\ldots,Y_k),Y_{k+1}],Y_{k+2},\ldots)
+(-1)^{k l}k P([Q(Y_1,\ldots,Y_k),Y_{k+1}],Y_{k+2},\ldots)
+(-1)^{k-1}(k l/2) Q(P([Y_1,Y_2],Y_3,\ldots),Y_{k+2},\ldots)
+(-1)^{(k-1)l}(k l/2) P(Q([Y_1,Y_2],Y_3,\ldots),Y_{k+2},\ldots) \right),$$
where $Y_i=X_{\sigma(i)}$ and $(-1)^\sigma$ is the sign of the [[permutation]] $\sigma$.

## Applications

The [[Nijenhuis tensor]] of an [[almost complex structure]] $J\in\Omega^1(M,TM)$ is $[J,J]$.
The explicit formula yields
$$[J,J](X,Y)=2([JX,JY]-[X,Y]-J[X,JY]-J[JX,Y]).$$

## Related concepts

* [[Schouten–Nijenhuis bracket]]

* [[Nijenhuis–Richardson bracket]]

* [[Nijenhuis tensor]]