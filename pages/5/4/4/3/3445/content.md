

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A locally constant [[sheaf]] $A$ over a [[topological space]] is a sheaf of [[section]]s of a [[covering space]] of $X$: there is a [[cover]] of $X$ by open subsets $\{U_i\}$ such that the [[inverse image|restrictions]] $A|_{U_i}$ are [[constant sheaf|constant sheaves]].

More elegantly said: locally constant sheaves are the sections of [[constant stack]]s:

Let $C = Core(FinSet)\in $ [[Grpd]] be the [[core]] of the [[category]] [[FinSet]] of finite set, let $const_C : Op(X)^{op} \to Grpd$ the presheaf constant on $C$, i.e. the [[functor]] on the [[opposite category]] of the [[category of open subsets]] of $X$ that sends everything to (the identity on) $C$. Then the [[constant stack]] on $C$ is the [[stackification]] $\bar const_C : Op(X)^{op} \to Grpd$.

Write then $X$ for the space $X$ regarded as a sheaf or trivial [[covering space]] over itself, i.e. the [[terminal object]] $X$ in sheaves and hence in stacks over $X$. Then by definition of stackification morphisms

$$
  X \to \bar const_C
$$

are represented by

* an open cover $\{U_i\}$ of $X$;

* over each $U_i$ a choice $F_i \in C$ of object in $C$, hence a finite set in $C$;

* over each double overlap $U_{i j} = U_i \cap U_j$ an morphism $g_{i j} : F_i|_{I_{i j}} \stackrel{\simeq}{\to} F_j|_{U_{i j}}$, hence a bijection of finite sets;

* such that on triple overlaps we have $g_{i k}|_{U_{i j k}}= g_{j k}|_{U_{i j k}}\circ g_{i j}|_{U_{i j k}}$.

Such data clearly is the local data for a [[covering space]] over $X$ with typical fiber any of the $F_i$.

## Definition

Let $(\Delta \dashv \Gamma) : \mathcal{E} \stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}} \mathcal{S}$ be the [[global section]] [[geometric morphism]] of a [[topos]] $\mathcal{E}$ over base $\mathcal{S}$.

Without further assumption on $\mathcal{E}$ we have the following definition.


+-- {: .un_defn}
###### Definition

For $U \to *$ an [[epimorphism]] in $\mathcal{E}$, an [[object]] $E \in \mathcal{E}$ is called **locally constant and split by $U$** if in the [[over category]] $\mathcal{E}/U$ we have an [[isomorphism]]

$$
  E \times U \simeq (\Delta F) \times U
  \,,
$$

for some $S \in $ [[Set]].

An object which is locally constant and $U$-split for _some_ $U$ is called **locally constant**.

A locally constant object $E$ which is in addition an $\Delta Aut(X)$-[[principal bundle]] is called a **[[Galois object]]** .

=--

If $\mathcal{E}$ is a [[locally connected topos]] there is another characterization of locally constant sheaves.

+-- {: .un_defn}
###### Definition

For $C$ and $C$ [[cartesian closed categories]], a [[functor]] $F : C \to D$ that preserves [[product]]s is called a **[[cartesian closed functor]]** if the canonical [[natural transformation]]

$$
  F(B^A) \to (F(B))^{F(A)}
$$ 

(which is the [[adjunct]] of $F(A) \times F(B^A) \simeq F(A \times B^A) \to F(B)$) is an [[isomorphism]].

=--

From the discussion at [[locally connected topos]] we have that

+-- {: .un_prop}
###### Proposition

The [[constant sheaf]]-functor $\Delta : \mathcal{S} \to \mathcal{E}$ is a [[cartesian closed functor]] precisely if $\mathcal{E}$ is a [[locally connected topos]].

=--

In this case the above definition is equivalent to the following one.

+-- {: .un_defn}
###### Definition

Let $\mathcal{E} = Sh(C)$ be a [[locally connected topos]]. Let $p : core(Set^\kappa_*) \to core(Set^\kappa)$ be the [[core]] of the [[generalized universal bundle]] for sets of [[cardinality]] less than some $\kappa$.

A **locally constant $\kappa$-bounded object** in $\mathcal{E}$ is the [[pullback]] of $\Delta(p)$ along a morphism $* \to core(Set^\kappa)$ in the [[2-topos|(2,1)-topos]] $Sh_{(2,1)}(C)$.

