
#Contents#
* automatic table of contents goes here
{:toc}

# Idea
Spectral measures are an essential tool of [[functional analysis]] on [[Hilbert space]]s. Spectral measures are projection-valued measures and are used to state various forms of [[spectral theorem]]s.

In the following, let $\mathbb{H}$ be a [[Hilbert space]] and $\mathcal{B}(\mathcal{H})$ be the algebra of bounded linear operators on $\mathbb{H}$ and $\mathcal{P}(\mathcal{H})$ the orthogonal projections.

##real spectral measure##
The following paragraphs explain the concept of a spectral measure in the real case, sufficient for [[spectral theorem]]s of [[selfadjoint operator]]s.

###resolution of identity###
Do not confuse this concept with the [[partition of unity]] in [[differential geometry]].

definition: A __resolution of the identity operator__ is a map $E: \mathbb{R} \to \mathcal{P}(\mathcal{H})$ satisfying the following conditions:

1. (**monotony**): For $\lambda_1, \lambda_2 \in \mathbb{R}$ with $\lambda_1 \leq \lambda_2$ we have $E(\lambda_1) \leq E(\lambda_2)$. 

2. (**continuity from above**): for all $\lambda \in \mathbb{R}$ we have $s-\lim_{\epsilon \to 0, \epsilon \gt 0} E(\lambda + \epsilon) = E(\lambda)$.

3. (**boundary condition**): $s-\lim_{\epsilon \to -\infty} E(\lambda) = 0$ and $s-\lim_{\epsilon \to \infty} E(\lambda) = \mathbb{1}$.

If there is a finite $\mu \in \mathbb{R}$ such that $E_{\lambda} = 0$ for all $\lambda \leq \mu$ and $E_{\lambda} = \mathbb{1}$ for all $\lambda \geq \mu$, than the resolution is called **bounded**, otherwise **unbounded**.

###spectral measure and spectral integral###
Let E be a spectral resolution and $I$ be a bounded interval in $\mathbb{R}$. The spectral measure of $I$ with respect to $E$ is given by 
$$
E(J):= \begin{cases}

           E(y-) - E(x)  & \text{for }\quad I=(x,y) \\
           E(y-) - E(x-) & \text{for }\quad I=[x,y) \\
           E(y)  - E(x)  & \text{for }\quad I=(x,y] \\
           E(y)  - E(x-) & \text{for }\quad I=[x,y] \\

        \end{cases}
$$

This allows us to define the integral of a step function $u = \sum_{k=1}^{n} \alpha_k \chi_{I_k} $ with respect to E as

$$
\integral u(\lambda) dE(\lambda) := \sum_{k=1}^{n} \alpha_k E(I_k)
$$

The value of this integral is a bounded operator.

As in conventional measure and integration theory, the integral can be extended from step functions to Borel-measurable functions. In this case one often used notation is
$$
E(u) = \integral u(\lambda) dE(\lambda)
$$
For general function $u, E(u)$ need not be a bounded operator of course, the domain of $E(u)$ is (theorem):
$$
D(E(u)) = \{ f \in \mathcal{H} : \int |u(\lambda)|^2 d\langle E(\lambda)f, f\rangle \lt \infty \}
$$

# Spectrum of Representations of Groups, the SNAG Theorem
The SNAG theorem is necessary to explain the spectrum condition of the [[Haag-Kastler axioms]].

Let $\mathcal{G}$ be a locally compact, abelian topological group, $\hat \mathcal{G}$ the character group of $\mathcal{G}$, $\mathcal{H}$ a  Hilbert space and $\mathcal{U}$ an unitary representation of $\mathcal{G}$ in the algebra of bounded operators of $\mathcal{H}$.
The following theorem is sometimes called (classical) **SNAG** theorem (SNAG = Stone-Naimark-Ambrose-Godement):

+-- {: .num_theorem #specmeasure}
* **Theorem**: There is a unique regular spectral measure $\mathcal{P}$ on $\hat \mathcal{G}$ such that:

$$
     \mathcal{U}(g) = \int_{\chi\in\hat \mathcal{G}} \langle g, \chi\rangle \mathcal{P}(d\chi) \qquad \forall g \in \mathcal{G}
$$
 =--
The equality holds in the weak sense, i.e. the integral converges in the weak operator topology.
The **spectrum** of $\mathcal{U}(\mathcal{G})$, denoted by $spec\mathcal{U}(\mathcal{G})$, is defined to be the support of this spectral measure $\mathcal{P}$.

## The Case of the Translation Group
The groups of translations $\mathcal{T}$ on $\R^n$ is both isomorph to $\R^n$ and to it's own character group, every character is of the form $a \mapsto exp(i \langle a, k\rangle)$ for a fixed $k \in \R^n$. So in this case theorem \ref{specmeasure} becomes:
$$
\mathcal{U}(t) = \int_{k\in \R^n} e^{i \langle t, k\rangle} \mathcal{P}(k) \qquad \forall t \in \mathcal{T}
$$
This allows us to talk about the support of the spectral measure, i.e. the spectrum of $\mathcal{U}(\mathcal{T})$, as a subset of $\R^n$.

## Related entries

* [[projection measure]]

## References

The theorem \ref{specmeasure} is theorem 4.44 in the following classic book:

* [[Gerald B. Folland]], *A course in abstract harmonic analysis*, Studies in Advanced Mathematics. CRC Press (1995) &lbrack;[pdf](https://sv.20file.org/up1/1415_0.pdf), [gBooks](http://books.google.com/books?hl=en&lr=&id=0VwYZI1DypUC)&rbrack;

See also:

* A. A. Kirillov, A. D. Gvi&#353;iani, &#1058;&#1077;&#1086;&#1088;&#1077;&#1084;&#1099; &#1080; &#1079;&#1072;&#1076;&#1072;&#1095;&#1080; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1086;&#1085;&#1072;&#1083;&#1100;&#1085;&#1086;&#1075;&#1086; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;&#1072; (theorems and exercises in functional analysis), Moskva, Nauka 1979, 1988 

[[!redirects spectral measures]]