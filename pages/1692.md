
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# The Chu construction

* table of contents
{: toc}

## Idea

In [[category theory]], the _Chu construction_ is a general method for constructing a [[star-autonomous category]] from a [[closed monoidal category|closed symmetric monoidal category]]. It is named after Po-Hsiang Chu, a student of [[Michael Barr]], who gave the construction in his master's thesis at McGill University. It has been extensively developed by [[Vaughan Pratt]] for its potential applications in [[computer science|Theoretical Computer Science]].

In outline, given a closed symmetric monoidal category $C$ with [[pullback]]s and an object $d$ of $C$, there is a star-autonomous category $Chu(C, d)$ and a strong symmetric monoidal functor 

$$i: C \to Chu(C, d)$$

which realizes $C$ as a [[coreflective subcategory]] of $Chu(C, d)$. Being star-autonomous, $Chu(C, d)$ is self-dual, hence $C^{op}$ also embeds as a full subcategory of $Chu(C, d)$, this time [[reflective subcategory|reflectively]]. 

Many concrete dualities in mathematics can be seen as embedded in a larger ambient self-duality on a Chu construction. This applies in particular to the category of _Chu spaces_, $Chu(Set, 2)$ (see below).

This construction may be [[categorified]] to what might be called a **2-Chu construction**, producing for example $Chu(Cat, Set)$ (see [Shulman17](#Shulman17)).  It also generalizes to a [[double Chu construction]] and to operations on [[multicategories]] and [[polycategories]].


## Definition ## 

### As a category with self-duality

Let $C$ be a closed symmetric monoidal category and $d\in C$ an object.  The objects of $Chu(C, d)$ are triples $(a, b; r: a \otimes b \to d)$ (called _$d$-valued pairings_ between $a$ and $b$), where $a$ and $b$ are objects of $C$ and $r$ is a morphism of $C$. The special triple $(d, I; \rho: d \otimes I \cong d)$, where $\rho$ is an instance of the canonical isomorphism (the right unitor) for the monoidal unit $I$, will play the role of [[dualizing object]] in $Chu(C, d)$. 

The morphisms of $Chu(C, d)$, 

$$(a, b; r: a \otimes b \to d) \to (x, y; s: x \otimes y \to d),$$

are pairs of morphisms $f: a \to x$, $g: y \to b$ which are adjoint with respect to the pairings, that is, making the diagram 

$$\array{
 & a \otimes y & \overset{1_a \otimes g}{\to} & a \otimes b\\
f \otimes 1_y & \downarrow & & \downarrow r\\
& x \otimes y & \overset{s}{\to} & d
}$$

commute. There is an evident self-duality 

$$Chu(C, d)^{op} \to Chu(C, d)$$ 

which takes an object $(a, b; r: a \otimes b \to d)$ to 

$$(b, a; r^\dagger = [b \otimes a \overset{\sigma}{\cong} a \otimes b \overset{r}{\to} d])$$ 

where $\sigma$ is an instance of the symmetry isomorphism, so that $r^\dagger$ is the evident transpose. On morphisms, it takes a pair $(f, g)$ to $(g, f)$; note well that the directions of the arrows make the functor contravariant on $Chu(C, d)$.

### As a $\ast$-autonomous category

Armed with just this much knowledge, and knowledge of how star-autonomous categories behave (as categorified versions of [[Boolean algebra]]s, or perhaps better [[Boolean rig]]s), the star-autonomous structure on $Chu(C, d)$ can pretty much be deduced (or strongly guessed) by the diligent reader, and this is actually a very good exercise. One could sketch this as follows: 

* The monoidal unit of $Chu(C, d)$ should be the dual of the dualizer, and so is $(I, d; \lambda: I \otimes d \cong d)$ where $\lambda$, the transpose of $\rho$, is a canonical isomorphism for the unit $I$. 

* The internal hom $A \multimap X$ in $Chu(C, d)$ should internalize the external hom, i.e., the set of maps from the monoidal unit to $A \multimap X$ should be in natural bijection with the set of maps $A \to X$ in $Chu(C, d)$. 

This suggests the first component $(A \multimap X)_0$ of the triple 

$$A \multimap X = ((A \multimap X)_0, (A \multimap X)_1; pairing)$$ 

should be the object of adjoint pairs of maps: given 

$$A = (a, b; r: a \otimes b \to d), \qquad X = (x, y; s: x \otimes y \to d)$$ 

define the first component as pullback: 

$$\array{
(A \multimap X)_0 & \to & x^a \\
\downarrow & & \downarrow \tilde{s} \\
b^y & \overset{\tilde{r}}{\to} & d^{a \otimes y}
}$$

where exponentials are used to denote internal homs in $C$, $\tilde{r}$ is the result of [[currying]] $r$ to $b \to d^a$ and exponentiating, and similarly for $\tilde{s}$. 

The pullback is paired with $a \otimes y$, i.e., there is a map 

$$(A \multimap X)_0 \otimes (a \otimes y) \to d$$ 

obtained by decurrying either leg of the pullback, so one defines (with fingers crossed) $(A \multimap X)_1$ to be $a \otimes y$, and the pairing to be this map into $d$. 

* To form the tensor product $A \otimes X$, use the formula $ A \otimes X \cong (A \multimap X^*)^* $ which holds true in any star-autonomous category (as a categorified analogue of the Boolean algebra equation $a \wedge x = \neg (a \Rightarrow \neg x)$). 

With notation as above, this works out to 

$$(a \otimes x, y^a \times_{d^{a \otimes x}} b^x)$$ 

where the second component is a pullback, and the pairing omitted but obvious. The main thing to check is the presence of a canonical isomorphism 

$$Chu(C, d)(A \otimes X, Y) \cong Chu(C, d)(X, A \multimap Y)$$ 

but this is left as an exercise. 

Also one should check that if $D$ is the dualizing object, that $ A^* \cong A \multimap D $, but this is straightforward. 

* There is a strong symmetric monoidal functor 
$$i: C \to Chu(C, d)$$ 
taking $c$ to $(c, d^c; eval: c \otimes d^c \to d)$. (This does **not** take $d$ to the dualizing object in $Chu(C, d)$, unless of course the canonical map $I \to d^d$ is an isomorphism.) This embedding admits a right adjoint 
$$p: Chu(C, d) \to C$$ 
given by the obvious projection, that is also strong symmetric monoidal. The unit of the adjunction is an isomorphism, hence $C$ is a coreflective (full) subcategory of $Chu(C, d)$. 

* If $C$ is complete and cocomplete, then so is $Chu(C, d)$. The formula for colimits is the obvious expected one: 
$$colim_i (a_i, b_i; r_i: a_i \otimes b_i \to d) = (colim_i a_i, lim_i b_i; r)$$ 
where $r$ is the decurrying of 
$$lim_i (b_i \to d^{a_i}) \cong lim_i b_i \to d^{colim_i a_i}$$ 
and the formula for limits is obtained by dualizing the formula for colimits in $Chu(C, d)$.  

### As a polycategory

We can also deduce the $\ast$-autonomous structure of $Chu(C,d)$ by constructing it directly as a [[star-polycategory]] and then observing that it is representable.  This has the additional benefit of giving a universal property to the tensor product, as well as applying to more general inputs $C$ (and giving a result that may not be representable), and giving a convenient way to phrase the universal property of $Chu(C,d)$ itself (see below).

Let $C$ be a (symmetric) [[polycategory]] in which every morphism has codomain arity 0 or 1 (a *co-subunary polycategory*).  For instance, if $C$ is any [[symmetric multicategory]] and $d\in C$ an object, we can obtain a co-subunary polycategory by defining $C(x_1,\dots,x_n; ) = C(x_1,\dots,x_n; d)$.  (In fact the construction can be generalized even further; see [Shulman 18](#Shulman18).)

The objects of $Chu(C)$ are now pairings $(a, b; r : (a,b) \to ())$ in the appropriate polycategorical sense.  A morphism $(a,b,r) \to (x,y,s)$ is a pair of morphisms $f:a\to x$ and $g:y\to b$ that are "adjoint" with respect to the pairings, in the sense that the following square commutes:
\begin{tikzcd}
  (a,y) \ar[r,"{(f,1)}"] \ar[d,"{(1,g)}"'] & (x,y) \ar[d,"s"] \\ (a,b) \ar[r,"r"'] & ().
\end{tikzcd}
More generally, we can directly make $Chu(C)$ into a polycategory by taking the morphisms to be a suitable kind of [[multivariable adjunctions]].  For instance, a morphism $((a,b,r),(x,y,s)) \to (u,v,t)$ consists of three morphisms
$$ f : (a,x) \to u \qquad g : (a,v) \to y \qquad h : (x,v) \to b $$
such that the following three composites are equal modulo symmetries:
$$ (a,x,v) \xrightarrow{(f,1)} (u,v) \xrightarrow{t} () $$
$$ (x,a,v) \xrightarrow{(1,g)} (x,y) \xrightarrow{s} () $$
$$ (a,x,v) \xrightarrow{(1,h)} (a,b) \xrightarrow{r} (). $$
Similarly, a morphism $(a,b,r) \to ((x,y,s),(u,v,t))$ consists of three morphisms
$$ f : (a,y) \to u \qquad g : (x,b) \to u \qquad h : (y,v) \to b $$
such that three composite morphisms $(a,y,v) \to ()$ are equal.  With a suitable extension to $m$-$n$-ary morphisms we obtain a polycategory, and indeed a $\ast$-polycategory: the dual of $(a,b,r)$ is $(b,a,r^\dagger)$.

It is then a straightforward exercise to check that if $C$ is closed, representable, has pullbacks, and a "counit" in the sense that $C(\Gamma;) \cong C(\Gamma;d)$, then $Chu(C)$ is representable on both sides and hence a $\ast$-autonomous category, where all the structure coincides with the previous definition.


## Chu spaces (General case)##

While the Chu construction is worthy of exploration for many types of symmetric monoidal categories $C$, a great deal of attention has been focused just on the particular case $Chu(Set, 2)$ (or $Chu(Set,TV)$, where $TV$ is the set of [[truth value]]s, to be [[constructive mathematics|constructive]]), called the category of **Chu spaces**, and on relatives like $Chu(E, \Omega)$ where $E$ is a [[topos]] and $\Omega$ its [[subobject classifier]]. The reason is that a great many concrete categories of interest are fully embedded in Chu spaces. Moreover, the 2-element set $TV$ carries a panoply of [[ambimorphic object|ambimorphic]] (formerly, schizophrenic) object structures which induce concrete dualities between these categories, and all of these dualities are embedded in (i.e., are restrictions of) the one overarching duality that obtains on Chu spaces. 

The way this works is invariably the same: if $U: C \to Set$ is a [[concrete category]] and $\mathbf{2}$ is an object of $C$ over the 2-element set $TV$, then there is a functor 

$$i: C \to Chu(Set, 2): c \mapsto (U c, hom(c, \mathbf{2}); U c \times hom(c, \mathbf{2}) \to U\mathbf{2} = 2)$$ 

which is faithful by the notion of concrete category. 

What is striking is that this functor $i$ is also *full* in many cases of interest. This is because the adjointness condition for a pair $(f, g): i c \to i d$ to be a Chu space morphism, together with faithfulness of $U$, forces 

$$g: hom(d, \mathbf{2}) \overset{monic}{\to} hom(U d, 2) \overset{f^*}{\to} hom(U c, 2)$$ 

to be a restriction of the [[preimage]] function $f^*$ -- and then the mere additional fact that $f^*(\phi) = \phi \circ f \in hom(c, \mathbf{2})$ whenever $\phi \in hom(d, \mathbf{2})$ is often enough to force $f$ to be (the underlying function of) a morphism of $C$. All that is required is that there be sufficiently many morphisms $d \to \mathbf{2}$ to detect $C$-structure on $d$. Some examples follow: 

* As explained above, $Set$ fully embeds in $Chu(Set, 2)$ by $X \mapsto (X, 2^X; eval: X \times 2^X \to 2)$. 

* For $C = Top$, taking $\mathbf{2}$ to be [[Sierpinski space]], we have for each [[topological space]] $c$ an identification $Open(c) = hom(c, \mathbf{2})$. Then the adjointness condition on a morphism $(f, g): i c \to i d$ between the corresponding Chu spaces expresses precisely the continuity condition that the [[preimage]] $f^*$ takes opens of $d$ to opens of $c$. Hence the functor $Top \to Chu(Set, 2)$ is full. 

* For $C = Pos$, the category of [[poset]]s, take $\mathbf{2}$ to be the partially ordered set of truth values. Here we have that for a partial order $c$, $hom(c, \mathbf{2})$ is the set of [[upper set]]s (upward-closed subsets) of $c$. Given a function $f: U c \to U d$ between posets, the condition that the preimage $f^*(v)$ of an upper set of $d$ is an upper set of $c$ is enough to force $f$ to be a poset map (consider $v = \{q \in d: f p \leq q\}$). It follows that the functor $Pos \to Chu(Set, 2)$ is full. 

* For $C = Sup$, the category of [[sup-lattice]]s (whose morphisms are those functors between the underlying posets that are left adjoints), take $\mathbf{2}$ to be the partially ordered set of truth values, but this time as the _opposite_ of the poset $TV$. For a sup-lattice $c$, $hom(c, \mathbf{2})$ may be identified with the set of representable functors $c(-, x): c^{op} \to TV$. The Chu condition then is that $d(-, y) \circ f = d(f-, y)$ is representable for every representable $d(-, y)$. But this condition is equivalent $f$'s being a left adjoint. Therefore the functor $Sup \to Chu(Set, 2)$ is full. 

For other examples of concrete categories, the presence of enough elements in $\hom_C(c, \mathbf{2})$ to detect the $C$-structure of $c$ often requires some form of choice principle, such as the [[axiom of choice]] or [[ultrafilter theorem]]: 

* For $C = Vect_{\mathbb{F}_2}$, the category of vector spaces over the 2-element field, any object $d$ has a [[basis theorem|basis]], let us say $S$. For each $s \in S$, the characteristic or indicator $\chi_{s}: S \to \mathbf{2}$ extends uniquely to a linear function $\phi_s: d \to \mathbf{2}$. If $f: U c \to U d$ is a function such that $\phi_s \circ f: c \to \mathbf{2}$ is linear for every basis element $s \in S$, then 
$$f(a x + b y) = \sum_{s \in S} \phi_s(f(a x + b y))s = \sum_s (a\phi_s(f(x)) + b\phi_s(f(y)))s = a f(x) + b f(y)$$
It follows that the functor $Vect_{\mathbb{F}_2} \to Chu(Set, 2)$ is full. 

Similar considerations apply to Boolean algebras, Stone Boolean algebras, algebraic lattices, and so on. 

In all of these cases, the fullness of these embeddings entitles one to identify a topological space, a Boolean algebra, a vector space over $\mathbb{F}_2$, etc. with its corresponding Chu space, and the same consideration applies to the duals (opposites) of these categories. 

Now many of these formal categorical duals are themselves concrete categories, as in the famous example of classical [[Stone duality]] between Boolean algebras and Stone spaces, i.e., [[compact space|compact]] [[Hausdorff space|Hausdorff]] [[connected space|totally disconnected]] [[topological space]]s. In many such Stone duality situations, and certainly wherever Stone duality applies to the categories listed above, a contravariant equivalence between a concrete category $C$ and an algebraic category $D$ (i.e., where $U: D \to C$ is monadic), 

$$\array{
 & C^{op} & \overset{\sim}{\to} & D & \\
hom(-, \mathbf{2}) & \searrow & & \swarrow & U\\
 & & Set, & & 
}$$

is effected by lifting the object $\mathbf{2}$ of $C$ to a $D$-algebra structure in $C$ (making $\mathbf{2}$ an [[ambimorphic object]], carrying $C$- and $D$-structures compatible with one another); equivalently, seeing $hom(-, \mathbf{2}): C^{op} \to Set$ as an algebra over the monad $U F$ for which $U: D \to Set$ is monadic. For example, classical Stone duality is the case where $C$ is the category of Stone spaces, $D$ is the category of Boolean algebras, and the Boolean operations on $\mathbf{2}$ are continuous with respect to its Stone space structure, making $\mathbf{2}$ a Boolean algebra object in the category of Stone spaces. (For much more on this, see Johnstone's classic treatise _[[Stone Spaces]]_, especially the chapter on general concrete dualities.) 

The point is that in each of these situations, a Stone duality is a restriction of the more global duality on Chu spaces, in that the diagram 

$$\array{
 C^{op} & \overset{hom(-, \mathbf{2})}{\to} & D \\
i^{op} \downarrow & & \downarrow i \\
Chu(Set, 2)^{op} & \overset{(-)^*}{\to} & Chu(Set, 2)
}$$ 

(where the vertical arrows are full embeddings as described above) commutes up to canonical isomorphism. 

The same principle extends to other situations. For example, [[Pontryagin duality]] is fully embedded in the larger duality which obtains on $Chu(TopAb, S^1)$, where $TopAb$ is the category of abelian groups internal to a [[nice category of spaces]].  ([Barr](#BarrTobAb) has also shown that Pontryagin duality is embedded in a sub-$\ast$-autonomous category of $Chu(Ab,S^1)$, and one might conceivably hope to find it in $Chu(Top,S^1)$ as well by analogy to the above appearance of algebras inside $Chu(Set,2)$.)

Similarly, the 2-Chu construction, $Chu(Cat, Set)$, exhibits dualities, such as [[Gabriel-Ulmer duality]].

+--{.query}
Hi Toby; could I get you to explain the aside about Boolean rigs above? I'm thinking Boolean algebras is appropriate, as we have $ I \to x^* \wp x $, $ x \otimes x^* \to D $ [where $\wp$ denotes Girard's "par" and $D$ denotes the dualizer], together with appropriate triangular equations, categorifying the inequalities $1 \leq (\neg x) \vee v$ and $x \wedge (\neg x) \leq 0$ in a Boolean algebra. ---Todd

Now that I go to write [[Boolean rig]], I\'m not so sure.  I just know that $Chu(P X,\empty)$ at [[measurable space]] is *not* (even classically) a Boolean algebra.  I\'ll get back to you in a day or less.  ---Toby

Right, I agree. The Chu construction applied to a complete Heyting algebra is merely a $*$-autonomous quantale, not a $*$-autonomous frame (which would be a complete Boolean algebra), as you noted at [[measurable space]]. ---Todd
=--

## Chu spaces (Simple examples)##

One of the simplest occurrences of Chu space constructions, and the one explored in Pratt's notes (see below), leads to examples that although extremely simple have a well developed theory with connections to areas of logic and to [[formal concept analysis]]. This will be explored in a separate entry, [[Chu spaces, simple examples]].

## Properties ##

* Chu spaces give fairly easy to construct examples of closed monoidal categories in which [[coproduct]] injections are not necessarily monic; see [this MO answer](http://mathoverflow.net/a/208643/49).

### Universal property

Recall from the above that $Chu(C)$ is a $\ast$-polycategory whenever $C$ is a co-subunary polycategory.  This construction is functorial, and we claim that it defines a right adjoint to the forgetful functor $U$ from $\ast$-polycategories to co-subunary polycategories.

To see this, consider first the $\ast$-polycategory $F 1$ freely generated by one object.  It has two objects $x$ and $x^*$, and in addition to identity morphisms it has a [[dual pair]] $(x^*,x)\to ()$ and  $() \to (x,x^*)$.  Of these, all but the last are co-subunary.  Thus, a morphism $U F 1 \to C$ consists of two objects $a$ and $b$ (plus their identity morphisms) and a morphism $(a,b)\to ()$ --- in other words, an object of $Chu(C)$.

Now consider the $\ast$-polycategory $F (1,1)$ freely generated by two objects $x$ and $y$ and a morphism $f:x\to y$.  It contains two copies of $F 1$ generated by $x$ and $y$, together with $f:x\to y$, its dual $f^*: y^* \to x^*$, and two other copies of it $f^\dagger : (x,y^*) \to ()$ and ${}^\dagger f : () \to (x^*,y)$.  Of these all but the last are co-subunary, so a morphism $U F 1 \to C$ is determined by two objects of $Chu(C)$ together with three more morphisms (and some composition laws relating them to the duality morphisms).  This yields the two morphisms $a\to x$ and $y\to b$ of a morphism in $Chu(C)$, along with their common composite $(a,y) \to ()$.

Similarly, one can characterize all the morphisms in $Chu(C)$ by mapping out of $U F (m,n)$, where $F(m,n)$ is the $\ast$-polycategory freely generated by a $m$-ary co-$n$-ary morphism.

As a special case of this universal property, if all the $\ast$-polycategories are representable and the subunary polycategories are representable, closed, with a counit, and have pullbacks, we obtain an adjunction between a certain category of $\ast$-autonomous categories and a certain category of closed symmetric monoidal categories with chosen objects.  This is the way it was phrased in [Pavlovic 97](#Pavlovic97).

## Related pages

* [[double Chu construction]]
* [[2-Chu construction]]
* [[Dialectica construction]]
* [[double gluing]]
* [[poset-valued set]]
* [[ternary frame]]
* [[multivariable adjunction]]

## References ##

* A nice post by [[Todd Trimble]] on the <a href="http://golem.ph.utexas.edu/category/2007/09/category_theory_in_machine_lea.html#c012536">n-Cafe</a>.
* Pratt, [Chu Spaces](http://boole.stanford.edu/pub/coimbra.pdf)
* [[Michael Barr]], [The Chu construction: history of an idea](http://www.math.mcgill.ca/barr/papers/chu-hist.pdf), in TAC 17 (2006-2007), special volume, _Chu spaces: theory and applications_.
* [Guide to Papers on Chu spaces](http://chu.stanford.edu/guide.html)

* [[Vaughan Pratt]], *Linear process algebra*, [pdf](http://boole.stanford.edu/pub/bhub.pdf), uses $Chu(Set,K)$ where $K$ is a 4-element set to model concurrency.

* {#Pavlovic97} Duško Pavlović, _Chu I: cofree equivalences, dualities and $\ast$-autonomous categories_, [doi](https://doi.org/10.1017/S0960129596002046)

* {#BarrTobAb} Michael Barr, On duality of topological abelian groups, [PDF](http://www.math.mcgill.ca/barr/ftp/pdffiles/abgp.pdf)

For categorifications and generalizations, see 

* {#Shulman17} Mike Shulman, _The 2-Chu Construction_, ([blog post](https://golem.ph.utexas.edu/category/2017/11/the_2chu_construction.html))

* {#Shulman18} Mike Shulman, _The 2-Chu-Dialectica construction and the polycategory of multivariable adjunctions_, 2018 [arxiv](https://arxiv.org/abs/1806.06082)

category: category

[[!redirects Chu space]]
[[!redirects Chu spaces]]
[[!redirects chu space]]
[[!redirects chu spaces]]
[[!redirects chu construction]]
