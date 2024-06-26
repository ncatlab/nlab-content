
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

A **cartesian bicategory** is a [[bicategory]] with properties that make it behave like a bicategory of generalized [[relations]].

Examples of cartesian bicategories include 

 * the bicategory [[Rel]] of sets and relations,
 * more generally, the [[bicategory of relations]] of a  [[regular category]],
 * the bicategory [[Span]] of sets and spans,
 * more generally, the bicategory of [[spans]] in a finitely [[complete category]],
 * the bicategory [[profunctor|Prof]] of (small) categories and profunctors,
 * more generally, the bicategory of internal categories and [[modules]] ([[profunctors]]) in a finitely complete category $C$,
 * as an alternative generalization, the bicategory of enriched categories and modules over a _cartesian_ monoidal category $V$.

Non-examples include

 * the locally-discrete bicategory [[Set]] of sets and functions,
 * the bicategory [[Cat]] of categories and functors,
 * the bicategory of profunctors and enriched in a _noncartesian_ monoidal category $V$.

Consider for example the bicategory [[Rel]]. This bicategory admits a symmetric monoidal structure given by the cartesian product. Because the cartesian product is _not_ the categorical product, this symmetric monoidal structure is _not_ [[cartesian monoidal category|cartesian monoidal]]. However, the cartesian product restricts to the locally-discrete sub-bicategory [[Set]] of sets and functions, on which it _is_  the categorical product. Note that a relation is the graph of a function if and only if it possesses a right adjoint (which is given by the opposite relation). In a general bicategory, a 1-cell is called _map-like_ if it possesses a right adjoint, and these are the 1-cells playing the role that functions play in $Rel$.

Generalizing this situation, a cartesian bicategory $B$ is a symmetric monoidal bicategory for which the monoidal product restricts to the categorical product on the sub-bicategory of map-like 1-cells, subject to natural compatibility conditions. Remarkably, the structure of such a tensor is [[property-like structure|property-like]] (is essentially unique when it exists). Thus the definition can be formulated directly in terms of the bicategory $B$ without mentioning a symmetric monoidal structure at all. Not only is this technically convenient (as the precise definition of a symmetric monoidal bicategory is quite technical), but it is moreover a very natural perspective to take.

Like allegories, cartesian bicategories provide a convenient abstract setting in which to study the calculus of relations, but unlike allegories they embrace higher examples like $Span$ and $Mod$. The original idea, as explained by Carboni and Walters in their paper, clearly had these various examples in mind but was initially confined to the locally posetal case; in part this was due to the lack at the time (circa 1987) of a complete definition of symmetric monoidal bicategories. In more recent years a full bicategorical treatment has emerged, due principally to Carboni, Kelly, Verity, and Wood. The alternative treatment we give below has not yet appeared in the literature as far as this author ([[Todd Trimble]]) is aware. 

## Technical preliminaries 

Note: All compositions will be written in the traditional order, in which application proceeds from right to left. 

We work with familiar notions of the theory of bicategories (which, for reasons of consonance with 2-terminology, we also call 2-categories) but in some cases under new names. We calculate with pasting diagrams in 2-categories as if they were strict 2-categories. 

Our notion of morphism between 2-categories has gone under various names: "homomorphism" in the sense of Bénabou, also known as "pseudofunctor" or weak 2-functor, where the structural constraints are isomorphisms. Here they are simply called **2-functors**. 

Each 2-category $B$ gives rise to a hom 2-functor $hom: B^{op} \times B \to Cat$, which we denote by $B(-, -)$, with the contravariant argument in the first place as is customary. 

Given 2-functors $F, G: B \to C$, it is for our purposes convenient to use the [[lax natural transformation|lax notion of morphism]] $\theta: F \to G$ between 2-functors for which the structural cells $\theta \cdot f$ (for 1-cells $f: a \to b$ in $B$) point in the direction 

