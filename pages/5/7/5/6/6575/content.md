
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Many important special cases of [[classical mechanics]] involve physical systems whose [[configuration space]] is a [[Lie group]], for instance [[rigid body dynamics]] but also (for infinite-dimensional Lie groups) [[fluid dynamics]].

All these systems have special properties, notably they are formall [[integrable system]]s.

## Details

Let $G$ be a [[Lie group]]. Write $\mathfrak{g}$ for its [[Lie algebra]]. 

Choose a [[Riemannian metric]] 

$$
  \langle -,-\rangle \in Sym^2_{C^\infty(G)} \Gamma(T G) 
$$

on $G$ which is [[left invariant]].

On the [[tangent bundle]] $T G$ this induces the [[Hamiltonian]]

$$
  H : (v \in T G) \mapsto \frac{1}{2}\langle v,v\rangle
  \,.
$$



This is now also called the [[Euler-Arnold equation]].

## Examples

* For $G = SO(n)$ the [[special orthogonal group]] the above yields is [[rigid body dynamics]]. The left invariant metric $\langle -,-\rangle$ is the [[moment of inertia]] of the body.

* For $G$ the infinite-dimensional Lie group of [[volume]]-preserving [[diffeomorphism]] of a [[compact space|compact]] [[smooth manifold]], the above yields is Euler's equations of [[hydrodynamics]].

## Related concepts

* [[Euler-Arnold equation]]

## References

The original influential article is 

* [[Vladimir Arnol'd]], _Sur la g&#233;om&#233;trie diff&#233;rentielle des groupes de Lie de dimension infinie et ses applications &#224; l'hydrodynamique des fluides parfaits._ Ann. Inst. Fourier (Grenoble) 16 (1966) fasc. 1, 319&#8211;361. ([MathSciNet](http://www.ams.org/mathscinet-getitem?mr=202082))

A standard textbook reference is section 4.4 of 

* [[Ralph Abraham]], [[Jerrold Marsden]], _[[Foundations of Mechanics]]_ 

[[!redirects Hamiltonian mechanics on Lie groups]]
[[!redirects dynamics on Lie groups]]