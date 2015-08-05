
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Yang--Mills [[field (physics)|field]]_ is the [[gauge theory|gauge field]] of [[Yang-Mills theory]]. 

It is modeled by a cocycle $\hat F \in \mathbf{H}(X, \mathbf{B}U(n)_{conn})$ in differential [[nonabelian cohomology]]. Here $\mathbf{B} U(n)_{conn}$ is the [[moduli stack]] of $U(n)$-[[principal connections]], the [[stackification]] of the [[groupoid of Lie-algebra valued forms]], regarded as a [[groupoid]] [[internal category|internal to]] [[smooth spaces]].

This is usually represented by a [[vector bundle]] [[connection on a bundle|with connection]]. 

As a [[nonabelian cohomology|nonabelian]] [[Čech cohomology|Čech cocycle]] the Yang-Mills field on a space $X$ is represented by

* a [[cover]] $\{U_i \to X\}$

* a collection of $Lie(U(n))$-valued 1-forms  $(A_i \in \Omega^1(U_i, Lie(U(n))))$;

* a collection of $U(n)$-valued smooth functions $(g_{i j} \in C^\infty(U_{i j}, U(n)))$;

* such that on double overlaps 
  $$
    A_j = Ad_{g_{i j}} \circ A_i + g_{i j} g g_{i j}^{-1}
    \,,
  $$

* and such that on triple overlaps
  $$
    g_{i j} g_{j k} = g_{i k}
    \,.
  $$

# Examples #

* For $U(n) = U(1)$ this is the [[electromagnetic field]].

* For $U(n) = SU(2) \times U(1)$ this is the "electroweak field";

* For $U(n) = SU(3) $ this is the strong nuclear force field.


[[!redirects Yang--Mills field]]
[[!redirects Yang–Mills field]]
[[!redirects Yang-Mills fields]]