$$\array{
F a & \overset{\theta a}{\to} & G a\\
F f \downarrow & \overset{\theta \cdot f}{\Rightarrow} & \downarrow G f\\
F b & \underset{\theta b}{\to} & G b
}$$ 

These are called "oplax transformations" by some authors such as B&#233;nabou and "lax transformations" by other authors such as Johnstone; on this page we will simply call them (2-)**transformations**. A transformation is **strong** if the structural cells $\theta \cdot f$ are isomorphisms. 

There is a well-known notion of morphism between transformation which has been called [[modification]]. We retain this usage, but as an aside we counsel against inventing a new term (e.g., "perturbation" between modifications) every time a new level of morphism is reached -- a more uniform terminology is called for. The term "transfor" (due to Sjoerd Crans) has been tentatively adopted elsewhere on this site; modifications may then be called **2-transfors**. 

In any case, given 2-categories $B$ and $C$, there is a 2-category of 2-functors, strong transformations and modifications from $B$ to $C$; this will be denoted $Hom_s(B, C)$. We have also the 2-category of 2-functors, transformations, and modifications; this will be denoted $Hom_l(B, C)$. 

### 2-adjunctions between 2-categories

A **2-adjunction** $F \dashv G$ consists of 2-functors $F: B \to C$, $G: C \to B$, and an adjoint equivalence 

$$C(F -, -) \simeq B(-, G -)$$ 

in the 2-category $Hom_s(B^{op} \times C, Cat)$. In more elementary terms, the data of a 2-adjunction is given by strong transformations 

$$\eta: 1_B \to G F \qquad \varepsilon: F G \to 1_C$$ 

and invertible modifications (called _triangulators_) 

$$\array{
G & \overset{\eta G}{\to} & G F G & & & & F & \overset{F\eta}{\to} & F G F\\ 
1_G \downarrow & \overset{s}{\Rightarrow} & \downarrow G \varepsilon & & & & 1_F \downarrow & \overset{t}{\Leftarrow} & \downarrow \varepsilon F\\ 
G & \underset{1_G}{\to} & G & & & & F & \underset{1_F}{\to} & F
}$$

such that the _triangulator coherence conditions_ hold: there are pasting diagram equalities 

$$\array{
1_B & \overset{\eta}{\to} & G F & \overset{1_{G F}}{\to} & G F\\
\eta \downarrow & \overset{\eta \cdot \eta}{\Rightarrow} & \downarrow G F \eta & & \downarrow 1_{G F}\\ 
G F & \underset{\eta G F}{\to} & G F G F & \overset{G t}{\Rightarrow} & G F & & & = & 1_{\eta}\\
1_{G F} \downarrow & & \overset{s F}{\Rightarrow} & G \varepsilon F \searrow & \downarrow 1_{G F} \\
G F & \underset{1_{G F}}{\to} & G F & \underset{1_{G F}}{\to} & G F 
}$$

$\, $ 

$$\array{
F G & \overset{1_{F G}}{\to} & F G & \overset{1_{F G}}{\to} & F G\\
1_{F G} \downarrow & F \eta G \searrow & \overset{t G}{\Rightarrow} & & \downarrow 1_{F G}\\
F G & \overset{F s}{\Rightarrow} & F G F G & \overset{\varepsilon F G}{\to} & F G & & & = & 1_{\varepsilon}\\
1_{F G} \downarrow & & F G \varepsilon \downarrow & \overset{\varepsilon \cdot \varepsilon}{\Rightarrow} & \downarrow \varepsilon\\
F G & \underset{1_{F G}}{\to} & F G & \underset{\varepsilon}{\to} & 1
}$$

### Lax adjunctions between 2-categories 

A **lax** adjunction is defined in the same way as a 2-adjunction, except that we relax (remove) the assumptions that $\eta$ and $\varepsilon$ are strong and that $s$, $t$ are invertible; the triangulator coherence conditions are still in effect. In that case, for objects $b$ of $B$ and $c$ of $C$, there is a local adjunction between hom-categories 

