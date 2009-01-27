##Idea##
For 'nice' spaces, i.e. CW-complexes, a weak equivalence is the same as a homotopy equivalence.  Here a weak equivalence is a map which induces an isomorphism on all homotopy groups:
$$f:X\to Y \Leftrightarrow \pi_k(f) : \pi_k(X)\to \pi_k(Y)$$
for all $k \geq 0$ and all choices of base point.

(For simplicial groups or groupoids, we have a similar notion.)

What if we only have that $\pi_k(f)$ is an isomorphism up to some dimension, $n$, what can we say about the 'homotopy types'. Any space is equivalent in this trunctaed form to a space with trivial homotopy groups above level $n$, so can we find reasonably complete 'algebraic' models fo such $n$-types.

We will use simplicial groups and simplicial groupoids rather than spaces below as they are already partially algebraicised.
 
##Definitions##



 A morphism $f : G \to H$ of [[simplicial group]](oid)s is an **$n$-equivalence** if the induced homomorphisms, $\pi_k(f) : \pi_k(G)\to \pi_k(H)$ are isomorphisms for all $k \lt n$.
 
 Inverting the $n$-equivalences in $Simp.Grps$ gives a category $Ho_n(Simp.Grps)$ and two simplicial groups have the same **$n$-type** if they are isomorphic in $Ho_n(Simp.Grps)$.

##Discussion##

Considerable effort has gone into finding 'good' algebraic models for (connected) homotopy $n$-types. In low dimensions the results are 'old' or 'classical'.  (We will consider connected cases only.  The extension to the non-connected case is 'routine'.)

* The