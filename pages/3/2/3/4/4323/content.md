<div class="rightHandSide toc">
[[!include manifolds and cobordisms - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea
The Thom spectrum $MO$ is a [[connective spectrum]] whose associated [[infinite loop space]] is the [[classifying space]] for [[cobordism]]:
$$
\Omega^\infty MO \simeq B Cob_\infty.
$$
In particular, $\pi_n MO$ is naturally identified with the set of cobordism classes of closed $n$-manifolds.

## Definition
For any $n\geq 1$, let $E_n\to BO(n)$ be the $\mathbb{R}^n$-bundle associated to the principal bundle $EO(n)\to BO(n)$ by the defining representation of $O(n)$. The inclusion $O(n)\equiv O(n)\times\{1\}\hookrightarrow O(n+1)$ induces a map $\varphi_n:BO(n)\to BO(n+1)$. One sees that $\varphi_n^*E_{n+1}\simeq E_n\oplus\mathbb{R}$. therefore, passing to [[Thom space]]s, 
$$
\Sigma Th(E_n)\simeq Th(E_n)\wedge Th(\mathbb{R})\simeq Th(E_n\oplus \mathbb{R})\simeq Th(\varphi_n^*E_{n+1})\to Th(E_{n+1}).
$$
Hence, setting $MO(n):=Th(E_n)$, we get a system of maps
$$
\Sigma MO(n) \to MO(n+1),
$$ 
and so a [[spectrum]] $MO$, which is called the Thom spectrum.

## Properties
The isomorphisms 
$$
\pi_n MO\simeq \Omega_n=\{closed n-manifolds\}/cobordism
$$
date back to the fundamental work of [[René Thom]] and is based on the [[fiber integration|Pontrjagin-Thom construction]]. The homotopy equivalence $\Omega^\infty MO \simeq B Cob_\infty$ is the content of Galatius-Madsen-Tillmann-Weiss theorem, and is now seen as a part of the [[cobordism hypothesis]] theorem.

## Generalizations
Instead of the sequence of groups $O(n)$, one can consider $SO(n)$, or $Spin(n)$, $String(n)$, $Fivebrane(n)$,..., i.e., any level in the [[Whitehead tower]] of $O(n)$. To any of these groups it corresponds a Thom spectrum, which is in turn related to oriented cobordism, spin cobordism, string cobordism, et cetera.