$$(L: B(b, G c) \to C(F b, c)) \dashv (R: C(F b, c) \to B(b, G c))$$ 

given by $L(g: b \to G c) = (F b \overset{F g}{\to} F G c \overset{\varepsilon c}{\to} c)$ and $R(f: F b \to c) = (b \overset{\eta b}{\to} G F b \overset{G f}{\to} G c)$. The unit of $L \dashv R$ at $g: b \to G c$ is given by the pasting 

$$\array{
b & \overset{g}{\to} & G c & \overset{1_{G c}}{\to} & G c\\
\eta b \downarrow & \overset{\eta \cdot g}{\Leftarrow} & \downarrow \eta G c & \overset{s c}{\Leftarrow} & \downarrow 1_{G c}\\
G F b & \underset{G F g}{\to} & G F G c & \underset{G \varepsilon}{\to} & G c
}$$

and the counit of $L \dashv R$ at $f: F b \to c$ is given by the pasting 

$$\array{
F b & \overset{F \eta b}{\to} & F G F b & \overset{F G f}{\to} & F G c\\
1_{F b} \downarrow & \overset{t b}{\Leftarrow} & \downarrow \varepsilon F b & \overset{\varepsilon \cdot f}{\Leftarrow} & \downarrow \varepsilon c\\
F b & \underset{1_{F b}}{\to} & F b & \underset{f}{\to} & c
}$$

The triangular equations for $L \dashv R$ follow from the triangulator coherence conditions. (Warning: it is not generally true that a lax adjunction induces an adjoint pair in $Hom_l(B^{op} \times C, Cat)$. Cf. lemma 1 below.) 

### The 2-category $Map(B)$ 

Let $B$ be a 2-category. Following Carboni and Walters, we define a *map* in $B$ to be a 1-cell in $B$ that possesses a right adjoint. It is useful to think of them as playing the role of "functional relations" in an ambient 2-category of relations. We let $Map(B)$ be the locally full sub-2-category whose 0-cells are those of $B$ and whose 1-cells are the maps in $B$. We observe that every 2-functor $F: B \to C$ restricts to a 2-functor $F|: Map(B) \to Map(C)$, and by the following proposition, every transformation $\theta: F \to G$ restricts to a strong transformation $\theta$ in $Hom_s(Map(B), C)$: 

**Proposition 1:** If $f: b \to c$ is a map in $B$, then $\theta \cdot f$ is invertible. 

**Proof:** Let $f^*$ denote a right adjoint of $f$. It is easily verified that the diagram 

$$\array{
F b & \overset{F f}{\to} & F c & \overset{\theta c}{\to} & G c & \overset{1_{G c}}{\to} & G c\\
1_{F b} \downarrow & \Rightarrow & F f^* \downarrow & \overset{\theta \cdot f^*}{\Rightarrow} & \downarrow G f^* & \Rightarrow & \downarrow 1_{G c}\\
F b & \underset{1_{F b}}{\to} & F b & \underset{\theta b}{\to} & G b & \underset{G f}{\to} & G c
}$$

pastes to give the inverse $(\theta \cdot f)^{-1}$, where the left and right squares are the unit and counit of adjunctions $F f \dashv F f^*$, $G f \dashv G f^*$. 

A transformation $\theta: F \to G: B \to C$ is **map-valued** if each 1-cell $\theta b$ is a map in $C$. By the previous proposition, a map-valued transformation $\theta$ in $Hom_l(B, C)$ restricts to a strong transformation $\theta|: F| \to G|$ in $Hom_s(Map(B), Map(C))$. 

* **Warning:** In general it is imprecise to identify maps in a 2-category with the "functional relations". That is, for some of the standard examples of cartesian bicategories, such as $B = Prof$, we cannot simply identify $Map(B)$ with $Cat$: 1-cell equivalences are only Morita equivalences, not $Cat$-equivalences. A better adapted framework is one of a bicategory with a proarrow equipment, or a [[framed bicategory]]. Eventually this article will be rewritten with this remark in mind... 

