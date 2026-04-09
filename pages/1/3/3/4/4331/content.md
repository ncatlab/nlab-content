
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


\tableofcontents



## Idea

A __$C^*$-dynamical system__ (or *$C^*$-system*, for short)
is a [[C-star-algebra|$C^\ast algebra$]] [[continuous function|continuously]] [[group action|acted]] upon by 
a [[topological group]] of [[star-algebra|$\ast$]]-[[automorphisms]]. 

In [[quantum mechanics]] and generally in [[AQFT]], where [[quantum observables]] of the theory are [[self-adjoint operators]] of (a [[local net]] of) [[C-star-algebra|$C^\ast$-algebras]], the [[global gauge group]] of the theory is the maximal group of [[unitary operators]] that leave all observables invariant, hence [[algebra of quantum observables]] equipped with this action of the [[global gauge group]] form a $C^*$-system.


## Definition


\begin{definition}

A **$C^*$-system** $(\mathcal{A}, \alpha_G)$ consists of a $C^*$-algebra $\mathcal{A}$, a [[locally compact space|locally compact]] group $G$ and a [[continuous map|continuous]] [[homomorphism]] $\alpha$ of $G$ into the [[group]] $aut(\mathcal{A})$  of $*$-[[automorphisms]] of $\mathcal{A}$ equipped with the [[topology]] of pointwise convergence.

\end{definition}


If the algebra is a [[star-algebra|$star$-algebra]] only, then some authors call it a __$\ast$-system__. 

Sometimes the continuity condition is dropped entirely or replaced by some weaker assumption, therefore one should always check what -- if any -- continuity assumption an author makes.


\begin{definition}

The **fixed point algebra** of a $C^*$-system  $(\mathcal{A}, \alpha_G)$ is $\{ A \in \mathcal{A}: a_g A = A \; \forall \; g \in G  \}$. If the fixed point algebra is trivial then $\alpha_G$ **acts ergodically**. 

\end{definition}

\begin{definition}

A [[state]] $\rho$ of the algebra $\mathcal{A}$ is an **invariant state** if 
$$
  \rho (A) 
    = 
  \rho(\alpha_g A) 
  \; 
  \forall A \in \mathcal{A}, \; \forall g \in G.
$$

\end{definition}


## Properties ##

\begin{lemma}
The [[set]] of [[invariant]] states is [[convex set|convex]], [[weak topology|weak-]]$*$ [[closed subset|closed]] and weak-$*$ [[compact topological space|compact]] (cf. *[[operator topology]]*).
\end{lemma}


## Related entries

* [[net of C-star-systems|net of $C^\ast$ systems]]


## References

* [[Hellmut Baumgärtel]], Manfred Wollenberg; chapter 6 of: *Causal nets of operator algebras --- Mathematical aspects of algebraic quantum field theory*, Mathematische Lehrbücher und Monographien. II. Abteilung: Mathematische Monographien **80**, Akademie Verlag (1992) &lbrack;[zbmath:0749.46038] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0749.46038)&rbrack;

* [[Gert K. Pedersen]]; chapter 6 in: *Pullback and pushout constructions in $C^\ast$-algebra theory*, J. Funct. Analysis __167__ (1999) 243--344 &lbrack;[doi:10.1006/jfan.1999.3456](https://doi.org/10.1006/jfan.1999.3456), [pdf](http://www.math.ru.nl/~mueger/ped2.pdf)&rbrack;


category: operator algebras

[[!redirects C-star-system]]
[[!redirects C-star-systems]]
[[!redirects C-star system]]
[[!redirects C-star systems]]
[[!redirects C-star dynamical systems]]
[[!redirects invariant state]]
