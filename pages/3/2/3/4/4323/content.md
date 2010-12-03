

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The Thom spectrum $M O$ is a [[connective spectrum]] whose associated [[infinite loop space]] is the [[classifying space]] for [[cobordism]]:

$$
\Omega^\infty M O \simeq B Cob_\infty.
$$

In particular, $\pi_n M O$ is naturally identified with the set of cobordism classes of closed $n$-manifolds.

## Definition

For any $n\geq 1$, let $E_n\to BO(n)$ be the $\mathbb{R}^n$-bundle [[associated bundle|associated to]] the [[universal principal bundle]] $E O(n)\to B O(n)$ by the defining [[representation]] of the [[orthogonal group]] $O(n)$. The inclusion $O(n)\equiv O(n)\times\{1\}\hookrightarrow O(n+1)$ induces a map $\varphi_n:B O(n)\to B O(n+1)$. One sees that $\varphi_n^*E_{n+1}\simeq E_n\oplus\mathbb{R}$. therefore, passing to [[Thom space]]s, 
$$
\Sigma Th(E_n)\simeq Th(E_n)\wedge Th(\mathbb{R})\simeq Th(E_n\oplus \mathbb{R})\simeq Th(\varphi_n^*E_{n+1})\to Th(E_{n+1}).
$$
Hence, setting $M O(n):=Th(E_n)$, we get a system of maps
$$
\Sigma M O(n) \to M O(n+1),
$$ 
and so a [[spectrum]] $M O$, which is called the **Thom spectrum** .

## Properties

The isomorphisms 

$$
  \pi_n M O\simeq \Omega_n=\{closed n-manifolds\}/cobordism
$$

date back to the fundamental work of [[René Thom]] and is based on the [[fiber integration|Pontrjagin-Thom construction]]. The homotopy equivalence $\Omega^\infty M O \simeq B Cob_\infty$ is the content of Galatius-Madsen-Tillmann-Weiss theorem, and is now seen as a part of the [[cobordism hypothesis]] theorem.

## Generalizations
Instead of the sequence of groups $O(n)$, one can consider $SO(n)$, or $Spin(n)$, $String(n)$, $Fivebrane(n)$,..., i.e., any level in the [[Whitehead tower]] of $O(n)$. To any of these groups it corresponds a Thom spectrum, which is in turn related to oriented cobordism, spin cobordism, string cobordism, et cetera.

## Cohomology

Under the [[Brown representability theorem]] the Thom spectrum represents the [[generalized (Eilenberg-Steenrod) cohomology]] theory called [[complex cobordism cohomology theory|cobordism cohomology theory]].

## References

A discussion of the relation of the Thom spectrum to [[(∞,n)-category of cobordisms]] for $n = \infty$ is in

* [[John Francis]], _Cobordisms_ (notes by [[Owen Gwilliam]]) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))


