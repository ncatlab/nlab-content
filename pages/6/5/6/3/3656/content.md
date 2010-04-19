
#Contents#
* automatic table of contents goes here
{:toc}

# Idea
Spectral measures are an essential tool of [[functional analysis]] on [[Hilbert space]]s. Spectral measures are a projection-valued measures and are used to state various forms of [[spectral theorem]]s.

In the following, let $\mathbb{H}$ be a [[Hilbert space]] and $\mathcal{B}(\mathcal{H})$ be the algebra of bounded linear operators on $\mathbb{H}$ and $\mathcal{P}(\mathcal{H})$ the orthogonal projections.

##resolution of identity
Do not confuse this concept with the "resolution of identity" in (real) [[differential geometry]].

definition: A resolution of identity is a map $E: \mathbb{R} \to \mathcal{P}(\mathcal{H})$ satisfying the following conditions:

1. (**monotony**): For $\lambda_1, \lambda_2 \in \mathbb{R}$ with $\lambda_1 \leq \lambda_2$ we have $E(\lambda_1) \leq E(\lambda_2)$. 

2. (**continuity from above**): for all $\lambda \in \mathbb{R}$ we have $s-\lim_{\epsilon \to 0, \epsilon \gt 0} E(\lambda + \epsilon) = E(\lambda)$.

3. (**boundary condition**): $s-\lim_{\epsilon \to -\infty} E(\lambda) = 0$ and $s-\lim_{\epsilon \to \infty} E(\lambda) = \mathbb{1}$.



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

## References

The theorem \ref{specmeasure} is theorem 4.44 in the following classic book:

* Folland, Gerald B.: A course in abstract harmonic analysis. CRC Press 1995 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0857.43001&format=complete)).
