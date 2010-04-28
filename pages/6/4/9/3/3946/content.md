#Contents#
* automatic table of contents goes here
{:toc}

#Idea
This page is about the concept of a wavefront set of generalized functions like [[hyperfunctions]] in the context of [[microlocal analysis]].
The wavefront set is used to further classify the kind of singularity that a generalized function exhibits in a point.

#Definition

##motivation
The definition of wavefront sets is motivated by a version of a [[Paley-Wiener]] theorem that characterizes smooth compactly supported functions ($\mathbb{R}^n \to \mathbb{R}$) by a growth condition on their [[Fourier transform]] $\mathcal{F}$:

* theorem (Paley-Wiener for $C^{\infty}_0$): The vector space of smooth compactly supported functions is (algebraically and topologically) isomorph, via the [[Fourier transform]], to the space of entire functions $F$ which satisfy the following estimate: there is a positive constant $B$ such that for every integer $n \gt 0$ there is a constant $C_n$ such that:
$$ 
      F(z) \le C_n (1 + |z|)^{-n} \exp{ (B \; |\operatorname{Im}(z)|)}
$$ 

##smoothness
We call a smooth compactly supported function that is identical $1$ in a neighbourhood of a point $x_0$ a **cutoff** function at $x_0$.
Let $U \subset \mathbb{R}$ be open, we identify the [[cotangent bundle]] of $U$ with $U \times \mathbb{R}^n$. A subset of $U \times \mathbb{R}^n$ is said to be **conic** if it stable under the transformation
$$
    (x, \zeta) \mapsto (x, \rho \zeta) \quad \text{with} \; \rho \gt 0
$$

* definition: Let $f$ be a distribution and $(x_0, \zeta_0)$ with $\zeta_0 \neq 0$ be a point of the cotangent bundle of $U$. f is **smooth** in $(x_0, \zeta_0)$ if there is a cutoff function $\chi$ in $x_0$ and an open cone $\Gamma_0$ in $\mathbb{R}^n$ containing $\zeta_0$ such that for every $m \gt 0$ there is a nonnegative constant $C_m$ such that for all $\zeta \in \Gamma_0$:
$$
\| \mathcal{F}(\chi f) (\zeta)   \| \le C_m (1 + \| \zeta \|)^{-m}
$$ 
where $\mathcal{F}(\chi f)$ is the [[Fourier transform]] (of the variable $\zeta$) of the function $\chi f$ (of the variable $x$).

* definition: A distribution $f$ is smooth in a conic subset $\Gamma$ of the $cotangent bundle$ of $U$ if $f$ is smooth in a neighbourhood of every point in $\Gamma$.

##wavefront set
Let $U \subseteq \mathbb{R}^n$ be an open subset, $T^* U$ its cotangent bundle and $f$ be a distribution on $U$. The complement of the union of all conic subsets of $T^* U$ where $f$ is smooth is the **wavefront set $WF(f)$**.

[[!redirects wavefront sets]]