## Definition of cartesian structure and basic results 

A **cartesian structure** on a bicategory $B$ consists of the following data: 

* 2-functors $\otimes: B \times B \to B$ and $I: \mathbf{1} \to B$, where $\mathbf{1}$ is the terminal 2-category; 

* Map-valued transformations 
$$\delta: 1_B \to \otimes \Delta, \qquad \pi: \Delta \otimes \to 1_{B \times B}, \qquad \varepsilon: 1_B \to I !$$ 
where $\Delta: B \to B \times B$ is the diagonal 2-functor and $!: B \to \mathbf{1}$ is the unique 2-functor; 

* Invertible modifications 
$$\array{
\otimes & \overset{\delta \otimes}{\to} & \otimes \Delta \otimes & & & & \Delta & \overset{\Delta \delta}{\to} & \Delta \otimes \Delta & & & & I & \overset{\varepsilon I}{\to} & I ! I\\
\mathllap{1_{\otimes}} \downarrow & \overset{s}{\Rightarrow} & \downarrow \mathrlap{\otimes \pi} & & & & \mathllap{1_{\Delta}} \downarrow & \overset{t}{\Leftarrow} & \downarrow \mathrlap{\pi \Delta} & & & & \mathllap{1_{I}} \downarrow & \overset{u}{\Rightarrow} & \downarrow \mathrlap{I \cdot id}\\
\otimes & \underset{1_{\otimes}}{\to} & \otimes & & & & \Delta & \underset{1_{\Delta}}{\to} & \Delta & & & & I & \underset{1_I}{\to} & I
}$$ 
satisfying the triangulator coherence conditions. $\Box$ 

The crucial observation is that, by proposition 1, this data restricts to give 2-adjunctions 

$$(Map(B) \overset{\Delta}{\to} Map(B) \times Map(B)) \dashv (Map(B) \times Map(B) \overset{\otimes}{\to} Map(B))$$ 

\linebreak

$$(Map(B) \overset{!}{\to} \mathbf{1}) \dashv (\mathbf{1} \overset{I}{\to} Map(B))$$ 

making the restriction of $\otimes$ to $Map(B)$ a _2-product_ on $Map(B)$ with 2-terminal object $I$. Naturally this finite 2-product structure on $Map(B)$ is property-like: is uniquely determined up to equivalence which is uniquely specified up to unique isomorphism. 

A little later we will argue that cartesian structure on the full bicategory $B$ is also property-like; the main thing is to see that the way in which $\otimes$ acts on 1-cells is essentially uniquely determined. 

### Symmetric monoidal structure via cartesian structure 

We now argue that a cartesian bicategory $B$ carries a symmetric monoidal structure whose tensor product is 

$$\otimes: B \times B \to B$$ 

The proof is pretty easy to sketch, once the fact is admitted that the induced 2-product structure makes $Map(B)$ a symmetric monoidal bicategory. This fact about 2-products, while never in dispute, was given a complete proof only in the past few years by the late Max Kelly, and we freely take advantage of it below. 

First, given objects $a, b, c$ of $B$, we may regard them as objects of $Map(B)$, where there is an associativity constraint 

$$\alpha_{a, b, c}: (a \otimes b) \otimes c \to a \otimes (b \otimes c)$$ 

on $Map(B)$ which is definable by exploiting 2-universal properties of the 2-product. The associativity thus has an expression in terms of $\otimes$, $\delta$, and $\pi$ which are globally defined on $B$, hence $\alpha$ is globally defined as a transformation on $B$. By similar considerations, the symmetry and unit constraints on $Map(B)$ also extend to globally defined transformations on $B$. We argue in a moment that these constraints are strong (adjoint) equivalences. 

