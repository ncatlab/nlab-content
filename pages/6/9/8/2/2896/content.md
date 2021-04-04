
> This page meant to recall the proof of the local recognition of [[Hurewicz fibrations]] (see [there](Hurewicz+fibration#LocalRecognition)). But it didn't and doesn't.

Let $\pi: E \to B$ be a [[principal bundle|principal]] $G$-[[fiber bundle]] which has a [[numerable cover]] (this condition obtains if for example $B$ is [[paracompact space|paracompact]]). Suppose given a commutative diagram in [[Top]]: 

$$\array{
X & \overset{f}{\to} & E \\
i_0 \downarrow & & \downarrow \pi \\
X \times I & \underset{\phi}{\to} & B
}$$ 

where $i_0$ is the composite inclusion $X \cong X \times \{0\} \hookrightarrow X \times I$. We are trying to show that $\phi$ lifts through $\pi$. 

As I recall, the trick proceeds by considering the bundle 

$$\array{
(\phi_0)^*E \times (-\infty, 0] \cup \phi^* E \cup (\phi_1)^* E \times [1, \infty) \\
\downarrow \\
(X \times (-\infty, 0]) \cup (X \times I) \cup (X \times [1, \infty)
}$$ 

where the base is $X \times \mathbb{R}$ and $\phi_t$ is the restriction of $\phi$ along $X \times \{t\} \hookrightarrow X \times I$, and then one constructs a bundle [[lifting]] of the homeomorphism 

$$X \times \mathbb{R} \to X \times \mathbb{R}: (x, t) \mapsto (x, t + 1)$$ 

This bundle lifting is "the slide". Now the bundle is [[trivial bundle|trivial]] over $X \times [-1, 0]$ (see below), so it has a [[section]], and one transports this section along the slide to give a section $\sigma$ over the part 

$$\array{
\phi^* E\\
\downarrow \\
X \times [0, 1]
}$$ 

and then the composition 

$$X \times I \overset{\sigma}{\to} \phi^* E \to E$$ 

gives the desired homotopy [[lifting]]. 

To see that the bundle restricted over $X \times (-\infty, 0]$ is trivial, we just need to check that $(\phi_0)^* E$ is trivial over $X$. However, by the original commutative square, $\phi_0$ equals the composite 

$$X \overset{f}{\to} E \overset{\pi}{\to} B$$ 

and already $\pi^* E$ is trivial (over $E$) essentially because $\pi$ is a $G$-[[torsor]]: there is a bundle isomorphism 

$$\pi^* E \cong E \times_B E \to E \times G$$ 

over $E$. 

The construction of the slide is where [[transfinite composition]] comes in. The details are at this moment a little hazy, but the rough idea is to construct a [[partition of unity]] $\rho_\alpha$ subordinate to the pulled back (locally finite) numerable cover $U_\alpha$ of $X \times I$. One is supposed to [[well-ordering theorem|well-order]] the $\alpha$, and then transfinitely compose a bunch of mini-slides over $(x, t) \mapsto (x, t + \rho_{\alpha}(x))$. The transfinite composition is well-defined on the fiber over any $x$ because the arrows in the composite are non-identity only for those $U_\alpha$ which contain $x$, and there are only finitely many of these by local finiteness. 

To be continued. 
    

