## Definition

Let either

* $G$ be a Hausdorff [[topological group]] and $F$ either the field of real or complex numbers or

* $G$ be a linear algebraic group over an infinite field $F$ .

Then an $F$-valued representative function on $G$ is $F$-valued function which arises in the form $t\circ\rho$ where $\rho:G\to End V$ is a representation of $G$ on a _finite dimensional_ $F$-vector space and $t:End V\to F$ a linear functional. 

In the (Hausdorff) topological group case the representative function is automatically continuous and in the algebraic case it is automatically a regular function.

On the other hand if we assume that a function $f:G\to F$ is continuous or respectively regular then it is a representative function iff

* all left translates $L_g f : h\mapsto f(h g)$ where $g\in G$ form a finite dimensional $F$-vector space

what is true iff

* all right translates $R_g f : h\mapsto f(g h)$ where $g\in G$ form a finite dimensional $F$-vector space

The set of all representative functions on $G$ is a Hopf $F$-algebra. 

[Hochschild1971](#Hochschild1971) If $G$ is an arbitrary monoid with multiplication $m:G\times G\to G$ then $m$ induces a map $m^*:Fun(G,k)\to Fun(G\times G,k)$, $m^*(f):f\mapsto f\circ m$. We say that $f\in Fun(G,k)$ is representative if $m^*(f)$ is in the image of the canonical map $Fun(G,k)\otimes Fun(G,k)\hookrightarrow Fun(G\times G,k)$. Equivalently, $f$ is representative if the span of all functions $g\cdot f : h\mapsto f(h\cdot g)$ is finite dimensional. It follows then that $m^*(f)$ is in fact in (the image of) $R(G)\otimes R(G)$ where $R(G)$ is the space of all representative functions on $G$. 

## Relations to other spaces of functions on a group

Let $G$ be an algebraic subgroup of $GL(d,k)$. The Hopf algebra of regular ("coordinate") functions $\mathcal{O}(G)$ is a finitely generated subHopf algebra of the Hopf algebra of continuous representative functions on $G$, [CartierHopf](#CartierHopf).

[[Peter-Weyl theorem]] says that the representative functions on a compact topological group form a dense subspace of the space of all continuous functions.

## Literature

Related entries include [[Tannaka duality]], [[locally compact topological group]], [[Hopf algebra]], [[harmonic analysis]], [[representation theory]], [[linear algebraic group]], [[distribution on an affine algebraic group]]

* G. Hochschild,  G. D. Mostow, _Representations and representative functions of Lie groups_, Annals of Mathematics, Second ser. 66 (1957) 495--542 [jstor](https://www.jstor.org/stable/1969906) [MR0098796](https://www.ams.org/mathscinet-getitem?mr=0098796)

* {#CartierHopf} [[Pierre Cartier]], _A primer of Hopf algebras_, Frontiers in number theory, physics, and geometry II, 537--615, Springer 2007.; preprint IH\'ES 2006/40 [pdf](http://preprints.ihes.fr/2006/M/M-06-40.pdf) 

* J. C. Jantzen, Representations of algebraic groups, Acad. Press 1987 (Pure and Appl. Math. vol 131); 2nd edition AMS Math. Surveys and Monog. 107 (2003; reprinted 2007)

* A. Derighetti, _Representative functions on topological groups_, Comm. Math. Helv. __44__:1 (1969) 476--483

* {#Hochschild1971} G. Hochschild, _Introduction to algebraic group schemes_, 1971

[[!redirects representative functions]]