Symmetric monoidal structure on $B$ also demands various structural modifications (such as a Yang-Baxter modification $R_{\bullet |\bullet, \bullet}$) satisfying various coherence conditions, but the components of such modifications ($R_{a|b, c}$, say) are defined by regarding their components $a, b, c$ as objects of $Map(B)$ and using the corresponding modifications there. Again, each such modification on $Map(B)$ is defined in terms of 2-adjunction data $\otimes$, $I$, $\delta$, $\pi$, $\varepsilon$, $s$, $t$, $u$ which are globally defined on $B$, so each such structure is a modification on $B$. Various coherence conditions on the modifications must be checked, but the conditions hold at every choice of objects of $B$ by regarding them as objects of $Map(B)$ and using the symmetric monoidal structure there, so the conditions hold on $B$. 

Now we check that the structural transformations $\alpha$ are strong adjoint equivalences. Indeed, when regarded as being defined on $Map(B)$, the constraint $\alpha$ is an equivalence and so has a left adjoint (with invertible unit and counit) $\alpha^-$ with components 

$$\alpha_{a, b, c}^{-}: a \otimes (b \otimes c) \to (a \otimes b) \otimes c$$ 

and just like $\alpha$, $\alpha^-$ is definable in terms of global structure on $B$, making $\alpha^-$ a transformation on $B$. Then $\alpha$, and by similar reasoning the symmetry and unit constraints, are strong transformations on $B$ by the following lemma: 

**Lemma 1:** If $\alpha$ is a right adjoint in $Hom_l(C, B)$, then the transformation $\alpha$ is strong. Consequently, if $\alpha^- \dashv \alpha$ is an adjoint equivalence, so that both $\alpha^- \dashv \alpha$ and $\alpha \dashv \alpha^-$, then $\alpha^- \dashv \alpha$ is a strong adjoint equivalence in $Hom_s(C, B)$. 

