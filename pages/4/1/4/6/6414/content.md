
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


## Definition

Let $k$ be a [[perfect field]] of [[characteristic]] $p\neq 0$. Let $W$ be the [[ring]] of [[Witt vectors]] over $k$. A **Cartier module** is a pair $(M, f)$ where $M$ is a [[free construction|free]] $W$-[[module]] of finite [[rank]] and $f:M\to M$ is a semi-[[linear map|linear]] [[endomorphism]] in the following sense: $f(a\cdot m)=\phi(a)f(a)$ where $\phi$ is the [[Frobenius map]]. 

Cartier modules form a [[category]] by taking [[morphisms]] to be in the [[Mod|category of W-modules]] that also respect the extra $f$ data.

### Examples

* $(W, \phi)$ is a Cartier module

* If $G$ is a [[p-divisible group]] of height $h$, then the [[Dieudonne module]] $D(G)$ is a free $W$-module of rank $h$. The natural action of Frobenius turns $D(G)$ into a Cartier module.

* If $X$ [[proper map|proper]], [[smooth scheme|smooth]] [[scheme]] over $k$ of dimension $n$, then all $H^m_{crys}(X/W)/torsion $ with the action of pullback by Frobenius $F^*$ is a Cartier module when $m$&lt;$n$.

## Slope Decomposition

Consider the Cartier module $(M, f)$. Let $K$ be the [[fraction field]] of $W$. Define the finite dimensional [[vector space]] $V=M\otimes_W K$. Extend $f$ linearly to $V$. Note that $f$ preserves the $W$-lattice $M$ inside $V$ by construction.

Define $A=K[T]$ to be the noncommutative [[polynomial]] ring with commutative relation $Ta=\phi(a)T$. This allows us to define a left $A$-[[action]] on $V$ by $T\cdot v=f(v)$. 

Define $U_{r,s}$ to be the left $A$-module $A/A\cdot (T^s-p^r)$. This is the canonical $A$-module of pure [[slope]] $r/s$ and multiplicity $s$. It is a $K$-vector space of dimension $s$.

When $r\geq 0$ $T$ preserves the $W$ lattice $W[t]/W[t]\cdot(T^s-p^r)\subset U_{r,s}$. We have that $U_{r,s}$ is simple if and only if $(r,s)=1$. It is a theorem of Dieudonne and Manin that when $k$ is algebraically closed there is a unique choice of integers $r_i, s_i$ with $s_i\geq 1$ such that $r_1/s_1$ &lt; $r_2/s_2$ &lt; $\cdots$ &lt; $r_i/s_i$ where $V$ decomposes as a direct sum $\bigoplus_{i=1}^t V_{r_i/s_i}$ where $V_{r_i/s_i}$ is noncanonically isomorphic as an $A$-module to $U_{r_i, s_i}$. This is called the *slope decomposition* of $V$.

The $r_i/s_i$ are called the [[slope]]s of $V$ with multiplicity $s_i$. Up to noncanonical isomorphism $V$ is completely determined by knowledge of the slopes and multiplicities.

### Examples

* Let $k=\mathbb{F}_q$ with $q=p^a$. Given a Cartier module $(M, F)$, the slopes of $(M\otimes_{W(k)}W(\overline{k}), F)$ are the $p$-adic valuations (chosen so $\nu(q)=1$) of the eigenvalues of the linear endomorphism $F^a$ of $M$, and the multiplicity is the (algebraic) multiplicity of this eigenvalue.

* In the second example above, if $G$ a [[p-divisible group]], then $(D(G), F)$ has all slopes in $[0,1)$.

* In the third example above if $X$ is projective, then since $F_*\circ F^* = p^n$, all the slopes of $H^m_{crys}(X/W)/torsion$ lie in $[0,n]$.






## References

* [[Michael Artin]], [[Barry Mazur]], _Formal Groups Arising from Algebraic Varieties_, [numdam](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663)

* Pierre Berthelot, _Slopes of Frobenius in Crystalline Cohomology_, Proceedings of Symposia in Pure Mathematics Vol 29, 1975.


[[!redirects Cartier modules]]