


#Contents#
* table of contents
{:toc}


## Notation

For the following discussion we suppose $\pi: X\to S$ is a [[smooth scheme|smooth]] map of [[scheme]]s. Let $d:\mathcal{O}_X\to \Omega^1_{X/S}$ be the standard differential. It is an integrable [[flat connection|connection]] on $\mathcal{O}_X$. We'll define the (relative) de Rham cohomology to be the [[hyper-derived functor]] pushforward applied to the de Rham complex $\mathbf{R}^q\pi_*(\Omega_{X/S}^\bullet)$. 

We will denote the relative Frobenius map $F: X\to X^{(p)}$ where $X^{(p)}$ is the pullback of the structure map and the absolute Frobenius $F_{ab}: S\to S$, i.e. $X^{(p)}=X\otimes_{\pi^{-1}(\mathcal{O}_S)} \pi^{-1}(\mathcal{O}_S)$. If $\mathcal{A}^\bullet$ is a complex of sheaves, then we denote by $\mathcal{H}^q(\mathcal{A}^\bullet)$ the sheaf that is obtained by taking cohomology with respect to the maps of the complex.


## The Cartier Isomorphism

Suppose that $S$ is an $\mathbb{F}_p$-scheme and $X/S$ is smooth, then there is a unique map of graded $\mathcal{O}_{X^{(p)}}$-algebras $C^{-1}: \Omega^i_{X^{(p)}/S} \stackrel{\sim}{\to} \mathcal{H}^i(F_*\Omega^\bullet_{X/S})$ that satisfies:

$C^{-1}(1)=1$, 

$C^{-1}(\omega\wedge \tau)=C^{-1}(\omega)\wedge C^{-1}(\tau)$ 

and $C^{-1}(d F_{ab}^{-1}(f))=[f^{p-1}d f]$ in $\mathcal{H}^1(F_*\Omega^\bullet_{X/S})$. 

The inverse of this isomorphism is the traditional Cartier isomorphism.

The construction is quite simple. First note that we can immediately reduce to constructing $C^{-1}$ for $i=1$. This is because if $C^{-1}(1)=1$ and $C^{-1}$ is $\mathcal{O}_{X^{(p)}}$-linear it is determined for $i=0$. Likewise, if $C^{-1}$ is determined for $i=1$, then the case $i\geq 1$ is determined from the second property.

Now to construct for $i=1$ we just note that such a map is equivalent to a $(\pi^{(p)})^{-1}$-linear derivation $\mathcal{O}_{X^{(p)}}\to \mathcal{H}^1(F_*\Omega_{X/S}^\bullet)$. This is equivalent to defining a map on local sections $\delta: \mathcal{O}_X\times \pi^{-1}(\mathcal{O}_S)\to \mathcal{H}^1(\Omega_{X/S}^\bullet)$ that is biadditive and satisfies the extra three properties 

$\delta(f s, s')=\delta(f, s^p s')$, 

$\delta(g f, s)=g^p\delta(f,s)+f^p\delta(g,s)$ and 

$\delta(f,1)=[f^{p-1}d f]$.

Now define the map explicitly by $\delta(f,s)=[s f^{p-1}d f]$. It can be checked that this map satisfies all the properties listed and is indeed an isomorphism. This is $C^{-1}$, the inverse of the Cartier isomorphism.

## Relation to the Hodge-de Rham Spectral Sequence

For this discussion let's assume that $X/k$ is proper and smooth. Deligne and Illusie had an insight that the degeneration of the Hodge-de Rham spectral sequence (HdR SS) is closely related to the Cartier isomorphism. Recall that the HdR SS is formed by taking the spectral sequence associated to hypercohomology $E_1^{p,q}=H^q(X, \Omega^p_{X/k})\Rightarrow H^{p+q}_{dR}(X/k)$.

Now notice that if we form the complex $\bigoplus_{i}\Omega^i_{X^{(p)}}[-i]$ which is $\Omega^i$ in degree $i$ and $d=0$ everywhere, then the left side of the inverse Cartier isomorphism is exactly $\mathcal{H}^i(\bigoplus_{i}\Omega^i_{X^{(p)}}[-i])$. Likewise, the right side is $\mathcal{H}^i$ of the complex $F_*\Omega_{X/k}^\bullet$. We can think of both of these complexes as living in $\mathbf{D}(X^{(p)}):=\mathbf{D}^b_{qCoh}(X^{(p)})$.

We can ask whether or not there is some map in the derived category $\phi: \bigoplus_{i}\Omega^i_{X^{(p)}}[-i] \to F_*\Omega_{X/k}^\bullet$ with the property that $\mathcal{H}^i(\phi)=C^{-1}$ for all $i$. It turns out this is a sufficient condition for convergence of the HdR SS. This is just because we get a string of isomorphisms

$\mathbf{H}^n(X, \Omega_X^\bullet)=\mathbf{H}^n(X^{(p)}, F_*\Omega_X^\bullet)\simeq \bigoplus_{i} H^{n-i}(X^{(p)}, \Omega_X^i)$. Thus the dimensions of the $k$-vector spaces at the $E_1$ term match the dimensions at the $E_\infty$ term. Since everything is a $k$-vector space this is all that is needed for degeneration (there can be no non-trivial quotients without dimension decreasing).


## The Generalization to Non-commutative algebra

See Kaledin Non-commutative Hodge-to-de Rham degeneration via the method of Deligne-Illusie <a href="http://arxiv.org/abs/math/0611623">on the arxiv</a>

## References

Nilpotent Connections and the Monodromy Theorem by Nicholas M. Katz

Relevements modulo $p^2$ et decomposition du complexe de de Rham by Deligne and Illusie


=--
