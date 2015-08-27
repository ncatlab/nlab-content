
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

An _extension_ of a [[Lie algebra]] $\mathfrak{g}$ is another Lie algebra $\hat {\mathfrak{g}}$ that is equipped with a surjective Lie algebra homomorphism to $\mathfrak{g}$

$$
  \array{
     \hat{\mathfrak{g}}
     \\
     \downarrow
     \\
     \mathfrak{g}
  }
  \,.
$$

For non-tivial extensions, this homomorphism has a [[kernel]] $\mathfrak{a} \hookrightarrow \hat \mathfrak{g}$ , consisting of those elements of $\hat{\mathfrak{g}}$ that map to the zero element in $\mathfrak{g}$. That kernel is a sub-Lie algebra of $\hat{\mathfrak{g}}$ and hence one says that $\hat\mathfrak{g}$ is an extension of $\mathfrak{g}$ by $\mathfrak{a}$.

$$
  \array{
     \mathfrak{a} &\hookrightarrow& \hat{\mathfrak{g}}
     \\
     &&\downarrow
     \\
     && \mathfrak{g}
  }
  \,.
$$

This means equivalently that there is a [[short exact sequence]] of Lie algebras of the form

$$
  0 \to \mathfrak{a} \longrightarrow \hat \mathfrak{g} \longrightarrow \mathfrak{g} \to 0
  \,.
$$


When $\mathfrak{a}$ happens to be abelian, hence when its Lie bracket is trivial, then one speaks of an abelian extension, and when furthermore the Lie bracket of $\hat\mathfrak{g}$ vanishes as soon as already one of its arguments is in $\mathfrak{a}$, then one has a [[central extension]] ($\mathfrak{a}$ is in the [[center]] of $\hat \mathfrak{g}$). 

Central extensions by the [[ground field]] (say $\mathbb{R}$) are equivalently induced by a 2-cocyle $\mu_2$ in the [[Lie algebra cohomology]] of $\mathfrak{g}$ with [[coefficients]] in the [[ground field]], say $\mathbb{R}$, i.e. by linear maps

$$
  \mu_2 \colon \mathfrak{g} \wedge \mathfrak{g} \longrightarrow \mathbb{R}
$$

satisfying some conditions. The corresponding extension of $\mathfrak{g}$ is then, at the level of underlying vector space, the [[direct sum]] $\hat \mathfrak{g} = \mathfrak{g} \oplus \mathbb{R}$, equipped with the Lie bracket given by the formula

$$
  [(x_1,t_1), (x_2,t_2)] = ([x_1,x_2], \mu_2(x_1,x_2))
$$

for all $x_1,x_2 \in \mathfrak{g}$ and $t_1,t_2 \in \mathbb{R}$. The condition on $\mu_2$ to be a 2-cocycle is precisely the condition that this formula satisfies the [[Jacobi identity]].

If one regards all Lie algebras here as being special cases of [[Lie 2-algebras]], then the 2-cocycle $\mu_2$ may itself be thought of as a homomorphism, namely from $\mathfrak{g}$ to the [[line Lie 2-algebra]] $b\mathbb{R}$. With this, then $\hat \mathfrak{g}$ given by the above formula is simply the [[homotopy fiber]] of $\mu_2$, and the whole story comes down to saying that there is a [[homotopy fiber sequence]] of [[L-∞ algebras]] of the form

$$
  \array{
     \mathbb{R} &\hookrightarrow& \hat{\mathfrak{g}}
     \\
     &&\downarrow
     \\
     && \mathfrak{g}
     &\stackrel{\mu_2}{\longrightarrow}& b \mathbb{R}
  }
  \,.
$$