**Proof:** Only the first statement requires proof. Given $r: c \to d$ in $C$, let $ev_c: Hom_l(C, B) \to B$ denote the 2-functor which evaluates at $c$ (keep in mind that the 1-cells in $Hom_l(C, B)$ are transformations which are oplax in the sense of B&#233;nabou), and let $ev_r: ev_c \to ev_d$ denote the evident transformation; this is _lax_ in the sense of B&#233;nabou. Then, by dualizing proposition 1, $ev_r(\alpha) = \alpha \cdot r$ is an isomorphism if $\alpha$ is a _right_ adjoint. Since $\alpha \cdot r$ is an isomorphism for all 1-cells $r$ in $C$, it follows that $\alpha$ is strong. $\Box$ 

This completes the argument that the symmetric monoidal structure on $Map(B)$ extends to $B$. 

### Comparison with Carboni-Walters 

Let us begin unpacking the terse definition of cartesian bicategory so that it becomes more recognizable. For the sake of notational convenience, we use the fact that as a monoidal bicategory, a cartesian bicategory may be strictified and replaced by a (monoidally biequivalent) $Gray$ monoid $B$. That is to say, if $\otimes_G$ denotes the tensor product of the symmetric monoidal closed category $Gray$, then there is firstly a biequivalence $B \times B \simeq B \otimes_G B$, and we may transfer the data of the cartesian structure across this biequivalence to get a $Gray$ monoid multiplication 

$$\otimes: B \otimes_G B \to B$$ 

together with a corresponding diagonal 

$$B \overset{\Delta}{\to} B \times B \simeq B \otimes_G B$$ 

which we again denote by $\Delta$. In that case, given a 1-cell $r: a \to b$ in $B$, we may write structure cells $\delta \cdot r$ for the transformation $\delta: 1_B \to \otimes \Delta$ in the form 

$$\array{
a & \overset{\delta a}{\to} & a \otimes a\\
r \downarrow & \overset{\delta \cdot r}{\Rightarrow} & \downarrow r \otimes r\\
b & \underset{\delta b}{\to} & b \otimes b
}$$

where to be definite we make the convention that $r \otimes r := (r \otimes 1)(1 \otimes r)$. 

An object $c$ of $B$, viewed as an object of a 2-category $Map(B)$ with 2-products, naturally carries a 2-comonoid (or pseudocomonoid) structure; the unit of the 2-adjunction $\Delta \dashv \otimes$ is the diagonal map 

$$\delta c: c \to c \otimes c,$$

i.e., the 2-comonoid comultiplication. The unit of the 2-adjunction $! \dashv I$ is the projection to the 2-terminal object

$$\varepsilon c: c \to I,$$ 

i.e., the 2-comonoid counit. (It is more usual to denote a (2-)terminal object by the symbol $1$, and from here on we will follow that practice, writing the projection as $\varepsilon c: c \to 1$, and forget $I$.) 

Spelling this out a little further, let us turn attention to the transformation $\pi: \Delta \otimes \to 1_{B \otimes_G B}$. The components of the transformation take the form 

$$\pi (a, b) = \langle \pi_1, \pi_2 \rangle: (a \otimes b, a \otimes b) \to (a, b)$$ 

where, as a consequence of how the 2-product $\otimes$ on $Map(B)$ is defined, we have the following formulas for the projections $\pi_1$, $\pi_2$: 

$$\pi_1 = (a \otimes b \overset{1_a \otimes \varepsilon}{\to} a \otimes 1 \cong a); \qquad \pi_2 = (a \otimes b \overset{\varepsilon \otimes 1_b}{\to} 1 \otimes b \cong b$$ 

Thus, the unit and counit data $\delta$, $\pi$ are expressible in terms of the symmetric monoidal 2-category structure and the comonoid structures on the objects therein.

Finally, for a given 1-cell $r: c \to d$ in $B$, the structure cells 

$$\array{
c & \overset{\delta c}{\to} & c \otimes c & & & & c & \overset{\varepsilon c}{\to} & 1\\
r \downarrow & \overset{\delta \cdot r}{\Rightarrow} & \downarrow r \otimes r & & & & r \downarrow & \overset{\varepsilon \cdot r}{\Rightarrow} & \downarrow id_1\\
d & \underset{\delta d}{\to} & d \otimes d & & & & d & \underset{\varepsilon d}{\to} & 1
}$$

exhibit $r: c \to d$ as a colax morphism of 2-comonoids; if $r$ is a map, then $\delta \cdot r$ and $\varepsilon \cdot r$ are isomorphisms and $r$ becomes a strong morphism of 2-comonoids. This may be appreciated more fully by considering specific examples such as $B = Rel$ (where maps are functions, which become comonoid morphisms by virtue of naturality of diagonal and projection maps), and $B = Mod$. 

Carboni and Walters define a cartesian bicategory to be a symmetric monoidal bicategory in which each object carries a 2-comonoid structure (for which the comultiplication and counit are _maps_), and each 1-cell is a colax morphism between the corresponding comonoid structures. However, spelling this approach out in full detail leads to a rather largish definition; it seems more efficient to approach the definition by taking advantage of some high-level 2-categorical algebra as we have done here, and deriving the structures envisaged by Carboni and Walters as a consequence. 

### Local cartesian products 

The definition of cartesian structure _a fortiori_ involves _lax_ adjunctions (in the sense explained earlier) 

$$\Delta \dashv_{lax} \otimes: B \times B \to B \qquad ! \dashv_{lax} I: \mathbf{1} \to B$$ 

and by our earlier discussion of lax adjunctions, this means we have local 1-adjunctions of the form 

$$(B(a, b \otimes c) \stackrel{\lambda}{\to} (B \times B)(\langle a, a \rangle, \langle b, c \rangle)) \dashv (B \times B)(\langle a, a \rangle, \langle b, c \rangle)) \stackrel{\rho}{\to} B(a, b \otimes c))$$

Now let $b = c$, and use the fact that we have an adjunction 

$$(b \stackrel{\delta b}{\to} b \otimes b) \dashv (b \otimes b \stackrel{\delta b^{\ast}}{\to} b)$$ 

to obtain an adjoint pair where 

