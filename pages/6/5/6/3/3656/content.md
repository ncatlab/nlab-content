
#Contents#
* automatic table of contents goes here
{:toc}

## Idea
This page is devoted right now to explain the spectrum condition of the [[Haag-Kastler axioms]], future versions of the page may go into more details of this vast subject.

## Spectrum of Representations of Groups
Let $\mathcal{G}$ be a locally compact, abelian topological group, $\hat \mathcal{G}$ the character group of $\mathcal{G}$, $\mathcal{H}$ a  Hilbert space and $\mathcal{U}$ an unitary representation of $\mathcal{G}$ in the algebra of bounded operators of $\mathcal{H}$.

+-- {: .num_theorem #specmeasure}
* **Theorem**: There is a unique regular spectral measure $\mathcal{P}$ on $\hat \mathcal{G}$ such that:

$$
     \mathcal{U}(g) = \int_{\chi\in\hat \mathcal{G}} \lt g, \chi\gt \mathcal{P}(d\chi) \qquad \forall g \in \mathcal{G}
$$
 =--
The equality holds in the weak sense, i.e. the integral converges in the weak operator topology.
The **spectrum** of $\mathcal{U}(\mathcal{G})$, denoted by $spec\mathcal{U}(\mathcal{G})$, is defined to be the support of this spectral measure $\mathcal{P}$.

### The Case of the Translation Group


## References

The theorem \ref{specmeasure} is theorem 4.44 in the following classic book:

* Folland, Gerald B.: A course in abstract harmonic analysis. CRC Press 1995 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0857.43001&format=complete)).
