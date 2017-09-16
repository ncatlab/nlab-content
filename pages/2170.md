Suppose $G$ is a group and $M$ a $G$-module and let $\delta : G \to M$ be a derivation. This means $\delta(g_1g_2) = \delta(g_1) +g_1\delta(g_2)$ for all $g_1, g_2 \in G$.

For calculations, the following lemma is very valuable, although very simple to prove.

**Lemma**

If  $\delta : G \to M$ is a derivation, then

(i) $ \delta(1_G) = 0$;

(ii) $\delta(g^{-1}) = -g^{-1}\delta(g)$ for all $g \in G$;


(iii) for any $g \in G$ and $n\geq 1$, 

$$\delta(g^n) = (\sum^{n-1}_{k=0}g^k)\delta(g).$$

**Proof:**  As was said, these are easy to prove.

$\delta(g) = \delta(1g) + 1\delta(g)$, so $\delta(1)= 0$, and hence (i); then 

$$\delta(1) = \delta(g^{-1}g) = \delta(g^{-1}) + g^{-1}\delta(g)$$ 

to get (ii), and finally induction to get (iii).