This perspective on Lie algebra extensions makes it evident how the concept generalizes to a concept of [L-∞ algebra extensions](infinity-Lie+algebra+cohomology#Extensions).

Of course extensions need not be central or even abelian. An important class of non-abelian extensions are [[semidirect product Lie algebras]]. These are given by an Lie [[action]] of $\mathfrak{g}$ on $\mathfrak{a}$, hence a [[homomorphism]] $\rho \colon \mathfrak{g}\longrightarrow \mathfrak{der}(\mathfrak{a})$ to the [[derivations]] on $\mathfrak{a}$ and with this the bracket on $\mathfrak{g} \oplus \mathfrak{a}$ is given by the formula

$$
  [(x_1,t_1), (x_2,t_2)]
  =
  ( [x_1,x_2], \;([t_1,t_2] + \rho(x_1)(t_2) - \rho(x_2)(t_1)) )
  \,.
$$


## Definition

A [[short exact sequence]] of [[Lie algebras]] is a [[diagram]]

$$ 0\to \mathfrak{k}
\overset{i}\to \mathfrak{g}\overset{p}\to\mathfrak{b}\to 0$$

where $\mathfrak{k},\mathfrak{g},\mathfrak{b}$ are Lie algebras, $i,p$ are homomorphisms of Lie algebras and the underlying diagram of vector spaces is exact, i.e. $Ker(p)=Im(i)$, $Ker(i)=0$ and $Im(p)=0$. 

We also say that this diagram (and sometimes, loosely speaking, $\mathfrak{g}$ itself) is a **Lie algebra extension** of $\mathfrak{b}$ by the "kernel" $\mathfrak{k}$. 

Lie algebra extensions may be obtained from [[Lie group]] [[group extensions]] via the tangent Lie algebra functor. 

## Properties

### Classification by nonabelian Lie algebra cohomology

We discuss how in general Lie algebra extensions are classified by cocycles in [[nonabelian Lie algebra cohomology]].

Each element $g \in \mathfrak{g}$ defines
a derivative $\phi(g)$ on $\mathfrak{k}$ by $\phi(g)(k) = [g,k]$.
The rule $g \mapsto \phi(g)$ defines a homomorphism of Lie algebras
$\phi : \mathfrak{g} \rightarrow Der(\mathfrak{k})$.
Indeed, 

$$\phi([g_1,g_2])(k) = [[g_1,g_2],k] =
[[g_1,k],g_2] + [g_1,[g_2,k]] = -\phi(g_2)([g_1,k]) + \phi(g_1)([g_2,k])
= [-\phi(g_2)\circ\phi(g_1) + \phi(g_1)\circ\phi(g_2)](k) = [\phi(g_1),\phi(g_2)](k),$$

for all $g_1,g_2 \in \mathfrak{g}$, for all $k \in \mathfrak{k}$.
The restriction $\phi|_{\mathfrak{k}}$ takes
(by definition) values in the Lie subalgebra $Int(\mathfrak{k})$ of inner derivatives of $\mathfrak{k}$.
If $g_1$ and $g_2$ are in the same coset, that is
$g_1 + \mathfrak{k} = g_2 + {\frak k}$,
then there is $k \in \mathfrak{k}$ with $g_1 + k = g_2$ and
such that for all $k' \in \mathfrak{k}$ we have
$\phi(g_1) + \phi(k) = \phi(g_1 + k') = \phi(g_2 + k + k') = \phi(g_2)+\phi(k + k')$ and therefore

$$\array{\phi(g_1) + Int(\mathfrak{k}) &=& \phi(g_1) + \phi(\mathfrak{k})\\ 
&=& \phi(g_1 + \mathfrak{k}) \\
&=& \phi(g_2 + \mathfrak{k}) \\
&=& \phi(g_2) + \phi(\mathfrak{k})\\
&=& \phi(g_2) + Int(\mathfrak{k}).}$$

Thus we obtain a well-defined map $\phi_* : \mathfrak{g}/\mathfrak{k} \to Der(\mathfrak{k})/Int(\mathfrak{k})$.

Choose a $k$-linear section of the projection
$\mathfrak{g} \rightarrow \mathfrak{g}/\mathfrak{k}\cong \mathfrak{b}$
and denote by $\psi$ the composition $\phi \circ \sigma$
where  $\sigma : \mathfrak{g}/\mathfrak{k} = \mathfrak{b} \rightarrow \mathfrak{g}$.
One considers the problem of reconstructing the group $\frak g$ from
the knowledge of $\psi : \mathfrak{g}/\mathfrak{k} \rightarrow Der(\mathfrak{k})$ and $\mathfrak{k}$.
In order to derive the necessary relations we
will identify $\mathfrak{g}$ with $\mathfrak{b} \times \mathfrak{k}$ (as a set).

Indeed, write each element $g \in G$ as
$\sigma(b) + k, b \in \mathfrak{g}/\mathfrak{k}$, $k \in \mathfrak{k}$ by setting $b := [g], k := -\sigma([g]) + g$. Elements $b \in \mathfrak{b}$ and
$k \in \mathfrak{k}$ in that decomposition are unique.
Thus we obtain a bijection $\mathfrak{g} \rightarrow \mathfrak{b} \times \mathfrak{k}$, $g \mapsto ([g], -\sigma([g]) + g )$.
The commutation rule has to be figured out.
If $(b_1,k_1) = g_1$, and $(b_2,k_2) = g_2$, then
\begin{equation}
[g_1,g_2] = [\sigma(b_1) + k_1,\sigma(b_2) + k_2] =
[\sigma(b_1),\sigma(b_2)] + [\sigma(b_1),k_2] - [\sigma(b_2),k_1] +[k_1,k_2].
\label{putkhilie}
\end{equation}

 Now $[\sigma(b_1),\sigma(b_2)] \in [b_1b_2]$ so it can be represented uniquely
in the form $\sigma([b_1,b_2]) + k$ where $k \in \mathfrak{k}$ can be obtained by evaluating the antisymmetric $k$-bilinear form
$\chi : \mathfrak{b} \wedge \mathfrak{b} \rightarrow \mathfrak{k}$ defined by
$\chi(b_1 \wedge b_2) = - \sigma([b_1,b_2]) + [\sigma(b_1),\sigma(b_2)]$
 on $(b_1,b_2)$.
Then formula \eqref{putkhilie} becomes
$$\array{
[g_1,g_2] & = & \sigma([b_1,b_2]) + \chi(b_1\wedge b_2)
+ \phi(\sigma(b_1))(k_2) + \phi(-\sigma(b_2))(k_1) + [k_1,k_2] \\
       & = & \sigma([b_1,b_2]) + \chi(b_1\wedge b_2) + \psi(b_1)(k_2)
        -\psi(b_2)(k_1) + [k_1,k_2].
}$$

so that

\begin{equation}
(b_1,k_1)(b_2,k_2) = ([b_1,b_2],\chi(b_1\wedge b_2) +
        \psi(b_1)(k_2) - \psi(b_2)(k_1) +  [k_1,k_2]).
\label{mrulelie}
\end{equation}

Thus all the information about the commutators is encoded
in functions $\chi : \mathfrak{n} \wedge \mathfrak{b} \rightarrow Der(\mathfrak{k})$
and $\psi : \mathfrak{b} \to Der(\mathfrak{k})$,
without knowledge of $\sigma$.

However, not every pair $(\chi,\psi)$ will
give some commutation rule on $\mathfrak{b} \times k$ satisfying Jacobi identity, and also some different pairs may lead to the isomorphic extensions. 

In order to satisfy the Jacobi identity, this pair needs to form a nonabelian 2-cocycle in the sense of [[nonabelian Lie algebra cohomology]].

## Examples

* The [[Heisenberg Lie algebra]] is an extension of $\mathbb{R}^{2}$, regarded as an abelian Lie algebra, by $\mathbb{R}$ with the corresponding 2-cocycle $\mu_2$ being the canonical commutation relation $\mu_2(q,q)= 0$, $\mu_2(p,p)= 0$, $\mu_2(q,p) = 1$. 

* More generally, the [[Kostant Souriau extension]] exhibits a [[Poisson bracket]] on a [[symplectic manifold]] as an extension of the Lie algebra of [[Hamiltonian vector fields]].

For more discussion putting these two examples in perspective see also at _[quantization -- Motivation from classical mechanics and Lie theory](quantization#MotivationFromClassicalMechanicsAndLieTheory)_.

## Related concepts

* [[central extension]], [[central charge]]

* [[Lie algebra contraction]]

## References

Discussion in the generality of [[super Lie algebras]] includes

* [[Dmitri Alekseevsky]], [[Peter Michor]], Wolfgang Ruppert, _Extensions of super Lie algebras_, J. Lie Theory 15 (2005) No. 1, 125--134 ([arXiv:math/0101190](http://arxiv.org/abs/math/0101190))

See also

* Wikipedia, _[Lie algebra extension](https://en.wikipedia.org/wiki/Lie_algebra_extension)_

[[!redirects Lie algebra extensions]]

[[!redirects extension of Lie algebras]]
[[!redirects extensions of Lie algebras]]