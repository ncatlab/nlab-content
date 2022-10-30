
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The term _double field theory_ has come to be used for [[field theory]] ([[prequantum field theory]]/[[quantum field theory]]) on [[spacetimes]] which are [[T-folds]] hence for "[[T-duality]]-[[equivariance|equivariant]] field theory".

## T-duality-covariant formalism 
### Para-hermitian geometry
The use of para-hermitian geometry in Double Field Theory was introduced by Izu Vaisman in ([I.Vaisman 2012](#Vaisman)), then by David Svoboda.

\begin{defn} An _almost para-complex manifold_ is a [[manifold]] $M$ equipped with a vector bundle endomorphism $F\in\mathrm{End}(T M)$ such that $F^2=1$ and its $\pm 1$ eigenbundles $T^\pm M$ have same rank. \end{defn}

\begin{defn} The _para-complex projectors_ are the canonical projectors onto $T^\pm M$ defined by $P_\pm = \frac{1}{2}(1\pm F)$ \end{defn} 

\begin{defn} A $\pm$_-para-complex manifold_ is an almost para-complex manifold $(M,F)$ such that $T^\pm M$ of $F$ is Frobenius integrable as a distribution. A _para-complex_ manifold is a manifold that is both $+$-para-complex and $-$-para-complex. \end{defn}

\begin{rmk} A doubled manifold $M$ equipped with the $O(d,d)$-structure $\eta$ carries a natural almost para-hermitian structure. On patches $U$ with coordinates $(x^\mu,\tilde{x}_\mu)$ we have the canonical para-complex structure
$$F\frac{\partial}{\partial x^\mu} = \frac{\partial}{\partial x^\mu},\,\, F\frac{\partial}{\partial \tilde{x}_\mu} = - \frac{\partial}{\partial \tilde{x}_\mu}$$
with eigenbundles 

* $T^+U=\big\langle\frac{\partial}{\partial x^\mu}\big\rangle$,

* $T^-U=\big\langle\frac{\partial}{\partial \tilde{x}_\mu}\big\rangle$,

with associated foliations

* $\mathcal{F}_+=\{x^\mu = \mathrm{const}\}$,

* $\mathcal{F}_-=\{\tilde{x}_\mu = \mathrm{const}\}$. 


In analogy with [[complex geometry]], if we define $\Omega^{r,s}(M)$ as the space of sections of $\Lambda^r(T^+M)\wedge\Lambda^s(T^-M)$, we have the decomposition
$$
    \Omega^k(M)=\bigoplus_{k=r+s}\Omega^{r,s}(M)
$$
Let us call $\pi^{r,s}:\Omega^{r+s}(M)\rightarrow\Omega^{r,s}(M)$ the canonical projector induced by $P_\pm$.

In analogy with complex geometry, there are _para-Dolbeault operators_:

* $\mathrm{d}^+=\pi^{r+1,s}\circ\mathrm{d} : \Omega^{r,s}(M)\longrightarrow \Omega^{r+1,s}(M)$,

* $\mathrm{d}^-=\pi^{r,s+1}\circ\mathrm{d} : \Omega^{r,s}(M)\longrightarrow \Omega^{r,s+1}(M)$.

with properties:

* $\mathrm{d} = \mathrm{d}^+ + \mathrm{d}^-$,

* $(\mathrm{d}^\pm)^2= 0$,

* $\mathrm{d}^+\mathrm{d}^-+\mathrm{d}^-\mathrm{d}^+ =0$.

We can also define [[Lie derivatives]] on the eigenbundles $T^\pm M$ by 
$$
    \mathcal{L}^\pm_{X_\pm}\xi = (\mathrm{d}^\pm\iota_{X_\pm} + \iota_{X_\pm}\mathrm{d}^\pm)\xi
$$
for any vector $X_\pm\in\Gamma(T^\pm M)$ and $\xi\in\Omega^{r,s}(M)$.
\end{rmk}

\begin{defn} An _almost para-hermitian manifold_ is an almost para-complex manifold $M$ equipped with a compatible metric, i.e a symmetric tensor $\eta\in\mathrm{Sym}^2(T M)$ such that $\eta(F\cdot\,,F\cdot\,)=-\eta(\,\cdot\,,\,\cdot\,)$. \end{defn}

\begin{rmk} The contraction with the metric $\eta$ defines two isomorphisms 

$$
  \phi^\pm : T^\pm M \rightarrow (T^\mp M)^\ast
$$

by 

* $\phi^\pm(X_\pm) =  X_\pm^\flat$ and

* $(\phi^\pm)^{-1}(\xi_\pm)=\xi^\sharp$

that map a vector in $T^\pm M$ to a $1$-form in $(T^\mp M)^\ast$ and vice-versa. We used the notation $\flat,\sharp$ for the musical isomorphisms induced by the metric $\eta$ between $T M$ and $T^\ast M$.

This can be used to define a new couple of isomorphisms
$$
    \Phi^\pm : T M \longrightarrow T^\pm M\oplus(T^\pm M)^\ast 
$$
that maps a vector a vector $X=X_++X_-$ with $X_\pm\in T^\pm M$ into $X_+ + X_-^\flat$. \end{rmk}

\begin{defn} A _para-hermitian manifold_ is an almost para-hermitian manifold $(M,\eta,F)$ such that $(M,F)$ is a para-complex manifold. \end{defn}


###Foliated Courant algebroid and spacetime
Given a $+$-para-hermitian manifold $(M,\eta,F)$, consider the triple $\big(T^+ M,[\,\cdot\,,\,\cdot\,]_+,1_{T^+M}\big)$ where 

* the skew-symmetric bracket $[\,\cdot\,,\,\cdot\,]_+:=[\,\cdot\,,\,\cdot\,]|_{T^+ M}$

* the anchor $1_{T^\pm M}:=1_{T M}|_{T^\pm M}$
are the restrictions of Lie bracket and identity of $T M$.

Since $M$ is $+$-para-hermitian we have that $T^+M$ is integrable and therefore it is the tangent bundle $T^+M = T\mathcal{F}_\pm$ of a foliation $\mathcal{F}_+$. This means that this triple is just the tangent Lie algebroid of the foliation $\mathcal{F}_+$:
$$
    \big(T^+ M,[\,\cdot\,,\,\cdot\,]_+,1_{T^+ M}\big) = \big(T\mathcal{F}_+,[\,\cdot\,,\,\cdot\,]_{T\mathcal{F}_+},1_{T\mathcal{F}_+}\big). 
$$
There is a natural Courant algebroid structure on the bundle $T^+ M\oplus(T^+ M)^\ast$ with skew-symmetric pairing 
$$
    [X+\alpha,Y+\beta]_{+} = [X,Y]_+ + \mathcal{L}_X^+\beta -\mathcal{L}_Y^+\alpha +\mathrm{d}_+(\iota_Y\alpha)
$$
and symmetric pairing
$$
    \langle X+\alpha,Y+\beta\rangle_+ = \iota_X\beta + \iota_Y\alpha.
$$

The isomorphism $\Phi^+:T^+ M\oplus (T^+ M)^\ast\rightarrow T^+ M\oplus T^- M = T M$ previously defined induces a Courant algebroid isomorphism and hence a Courant algebroid structure on $T M$. This induces a metric $\eta$ on $M$ and a skew-symmetric pairing on $T M$ by
$$
   [[X_++X_-,Y_++Y_-]]_+ := [X_+,Y_+] + \Big[\mathcal{L}_{X_+}^+ Y_-^\flat -\mathcal{L}_{Y_+}^+ X_-^\flat +\mathrm{d}_+\big(\eta(X_-,Y_+)\big)\Big]^\sharp,
$$
where $X\in T M$ is split in $X_\pm=P_\pm X$. 

\begin{rmk} Since $M$ is assumed $+$-para-hermitian, $T^+ M\oplus (T^+ M)^\ast$ can be written as $T\mathcal{F}_+\oplus T^\ast\mathcal{F}_+$. Therefore we constructed an isomorphism between the Courant algebroid on the whole $T M$ and the generalized tangent bundle $T\mathcal{F}_+\oplus T^\ast\mathcal{F}_+$ of the foliation. In other terms para-hermitian geometry of the doubled manifold $M$ reduces to Generalized Geometry of physical spacetime. \end{rmk}

\begin{rmk} The same argument can be clearly applied to $T^-M$ too. \end{rmk}

###C-bracket
In previous section we assumed that the $+1$-eigenbundle $T^+M$ is integrable. This is equivalent to assuming that there exists a well defined foliation that can be interpreted as the physical spacetime. However it is possible to construct a more general bracket that does not require such an assumption, but only an almost para-complex structure. Therefore it works even when a global physical spacetime foliation is not defined. This is achieved by Vaisman with the definition of _C-bracket_ by using a generalization of the notion of Levi-Civita connection (look ([I.Vaisman 2012](#Vaisman))).

In the special case of an (inetgrable) para-hermitian manifold C-bracket is given by

$$
    [[ X+\alpha,Y+\beta ]]_{\mathrm{C}} = [X,Y] + \mathcal{L}_X\beta -\mathcal{L}_Y\alpha + \mathrm{d}\big(\eta(X+\alpha,Y+\beta)\big) +
    [\alpha,\beta]^\ast + \mathcal{L}^\ast_\alpha Y -\mathcal{L}^\ast_\beta X - \mathrm{d}^\ast\big(\eta(X+\alpha,Y+\beta)\big)
$$

where $[\,\cdot\,,\,\cdot\,]$, $\mathcal{L}_X$ and $\mathrm{d}$ are usual Lie bracket, Lie derivative and differential on $T\mathcal{F}_+$. On the other hand $[\,\cdot\,,\,\cdot\,]^\ast$, $\mathcal{L}^\ast_\alpha$ and $\mathrm{d}^\ast$ are Lie bracket, Lie derivative and differential on $T\mathcal{F}_+^\ast$ induced by the former ones. 

### Analogy with geometric quantization
The analogy between [[geometric quantization]] and DFT was firstly noticed by [[David Berman]]. 

Given a symplectic manifold $(M,\omega)$ there exist couples of lagrangian foliations $\mathcal{F}_+,\mathcal{F}_-$ of $M$ defined by
$$
\forall X,Y\in T\mathcal{F}_\pm, \: \omega(X,Y)=0.
$$
For example for a symplectic space $(\mathbb{R}^{2d},\omega=\mathrm{d}x^\mu\wedge\mathrm{p}_\mu)$ we can have $\mathcal{F}_+ = \{x^\mu = \mathrm{const} \}$ and $\mathcal{F}_-= \{p_\mu = \mathrm{const} \}$. But notice that any symplectic rotation of this choice is a couple of lagrangian foliations that works fine.

Heuristically, in geometrical quantization we make a choice of a couple of lagrangian foliations $\mathcal{F}_\pm$ to "select" a physical spacetime $\mathcal{F}_+$ from the whole symplectic-covariant theory on $M$.

Similarly in DFT, when $M$ is an (integrable) para-hermitian manifold we make a choice of a couple of lagrangian foliations $\mathcal{F}_\pm$ to "select" a physical spacetime $\mathcal{F}_+$ from the whole T-duality-covariant theory on $M$.

## Related concepts

* [[exceptional field theory]]

* [[T-fold]]

## References

The idea of "doubled spacetime geometry" is a variant of the idea of [[T-folds]], due to

* {#Hull06} [[Chris Hull]], _Doubled geometry and T-folds_ JHEP0707:080,2007  ([arXiv:hep-th/0605149](http://arxiv.org/abs/hep-th/0605149))

The coinage of the term "double field theory" for field theory on such doubled geometry goes back to

* [[Chris Hull]], [[Barton Zwiebach]], _Double Field Theory_, JHEP 0909:099,2009 ([arXiv:0904.4664](http://arxiv.org/abs/0904.4664))

Discussion in the context of [[L-infinity algebra]] includes

* [[Andreas Deser]], [[Jim Stasheff]], _Even symplectic supermanifolds and double field theory_, Communications in Mathematical Physics November 2015, Volume 339, Issue 3, pp 1003-1020 ([arXiv:1406.3601](http://arxiv.org/abs/1406.3601))

Discussion of an extended version of Riemannian geometry suitable for the description of double field theory

* [[Andreas Deser]], [[Christian Saemann]], _Extended Riemannian Geometry I: Local Double Field Theory_, ([arXiv:1611.02772](https://arxiv.org/abs/1611.02772))

Discussion about para-hermitian formalism started in

* {#Vaisman} Izu Vaisman, _On the geometry of double field theory_ Journal of Mathematical Physics 53, 033509 (2012)  ([arXiv:1203.0836](https://arxiv.org/abs/1203.0836v1))

