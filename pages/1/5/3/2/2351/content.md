## Idea 

A cartesian bicategory is a bicategory with properties that make it behave like a bicategory of generalized relations. The bicategory of relations of a regular category, the bicategory of spans in a finitely complete category, and the bicategory of modules (profunctors) in a finitely complete category are all examples of cartesian bicategories. 

The rough idea is that a cartesian bicategory, viewed as an abstract bicategory of relations, should possess a tensor product which behaves like cartesian product on relations, and therefore like a categorical product for relations that are "functional". The structure of such a tensor is property-like (is essentially unique when it exists). Like allegories, cartesian bicategories are a convenient abstract setting in which to study the calculus of relations, but unlike allegories they embrace important examples like $Span$ and $Mod$. 

The original idea, due to Carboni and Walters, clearly envisioned these various examples but was initially confined to the locally posetal case; in part this was due to the lack at the time (circa 1987) of a solid theory of symmetric monoidal bicategories. In more recent years a full bicategorical treatment has been given, due principally to Carboni, Kelly, Verity, and Wood. The alternative treatment which we give below has not yet appeared in the literature as far as this author ([[Todd Trimble]]) is aware. 

## Technical preliminaries 

Note: All compositions will be written in the traditional order, in which application proceeds from right to left. 

We work with familiar notions of bicategory theory (which we often call 2-categories) but in some cases under new names. We calculate with pasting diagrams in 2-categories as if they were strict 2-categories. 

Our notion of morphism between 2-categories has gone under various names: "homomorphism" in the sense of B&#233;nabou, also known as "pseudofunctor" or weak 2-functor, where the structural constraints are isomorphisms. Here they are simply called **2-functors**. 

Each 2-category $B$ gives rise to a hom 2-functor $hom: B^{op} \times B \to Cat$, which we denote by $B(-, -)$, with the contravariant argument in the first place as is customary. 

Given 2-functors $F, G: B \to C$, it is for our purposes convenient to use the [[lax natural transformation|lax notion of morphism]] $\theta: F \to G$ between 2-functors for which the structural cells $\theta \cdot f$ (for 1-cells $f: a \to b$ in $B$) point in the direction 

$$\array{
F a & \overset{\theta a}{\to} & G a\\
F f \downarrow & \overset{\theta \cdot f}{\Rightarrow} & \downarrow G f\\
F b & \underset{\theta b}{\to} & G b
}$$ 

These are called "oplax transformations" by B&#233;nabou and "lax transformations" by other authors such as Johnstone; on this page we will simply call them (2-)**transformations**. A transformation is **strong** if the structural cells $\theta \cdot f$ are isomorphisms. 

There is a well-known notion of morphism between transformation which has been called [[modification]]. We retain this usage, but note that for the purposes of higher category theory, it is probably ill-advised to invent a new term (e.g. "perturbation" between modifications) each time one reaches a new depth of morphism -- a more uniform terminology is called for. The term "transfor" (due to Sjoerd Crans) has been gaining some recent currency; modifications may then be called **2-transfors**. 

Given 2-categories $B$ and $C$, we have then a 2-category of 2-functors, strong transformations and modifications from $B$ to $C$; this will be denoted $Hom_s(B, C)$. We have also the 2-category of 2-functors, transformations, and modifications; this will be denoted $Hom_l(B, C)$. 

A **2-adjunction** $F \dashv G$ consists of 2-functors $F: B \to C$, $G: C \to B$, and an adjoint equivalence 

$$C(F -, -) \simeq B(-, G -)$$ 

in the 2-category $Hom_s(B^{op} \times C, Cat)$. In more elementary terms, the data of a 2-adjunction is given by strong transformations 

$$\eta: 1_B \to G F \qquad \varepsilon: F G \to 1_C$$ 

and invertible modifications 

$$\array{
G & \overset{\eta G}{\to} & G F G & & & & F & \overset{F\eta}{\to} & F G F\\ 
1_G \searrow & \overset{s}{\Rightarrow} & \downarrow G \varepsilon & & & & 1_F \searrow & \overset{t}{\Leftarrow} & \downarrow \varepsilon F\\ 
 & & G & & & & & & F
}$$

such that the triangulator coherence conditions hold: there are pasting diagram equalities 

$$\array{
1_C & \overset{\eta}{\to} & G F & \overset{1_{G F}}{\to} & G F & & & & 1_C & \overset{\eta}{\to} & G F & \overset{1_{G F}}{\to} & G F\\ 
\eta \searrow & \swArrow \eta\eta & G F \eta \searrow & \Downarrow (s F)^{-1} & \nearrow G \varepsilon F & & = & & \eta \searrow & = & G F \eta \searrow & \Downarrow G t & \nearrow G \varepsilon F\\ 
 & G F & \underset{G F \eta}{\to} & G F G F & & & & & & G F & \underset{G F \eta}{\to} & G F G F &
}$$

$\, $ 