=--


+-- {: .un_remark}
###### Remark

This says that locally constant sheaves are the sections of the [[constant stack]] on the [[groupoid]] $core(Set^\kappa)$.

Notice that 

$$
  core(Set \kappa) \simeq \coprod_i \mathbf{B}Aut(F_i) 
  \,,
$$

where the [[coproduct]] is over all [[cardinal]]s smaller than $\kappa$ and where $\mathbf{B}Aut(F_i)$ denotes the [[delooping]] [[groupoid]] of the [[automorphism group]] of the set $F_i$: the [[symmetric group]] on $F_i$.

This means that on each connected component of $\mathcal{E}$ a locally constant sheaf is the $\Delta \rho$-[[associated bundle]] to an $\Delta Aut(F)$-[[principal bundle]] induced by the canonical [[permutation representation]] $\rho : \mathbf{B} Aut(F) \to Set$ of the [[automorphism group]] $Aut(F)$ on $F$.

Specifically for $g : * \to \Delta \mathbf{B} Aut(F) \simeq \mathbf{B} \Delta Aut(F) \hookrightarrow \Delta core(set)$ the classifying morphism of a locally constant sheaf and for $U \to *$ an [[epimorphism]] on which it trivializes, we have a pasting diagram of [[pullback]]s

$$
  \array{
    U \times \Delta F 
    &\to&
    P \times_{\Delta Aut(F) (\Delta (F // Aut(F)))}
    &\to&
    \Delta(F // Aut(F))
    &\to&
    \Delta Set^\kappa
    \\
    \downarrow &&
    \downarrow &&
    \downarrow &&
    \downarrow
    \\
    U &\to& * &\stackrel{g}{\to}& \mathbf{B} \Delta Aut(F)
    &\hookrightarrow&
    \Delta core(Set^\kappa)
  }
  \,,
$$

where $F//Aut(F)$ is the [[action groupoid]], the [[2-colimit]] of $\rho \mathbf{B}Aut(F) \to Grpd$.

=--

## Applications

* Locally constant sheaves are sheaves of sections of [[covering space]]s. 

* When used as coefficient objects in [[cohomology]] they are also called [[local system]]s.

* The [[action]] of the [[fundamental groupoid]] $\Pi_1(X)$ on the fibers of a local system give rise to the notion of [[monodromy]].

* This may be used to define [[homotopy group (of an infinity-stack)|homotopy groups of]] general objects in a [[topos]], and the [[fundamental group of a topos]].

* This is the content of [[Galois theory]].

## Pattern

In sufficiently highly locally connected cases, we have:

* A [[locally constant function]] is a section of a [[constant sheaf]];

* a **locally constant sheaf** is a section of a [[constant stack]];

* a [[locally constant stack]] is a section of (... and so on...)

* a [[locally constant ∞-stack]] is a section of a [[constant ∞-stack]].

A locally constant sheaf / $\infty$-stack is also called a [[local system]].



## References

The definition of _locally constant sheaf_ originates in the notion of _covering projection_

* [[SGA]] 4, Expos&#233; IX, 2.0 .

The topos-theoretic definition is reproduced in the context of a discussion of the notion of [[Galois topos]] as definition 5.1.1 in

* [[Eduardo Dubuc]], _On the representation theory of Galois and Atomic Topoi_ ([arXiv:0208222](http://arxiv.org/abs/math/0208222))

and definition 2.2 in 

* [[Eduardo Dubuc]], _The fundamental progroupoid of a general topos_ ([arXiv:0706.1771](http://arxiv.org/abs/0706.1771))

or as definition 1 in

* [[Michael Barr]], [[Radu Diaconescu]], _On locally simply connected toposes and their fundamental groups_ ([NUMDAM](http://www.numdam.org/item?id=CTGDC_1981__22_3_301_0))
{#BarrDiaconescu}

Discussion of the notions of locally constant sheaves is at 

* [[Michael Shulman]], _Locally constant sheaves_ (<a href="http://golem.ph.utexas.edu/category/2010/11/locally_constant_sheaves.html">blog discussion</a>)
















[[!redirects locally constant sheaves]]

[[!redirects locally constant object]]
[[!redirects locally constant objects]]