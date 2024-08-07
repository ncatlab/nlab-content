[[!redirects Lagrangian]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For a [[classical mechanics|classical mechanical]] system, the [[equations of motion|laws of motion]] can be expressed in terms of an [[action]] principle: the actual paths must be the (locally) extremal paths of the [[action functional]]. 

In one of the formulations of the classical mechanics, called Lagrangean formalism, every mechanical system is characterized by its configuration space and a single function called Lagrangian which determines the laws of motion (the initial configuration should be given independently).

The **Lagrangian**, Lagrangian function or Lagrangean $L = L(q,\stackrel{\cdot}q,t)$ is a real valued function of the points in [[configuration space]] and their time derivatives (for some sytems also depending on time), such that the corresponding action principle can be expressed as [[Euler-Lagrange equation|Euler-Lagrange equations]]: for all $i$, 

$$
\frac{d}{dt} \left( \frac{\partial L}{\partial \stackrel{\cdot}{q}_i} \right) - \frac{\partial L}{\partial {q}_i}  = 0
$$

Here $q = (q_1,\ldots, q_n)$ is the coordinate in the configuration space. 

For continuum systems satisfying reasonable locality, Lagrangians can be expressed in terms of integrating a local quantity, so-called Lagrangian density. 

## Definition

For $X$ a ([[spacetime]]/[[worldvolume]]) [[smooth manifold]] of [[dimension]] $n$, let $E \to X$ be a [[vector bundle]],
to serve as the _[[field bundle]]_ for the $n$-dimensional [[field theory]] Lagrangian to be defined.

Denote the [[jet bundle]] by $j_\infty E \to X$ and write $\Omega^{\bullet, \bullet}(j_\infty E)$ be the corresponding [[variational bicomplex]].

+-- {: .num_defn}
###### Definition

A **local Lagrangian** on [[field (physics)|fields]] given by the [[field bundle]] $E \to X$ is given by an element

$$
  L \in \Omega^{n,0}(j_\infty E)
  \,,
$$

hence a [[horizontal differential form]] of degree $n$ on the [[jet bundle]] of $E$.

The local Lagrangian itself is the [[pullback of differential forms|pullback]] of this along the [[jet prolongation]] map
$j_\infty \colon \Gamma_X(E) \longrightarrow \Gamma(j_\infty E)$,
hence the [[differential form]]-valued [[functional]] on the 
[[space of sections]] of $E$ given by

$$
  L : (\phi \in \Gamma(E)) \mapsto L(j_\infty \phi) \in \Omega^n(X)
  \,.
$$

The [[integral]] (for [[compact topological space|compact]] $X$)

$$
  \int_X L(j_\infty(-)) \;\colon\; 
  \Gamma(E) \longrightarrow \mathbb{R}
$$

is the corresponding [[local action functional]].

=--

## Related concepts

* [[action functional]]

* [[extended Lagrangian]], 

* [[BV-Lagrangian density]], [[gauge fixing Lagrangian density]]

* traditional [[Lagrangian mechanics]] and [[Hamiltonian mechanics]] are naturally embedding into [[local prequantum field theory]] by the notion of [[prequantized Lagrangian correspondences]]

* [[Lagrangian quantum field theory]]

* [[non-Lagrangian field theory]]

[[!include Hamiltonian and Lagrangian -- table]]


## References

Named after [[Joseph-Louis Lagrange]].

Textbooks:

* [[Garth Warner]]: *Lagrangian Mechanics*, EPrint Collection, University of Washington (2009) &lbrack;[hdl:1773/4606](http://hdl.handle.net/1773/4606), [pdf](https://sites.math.washington.edu//~warner/LM_Warner.pdf), [[WarnerLagrangianMechanics.pdf:file]]&rbrack;


Textbook account in the context of [[gauge theory]]:

* [[Marc Henneaux]], [[Claudio Teitelboim]], §1.1.1 in: _[[Quantization of Gauge Systems]]_, Princeton University Press (1992) &lbrack;[ISBN:9780691037691](https://press.princeton.edu/books/paperback/9780691037691/quantization-of-gauge-systems), [jstor:j.ctv10crg0r](https://www.jstor.org/stable/j.ctv10crg0r)&rbrack;

Discussion in the convenient context of [[smooth sets]]:

* {#GiotopoulosSati23} [[Grigorios Giotopoulos]], [[Hisham Sati]], §3 in: *Field Theory via Higher Geometry I: [[schreiber:Smooth Sets of Fields]]* &lbrack;[arXiv:2312.16301](https://arxiv.org/abs/2312.16301)&rbrack;



See also 

* Wikipedia, *[Lagrangian mechanics](https://en.wikipedia.org/wiki/Lagrangian_mechanics)*

* [[Daniel Freed]], _Lecture 2 of [[Five lectures on supersymmetry]]_


[[!redirects Lagrangean]]
[[!redirects Lagrangian function]]
[[!redirects Lagrangian density]]

[[!redirects Lagrangian mechanics]]

[[!redirects Lagrangians]]

[[!redirects local Lagrangian]]
[[!redirects local Lagrangians]]

[[!redirects Lagrangian densities]]
[[!redirects local Lagrangian density]]
[[!redirects local Lagrangian densities]]
