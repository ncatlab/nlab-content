
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A Noetherian (or often, as below, noetherian) [[ring]] (or [[rng]]) is one where it is possible to do [[induction]] over its ideals, because the ordering of ideals by reverse inclusion is [[well-founded relation|well-founded]]. 

## Definition

(In this section, "ring" means [[rng]], where the presence of a multiplicative identity is not assumed unless we say "unital ring".) 

A (left) __noetherian ring__ $R$ is a [[ring]] for which every ascending chain of its (left) [[ideals]] stabilizes. In other words, it is noetherian if its underlying $R$-module ${}_R R$ is a noetherian object in the category $R Mod$ of left $R$-modules (recall that a left ideal is simply a submodule of ${}_R R$). Similarly for right noetherian rings. Left noetherianness is independent of right noetherianness. A ring is noetherian if it is both left noetherian and right noetherian. 

An equivalent condition is that all (left) ideals are finitely generated. 

A dual condition is artinian: an __[[artinian ring]]__ is a ring satisfying the descending chain condition on ideals. The symmetry is severely broken if one considers unital rings: for example every unital artinian ring is noetherian; artinian rings are intuitively much smaller than generic noetherian rings.

Spectra of noetherian rings are glued together to define [[noetherian scheme|locally noetherian schemes]]. 


## Properties 

One of the best-known properties is the Hilbert basis theorem. Let $R$ be a (unital) ring. 

+-- {: .num_theorem} 
###### Theorem 
**(Hilbert)** 
If $R$ is left Noetherian, then so is the [[polynomial|polynomial algebra]] $R[x]$. (Similarly if "right" is substituted for "left".) 
=-- 

+-- {: .proof} 
###### Proof 
(We adapt the proof from [Wikipedia](https://en.wikipedia.org/wiki/Hilbert%27s_basis_theorem#First_Proof).) Suppose $I$ is a left ideal of $R[x]$ that is not finitely generated. Using the [[axiom of dependent choice]], there is a [[sequence]] of polynomials $f_n \in I$ such that the left ideals $I_n \coloneqq (f_0, \ldots, f_{n-1})$ form a strictly increasing chain and $f_n \in I \setminus I_n$ is chosen to have degree as small as possible. Putting $d_n \coloneqq \deg(f_n)$, we have $d_0 \leq d_1 \leq \ldots$. Let $a_n$ be the leading coefficient of $f_n$. The left ideal $(a_0, a_1, \ldots)$ of $R$ is finitely generated; say $(a_0, \ldots, a_{k-1})$ generates. Thus we may write 

$$\label{kill} a_k = \sum_{i=0}^{k-1} r_i a_i$$ 

The polynomial $g = \sum_{i=0}^{k-1} r_i x^{d_k - d_i} f_i$ belongs to $I_k$, so $f_k - g$ belongs to $I \setminus I_k$. Also $g$ has degree $d_k$ or less, and therefore so does $f_k - g$. But notice that the coefficient of $x^{d_k}$ in $f_k - g$ is zero, by (eq:kill). So in fact $f_k - g$ has degree less than $d_k$, contradicting how $f_k$ was chosen. 

=-- 

## A homological characterization

+-- {: .num_theorem}
###### Theorem
For a unital ring $R$ the following are equivalent:

1. $R$ is left Noetherian
1. Any small direct sum of injective left $R$-modules is injective.
1. $\operatorname{Ext}^k_R(A, \cdot)$ commutes with small direct sums for any finitely generated $A$.
=--

Direct sums here can be replaced by filtered colimits.

+-- {: .proof} 
###### Proof 
$1 \Rightarrow 2$: assume that $R$ is Noetherian and $I_\alpha$ are injective modules. In order to verify that $I := \bigoplus_\alpha I_\alpha$ is injective it is enough to show that for any ideal $\mathfrak{j}$ any morphism of left modules $f : \mathfrak{j} \to I$ factors through $\mathfrak{j} \to R$. Since $R$ is Notherian, $\mathfrak{j}$ is finitely generated, so the image of $f$ lies in a finite sum $I_{\alpha_1} \oplus \dots \oplus I_{\alpha_n}$. Thus an extension to $R$ exists by the injectivity of each $I_{\alpha_k}$.

$2 \Rightarrow 1$: if $R$ is not left Noetherian then there is a sequence of left ideals $\mathfrak{j}_1 \subsetneq \mathfrak{j}_2 \subsetneq \dots$. Take $\mathfrak{j} := \bigcup_k \mathfrak{j}_k$. The obvious map $j \to \prod_k (\mathfrak{j} / \mathfrak{j}_k)$ factors through $\bigoplus_k (\mathfrak{j} / \mathfrak{j}_k)$, since any element lies in all but finitely many $\mathfrak{j}_k$. Now take any injective $I_k$ with $0 \to \mathfrak{j} / \mathfrak{j}_k \to I_k$. The map $\mathfrak{j} \to \bigoplus_k I_k$ cannot extend to the whole $R$, since otherwise its image would be contained in a sum of finitely many $I_k$. Therefore, $\bigoplus_k I_k$ is not injective.

$2 \Rightarrow 3$: $\operatorname{Ext}^k_R(A, \bigoplus_\alpha X_\alpha)$ can be computed by taking an injective resolution of $\bigoplus_\alpha X_\alpha$. Since direct sums of injective modules are assumed to be injective, we can take a direct sum of injective resolutions of each $X_\alpha$. It remains to note that Hom out of a finitely generated module commutes with arbitrary direct sums.

$3 \Rightarrow 2$: Follows from the fact that $I$ is injective iff $\operatorname{Ext}^1_R(R / \mathfrak{i}, I) = 0$ for any ideal $\mathfrak{i}$.
=--
## Related concepts

* [[Noetherian module]]

* [[Noetherian poset]]

* [[Noetherian E-∞ ring]]

## References

* [wikipedia](http://en.wikipedia.org/wiki/Noetherian_ring), _[[noetherian object]]_


[[!redirects noetherian ring]]
[[!redirects noetherian rings]]
[[!redirects Noetherian ring]]
[[!redirects Noetherian rings]]
