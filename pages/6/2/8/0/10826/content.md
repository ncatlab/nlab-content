
#Contents#
* table of contents
{:toc}

## Definition

Let $X$ be a [[reduced scheme|reduced]] [[scheme]] of [[characteristic]] the [[prime number]] $p$, hence such that for all points $x \in X$

$$
  p \cdot \mathcal{O}_{X,x} = 0
  \,.
$$

Write

$$
  F - id \coloneqq (-)^p - (-) \;\colon\; (\mathbb{G}_a)_X \longrightarrow (\mathbb{G}_a)_X
$$

for the [[endomorphism]] of the [[additive group]] over the [[étale site]] $X_{et}$ of $X$ (the [[structure sheaf]] regarded as just a [[sheaf of abelian groups]]) which is the [[Frobenius endomorphism]] $F(-) \coloneqq (-)^p$ minus the identity.

+-- {: .num_prop}
###### Proposition

There is a [[short exact sequence]] of [[abelian sheaves]] over the [[étale site]]

$$
  0 \to (\mathbb{Z}/p\mathbb{Z})_X \to (\mathbb{G}_a)_X \stackrel{F-id}{\to} (\mathbb{G}_a)_X \to 0
  \,.
$$


=--

This is called the _Artin-Schreier sequence_ (e.g. [Tamme, section II 4.2](#Tamme), [Milne, example 7.9](#Milne)).


+-- {: .proof}
###### Proof

By the discussion at [category of sheaves -- Epi-/Mono-morphisms](category+of+sheaves#EpiMonoIsomorphisms) we need to show that the left morphism is an injection over any [[étale morphism]] $U_Y \to X$, and that for every element $s \in \mathcal{O}_X$ there exists an [[étale site]] [[covering]] $\{U_i \to X\}$ such that $(-)^p- (-)$ restricts on this to a morphism which hits the restriction of that element.

The first statement is clear, since $s = s^p$ says that $s$ is a constant section, hence in the image of the [[constant sheaf]]
$\mathbb{Z}/p\mathbb{Z}$  and hence for each connected $U_Y \to X$ the left morphism is the inclusion

$$
  \mathbb{Z}/p\mathbb{Z} \hookrightarrow \mathcal{O}_{X'}
$$ 

induced by including the unit [[section]] $e_{X'}$ and its multiples $r e_{X'}$ for $0 \leq r \lt p$. (This uses the "[[freshman's dream]]"-fact that in [[characteristic]] $p$ we have $(a + b)^p = a^p + b^p$).

This is injective by assumption that $X$ is of characteristic $p$.

To show that $(-)^p - (-)$ is an epimorphism of sheaves, it is sufficient to find for each element $s \in \mathcal{O}_X = A$ an [[étale site|étale cover]] $Spec(B) \to Spec(A)$ such that its restriction along this cover is in the image of $(-)^p - (-) \colon B \to B$. The choice

$$
  B \coloneqq A[t]/(t- t^p - s)
$$

by construction has the desired property concerning $s$, the preimage of $s$ is the equivalence class of $t$. 

To see that with this choice $Spec(B) \to Spec(A)$ is indeed an [[étale morphism of schemes]] it is sufficient to observe that it is a [[morphism of finite presentation]] and a [[formally étale morphism]]. The first is true by construction. For the second observe that for a ring homomorphism $B \to T$ the generator $t$ cannot go to a nilpotent element since otherwise $s$ would have to be nilpotent. This implies [[formally étale morphism|formal étaleness]] analogous to  the discussion at [&#233;tale morphism of schemes -- Open immersion is Etale](etale+morphism+of+schemes#OpenImmersionIsEtale).



=--




## Related concepts

* [[étale cohomology]]

* [[Kummer sequence]]

* [[Kummer-Artin-Schreier-Witt exact sequence]]

* [[exponential exact sequence]]

## References

* [[Günter Tamme]], section II 4.2_[[Introduction to Étale Cohomology]]_

* [[James Milne]], example 7.9 of _[[Lectures on Étale Cohomology]]_


[[!redirects Artin-Schreier sequences]]

[[!redirects Artin-Schreier exact sequence]]
[[!redirects Artin-Schreier exact sequences]]

