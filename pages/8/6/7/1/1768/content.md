
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


# Cauchy sequences
* table of contents
{: toc}


## Idea

A _Cauchy sequence_ is an infinite [[sequence]] which ought to [[convergence|converge]] in the sense that successive terms get arbitrarily close together, as they would if they were getting arbitrarily close to a limit.  Among sequences, only Cauchy sequences will converge; in a [[complete space]], all Cauchy sequence converge.


## Definitions

The precise definition varies with the context.


A sequence $(x_i)_i$ of [[real numbers]] is __Cauchy__ if, for every positive number $\epsilon$, almost all terms are within $\epsilon$ of one another.  Explicitly:
$$ \forall \epsilon,\; \exists N,\; \forall i, j \geq N,\; |x_i - x_j| \lt \epsilon .$$


In a [[metric space]], a sequence $(x_i)_i$ is __Cauchy__ under the same condition, now relative to the metric $d$ on that space.  Explicitly:
$$ \forall \epsilon,\; \exists N,\; \forall i, j \geq N,\; d(x_i,x_j) \lt \epsilon .$$

The same definition immediately applies to an extended quasipseudometric space (aka a Lawvere metric space), or anything in between.

In a [[gauge space]], a sequence $(x_i)_i$ is __Cauchy__ if this condition is satisfied for each gauging distance separately.  Explicitly:
$$ \forall d,\; \forall \epsilon,\; \exists N,\; \forall i, j \geq N,\; d(x_i,x_j) \lt \epsilon .$$

In a [[Booij premetric space]], a sequence $(x_i)_i$ is __Cauchy__ if this condition is satisfied for the premetric for all positive rational numbers $\epsilon$.  Explicitly:
$$ \forall \epsilon,\; \exists N,\; \forall i, j \geq N,\; x_i \sim_\epsilon x_j .$$

In a [[uniform space]], a sequence $(x_i)_i$ is __Cauchy__ if an analogous condition is satisfied for each [[entourage]] $U$.  Explicitly:
$$ \forall U,\; \exists N,\; \forall i, j \geq N,; x_i \approx_U x_j .$$

In a [[preuniform space]], a sequence $(x_i)_i$ is __Cauchy__ if this condition is satisfied for each [[preuniformity]] $U$.  Explicitly:
$$ \forall U,\; \exists N,\; \forall i, j \geq N,\; x_i \approx_U x_j .$$

Generalizing both [[Booij premetric spaces]] and [[preuniform spaces]], in a $T$-premetric space with set $T$, a sequence $(x_i)_i$ is __Cauchy__ if this condition is satisfied for each element $U \in T$. Explicitly:
$$ \forall U,\; \exists N,\; \forall i, j \geq N,\; x_i \sim_U x_j .$$

In a [[Cauchy space]], a sequence $(x_i)_i$ is __Cauchy__ if it generates a [[Cauchy filter]].  Explicitly:
$$ \{ A \;|\; \exists N,\; \forall i, j \geq N,\; x_i \in A \} \in \mathcal{C} ,$$
where $\mathcal{C}$ is the collection of [[Cauchy filters]] that defines the structure of the Cauchy space.

All of the above are in fact special cases of this.

## Generalizations

### Multivalued sequences

A [[multivalued function|multivalued]] [[sequence]] on a set $A$ is a function $f:\mathbb{N} \to \mathcal{P}(T)$ such that for every natural number $n \in \mathbb{N}$, $f(n)$ is an [[inhabited]] [[subset]] of $A$. 

A multivalued sequence $x:\mathbb{N} \to \mathcal{P}(\mathbb{R})$ of [[real numbers]] is __Cauchy__ if, for every positive number $\epsilon$, there exist a natural number $N$ such that for all $i, j \geq N$, there exist real numbers $a, b$ such that $x(i)(a)$ and $x(j)(b)$ holds and $\vert a - b \vert \lt \epsilon$. 

In a [[metric space]] $S$, a multivalued sequence $x:\mathbb{N} \to \mathcal{P}(S)$ is __Cauchy__ if, for every positive number $\epsilon$, there exist a natural number $N$ such that for all $i, j \geq N$, there exist elements $a, b \in S$ such that $x(i)(a)$ and $x(j)(b)$ holds and $d(a, b) \lt \epsilon$. 