$$B(a, b) \stackrel{B(a, \delta b)}{\to} B(a, b \otimes b) \stackrel{\lambda}{\to} B \times B(\langle a, a \rangle, \langle b, b \rangle)$$ 

is left adjoint to 

$$B \times B(\langle a, a \rangle, \langle b, b \rangle) \stackrel{\rho}{\to} B(a, b \otimes b) \stackrel{B(a, \delta b^\ast)}{\to} B(a, b).$$ 

The first of these arrows is just the diagonal functor 

$$B(a, b) \stackrel{\delta_{loc}}{\to} B(a, b) \times B(a, b)$$ 

on the local hom-category $B(a, b)$. Therefore the second arrow, being right adjoint to the first, provides a product functor on $B(a, b)$. Similarly, each local hom-category carries a terminal object $1 \to \hom(a, b)$. We may summarize this by saying that cartesian bicategories are _locally cartesian_. 

### Essential uniqueness of cartesian structure 

So far we have seen that for a cartesian bicategory $B$, 

* $Map(B)$ carries 2-products, 

* Local hom-categories carry products. 

It is clear that 2-product data on $Map(B)$ and local product data on local hom-categories are uniquely determined up to appropriate notions of equivalence, since they are determined by appropriate universal properties. 
Now we show that these data actually determine the whole of the cartesian structure. We may therefore conclude that a cartesian structure on a bicategory must be essentially unique, if it exists. 

To explain how this works, it helps to consider some simple examples of cartesian bicategories such as $Rel$. First, let us reconstruct 

$$\otimes: B \times B \to B$$ 

from the data above. Suppose given two 1-cells $r: a \to b$, $s: c \to d$ in $B$, e.g., relations between sets, or even just subsets $r \subseteq b$, $s \subseteq d$. The tensor product $r \otimes s$ is intuitively a "rectangle", like $r \times s \subseteq b \times d$ in the case of $Rel$, obtained by "pulling back" $r$ along the projection $\pi_1: b \times d \to b$, pulling back $s$ along the projection $\pi_2: b \times d \to d$, and taking the intersection -- more generally, taking a local product. By formalizing this procedure, we are led to the general formula 

$$r \otimes s \cong (\pi_{1, b, d}^{\ast} r \pi_{1, a, c}) \times_{loc} (\pi_{2, b, d}^{\ast} s \pi_{2, a, c})$$ 

where $r$ and $s$ play the role of mere placeholders. 

It is a theorem (whose proof we defer) is that in a cartesian bicategory, we may reconstruct the functor $- \otimes -$ by the formula 

$$(\pi_{1}^{\ast} (-) \pi_{1}) \times_{loc} (\pi_{2}^{\ast} (-) \pi_{2})$$ 

where each of the displayed data is manifestly part of the 2-product structure on $Map(B)$ or the local cartesian structure. 

The other data we are required to reconstruct are structure cells like $\delta r$, $\pi \langle r, s\rangle$ which pertain to the transformations $\delta$, $\pi$. As an example, consider $\delta r$. This is a 2-cell 

$$\delta r: (\delta b)r \to (r \otimes r)(\delta a)$$ 

which is mated to a 2-cell

$$r \to (\delta b)^\ast (r \otimes r) \delta = r \times_{loc} r.$$ 

This 2-cell is precisely the local diagonal $r \to r \times r$, manifestly part of the local cartesian structure. Thus the structure cells for $\delta$ are uniquely determined, and similarly for the transformations $\pi$ and $\varepsilon$. 

This completes the sketched proof of essential uniqueness. 

## Cartesian bicategories and hyperdoctrines 

Each cartesian bicategory $\mathbf{B}$ gives rise to a bifibration, or in other language a (weak) 2-functor 

$$\mathbf{B}(i-, i-): Map(\mathbf{B})^{op} \times Map(\mathbf{B}) \to Cat$$ 

or in other words a $Cat$-valued bimodule over $Map(\mathbf{B})$, for which each $\mathbf{B}(i f, i c): \mathbf{B}(i b, i c) \to \mathbf{B}(i a, i c)$ has a left adjoint 

