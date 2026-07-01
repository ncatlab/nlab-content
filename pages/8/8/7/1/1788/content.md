> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


***


\linebreak

\linebreak


Let $A$ be a ring. Its [[maximal spectrum]], denoted $Spm A$ in EGA (and sometimes $Spec_m A$ by some authors), is the set of the maximal ideals of $A$. As a subset of the topological space $Spec A$, it inherits a topology. The structure sheaf on $Spm A$ is $\mathcal{O}_{Spm A}\coloneqq i^{-1}\mathcal{O}_{Spec A}$, where $i\colon Spm A\hookrightarrow Spec A$ is the inclusion. An *affine ultra-scheme* is a locally ringed space $X$ isomorphic to $(Spm A,\mathcal{O}_{Spm A})$, for some [[Jacobson ring]] $A$ (one also says that $X$ is *ultra-affine*). An **ultra-scheme** is a locally ringed space that has a cover by ultra-affine open subsets.

The mutual quasi-inverse functors that give the equivalence are the following. The functor to the left sends a Jacobson scheme $X$ and sends it to its subset of closed points $X_0$ with the restriction topology and structure sheaf $\mathcal{O}_{X_0}\coloneqq i^{-1}\mathcal{O}_X$, where $i\colon X_0\hookrightarrow X$ is the inclusion. The functor to the right sends an ultra-scheme $U$ to its [[sober topological space|sobrification]] $SU$, with structure sheaf $\mathcal{O}_{SU}\coloneqq i_*\mathcal{O}_U$, where $i:U\to SU$ is the canonical morphism.

