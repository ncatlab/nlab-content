
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents 
{: toc}

## Idea

A _group object_ in a [[cartesian category|cartesian]] [[category]] $C$ is a [[group]] [[internalization|internal]] to $C$ (see at *[[internalization]]* for more on the general idea).

Given a non-cartesian [[monoidal category]] one can still make sense of group objects in the [[formal duality|dual]] guise of [[Hopf monoids]], see there for more and see Rem. \ref{GroupObjectsInGeneralMonoidalCategories} below.

## Definition 

### In terms of internal group objects

\begin{definition}
\label{GroupObjectInCartesianCategory}
**(group object in [[cartesian monoidal category]])**
\linebreak
A **group object** or **internal group** [[internalization|internal to]] a category $\mathcal{C}$ with [[finite products]] (binary [[Cartesian products]] and a [[terminal object]] $\ast$) is 

* an [[object]] $G$ in $\mathcal{C}$ 

* and [[morphisms]] in $\mathcal{C}$ as follows:

  * [[neutral element]]: 

    $\mathrm{e} \,\colon\,  \ast \to G$

  * [[inverse elements]]:

    $(-)^{-1} \,\colon\, G\to G$

  * [[binary operation]] $m \colon G\times G \to G$,

such that the following [[commuting diagram|diagrams commute]]:

$$
\array{
  G\times G\times G 
  & \stackrel{id\times m}{\longrightarrow} 
  & 
  G\times G
  \\
  {}^{
    \mathllap{
    m\times id
    }
  }
  \big\downarrow && \big\downarrow m 
  \\
  G\times G & \stackrel{m}{\longrightarrow} & G
}
$$
(expressing the fact multiplication is associative),
$$
\array{
  G 
  & \stackrel{(\mathrm{e},id)}{\longrightarrow} 
  & G\times G
  \\
  {}^{\mathllap{(\id,\mathrm{e})}}
  \big\downarrow 
  &\underset{\id}{\searrow}& 
  \big\downarrow m 
  \\
  G\times G & \underset{m}{\longrightarrow} &G
}
$$
(telling us that the [[neutral element]] is a left and right [[unit element]]), and
$$
\array{
G 
  & 
   \overset{
     ((-)^{-1},id)
   }
   {\longrightarrow} 
   & 
   G\times G
   \\
   {}^{
     \mathllap{
       (id,(-)^{-1})
     }
   }
   \big\downarrow 
   & 
   \underset{id}{\searrow}
   & 
   \big\downarrow m 
   \\
   G\times G 
   & 
   \stackrel{m}{\longrightarrow} 
   &
   G
}
$$
(telling us that the inverse map really does take an [[inverse element|inverse]]).
\end{definition}

\begin{remark}
\label{UseOfDiagonalMorphism}
The [[associativity law]] technically factors through the [[isomorphisms]] between $(G\times G)\times G$ and $G\times (G\times G)$. 

The [[pairing]] $(f,g)$ denotes $(f\times g)\circ\Delta$ where $\Delta$ is a [[diagonal morphism]].
\end{remark}

\begin{remark}
Even if $C$ doesn\'t have *all* binary products, as long as products with $G$ (and the terminal object $*$) exist, then one can still speak of a group object $G$ in $\mathcal{C}$, as above.
\end{remark}

\begin{remark}
\label{GroupObjectsInGeneralMonoidalCategories}
**(group objects in general monoidal categories: [[Hopf monoids]])**
\linebreak

Notice that the use of [[diagonal maps]] (Rem. \ref{UseOfDiagonalMorphism}) in Def. \ref{GroupObjectInCartesianCategory} precludes direct generalization of this definition of group objects to non-[[cartesian monoidal category|cartesian]] [[monoidal categories]], where such maps in general do not exist.

Hence, while the [[underlying]] [[monoid object]] may generally be defined in any [[monoidal category]], the internal formulation of existence of [[inverse elements]] requires [[extra structure]], such as that of a compatible [[comonoid object]]-[[structure]] to substitute for the missing [[diagonal maps]].

Given this, inverses may be encoded by an *[[antipode]]* map and the resulting "monoidal group objects" are known as *[[Hopf monoids]]*. These subsume and generalize *[[Hopf algebras]]*, which are widely studied, for instance in their role as [[quantum groups]].
\end{remark}

