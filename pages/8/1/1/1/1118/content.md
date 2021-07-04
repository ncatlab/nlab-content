
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

A _group object_ in a [[category]] $C$ is a [[group]] [[internalization|internal]] to $C$.


## Definition 

### In terms of internal group objects

A **group object** or **internal group** in a category $C$ with binary [[product]]s and a [[terminal object]] $*$ is an object $G$ in $C$ and arrows
$$
1:* \to G
$$
(the unit map)
$$
(-)^{-1}:G\to G
$$
(the inverse map) and
$$
m:G\times G \to G
$$
(the multiplication map),
such that the following diagrams commute:
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
  \big\downarrow && \downarrow m 
  \\
  G\times G & \stackrel{m}{\longrightarrow} & G
}
$$
(expressing the fact multiplication is associative),
$$
\array{
  G 
  & \stackrel{(1,id)}{\longrightarrow} 
  & G\times G
  \\
  {}^{\mathllap{(\id,1)}}
  \big\downarrow 
  &\underset{=}{\searrow}& 
  \big\downarrow m 
  \\
  G\times G & \stackrel{m}{\longrightarrow} &G
}
$$
(telling us that the unit map picks out an element that is a left and right identity), and
$$
\array{
G 
  & 
   \overset{
     (id,(-)^{-1})\circ\Delta
   }
   {\longrightarrow} 
   & 
   G\times G
   \\
   {}^{
     \mathllap{
       ((-)^{-1},id)\circ\Delta
     }
   }
   \big\downarrow 
   & 
   \underset{1}{\searrow}& \downarrow m 
   \\
   G\times G 
   & 
   \stackrel{m}{\longrightarrow} 
   &
   G
}
$$
(telling us that the inverse map really does take an inverse), where we have let $1: G \to G$ denote the composite $G \to * \stackrel{1}{\to} G$ and $\Delta$ is a [[diagonal morphism]].

Even if $C$ doesn\'t have *all* binary products, as long as products with $G$ (and the terminal object $*$) exist, then one can still speak of a group object $G$ in $C$.


### In terms of presheaves of groups
 {#InTermsOfPresheavesOfGroups}

+-- {: .num_prop}
###### Proposition

Given a [[cartesian monoidal category]] $C$, the category of internal groups in $C$ is equivalent to the [[full subcategory]] of the category of [[presheaves]] of [[groups]] $Grp^{C^{op}}$ on $C$, spanned by those presheaves whose underlying set part in $Set^{C^{op}}$ is [[representable functor|representable]]. 

=--

This is a special case of the general theory of _[[structures in presheaf toposes]]_.

In other words, the [[forgetful functor]] from $Grp^{C^{op}}$ to $Set^{C^{op}}$ (obtained by composing with the [[forgetful functor]] [[Grp]] $\to$ [[Set]]) creates representable group objects from  representable objects. 

An object $G$ in $C$ with an internal group structure is a diagram

$$
  \array{
    && Grp
    \\
    & {}^{(G,\cdot)}\nearrow & \downarrow
    \\
    C^{op} &\stackrel{Y(G)}{\to}& Set
  }
  \,.
$$

This equips each object $S \in C$ with an ordinary group 
$(G(S), \cdot)$ structure, so in particular a product operation

$$
  \cdot_S : G(S) \times G(S) \to G(S)
  \,.
$$

Moreover, since morphisms in $Grp$ are group homomorphisms, it follows
that for every morphism $f : S \to T$ we get a 
commuting diagram

$$
  \array{
    G(S) \times G(S) &\stackrel{\cdot_S}{\to}& G(S)
    \\
    \uparrow^{G(f)\times G(f)}  && \uparrow^{G(f)}
    \\
    G(T) \times G(T) &\stackrel{\cdot_T}{\to}& G(T)     
  } 
$$

Taken together this means that there is a morphism

$$
  Y(G \times G)  \to Y(G)
$$

of representable presheaves. By the [[Yoneda lemma]], this uniquely
comes from a morphism $\cdot : G \times G \to G$, which is the 
product of the group structure on the object $G$ that we are after.

etc.  


## Examples 
 {#Examples}

* A group object in [[Set]] is a [[group]].

* A group object in [[Top]] is a [[topological group]].

* A group object in [[sSet]] is a [[simplicial group]].

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



On [[internalization]], [[H-spaces]], [[monoid objects]], [[group objects]] in [[algebraic topology]]/[[homotopy theory]] and introducing the [[Eckmann-Hilton argument]]:

* [[Beno Eckmann]], [[Peter Hilton]], *Structure maps in group theory*, Fundamenta Mathematicae 50 (1961), 207-221 ([doi:10.4064/fm-50-2-207-221](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/50/2/94854/structure-maps-in-group-theory))

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories I multiplications and comultiplications_, Math. Ann. 145, 227–255 (1962) ([doi:10.1007/BF01451367](https://doi.org/10.1007/BF01451367))

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories III primitive categories_,  Math. Ann. **150** 165–187 (1963) ([doi:10.1007/BF01470843](https://doi.org/10.1007/BF01470843)) 

With emphasis of the role of the [[Yoneda lemma]]:

* [[Saunders MacLane]], chapter III, section 6 in: _[[Categories for the Working Mathematician]]_, Springer (1971) 

In the broader context of internalization via [[sketches]]:

* [[Michael Barr]], [[Charles Wells]], Section 4.1 of: _[[Toposes, Triples, and Theories]]_, Originally published by: Springer-Verlag, New York, 1985, republished in: Reprints in [Theory and Applications of Categories, No. 12 (2005) pp. 1-287](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)


With focus on internalization in [[sheaf toposes]]:

* [[Saunders Mac Lane]], [[Ieke Moerdijk]], Section II.7 of: _[[Sheaves in Geometry and Logic]]_, Springer 1992 ([doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0))


[[!redirects group objects]]

[[!redirects internal group]]
[[!redirects internal groups]]
[[!redirects inner group]]
[[!redirects inner groups]]
[[!redirects group object]]
[[!redirects group objects]]

[[!redirects abelian group object]]
[[!redirects abelian group objects]]



