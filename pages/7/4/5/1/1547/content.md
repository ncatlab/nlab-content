## Idea ##

A **vector bundle** is a vector space which "continuously varies" over a topological space $X$. 

## Definition ## 

Classically, a **vector bundle** over a space $X$ is a [[bundle]] over $X$, i.e., a continuous map $\pi: E \to X$, such that each fiber $\pi^{-1}(x)$ is endowed with a vector space structure, and which is **locally trivial** in the sense that there exists an open cover $U_\alpha$ of $X$ such that the restriction of $\pi$ to $U_\alpha$ is isomorphic to a product bundle with vector space fiber $V$:  

$$\array{
E|_{U_\alpha} := \pi^{-1}(U_\alpha) & \overset{\phi_\alpha}{\to} & U \times V\\
\pi|_{U_\alpha} \searrow & & \swarrow proj\\
& U_\alpha &
}$$ 

where $\phi_\alpha$ is linear on each fiber, i.e., the restriction $\phi_\alpha: \pi_{\alpha}^{-1}(x) \to proj^{-1}(x) = V$ is a linear isomorphism. 

Remarks: 

* In most applications, the ground field of scalars is assumed to be $\mathbb{R}$ or $\mathbb{C}$, although sometimes other fields are allowed, as in the study of algebraic vector bundles. 

* In most cases (as in K-theory), it is implicitly assumed that the vector space $V$ is finite-dimensional. 

* In the context of differential topology or differential geometry, one also assumes that $\pi$ is smooth and that the local bundle isomorphisms $\phi_{\alpha}$ are diffeomorphisms. 

Vector bundles can also be defined via sheaf theory, which permits easy transport to general Grothendieck toposes and contexts where "pointless topology" comes to the fore ([[locale]] theory). Let $Sh(X)$ be the category of (set-theoretic) sheaves on $X$. The sheaf of continuous local sections of the product projection 

$$X \times \mathbb{R} \to X$$ 

forms a local ring object $R$, when interpreted in the [[internal logic]] of $Sh(X)$; it is the [[Dedekind real number object]]. Then, according to a theorem of Richard Swan, in its sheaf-theoretic incarnation a vector bundle is the same thing as a (usually finitely generated) projective $R$-module. 

* A theorem of Kaplansky states "every projective module over a local ring is free". When interpreted in [[sheaf semantics]] ([[Kripke-Joyal semantics]]), the existential quantifier implicit in "free" is interpreted _locally_, so we can consider a vector bundle as a locally free module over the Dedekind reals. 

Much else to be discussed...