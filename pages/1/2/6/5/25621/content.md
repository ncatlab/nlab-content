## Definition

Suppose $M$ is a [[smooth manifold]].
Recall that any differential $(k+1)$-form $K\in\Omega^{k+1}(M,TM)$ valued in the [[tangent bundle]] of $M$ gives rise to a [[graded derivation]] $\iota_K$ of degree $k$ on the algebra of [[differential forms]] on $M$: on 1-forms we have $\iota_K \omega=\omega\circ K$ and on higher forms we extend using the Leibniz identity.

Concretely,
$$\iota_K \omega(X_1,\ldots,X_{k+l})=1/((k+1)!(l-1)!)\sum_\sigma (-1)^\sigma \omega(K(Y_1,\ldots,Y_{k+1}),Y_{k+2},\ldots),$$
where $Y_i=X_{\sigma(i)}$.

The map $\iota$ defined an injective homomorphism of [[graded vector spaces]] from $\Omega^{\bullet+1}(M,TM)$ to graded derivations of $\Omega(M)$.  Its image comprises precisely those derivations that vanish on 0-forms and is closed under the commutator operation.  Transferring the bracket to its source yields the __Nijenhuis–Richardson bracket__:
$$[K,L]^\wedge = \iota_K L-(-1)^{k l}\iota_L K,$$
where $\iota_K(\omega\otimes X)=\iota_K \omega\otimes X$.

## Classification of graded derivations of differential forms

The Nijenhuis–Richardson bracket is an important ingredient in the classification of graded derivations of differential forms.

See the article [[Frölicher–Nijenhuis bracket]] for more information.

## Related concepts

* [[Frölicher–Nijenhuis bracket]]

* [[Schouten–Nijenhuis bracket]]