In a [[gauge space]] $S$, a multivalued sequence $x:\mathbb{N} \to \mathcal{P}(S)$ is __Cauchy__ if, for every positive number $\epsilon$ and every gauge $d:S \times S \to \mathbb{R}_{\geq 0}$, there exist a natural number $N$ such that for all $i, j \geq N$, there exist elements $a, b \in S$ such that $x(i)(a)$ and $x(j)(b)$ holds and $d(a, b) \lt \epsilon$. 

In a [[uniform space]] $S$, a multivalued sequence $x:\mathbb{N} \to \mathcal{P}(S)$ is __Cauchy__ if, for every [[entourage]] $U$, there exist a natural number $N$ such that for all $i, j \geq N$, there exist elements $a, b \in S$ such that $x(i)(a)$ and $x(j)(b)$ holds and $a \approx_U b$. 

### Nets and filters

A [[net]] is a generalization of a sequence; the definitions above serve to define a __Cauchy net__ without any change, other than allowing $(x_i)_i$ to be a net.  This is precisely the structure of a [[Cauchy space]]; instead of defining Cauchy nets in terms of Cauchy filters as above, we may equally well define a Cauchy filter to be a [[proper filter]] whose [[canonical net]] is Cauchy.

Note that in a [[complete space]], every Cauchy net has a limit, not just every Cauchy sequence.  Rather, a space in which every Cauchy sequence converges is called __sequentially complete__ or __[[sequentially Cauchy complete]]__.  Note that a metric space (or even a Lawvere metric space) is in fact complete if it is sequentially complete (although this result is not valid in some weak [[foundations]]); in particular, the [[real line]] $\mathbf{R}$ is complete.

When [[Bill Lawvere]] idenitified Lawvere metric spaces with [[enriched categories]] over the [[closed monoidal category|closed monoidal]] [[poset]] $(\mathbf{R}^+,+)$, he identified Cauchy sequences in such spaces with certain [[adjunctions]] of [[bimodules]], enough so that a metric space would be a Cauchy-[[complete space]] if and only if every adjunction of bimodules is induced by an [[enriched functor]].  Generalising this condition from $(\mathbf{R}^+,+)$ to an arbitrary closed monoidal category, we have the concept of [[Cauchy-complete category]].

### Modulated sequences and nets

One can also consider sequences and nets with a [[modulus of convergence]] $\alpha$ from the positive numbers or the set of [[entourages]] to the [[natural numbers]] or the [[directed set]] of a [[net]]. This is common in [[constructive mathematics]] or in other foundations which do not assume the [[axiom of choice]]. 

A sequence or net $(x_i)_i$ of [[real numbers]] is __modulated Cauchy__ if there exists a [[modulus of convergence]] $\alpha$ for $(x_i)_i$. Explicitly:
$$ \forall \epsilon,\; \forall i, j \geq \alpha(\epsilon),\; |x_i - x_j| \lt \epsilon .$$

In a [[metric space]], a sequence or net $(x_i)_i$ is __modulated Cauchy__ under the same condition, now relative to the metric $d$ on that space.  Explicitly:
$$ \forall \epsilon,\; \forall i, j \geq \alpha(\epsilon),\; d(x_i,x_j) \lt \epsilon .$$

In a [[gauge space]], a sequence or net $(x_i)_i$ is __modulated Cauchy__ if this condition is satisfied for each gauging distance separately.  Explicitly:
$$ \forall d,\; \forall \epsilon,\; \forall i, j \geq \alpha(\epsilon),\; d(x_i,x_j) \lt \epsilon .$$

In a [[uniform space]], a sequence or net $(x_i)_i$ is __modulated Cauchy__ if an analogous condition is satisfied for each [[entourage]] $U$. Explicitly:
$$ \forall U,\; \forall i, j \geq \alpha(U),\; x_i \approx_U x_j .$$

## Related concepts

* [[sequence]], [[net]]
* [[modulus of convergence]]
* [[metric space]], [[gauge space]], [[uniform space]], [[Cauchy space]]
* [[limit of a sequence]], [[limit of a net]]
* [[complete space]]
* [[sequentially complete space]]

## References

* Wikipedia, _[Cauchy sequence](https://en.wikipedia.org/wiki/Cauchy_sequence)_

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects Cauchy sequence]]
[[!redirects Cauchy sequences]]

[[!redirects Cauchy net]]
[[!redirects Cauchy nets]]

[[!redirects multivalued Cauchy sequence]]
[[!redirects multivalued Cauchy sequences]]

[[!redirects modulated Cauchy sequence]]
[[!redirects modulated Cauchy sequences]]

[[!redirects modulated Cauchy net]]
[[!redirects modulated Cauchy nets]]
