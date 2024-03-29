
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
#### Topos Theory
+--{: .hide}
[[!include type theory - contents]]
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects theory of divisible abelian groups]]
[[!redirects theory of torsion-free abelian groups]]
[[!redirects theory of torsion abelian groups]]
[[!redirects theory of ordered abelian groups]]

##Idea##
The _theory of abelian groups_ $T$ is the logical [[theory]] whose models in a [[cartesian category]] are the [[abelian group]] objects.

##Definition##
The _theory of abelian groups_ $T$ is the theory over the signature with one sort $X$, one constant $0$, two function symbols $+$ (of sort $X\times X\to X$) and $-$ (of sort $X\to X$) and equality with axioms:

* $\top\vdash_x x+0=x \quad$
* $\top\vdash_{x,y,z} x+(y+z)=(x+y)+z\quad$,
* $\top\vdash_x  x+(-x)=0\quad$.
* $\top\vdash_{x,y} x+y=y+x\quad$.

The theory of abelian groups is [[algebraic theory|algebraic]]. In the following we list some extensions that use increasingly stronger fragments of geometric logic.

## Extensions of the theory of abelian groups

The **theory of torsion-free abelian groups** $T^\infty$ results from $T$ by addition of the following axioms:

* For all $n\geq 2$: $((nx=0))\vdash_x (x=0))\quad$.

The resulting theory is a Horn theory.

The **theory of divisible abelian groups** $T^\backslash$ results from $T$ by addition of the following regular axioms:

* For all $n\geq 2$: $\top\vdash_x (\exists y) (ny=x)\quad$.

The **theory of divisible torsion-free abelian groups** $T^{\backslash\infty}$ results from $T^\backslash$ by adding the above axioms for torsion-freeness. The resulting theory is cartesian.

The **theory of torsion abelian groups** $T^~$ is an infinitary geometric theory resulting from $T$ by addition of:

* $\top\vdash_x \bigvee_{n\geq 2} (nx=0)\quad$.

##Related concepts##

* [[abelian group]]

* [[torsion]]

* [[geometric theory]]

* [[theory of objects]]

* [[theory of decidable objects]]

##References##

* [[Peter Johnstone]], _Sketches of an Elephant II_, Oxford UP 2002. pp.812-815.