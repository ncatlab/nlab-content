[[!redirects Non-commutative global analytic index theory]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## The motivation for the development of non-commutative index theory

There has been various non-commutative index theorems, such as for example, the [[Connes-Moscovisci index theorem]], and the [[Kashiwara-Schapira index theorem]], the [[Arthur-Selberg trace formula]] and the [[Lefschetz trace formula]]. All these index type results should be treated in a uniform setting. This ideas was present in the litterature since a long time (Dold maybe; see the references at the end of this section).

It is not yet clear how one may give an optimal setting for a non-commutative global analytic index theory, but here is what one may try to do: using $\infty$-stacks (e.g., group actions) and formal stacks (foliations), one may try to treat Connes-Moscovisci formulae in a more geometric way. However, if one looks at the $\mathcal{D}$-module setting, for example, one sees a deeply non-commutative situation. This means that the following generalized geometry may be use to define a very general notion of trace and Chern character:

1. First, one may try to work with an $\infty$-topos $X$ together with a sheaf of associative algebras $\mathcal{A}$. The ideas here extend the work of Kashiwara-Schapira and someone else that will be cited later on: one will use the category $BiMod_f(\mathcal{A})$ of modules on $\mathcal{A}$ with good finiteness properties (e.g., coherent good in the case of $\mathcal{D}$-modules; perfect for $\mathcal{O}$-modules on a stack; coherent for $\mathcal{O}$-modules on a usual space, etc...). This category is equipped with two monoidal structure. Let's use the first (left) one, that is given by
$$
(\mathcal{M},\mathcal{N})\mapsto \mathcal{M}\circ\mathcal{N}:=\mathcal{M}\otimes_\mathcal{A}\mathcal{N}.
$$
Remark that one may define the notion of direct sum of $\mathcal{A}$-bimodule, denoted $\oplus$. We thus actually have a bimonoidal category
$$(BiMod_f(\mathcal{A}),\oplus,\circ)$$
that is not symmetric in $\circ$ but symmetric in $\oplus$. This is thus a categorification of an associative ring. One may easily define the notion of a seminorm $|\cdot|$ on such an associative categorical ring $(\Ac,\oplus,\circ)$, following the approach explained in [[generalized global analytic geometry]], and also define a Berkovich spectrum $\mathcal{M}(\mathcal{A},\oplus,\circ)$. This will give a topological space or a $G$-topological space (or an $\infty$-topos, in the &#233;tale topology situation) together with a sheaf $U\mapsto \mathcal{A}(U)$ of seminormed associative categorical rings. Remark that to every multiplicative seminorm on $\mathcal{A}$, one may associate a prime ideal in $\mathcal{A}$. We are thus in a conceptually abstract situation that is very close to the Toen-Vezzosi approach to the Chern character (the monoidal structure is not symmetric).

2. The definition of a categorical trace for objects of $\mathcal{A}$ acting on $\mathcal{A}$ by the left tensor product $\circ$ may be given if $\mathcal{A}$ is equipped with a kind of rigidity structure. In the $\mathcal{D}$-module setting, if we work with bimodules such as $\mathcal{M}\boxtimes D\mathcal{M}$, Kashiwara and Schapira use the notion of trace kernel to define the corresponding class in Hochschild homology. One may try to give a similar construction using rigidity, e.g., the fact that a natural dual for the above bimodule is simply $D\mathcal{M}\omega\boxtimes \omega\mathcal{M}$. The diagonal $\Delta$ seems to play an important role here.

Now a natural constraint on this situation if we look at the Kashiwara and Schapira results is to use the associated Hochschild or negative cyclic homology to define a trace: one must not suppose that $(\mathcal{A},\circ)$ is a rigid monoidal category, because this is not true in the example of elliptic pairs (Atiyah-Singer) (the corresponding trace kernel is given by tensor product of a $\mathcal{D}$-module kernel with a constructible kernel). One should only suppose something weaker, related to the fact that one wants a trace to be defined on cyclic and/or Hochschild cohomology of the situation (a global invariant on $X$, that has a meaning in the Atiyah-Singer situation).

To be continued.
 

## Possible references

Connes-Moscovisci

Kashiwara-Schapira

Selberg

Arthur

Ramados-Tang-Tsen Hochschild-Lefschetz class for $\mathcal{D}$-modules

PoNing Chen, Vasiliy Dolgushev: A Simple Algebraic Proof of the Algebraic Index Theorem