### In terms of presheaves of groups
 {#InTermsOfPresheavesOfGroups}

+-- {: .num_prop}
###### Proposition

Given a [[cartesian monoidal category]] $\mathcal{C}$, the category of internal groups in $\mathcal{C}$ (in the sense of Def. \ref{GroupObjectInCartesianCategory}) is [[equivalence of categories|equivalent]] to the [[full subcategory]] of the category of [[presheaves]] of [[groups]] $Grp^{C^{op}}$ on $C$, spanned by those presheaves whose underlying set part in $Set^{C^{op}}$ is [[representable functor|representable]]. 

=--

This is a special case of the general theory of _[[structures in presheaf toposes]]_. 

It means that the [[forgetful functor]] from the [[functor category]] $Func\big(\mathcal{C}^{op}, Grp\big)$ to the [[presheaf category]] $Func\big(\mathcal{C}^{op}, Set\big)$ (obtained by composing with the [[forgetful functor]] [[Grp]] $\to$ [[Set]]) creates representable group objects from  representable objects. 

We unwind how this works:

An object $G$ in $\mathcal{C}$ equipped with internal group structure is identified equivalently with a [[diagram]] of [[functors]] of the form

\[
  \label{PresheafWithValuesInGroups}
  \array{
    && Grp
    \\
    & \mathllap{{}^{(G,\cdot)}}\nearrow & \big\downarrow
    \\
    \mathcal{C}^{op} &\underset{y(G)}{\longrightarrow}& Set
  }
  \,,
\]

where $\mathcal{C}^{op}$ is the [[opposite category]] of $C$, [[Grp]] is the category of [[groups]] with [[group homomorphisms]] between them, and [[Set]] is the category of [[sets]] with [[maps]]/[[functions]] between them. Finally,

$$
  \array{
    y \colon & C &\xhookrightarrow{\phantom{--}}& PSh(C)
    \\
    & G &\mapsto& Hom_C(-,G)
  }
$$

is the [[Yoneda embedding]] of $\mathcal{C}$ into its [[category of presheaves]] $PSh(C) \,\coloneqq\, Func(C^{op}, Set)$, which sends each [[object]] $G$ to the [[representable presheaf]] that it represents.

Since the [[Yoneda embedding]] is [[fully faithful functor|fully faithful]], it is natural to leave it notationally implicit and to write $G(S)$ (for $S \in \mathcal{C}$) as shorthand for

$$
  G(S) \coloneqq  y(G)(S) \coloneqq  Hom_C(S,G)
  \,.
$$

(This a also referred to as "$G$ seen at stage $S$", or similar.)

Now, the lift (eq:PresheafWithValuesInGroups) of such a presheaf of sets to a presheaf of groups equips for each object $S \in \mathcal{C}$ the set $G(S) \coloneqq y(G)(S) \coloneqq Hom_C(S,G) $ with an ordinary group [[structure]]
$\big(G(S), \cdot_S, \athrm{e}_S\big)$, in particular with a product operation (a map of sets) of the form

$$
  \cdot_S 
    \,\colon\, 
  G(S) \times G(S) \longrightarrow G(S)
  \,.
$$

Moreover, since morphisms in [[Grp]] are [[group homomorphisms]], it follows
that for every morphism $f \colon S \to T$ in $C$ we get a 
[[commuting diagram]] of the form

$$
  \array{
    G(S) \times G(S) &\stackrel{\cdot_S}{\to}& G(S)
    \\
    \big\uparrow\mathrlap{^{G(f)\times G(f)}}  
    && \big\uparrow\mathrlap{^{G(f)}}
    \\
    G(T) \times G(T) &\underset{\cdot_T}{\longrightarrow}& G(T)     
    \mathrlap{\,.}
  } 
$$

Taken together this means that there is a morphism

$$
  y(G \times G)  \longrightarrow y(G)
$$

of [[representable presheaves]]. By the [[Yoneda lemma]], this *uniquely*
comes from a morphism $\cdot \colon G \times G \to G$ in $\mathcal{C}$, which is the 
product of the group structure on the object $G$ that we are after.

etc.  


### As data structure
 {#AsDataStructure}

In the language of [[dependent type theory]] (using the notation for [[dependent pair types]] *[[dependent functions and dependent pairs -- table|here]]*) the type of group data structures is:


<img src="/nlab/files/GroupDataType-230121.jpg" width="740">






## Examples 
 {#Examples}

* A group object in [[Sets]] is a [[group]].

* A group object in [[TopologicalSpaces]] is a [[topological group]].

* A group object in [[SimplicialSets]] is a [[simplicial group]].

* A group object in [[Ho(Top)]] is an [[H-group]].

* A group object in [[Diff]] is a [[Lie group]].

* A group object in [[SDiff]] is a [[supergroup|super Lie group]].

* A group object in [[Grp]] is an [[abelian group]] (using the [[Eckmann-Hilton argument]]).

* A group object in [[Ab]] is an abelian group again.

* A group object in [[Cat]] is a strict [[2-group]].

* A group object in [[Grpd]] is a strict $2$-group again.

* A group object in [[CRing]]$^{op}$ is a commutative [[Hopf algebra]].

* A group object in a [[functor category]] is a [[group functor]].

* A group object in [[schemes]] is a [[group scheme]].

* A group object in an [[opposite category]] is a [[cogroup object]].

* A group object in [[G-sets]]/[[G-spaces]] is a $G$-[[equivariant group]], namely a [[semidirect product group]].



* A group object in [[stacks]] is a [[group stack]].

## Theory 

The basic results of elementary group theory apply to group objects in any category with finite products.  (Arguably, it is precisely the *elementary* results that apply in any such category.)

The theory of group objects is an example of a [[Lawvere theory]].


## Related concepts

* [[monoid]], [[monoid object]], [[monoid object in an (∞,1)-category]]

* [[group]], **group object**, [[group object in an (∞,1)-category]]

* [[group action]], [[action object]]

* [[groupoid]], [[groupoid object]], [[groupoid object in an (∞,1)-category]]

* [[infinity-groupoid]], [[infinity-groupoid object]], [[groupoid object in an (∞,1)-category]]

* [[ring]], [[ring object]]

## References
 {#References}

The general definition of internal groups seems to have first been formulated in:

* {#Grothendieck61} [[Alexander Grothendieck]], p. 104 (7 of 21) of: [[FGA]] _Techniques de construction et théorèmes d'existence en géométrie algébrique III: préschémas quotients_, Séminaire Bourbaki: années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf), [English transl. pdf](https://labs.thosgood.com/builds/fga-3-III.pdf))

following the general principle of [[internalization]] formulated in:

* {#Grothendieck60} [[Alexander Grothendieck]], p. 340 (3 of 23) in: [[FGA]] *Technique de descente et théorèmes d'existence en géométrie algébriques. II: Le théorème d'existence en théorie formelle des modules*, Séminaire Bourbaki : années 1958/59 - 1959/60, exposés 169-204, Séminaire Bourbaki, no. 5 (1960), Exposé no. 195 ([numdam:SB_1958-1960__5__369_0](http://www.numdam.org/item/SB_1958-1960__5__369_0), [pdf](http://www.numdam.org/item/SB_1958-1960__5__369_0.pdf), [English transl. pdf](https://labs.thosgood.com/builds/fga-3-II.pdf))

reviewed in:

* [[Barbara Fantechi]], [[Lothar Göttsche]], [[Luc Illusie]], [[Steven L. Kleiman]], [[Nitin Nitsure]], [[Angelo Vistoli]], Section 2.2 of: _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. (2005) &lbrack;[MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001), [ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [lecture notes](http://indico.ictp.it/event/a0255/other-view?view=ictptimetable)&rbrack;


On [[internalization]], [[H-spaces]], [[monoid objects]], [[group objects]] in [[algebraic topology]]/[[homotopy theory]] and introducing the [[Eckmann-Hilton argument]]:

* [[Beno Eckmann]], [[Peter Hilton]], *Structure maps in group theory*, Fundamenta Mathematicae 50 (1961), 207-221 ([doi:10.4064/fm-50-2-207-221](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/50/2/94854/structure-maps-in-group-theory))

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories I multiplications and comultiplications_, Math. Ann. 145, 227–255 (1962) ([doi:10.1007/BF01451367](https://doi.org/10.1007/BF01451367))

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories III primitive categories_,  Math. Ann. **150** 165–187 (1963) ([doi:10.1007/BF01470843](https://doi.org/10.1007/BF01470843)) 

With emphasis of the role of the [[Yoneda lemma]]:

* [[Saunders MacLane]], chapter III, section 6 in: _[[Categories for the Working Mathematician]]_, Springer (1971) 

Review:

* [[John Michael Boardman]], *Algebraic objects in categories*, Chapter 7 of: _Stable Operations in Generalized Cohomology_ &lbrack;[pdf](https://math.jhu.edu/~wsw/papers2/math/28a-boardman-stable.pdf), [[Boardman-StableOperations.pdf:file]]&rbrack; in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford (1995) &lbrack;[doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7)&rbrack;

* [[Magnus Forrester-Barker]], *Group Objects and Internal Categories* &lbrack;[arXiv:math/0212065](https://arxiv.org/abs/math/0212065)&rbrack;


In the broader context of internalization via [[sketches]]:

* [[Michael Barr]], [[Charles Wells]], Section 4.1 of: _[[Toposes, Triples, and Theories]]_, Originally published by: Springer-Verlag, New York, 1985, republished in: Reprints in [Theory and Applications of Categories, No. 12 (2005) pp. 1-287](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)


With focus on internalization in [[sheaf toposes]]:

* [[Saunders Mac Lane]], [[Ieke Moerdijk]], Section II.7 of: _[[Sheaves in Geometry and Logic]]_, Springer 1992 ([doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0))


[[!redirects group objects]]

[[!redirects internal group]]
[[!redirects internal groups]]
[[!redirects inner group]]
[[!redirects inner groups]]


[[!redirects abelian group object]]
[[!redirects abelian group objects]]



