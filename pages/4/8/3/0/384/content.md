A **CW-complex** is a [[nice topological space]] which can be built up inductively, by a process of attaching disks along their boundaries. They are principal objects of interest in algebraic topology; in fact, most spaces of interest to algebraic topologists are [[homotopy equivalence|homotopy equivalent]] to CW-complexes. (And every space is [[homotopy equivalence|weakly homotopy equivalent]] to a CW-complex.) 

##Definition 

A CW-complex is a topological space $X$ which can be presented as the colimit (in [[Top]], or in a category of nice spaces such as [[compactly generated space|compactly generated spaces]]) of spaces $X_n$ (called $n$-skeleta of the presentation) 

$$X_0 \hookrightarrow X_1 \hookrightarrow \ldots \hookrightarrow X_n \hookrightarrow \ldots \qquad (1)$$ 

where each space $X_n$ is the result of attaching copies of the $n$-disk $D^n = \{x \in \mathbb{R}^n: ||x|| \leq 1\}$ along their boundaries $S^{n-1} = \partial D^n$ to $X_{n-1}$. Specifically, $X_0$ (the 0-skeleton) is a discrete space, and each $X_n$ is a pushout in [[Top]] of a diagram of the form 

$$X_{n-1} \stackrel{(f_i)}{\leftarrow} \sqcup_{i \in I} S_{i}^{n-1} \stackrel{\sqcup_i j_i}{\to} \sqcup_{i \in I} D_{i}^n$$ 

where $I$ is some index set, each $j_i: S_{i}^{n-1} \to D_{i}^n$ is the boundary inclusion of a copy of $D^n$, and 
$f_i: S_{i}^{n-1} \to X_{n-1}$ is a continuous map, often called an _attaching map_. The coprojections $X_{n-1} \to X_n$ of these pushouts give the arrows on which diagram (1) is based. 

A "relative" CW-complex $(X, A)$ is similar, except $X_0$ is the disjoint union of $A$ with a discrete space. 

A _finite CW-complex_ is one which admits a presentation in which there are only finitely many attaching maps, and similarly a _countable CW-complex_ is one which admits a presentation with countably many attaching maps. 

Milnor has argued that the category of spaces which are homotopy equivalent to CW-complexes is a convenient category of spaces for algebraic topology. It is not [[cartesian monoidal category|cartesian closed]] (is not closed under formation of function spaces), but Milnor proved that if $Y$ is such a space and $X$ is compact Hausdorff, then $Y^X$ is another such space. Hence many desirable constructions are still available, in particular infinite loop space constructions. 

##References

* J.P. May, A Concise Course in Algebraic Topology, U. Chicago Press, 1999. 

* J. Milnor, On spaces having the homotopy type of a CW-complex, Trans. Amer. Math. Soc. 90 (2) (1959), 272-280.