$$\array{
F G & \overset{1_{F G}}{\to} & F G & \overset{\varepsilon}{\to} & 1_B & & & & F G & \overset{1_{F G}}{\to} & F G & \overset{\varepsilon}{\to} & 1_B\\ 
F \eta G \searrow & \Downarrow (F s)^{-1} & \nearrow F G \varepsilon & \seArrow \varepsilon \varepsilon & \nearrow \varepsilon & & = & & F \eta G \searrow & \Downarrow t G & \nearrow \varepsilon F G & = & \nearrow \varepsilon & \\
 & F G F G & \underset{\varepsilon F G}{\to} & F G & & & & & & F G F G & \underset{\varepsilon F G}{\to} & F G & 
}$$

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

The triangular equations for $L \dashv R$ follow from the triangulator coherence conditions. (Warning: it is not generally true that a lax adjunction induces an adjoint pair in $Hom_l(B^{op} \times C, Cat)$.) 

Let $B$ be a 2-category. By definition, a *map* in $B$ is a 1-cell in $B$ that possesses a right adjoint. It is useful to think of them as playing the role of "functional relations" in an ambient 2-category of relations. We let $Map(B)$ be the locally full sub-2-category whose 0-cells are those of $B$ and whose 1-cells are the maps in $B$. We observe that every 2-functor $F: B \to C$ restricts to a 2-functor $F|: Map(B) \to Map(C)$, and by the following proposition, every transformation $\theta: F \to G$ restricts to a strong transformation $\theta$ in $Hom_s(Map(B), C)$: 

**Proposition 1:** If $f: b \to c$ is a map in $B$, then $\theta \cdot f$ is invertible. 

**Proof:** Let $f^*$ denote a right adjoint of $f$. It is easily verified that the diagram 

$$\array{
F b & \overset{F f}{\to} & F c & \overset{\theta c}{\to} & G c & \overset{1_{G c}}{\to} & G c\\
1_{F b} \downarrow & \Rightarrow & F f^* \downarrow & \overset{\theta \cdot f^*}{\Rightarrow} & \downarrow G f^* & \Rightarrow & \downarrow 1_{G c}\\
F b & \underset{1_{F b}}{\to} & F b & \underset{\theta b}{\to} & G b & \underset{G f}{\to} & G c
}$$

pastes to give the inverse $(\theta \cdot f)^{-1}$, where the left and right squares are the unit and counit of adjunctions $F f \dashv F f^*$, $G f \dashv G f^*$. 

A transformation $\theta: F \to G: B \to C$ is **map-valued** if each 1-cell $\theta b$ is a map in $C$. By the previous proposition, a map-valued transformation $\theta$ in $Hom_l(B, C)$ restricts to a strong transformation $\theta|: F| \to G|$ in $Hom_s(Map(B), Map(C))$. 

## Definition of cartesian bicategory 

A **cartesian structure** on a bicategory $B$ consists of the following data: 

* 2-functors $\otimes: B \times B \to B$ and $I: \mathbf{1} \to B$, where $\mathbf{1}$ is the terminal 2-category; 

* Map-valued transformations 
$$\delta: 1_B \to \otimes \Delta, \qquad \pi: \Delta \Pi \to 1_{B \times B}, \qquad \varepsilon: 1_B \to I !$$ 
where $\Delta: B \to B \times B$ is the diagonal 2-functor and $!: B \to \mathbf{1}$ is the unique 2-functor; 

* Invertible modifications 
$$\array{
\otimes & \overset{\delta \otimes}{\to} & \otimes \Delta \otimes & & & & \Delta & \overset{\Delta \delta}{\to} & \Delta \otimes \Delta & & & & I & \overset{\varepsilon I}{\to} & I ! I\\
1_{\otimes} \downarrow & \overset{s}{\Rightarrow} & \downarrow \otimes \pi & & & & 1_{\Delta} \downarrow & \overset{t}{\Leftarrow} & \downarrow \pi \Delta & & & & 1_{I} \downarrow & \overset{u}{\Rightarrow} & \downarrow I \cdot id\\
\otimes & \underset{1_{\otimes}}{\to} & \otimes & & & & \Delta & \underset{1_{\Delta}}{\to} & \Delta & & & & I & \underset{1_I}{\to} & I
}$$ 
satisfying the triangulator coherence conditions. $\Box$ 

The crucial observation is that, by proposition 1, this data restricts to give 2-adjunctions 

$$(Map(B) \overset{\Delta}{\to} Map(B) \times Map(B)) \dashv (Map(B) \times Map(B) \overset{\otimes}{\to} Map(B))$$ 

$\, $

$$(Map(B) \overset{!}{\to} \mathbf{1}) \dashv (\mathbf{1} \overset{I}{\to} Map(B))$$ 

so that $\otimes$ is a _2-product_ on $Map(B)$ and $I$ is 2-terminal in $Map(B)$. Naturally this finite 2-product structure on $Map(B)$ is property-like: is uniquely determined up to equivalence which is unique up to unique isomorphism. 

We now argue that cartesian structure on the full 2-category $B$ is also property-like.  