$$\mathbf{B}(f^\ast, i c): \mathbf{B}(i a, i c) \to \mathbf{B}(i b, i c)$$ 

and similarly each $\mathbf{B}(i c, i f): \mathbf{B}(i c, i a) \to \mathbf{B}(i c, i b)$ has a right adjoint $\mathbf{B}(i c, f^\ast)$. 

Thus, each cartesian bicategory gives rise to an $Ob(\mathbf{B})$-indexed family $\mathbf{B}(i-, c)$ of what we shall call ([_faute de mieux_]) generalized coherent hyperdoctrines: 

+-- {: .un_def} 
######Definition  
Let $C$ be a 2-category with 2-products. A **generalized coherent hyperdoctrine** over $C$ is a 2-functor 
$$P: C^{op} \to FPCat$$
to the 2-category of categories with finite products, such that for each 1-cell $f$ in $C$, the functor $P(f)$ has a left adjoint. 
=-- 

This is called a generalized coherent hyperdoctrine because it deals with a generalized form of coherent logic (involving finite "conjunctions", i.e., local finite cartesian products and existential quantifiers $\exists_f \dashv P(f)$). It is actually a weak form of coherent logic because we have not included finite "disjunctions", and we have said nothing yet about appropriate Beck-Chevalley conditions. (More will be said on this in a [section to follow](#frobenius).) It is generalized in the sense that the base category $C$ is actually a 2-category. 

If the symmetric monoidal bicategory $\mathbf{B}$ is _compact_ (e.g., if $\mathbf{B}$ is of type $Rel_C$ for $C$ a regular category, or $Span_C$ for $C$ a finitely complete category, or the bicategory of small categories and profunctors between them), then without loss of generality, we may restrict attention to the single hyperdoctrine 

$$\mathbf{B}(i-, 1): Map(\mathbf{B})^{op} \to FPCat$$ 

## Frobenius conditions
{#frobenius}  

A major class of examples of cartesian bicategories, including $Rel$, $Span$, and the bicategory of profunctors between groupoids, have the properties that 

* Each object is self-dual (in the sense of compact closed bicategories), 

* The bicategory of maps is locally groupoidal.

These arise as follows. In any cartesian bicategory and for each object $b$, there is a canonical 2-cell 

$$Frob_b: (\delta b)(\delta b)^\ast \to (1_b \otimes \delta b^\ast)(\delta b \otimes 1_b)$$ 

mated to the coassociativity isomorphism for $\delta$. We say the **Frobenius condition** holds if $Frob_b$ is an isomorphism for each $b$. This is equivalent to demanding that a similar canonical 2-cell 

$$Frob_{b}': (\delta b)(\delta b)^\ast \to (\delta b^\ast \otimes 1_b)(1_b \otimes \delta b)$$

be an isomorphism for each $b$. 

## References

* [[Aurelio Carboni]], [[Bob Walters]], _Cartesian Bicategories, I_, Journal of Pure and Applied Algebra, Volume 49, Issues 1–2, November 1987,  (<a href="https://doi.org/10.1016/0022-4049(87)90121-6">doi:10.1016/0022-4049(87)90121-6</a>)

* [[Aurelio Carboni]], [[Max Kelly]], [[Bob Walters]], [[Richard Wood]], _Cartesian Bicategories II_, Theory and Applications of Categories, Vol. 19, 2008, No. 6, pp 93-124. ([arXiv:0708.1921](https://arxiv.org/abs/0708.1921), [tac:19-06](http://www.tac.mta.ca/tac/volumes/19/6/19-06abs.html))

* [[Evan Patterson]], _Transposing cartesian and other structure in double categories_, [arXiv](https://arxiv.org/abs/2404.08835), 2024



[[!redirects cartesian bicategories]]
[[!redirects Cartesian bicategory]]
[[!redirects Cartesian bicategories]]