* Mark Haiman, *[Varieties as Schemes](https://math.berkeley.edu/~mhaiman/math256-fall18-spring19/varieties-as-schemes-v2.pdf)*

$$
  \left(
  \begin{matrix}
    A & B 
    \\
    0 & C
  \end{matrix}
  \right)
  \left(
  \begin{matrix}
    A^{-1}
    & 
    - A^{-1} B C^{-1}
    \\
    0 & C^{-1}
  \end{matrix}
  \right)
  =
  \begin{matrix}
    1 & 
    \\
  \end{matrix}
$$

\begin{conjecture}
Test conjecture. 
\end{conjecture}


## Idea
 {#Idea}

An ultrascheme is a locally ringed space locally isomorphic to the maximal spectrum of a Jacobson ring. The category of ultraschemes is equivalent to a certain non-full subcategory of schemes. Namely, the Jacobson schemes with the morphisms locally of finite type between them. One can understand this equivalence as a “scheme theory with only closed points.”

Ultraschemes were defined by Grothendieck in EGA IV₃ to show that the category of algebraic varieties in the sense of Serre's [[FAC]] (over an algebraically closed field $k$) is equivalent to that of reduced separated schemes of finite type over $k$. Actually, this latter equivalence is a subequivalence of the former one.

## Definition

Let $A$ be a commutative ring with unit. Its [[maximal spectrum]], denoted $Spm A$ in EGA (and $Spec_m A$ or $MaxSpec A$ by some authors), is the set of maximal ideals of $A$. As a subset of the topological space $Spec A$, the maximal spectrum inherits a topology. The structure sheaf on $Spm A$ is $\mathcal{O}_{Spm A}\coloneqq i^{-1}\mathcal{O}_{Spec A}$, where $i\colon Spm A\hookrightarrow Spec A$ is the inclusion. An **affine ultra-scheme** is a locally ringed space $X$ isomorphic to $(Spm A,\mathcal{O}_{Spm A})$, for some [[Jacobson ring]] $A$ (one also says that $X$ is **ultra-affine**). An **ultra-scheme** is a locally ringed space that has a cover by ultra-affine open subsets. Every ultra-scheme is a [[accessible topological space|T₁ topological space]].

A morphism of ultra-schemes $f:X\to Y$ is a morphism of locally ringed spaces that is “locally of finite type” in the following sense: every point in $X$ has an ultra-affine open neighborhood $U\subset X$ for which there is an ultra-affine open neighborhood $V\subseteq Y$ such that $f(U)\subseteq V$ and $\Gamma(\mathcal{O}_Y,V)\to\Gamma(\mathcal{O}_X,U)$ is a morphism of rings of finite type.

## Equivalence of categories with schemes

+-- {: .num_theorem}
###### Theorem

(EGA IV, 10.9.6)

The category of ultra-schemes is equivalent to the category of Jacobson schemes with all morphisms that are locally of finite type between them.
=--

The mutual quasi-inverse functors that give the equivalence are the following. The functor to the left sends a Jacobson scheme $X$ to its subset of closed points $X_0$ with the restriction topology and structure sheaf $\mathcal{O}_{X_0}\coloneqq i^{-1}\mathcal{O}_X$, where $i\colon X_0\hookrightarrow X$ is the inclusion. The functor to the right sends an ultra-scheme $U$ to its [[sober topological space|sobrification]] $S U$ (see also EGA I, 1971 ed., p. 68, or [Tag 0A2N](https://stacks.math.columbia.edu/tag/0A2N)) with structure sheaf $\mathcal{O}_{S U}\coloneqq i_*\mathcal{O}_U$, where $i:U\to S U$ is the canonical morphism. This latter functor, $U\maspto S U$, is called the *schematization functor*.

Let $i:X'\to X$ be a morphism of locally ringed spaces that is isomorphic to a morphism of the form $X_0\hookrightarrow X$, where $X$ is a scheme, or $U\hookrightarrow S U$, where $U$ is an ultra-scheme. The morphism $i:X'\to X$ satisfies the following universal property: Given any scheme $Y$ and morphism of locally ringed spaces $f':X'\to Y$, there exists a unique morphism of schemes $f:X\to Y$ such that $f\circ i=f'$ ([Guisado Villalgordo, Lemma 2.28](#GuisadoVillalgordo)). In other words, we have a [[relative adjoint functor|relative adjunction]]: the schematization functor is left adjoint to the forgetful $R\colon JacSch_{flt}\to LRS$, relative to the forgetful $J\colon UltSch\to LRS$. Here, $UltSch$, $LRS$ and $JacSch_{flt}$ denote respectively the categories of ultra-schemes, that of locally ringed spaces and that of Jacobson schemes with locally of finite type morphisms. The morphism $X'\to X$ is then interpreted as the unit of this relative adjunction.

Given an algebraically closed field $k$, a **(pre)variety over $k$ in the sense of [[FAC]]** (without the quasi-compactness restriction) is essentially the same as a (separated) reduced ultra-scheme over $Spec k=Spm k$ (an ultra-scheme $U$ is separated or reduced if the scheme $S U$ is). Morphisms of (pre)varieties are always over $Spm k$. The equivalence from the theorem restricts to an equivalence between (pre)varieties in the sense of [[FAC]] and (separated) reduced schemes locally of finite type over $Spec k$.

## References  
 {#References}

The original definition (with the name *ultra-préschéma*) appeared in section 10.9 of:

* {#EGAIV3} Alexander Grothendieck, *&#201;tude locale des sch&#233;mas et des morphismes de sch&#233;mas* (Troisi&#232;me partie) Inst. Hautes &#201;tudes Sci. Publ. Math. 28 (1966), 5&#8211;255. ([numdam:PMIHES_1966__28__5_0/](http://www.numdam.org/item/PMIHES_1966__28__5_0/))

They were later renamed to *ultra-schémas* in the Appendix of:

* {#EGAInew} Alexander Grothendieck, *Éléments de Géométrie Algébrique I*. (2nd ed.) Grundlehren der Mathematischen Wissenschaften (1971). 166. Springer-Verlag.

Ultra-schemes are considered in Chapter 5 of:

* Yves Diers, *Categories of Commutative Algebras*, Oxford University Press ([https://doi.org/10.1093/oso/9780198535867.001.0001](https://doi.org/10.1093/oso/9780198535867.001.0001))

See also:

* {#GuisadoVillalgordo} Elías Guisado Villalgordo, *[The Classical-Schematic Equivalence](https://eliasguisado.wordpress.com/wp-content/uploads/2025/09/the_classical_schematic_equivalence.pdf)*

* Mark Haiman, *[Varieties as Schemes](https://math.berkeley.edu/~mhaiman/math256-fall18-spring19/varieties-as-schemes-v2.pdf)*

* _Secret blogging seminar_: [algebraic geometry without prime ideals](http://sbseminar.wordpress.com/2009/08/06/algebraic-geometry-without-prime-ideals).


[[Notation]]