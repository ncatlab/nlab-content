
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea and definition
In a broad, non-technical sense, an "element" is a "building block", "component", or "basic part" of a more substantial whole. Ordinary or [[global elements|global]] elements of a [[set]] are simply the [[points]] of that set, and hence sufficiently capture this broad notion of "element" in [[Set]], since by definition sets are no more than collections of points.

However, in general, knowing about the points of an object is insufficient to count as knowing its elements (construed broadly). From the point of view of the category [[Set]], most things that can be said and done about elements of a set $X$, can more generally be said and done for morphisms $x \colon U\to X$, for _any_ other set $U$.  The point is just that many constructions can be performed "elementwise".  For instance, the fact that elements of $X\times Y$ are exactly pairs $(x,y)$ of an element of $X$ and an element of $Y$, when performed "elementwise" for morphisms out of $U$, expresses the universal property of a [[product]].  In [[structural set theory]] such as [[ETCS]], one sometimes (but not necessarily) takes this point of view for axiomatizing the structure of $Set$.

On the other hand, once elements of objects are regarded as morphisms into these objects, the same reasoning applies to _every_ [[category]] $C$.  Accordingly, for $C$ any [[category]] and $X$ an [[object]] of $C$, one may refer to a [[morphism]] $x \colon U \to X$ a **generalized element** of $X$. One says this is a generalized element with **stage of definition** given by $U$, or a **figure** of shape $U$ in $X$.

The perspective of generalized elements of objects of a category $C$ is related to regarding $C$ as its image under the [[Yoneda embedding]]

$$
  Y : C \hookrightarrow [C^{op}, Set]
$$

into its [[presheaf category]]. Under this embedding, every object $X$ of $C$ is mapped to the [[functor]] -- the [[representable functor]] represented by it --

$$
  GenEl(X) : C^{op} \to Set
$$ 

that sends each object $U$ of $C$ to the set of generalized elements of $X$ at stage $U$.

It is also worth noting that the [[internal logic]] or [[type theory]] of a category provides us a way to go backwards formally.  By reasoning about "abstract elements" in a set-theoretic style like ordinary elements, the interpretation then "compiles" such proofs to category-theoretic ones which actually apply to all generalized elements.


## Examples 


### In $Set$

The primordial example is when $C$ is the category [[Set]] of sets and $I$ is a [[terminal object]] in $Set$ --- that is, a set with one element.  Then elements of any set $c$ are in one-to-one correspondence with functions $f: I \to c$.  This correspondence works as follows: given any element of $c$ there is a unique function $f: I \to c$ with this element in its image, and conversely each function $f: I \to c$ has a unique element of $c$ in its image. 

### In concrete categories

In the same way, in a [[concrete category]] whose underlying-set functor is represented by $I$, the $I$-elements of an object are the same as the elements of its underlying set.  (The category of sets is actually a special case of this, since it is concrete, with the identity functor represented by a terminal object.)

### Global elements

Generalizing from $Set$ in another way, in any category with a terminal object $I$, we call a morphism $f : I \to c$ a [[global element]] of the object $c$. 

### In toposes 

The stability or [[fundamental theorem of topos theory|slice theorem]] for [[toposes]] says that if $\mathbf{E}$ is a topos, then also the [[slice category]] $\mathbf{E}/U$ is a topos for any object $U$, and the [[pullback#PullbackFunctor|pullback functor]] $U^\ast: \mathbf{E} \to \mathbf{E}/U$ is a [[logical functor]]. 

Observe that in $\mathbf{E}/U$, an ordinary (i.e. global) point of an object $U^\ast X$, a section $U^\ast 1 \to U^\ast X$, corresponds to a generalized element $U \to X$ in $\mathbf{E}$. Thus the slice theorem guarantees that generalized points with domain $U$ may be treated exactly as ordinary points, just in a more variable topos $\mathbf{E}/U$. 

### In monoidal categories

On the other hand, it is common to take $I$ to be the unit object whenever $C$ is a [[monoidal category]].  The generalized elements defined over this $I$ are important in [[enriched category|enriched category theory]]).

### For generators

Arguably, the most general case where generalized elements defined at only one stage $I$ are "sufficient" when $I$ is some sort of [[generator]] of the category.  However, not every category has a single object as any sort of generator!  Instead, in arbitrary categories, generalized elements of *all* possible stages of definition must often be used to replace global elements.  Thus while a set is determined by its global elements, an object of an arbitrary category is determined by all of its generalized elements (this is one way to state the [[Yoneda lemma]]).

### In presheaf categories

For $C = [D^{op}, Set]$  a [[presheaf]] category and for $I = \Delta_{pt} = (d \mapsto \{\bullet\})$ the presheaf constant at the singleton set, the generalized elements of a presheaf $F$ are the _[[global section|global sections]]_ of this presheaf, equivalently these are the elements in the [[limit]] set over $F$.

On the other hand, if $I=D(-,d)$ is a [[representable functor|representable]] presheaf, then the generalized elements of $F$ at stage $d$ are precisely the elements of the set $F(d)$, by the [[Yoneda lemma]].

### In abelian categories

An [[element in an abelian category]] is an equivalence class of generalised elements.

## Relationship to type theory

In the [[internal language|internal]] [[type theory]] of a category $C$, the generalized elements of $X$ at stage $U$ can be identified with [[terms]] of type $X$ in [[context]] $u\colon U$:
$$ 
   u\colon U \vdash x(u) \colon X
  \,. 
$$
See the references [below](#ReferencesInTypeTheory).

The fact that all type-theoretic constructions can be performed in any context implies that we can manipulate ordinary elements, and end up speaking also about generalized elements defined at arbitrary stages.


## References

### In type theory
 {#ReferencesInTypeTheory}

The interpretation of [[terms]] in [[type theory]] as generalized elements of objects in a category is discussed for instance on p. 8 of

* [[Steve Awodey]], [[Andrej Bauer]], _Propositions as $[$Types$]$_, Journal of Logic and Computation. Volume 14, Issue 4, August 2004, pp. 447-471 ([pdf](http://math.andrej.com/data/bracket_types.pdf))


[[!redirects generalised element]]
[[!redirects generalised elements]]
[[!redirects generalized elements]]
