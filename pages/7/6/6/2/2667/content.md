#Contents#
* automatic table of contents goes here
{:toc}


## Idea and definition ##

Classically, a **Schur functor** is a specific sort of [[functor]] 

$$F: FinVect_{\mathbb{C}} \to FinVect_{\mathbb{C}}$$ 

on the category of finite-dimensional complex [[vector space|vector spaces]].  Namely, it is a functor where $F(V)$ is obtained by taking a [[tensor power]] of $V$, say $V^{\otimes n}$, and then picking out the subspace that transforms according to a particular [[irreducible representation]] of the [[symmetric group]] $S_n$, which acts on $V^{\otimes n}$ by permuting the tensor factors.  

The irreducible complex representations of $S_n$ correspond to $n$-box [[Young diagram|Young diagrams]], so Schur functors of this sort are usually described with the help of Young diagrams.   An $n$-box Young diagram is simply a handy notation for a way of writing $n$ as a sum of natural numbers written in decreasing order.  For example, this 17-box Young diagram:

+-- {: #Young style="text-align:center"}
<svg width="120" height="140" xmlns="http://www.w3.org/2000/svg" se:nonce="39384" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <desc>Young diagram (5,4,4,2,1,1)</desc>
 <g>
  <title>Layer 1</title>
  <rect x="10" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_1"/>
  <rect x="30" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_2"/>
  <rect x="50" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_3"/>
  <rect x="70" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_4"/>
  <rect x="90" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_5"/>
  <rect x="10" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_6"/>
  <rect x="30" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_7"/>
  <rect x="50" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_8"/>
  <rect x="70" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_9"/>
  <rect x="10" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_10"/>
  <rect x="30" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_11"/>
  <rect x="50" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_12"/>
  <rect x="70" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_13"/>
  <rect x="10" y="70" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_14"/>
  <rect x="30" y="70" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_15"/>
  <rect x="10" y="90" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_16"/>
  <rect x="10" y="110" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_17"/>
 </g>
</svg>
=--

describes the partition of $17$ as $5 + 4 + 4 + 2 + 1 + 1$.  However, it also can be used to construct an irreducible complex representation of the permutation group $S_{17}$, and thus a Schur functor.

This is the beginning of a long and fascinating story connecting Schur functors with other objects that are named by Young diagrams: for example, elementary [[symmetric function|symmetric functions]] and [[cohomology]] classes on $BGL$, the classifying space for [[vector bundles]].  However, it is not really necessary to understand Young diagrams to begin understanding Schur functors.  As we shall see, one can go quite far simply noting that each irreducible representation of $S_n$ gives a functor from $Vect_{\mathbb{C}}$ to itself, as we have described.

More generally, any finite direct sum of such functors is also called a **Schur functor**.  There is a category $Schur_{\mathbb{C}}$ with these Schur functors as objects and natural transformations between them as morphisms.  Since the coproduct of all the symmetric groups $S_n$ is equivalent to the groupoid of finite sets and bijections, say $\mathbb{P}$, it is not surprising that

$$ Schur_{\mathbb{C}} \simeq [\mathbb{P}, FinVect_{\mathbb{C}}] \, , $$

where the the right-hand expression standard for the category with 

* functors $f: \mathbb{P} \to FinVect_{\mathbb{C}}$ as objects

* natural transformations between these as morphisms.

This category could be called the 'category of finite-dimensional complex representations of the groupoid of finite sets', but following the work of Joyal we shall call it the 'category of linear [[species]]'.  

The category of representations of any groupoid has many nice features: for example, it is a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]], meaning roughly that it has a well-behaved tensor product, direct sums, kernels, and cokernels.   So, the category $Schur$
has all these features.  But it is also [[semisimple abelian category|semisimple]]: indeed, every Schur functor is a finite direct sum of 'irreducible' Schur functors, which correspond to Young diagrams.

The category of representations of a groupoid has even more nice features when the groupoid itself has a [[monoidal category|monoidal structure]]: then the representation category acquires a monoidal structure thanks to [[Day convolution]].  The groupoid $\mathbb{P}$ has, in fact, _two_ important monoidal structures, coming from the product and disjoint union of finite sets --- and since product distributes over disjoint union, $\mathbb{P}$ is a [[rig category]].  This is all reflected in the category of Schur functors.

On top of all this, it turns out that the composite of Schur functors is again a Schur functor.    This gives the category

$$  [\mathbb{P}, FinVect_{\mathbb{C}}] \, , $$

yet another, perhaps unexpected monoidal structure.  In the classical literature this is called '[[plethysm]]'.

In more modern treatments, a Schur functor is a functor defined on [[module|modules]] over more general [[commutative ring]] $R$ (possibly with some conditions on $R$), so that "Schur functor" really connotes a family of functors 

$$F_R: Mod_R \to Mod_R  \, .$$ 

And indeed, much of the theory of Schur functors can be generalized even further, to categories of [[group representations]], [[vector bundles]], [[coherent sheaves]] and the like.  In this article, Todd Trimble and John Baez plan to explore the scope of such generality and --- we hope --- write a paper about what we find.

## Examples ##

The first thing that should be understood from the beginning is that a general Schur functor $F$ is _nonlinear_: the action on [[hom-set|hom-sets]] 

$$hom(V, W) \to hom(F(V), F(W))$$ 

is not assumed to respect the linear structure. In fact, linear Schur functors are rather uninteresting: because every finite-dimensional space is a finite [[direct sum]] of copies of the $1$-dimensional space $\mathbb{C}$, and because [[linear functor|linear functors]] preserve finite direct sums (that is, [[biproduct|biproducts]], it turns out that every linear Schur functor $F$ is [[representable functor|representable]] as $hom(X, -)$ where $X = F(\mathbb{C})$.  So, the category of linear Schur functors is equivalent to $FinVect_{\mathbb{C}}$. 

More representative examples of Schur functors include: 

* For each $k \geq 0$, the $k^{th}$ [[tensor power]] $V \mapsto V^{\otimes k}$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[symmetric algebra|symmetric power]] $V \mapsto S^k(V)$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[exterior algebra|alternating power]] $V \mapsto \Lambda^k(V)$ is a Schur functor. 

Even though Schur functors do not respect the linear structure on homsets, the category $Schur$ of Schur functors is nevertheless a [[linear category]], so we can talk about [[simple objects]], decompositions into [[direct sum|direct sums]], and so on. It turns out that every Schur functor $F$ can be expressed as a direct sum of irreducible $Schur$-objects $S_\lambda$ indexed by [[Young diagram]]s $\lambda$, and these $S_\lambda$ are usually what people think of when they say "Schur functors". 

## Schur functors associated with Young diagrams ##

Functors such as the $k^{th}$ alternating power, $k^{th}$ symmetric power, etc. make sense in much wider contexts than just $FinVect_{\mathbb{C}}$.   In fact they can be applied to any [[symmetric monoidal category|symmetric monoidal]]
[[Cauchy complete category|Cauchy complete]] $k$-[[linear category]].  Here by **_k_-linear category** we mean a category enriched over $Vect_k$, where $k$ is a fixed field of characteristic zero.  Such a category is **Cauchy complete** when:

* it has [[biproducts]], also known as [[direct sums]], and 

* [[idempotent|idempotents]] [[split idempotent|split]].)

Henceforth we shall use $C$ to stand for any symmetric monoidal Cauchy-complete $k$-linear category.  To illustrate the full breadth of this generalization, here are a few examples:

* the category $FinVect_k$ of finite-dimensional vector spaces over $k$

* the category of [[representation|representations]] of any [[group]] on finite-dimensional vector spaces over $k$

* the category of finite-dimensional [[super vector space|super vector spaces]], [[graded vector space|super vector spaces]] or [[chain complexes]] of vector spaces over $k$

* for $k = \mathbb{R}$ (or $\mathbb{C})$, the category of finite-dimensional real (or complex) [[vector bundle|vector bundles]] over any [[topological space]], or smooth vector bundles over any smooth [[manifold]]

* the category of finite-dimensional algebraic vector bundles over any [[algebraic variety]] (or more generally, [[scheme]] or [[algebraic stack]]) over $k$

* the category of [[coherent sheaves]] of vector spaces over any algebraic variety (or scheme or algebraic stack) over $k$

These examples can be hybridized, and thus they multiply indefinitely: for example, we could take coherent sheaves of representations of some algebraic supergroup on finite-dimensional chain complexes of super-vector spaces, etc..  

Recall that by Maschke's theorem, for any finite group $G$, the [[group algebra]] $k[G]$ decomposes as a direct sum of matrix algebras 

$$\bigoplus_{\lambda} hom(V_\lambda, V_\lambda)$$ 

where $\lambda$ ranges over isomorphism classes of irreducible representations of $G$.   The identity elements of these matrix algebras $hom(V_\lambda, V_\lambda)$ thus correspond to certain special elements $p_\lambda \in k[G]$.   Clearly these elements are [[idempotent]]:

$$ p_\lambda^2 = p_\lambda \, . $$

We are particularly interested in the case $G = S_n$.  In this case, there is one idempotent $p_\lambda \in k[S_n]$ for each $n$-box Young diagram.  An explicit formula for it is well-known.   However, one of the charms of our treatment is that we do _not require Young diagrams to define and study Schur functors_.

The group algebra $k[S_n]$ lives as a [[monoid]] in the symmetric monoidal category $FinVect_k$.  In the next section we describe how to interpret it as living in $C$, by "change of base" from $FinVect_k$ to $C$.   This will let us use the idempotents $p_\lambda$ to construct idempotents on $V^{\otimes k}$ for any object $V \in C$.  Splitting these idempotents, we shall obtain the Schur functors $S_\lambda : C \to C$.

### Change of base ###

To achieve the desired change of base, let $Mat$ be the $k$-linear category whose objects are integers $m \geq 0$ and whose morphisms $m \to n$ are $m \times n$ matrices with entries in $k$. Because $C$ is Cauchy complete and in particular has finite biproducts (direct sums), there is an evident linear functor 

$$Mat \to C$$ 

which takes $m$ to $I^m$, the direct sum of $m$ copies of the tensor unit $I$. It is the unique linear functor taking $1$ to $I$, up to unique linear isomorphism. In the case $C = FinVect_k$, the linear functor 

$$Mat \to FinVect_k,$$ 

taking $1$ to $k$, is a linear equivalence (exhibiting $Mat$ as a [[skeleton]] of $C$). Thus we could equally well say that there is a linear functor 

$$i: FinVect_k \to C$$ 

which, up to unique linear isomorphism, is the unique linear functor taking $k$ to $I$. Notice that a [[symmetric monoidal functor]] of this form must take the tensor unit $k$ to $I$ (up to coherent isomorphism, as always), and in fact $i$ is symmetric monoidal, because there is a canonical isomorphism

$$I^m \otimes I^n \cong I^{m n},$$ 

using the fact that $\otimes$ preserves direct sums in each argument, and the fact that there is a canonical isomorphism $I \otimes I \cong I$. 

In summary, we have the following proposition. 

+-- {: .un_prop}
######Proposition 
There is exactly one symmetric monoidal linear functor 
$i: FinVect_k \to C$, up to symmetric monoidal linear isomorphism. 
=--

The symmetric monoidal functor $i$ therefore maps the group algebra $k[S_n]$, as a [[monoid]] in the monoidal category $FinVect_k$, to a monoid in $C$, which we again call $k[S_n]$ by abuse of notation.

How can we intepret the idempotents $p_\lambda \in k[S_n]$ in the category $C$?  The easiest way is to use the category-theoretic treatment of [[element|elements]].  Any element $v$ of a vector space $V$ can be reinterpreted as a morphism from $k$ to $V$, namely the unique map sending $1 \in k$ to $v \in V$.  So, we can think of $p_\lambda$ as a morphism from $k$ to $k[S_n]$.  Applying the functor $i$ to this, we obtain a morphism which we call

$$f_\lambda : I \to k[S_n]  $$

### Modules over a bimonoid ###

Next we exploit the fact that, just like any [[group algebra]], $k[S_n]$ is a [[bialgebra]] --- or in fancier language, a  [[bimonoid]] in the symmetric monoidal category $FinVect_k$.  Since $i : FinVect_k \to C$ is a symmetric monoidal functor, this means that $i$ carries $k[S_n]$ to a  bimonoid in $C$.  As noted above, we call this bimonoid by the same name, $k[S_n]$.

The category of modules over a bimonoid is a monoidal category. More explicitly, in the case of the bimonoid $k[S_n]$ in $C$ with comultiplication 

$$\delta: k[S_n] \to k[S_n] \otimes k[S_n] \,,$$

the tensor product $V \otimes W$ of two $k[S_n]$-modules in $C$ carries a module structure where the action is defined by 

$$k[S_n] \otimes V \otimes W \stackrel{\delta \otimes 1_{V \otimes W}}{\to} k[S_n] \otimes k[S_n] \otimes V \otimes W \stackrel{1 \otimes \sigma \otimes 1}{\to} k[S_n] \otimes V \otimes k[S_n] \otimes W \stackrel{\alpha_V \otimes \alpha_W}{\to} V \otimes W$$ 

where $\sigma$ is a symmetry isomorphism and $\alpha_V$, $\alpha_W$ are the actions on $V$ and $W$. 

### Definition of Schur functors on $C$ ###

Now we consider a particular case of tensor product representations. If $X$ is an object of $C$, the symmetric group $S_n$ has a representation on $X^{\otimes n}$.  Indeed, for each $\sigma \in S_n$, there is a corresponding symmetry isomorphism $X^{\otimes n} \to X^{\otimes n}$.  From this one may construct an action 

$$k[S_n] \otimes X^{\otimes n} \to X^{\otimes n}$$ 

which is the required representation.  

Next, note that each element $f_\lambda : I \to k[S_n]$ gives an endomorphism of $X^{\otimes n}$ defined by

$$ X^{\otimes n} \cong I \otimes X^{\otimes n} \stackrel{f_\lambda \otimes 1}{\to} k[S_n] \otimes X^{\otimes n} \to X^{\otimes n} $$

We call this endomorphism

$$ P_\lambda : X^{\otimes n} \to X^{\otimes n} $$

Note that in fact these morphisms are the components of a natural transformation from the functor $X \mapsto X^{\otimes n}$ to itself.  

A calculation shows that because $p_\lambda$ in the original group algebra $k[S_n]$ is idempotent, so is $P_\lambda$.  (Do it!!!)  Since idempotents split in $C$, we can form the cokernel of this idempotent.  

+-- {: .un_def}
######Definition 
The **Schur functor** $S_\lambda: C \to C$ is defined as follows.  Given an object $X$ of $C$, let $S_\lambda(X)$ be the cokernel of $P_\lambda : X^{\otimes n} \to X^{\otimes n}$.
Given a morphism $f: X \to Y$ in $C$, let $S_\lambda(f)$ be the unique map $S_\lambda(X) \to S_\lambda(Y)$ such that 
$$\array{
X^{\otimes n} & \to & S_\lambda(X) \\
f^{\otimes n} \downarrow \; \; & & \downarrow S_\lambda(f) \\
Y^{\otimes n} & \to & S_\nu(Y)
}$$ 
commutes, where the horizontal arrows are the cokernel maps.
=--

More generally we can define a **Schur functor**

$$  S_R : C \to C  $$

for any finite-dimensional representation $R$ of $S_n$, as follows.  We can write $R$ as a finite direct sum of irreducible representations:

$$  R = \bigoplus_i V_{\lambda_i}  $$

and then define 

$$  S_R(-) = \bigoplus_i S_{\lambda_i}(-) \, .$$ 

### Schur functors are "natural" ### 

Suppose now that we have a symmetric monoidal linear functor $G: C \to D$. We can think of $G$ as a "change of base category", and Schur functors are "natural" with respect to change of base. 

That is to say: if $G$ is a symmetric monoidal $k$-linear functor $C \to D$, then by definition $G$ preserves tensor products (at least up to coherent natural isomorphism), and $G$ will automatically preserve both direct sums (by linearity) as well as splittings of idempotents (as all functors do). Therefore, for a Schur functor $S_\lambda(X) = V_\lambda \otimes_{S_n} X^{\otimes n}$, we have natural isomorphisms 

$$\array{
S_{\lambda, D} (G X) = V_{\lambda, D} \otimes_{S_n} (G X)^{\otimes n} & \cong & V_{\lambda, D} \otimes_{S_n} G(X^{\otimes n}) \\
 & \cong & G(V_{\lambda, C}) \otimes_{S_n} G(X^{\otimes n}) \\
 & \cong & G(V_{\lambda, C} \otimes_{S_n} X^{\otimes n})
}$$ 

where the first isomorphism uses the symmetric monoidal structure of $G$; the second uses the fact that $V_{\lambda, D} \cong G(V_{\lambda, C})$ because there is, up to isomorphism, only one symmetric monoidal linear functor $FinVect_k \to D$; the third uses the symmetric monoidal structure again and preservation of idempotent splittings. 

The same principle holds if $R$ is any representation, obtained as a direct sum of irreducible representations $V_\lambda$ (precisely because $G$ preserves direct sums). In summary, Schur functors $S_R$ transfer "naturally" across change of base functors $G: C \to D$. 

## Conceptual description of Schur functors ##

As we have seen, Schur functors $S_R$ are definable under fairly mild hypotheses: for fields $k$ of characteristic zero, they can be defined on any symmetric monoidal $k$-linear category $C$ satisfying a mild cocompleteness condition: Cauchy completeness. So, for such $C$ we can define a Schur functor 

$$S_R: C \to C$$ 

and moreover, if $G: C \to D$ is a symmetric monoidal $k$-linear functor, the Schur functors on $C$ and $D$ are "naturally" compatible, in the sense that the diagram 

$$\array{
C & \stackrel{S_{R, C}}{\to} & C \\
G \downarrow & & \downarrow G \\
D & \underset{S_{R, D}}{\to} & D
}$$ 

commutes up to a canonical isomorphism $\phi_G: S_{R, D} \circ G \cong G \circ S_{R, C}$, and moreover these $\phi_G$ fit together sensibly when we compose symmetric monoidal linear functors. 

In this highly abstract framework, it may be wondered what is the essential role played by the representations $R$ of the symmetric group. The natural isomorphisms $\phi_G$ which relate the Schur functors across change of base $G: C \to D$ are a pleasant observation, but surely this is merely some general nonsense in the larger story of Schur functors, which are after all deeply studied and incredibly rich classical constructions? 

Let us put the question another way.  We have seen the Schur functors $S_R$ have a uniform (or "polymorphic") definition across all symmetric monoidal $k$-linear Cauchy complete categories $C$, one which is natural with respect to symmetric monoidal change of base functors $G: C \to D$.  More precisely: not quite natural in a strict sense, but _pseudonatural_ in the sense of making the naturality squares commute up to isomorphism. Now pseudonaturality is a very general phenomenon in 2-category theory.  So the question is: among all such pseudonatural transformations, what is special about the Schur functors? What extra properties pick out exactly the Schur functors from this class? 

The perhaps surprising answer is: no extra properties! That is, the Schur functors are _precisely_ those uniformly defined functors that are pseudonatural with respect to change of base! 

Let us now make this precise. Schur functors $S$ are defined on certain symmetric monoidal linear categories but respect neither the symmetric monoidal structure nor the linear structure. So, we have to forget some of the structure of the objects on which Schur functors are defined.   This focuses our attention on the 'forgetful' 2-functor

$$U: SymMonLinCauch \to Cat$$ 

where:

+-- {: .un_def}
######Definition 
**SymMonLinCauch** is the 2-category with

* small symmetric monoidal Cauchy-complete $k$-linear categories as objects,

* symmetric monoidal $k$-linear functors as morphisms,

* symmetric monoidal $k$-linear natural transformations as 2-morphisms.
=--

As we shall see, Schur functors correspond to [[pseudonatural transformations]] from $U$ to itself, and morphisms between Schur functors correspond to [[modifications]] between these pseudonatural transformations.  For the reader unaccustomed to these 2-categorical concepts, recall:

+-- {: .un_def} 
######Definition 
Given two 2-functors $U, V: S \stackrel{\to}{\to} C$ between 2-categories, a **pseudonatural transformation** $\phi: U \to V$ is a rule that assigns to each 0-cell $s$ of $S$ a 1-cell $\phi(s): U(s) \to V(s)$ of $C$, and to each 1-cell $f: s \to t$ a 2-cell $\phi(f)$:  
$$\array{
U(s) & \stackrel{\phi(s)}{\to} & V(s) \\
U(f) \downarrow & \phi(f) \swArrow & \downarrow V(f) \\
U(t) & \underset{\phi(t)}{\to} & V(t)
}$$ 
such that the following pasting diagram equalities hold (to be filled in). 
=-- 

+-- {: .un_def} 
######Definition 
With notation as above, let $\phi, \psi: U \to V$ be two pseudonatural transformations. A **modification** $x: \phi \to \psi$ is a rule which associates to each 0-cell $s$ of $S$ a 2-cell $x(s): \phi(s) \to \psi(t)$ of $C$, such that the following compatibility condition holds (to be filled in). 
=-- 

We now propose our conceptual definition of Schur functor:

+-- {: .un_def} 
######Definition 
A **Schur functor** is a pseudonatural transformation $U \to U$, where 
$$U: SymMonLinCauch \to Cat$$ 
is the forgetful 2-functor. A **morphism** of Schur functors is a modification between such pseudonatural transformations. 
=-- 

What this proposed definition makes immediately clear is that _Schur functors are closed under composition_. This provides a satisfying conceptual explanation of _plethysm_, as we will explore in the next two sections. 

However, we must begin by checking that this proposed definition is equivalent to the more familiar one given earlier!

## Representability ##

To build a bridge from our abstract description of Schur functors as pseudonatural transformations to the more classical descriptions, we start with the following key result. 

+-- {: .un_thm}
######Theorem 
The underlying functor 
$$U: SymMonLinCauch \to Cat$$ 
is representable, in fact is represented by the Cauchy completion of the $k$-linearization of the groupoid of finite permutations $\mathbb{P}$. (If $k \mathbb{P}$ denotes the $k$-linearization, then $\widebar{k \mathbb{P}}$ denotes its Cauchy completion.) 
=-- 

+-- {: .proof} 
######Proof (Sketch)
It is well-known that the permutation category $\mathbb{P}$, whose objects are integers $m \geq 0$ and whose morphisms are precisely automorphisms $m \to m$ given by permutation groups $S_m$, is the representing object for the underlying 2-functor 

$$U_0: SymMonCat \to Cat \, .$$

Let $SymMonLin$ denote the 2-category of symmetric monoidal $k$-linear (but not necessarily linearly Cauchy complete) categories, and let $Lin$ denote the 2-category of small $k$-linear categories. Let $k(-): Cat \to Lin$ denote $k$-linearization, given by change of hom-base 

$$k \cdot - : Set \to Vect_k$$ 

applied to a small $Set$-enriched category $(C_0, hom: C_0 \times C_0 \to Set)$ to yield a $k$-linear category $(C_0, C_0 \times C_0 \to Vect_k)$. $k(-): Cat \to Lin$ is left 2-adjoint to the underlying 2-functor $u: Lin \to Cat$, and the 2-adjunction $k(-) \dashv u$ has a lifts to the level of symmetric monoidal structure, where we obtain a 2-adjunction 

$$(k(-): SymMonCat \to SymMonLin) \dashv (U_1: SymMonLin \to SymMonCat)$$ 

Finally, let $LinCauch$ denote the 2-category of $k$-linearly Cauchy-complete categories. The linear Cauchy completion gives a 2-reflector $\widebar{(-)}: Lin \to LinCat$ which is left 2-adjoint to the 2-embedding $i: LinCauch \to Lin$, and again the 2-adjunction $\widebar{(-)} \dashv i$ lifts to the level of symmetric monoidal structure to give a 2-adjunction 

$$(\widebar{(-)}: SymMonLin \to SymMonLinCauch) \dashv (U_2: SymMonLinCauch \to SymMonLin)$$ 

Putting this all together, the underlying functor $U: SymMonLinCauch \to Cat$ is the evident composite 

$$SymMonLinCauch \stackrel{U_2}{\to} SymMonLin \stackrel{U_1}{\to} SymMonCat \stackrel{U_0}{\to} Cat$$ 

and therefore we have pseudonatural equivalences 

$$\array{
SymMonLinCauch(\widebar{k(\mathbb{P})}, -) & \cong & SymMonLin(k(\mathbb{P}), U_2 -) \\
 & \cong & SymMonCat(\mathbb{P}, U_1 U_2 -) \\
 & \cong & U_0 U_1 U_2 \\
 & \cong & U
}$$ 

so that $\widebar{k \mathbb{P}}$ is the representing object. 
=--

+-- {: .query}

[[John Baez]]: Todd, you write "It is well-known that the permutation category $\mathbb{P}$, whose objects are integers $m \geq 0$ and whose morphisms are precisely automorphisms $m \to m$ given by permutation groups $S_m$, is the representing object for the underlying 2-functor $U_0: SymMonCat \to Cat.$"  Could you provide a reference?  It seems obvious to me, but I'm really bad at proving these obvious-sounding things.  

Isn't this statement a way of saying that $\mathbb{P}$ is the free symmetric monoidal category on one object?   It seems you're starting with that idea and then using a chain of pseudoadjunctions to show that:

* $k \mathbb{P}$ is the free symmetric monoidal $k$-linear category on one object, and 

* $\overline{k \mathbb{P}}$ is the free symmetric monoidal Cauchy complete $k$-linear category on one object.

Maybe something very general is going on here, which I shudder to contemplate.  We know that if $X$ is a 2-category of pseudoalgebras for some pseudomonoid on $Cat$, we get a pseudoadjunction 

$$  U : X \to Cat $$ 

$$  F: Cat \to X $$

But in the examples we're dealing with --- namely $X = SymMonCat, SymMonLin$ and $SymMonLinCauch$ --- the forgetful 2-functor $U$ is representable by $F(1)$.  How often is that true?   Always, or only when some nice condition holds?

And then, in your big theorem below, you seem to be saying that in the examples we're dealing with, $U(F(1))$ can be recovered as the category of pseudonatural transformations from $U$ to itself, and modifications between these.  How often is that true?
  
Very cool stuff.

[[Todd Trimble|Todd]]: I'll respond in bits and pieces. Yes, precisely, you can rephrase the result I stated about $\mathbb{P}$ in terms of the free symmetric monoidal category on one generator. Thus, for the underlying functor $U: SymMonCat \to Cat$, the category of functors $1 \to U(M)$ (which is equivalent to $U(M)$) is equivalent to the category of symmetric monoidal functors $F(1) \to M$, or $\mathbb{P} \to M$. Hence $SymMon(\mathbb{P}, -)$ is equivalent to $U$. A reference might be your opetopes and weak n-cats paper with Jim, is it HDA3? :-) 

As far as those adjunction liftings go: for one of them, I'm taking advantage of something special about Cauchy completion. As you know, Cauchy completion is something that makes sense generally in enriched category theory. The special feature I seem to be using is that if $A \otimes B$ denotes the tensor product of two $V$-enriched categories, then there is a canonical enriched equivalence  
$$\overline{A} \otimes \overline{B} \simeq \overline{A \otimes B}$$
So Cauchy completion is, I assert, a strong 2-monoidal) functor on $V$-$Cat$. If you accept that, then it is fairly automatic that the Cauchy completion of an enriched monoidal category (i.e., a pseudomonoid in $V$-$Cat$) is automatically a monoidal category. Therefore, the Cauchy completion monad lifts to the level of monoidal categories. 

Jazzing this up slightly: Cauchy completion is actually 2-(symmetric monoidal) on $V$-$Cat$, and so takes pseudo-(commutative monoids) in $V$-$Cat$ (i.e., enriched symmetric monoidal categories) to pseudo-(commutative monoids). Hence the Cauchy completion monad lifts to the level of symmetric monoidal enriched categories. This sort of thing is generalizable to other sorts of doctrines involving operations $D^{\otimes n} \to D$ on $V$-$Cat$ -- hopefully the idea is clear by now. 

Something similar is happening for the other adjunction lifting I cited, the one involving $k$-linearization. Here, we start with the fact that if $V$ is a nice closed category (here $Vect_k$) -- in particular cocomplete -- then the lax monoidal functor $\hom(I, -): V \to Set$ has a left adjoint $- \cdot I: Set \to V$ (here $k$-linearization) which is strong (symmetric) monoidal. This induces a 2-functor $Cat = Set$-$Cat \to V$-$Cat$ which is strong 2-monoidal. It therefore sends pseudomonoids in $Set$-$Cat$ to pseudomonoids in $V$-$Cat$. Even the lax monoidal 2-functor $V$-$Cat \to Set$-$Cat$ sends pseudomonoids to pseudomonoids. Therefore, the monoidal 2-adjunction between $Cat$ and $V$-$Cat$ lifts to the level of pseudomonoids. Something similar can be said for pseudo-(commutative monoids). 

So getting now to your general question: if you have a 2-adjunction between 
a 2-(monoidal category) $X$ and the 2-(monoidal category) $Cat$, and if this 2-adjunction is lax 2-monoidal, then we can lift to a 2-adjunction between $PseudoMon(X)$ and $PseudoMon(Cat)$. If the 2-adjunction is lax 2-(symmetric monoidal), then you can similarly lift to the level of pseudo-(commutative monoids) in $X$ and in $Cat$. That seems to be the principle I'm implicitly using in both cases. 

As for your final question: if $U: X \to Cat$ is representable by an object $F(1)$ of $X$, then formally we have 
$$[U, U] \simeq [hom_X(F(1), -), hom_X(F(1), -)] \simeq hom_X(F(1), F(1)) \simeq U(F(1))$$ 
where the second equivalence is the 2-categorical Yoneda lemma and the third uses the equivalence $hom_X(F(1), -) \simeq U$. 

=--


### Structure of the representing object

Let us now calculate $\widebar{k \mathbb{P}}$. It is the linear category of all $k$-linear functors 

$$k\mathbb{P}^{op} \to Vect_k$$  

which as modules are left adjoint to modules 

$$k\mathbb{P} \to Vect_k .$$ 

But since $k\mathbb{P}$ is the coproduct of the one-object $k$-linear categories $k S_n$, this comes down to a sequence of right modules 

$$(k S_n)^{op} \to Vect_k$$ 

which are left adjoint to modules $k S_n \to Vect_k$. As is well known, these adjoint modules are the finitely generated projective right modules over $S_n$. 

Hence an object of the Cauchy completion $\widebar{k \mathbb{P}}$ is given by a sequence of finitely generated projective $S_n$-modules, one for each $n$. Now in characteristic zero, Maschke's theorem (all short exact sequences of $S_n$-modules split) implies that all finitely generated $S_n$-modules are projective. Thus, finitely generated projective $S_n$-modules boil down to finite-dimensional representations of $S_n$. 

Therefore an object of the Cauchy completion is a sequence of finite-dimensional $S_n$-modules, in other words a functor $\mathbb{P}^{op} \to Vect_k$ valued in finite-dimensional spaces. In summary, we have the following result. 

+-- {: .un_thm} 
######Theorem 
The representing object $\widebar{k \mathbb{P}}$ is equivalent to the symmetric monoidal category of functors $\mathbb{P}^{op} \to FinVect_k$. 
=-- 

Functors of the form $\mathbb{P}^{op} \to V$ go by many names, but here we will call them _species_ (after Joyal). 

The linear symmetric monoidal structure on species is inherited from the monoidal structure of $\mathbb{P}$. Explicitly, the monoidal structure on $\mathbb{P}$ is at the object level given by adding integers, and on the morphism level given by group homomorphisms 

$$S_m \times S_n \to S_{m+n}$$ 

which juxtapose permutations. This is linearized to give algebra maps 

$$k[S_m] \otimes k[S_n] \to k[S_{m+n}]$$ 

which gives the structure of $k\mathbb{P}$. This structure uniquely extends to the Cauchy completion $\widebar{k\mathbb{P}}$, which is intermediate between $k\mathbb{P}$ and $Vect_k$-valued presheaves on $k\mathbb{P}$, according to Day convolution. The general formula for presheaves (species) $F, G: \mathbb{P}^{op} \to Vect_k$ is 

$$(F \otimes G)(n) = \sum_{j+k = n} (F(j) \otimes G(k)) \otimes_{S_j \times S_k} S_n$$

or, in other notation, 

$$(F \otimes G)(n) = \sum_{j+k = n} Ind_{S_j \times S_k}^{S_n} F(j) \otimes G(k)$$

and by restriction this formula gives the tensor product on species $F$ valued in finite-dimensional spaces. 

This completes the description of the representing object $\widebar{k\mathbb{P}}$. 

Now, having defined Schur functors abstractly as pseudonatural transformations $U \to U$, the representability theorem together with the 2-categorical Yoneda lemma means that the category of Schur functors is equivalent to the category of symmetric monoidal linear functors on $\widebar{k \mathbb{P}}$. Accordingly, we calculate 

$$[U, U] \cong SymMonLinCauch(\widebar{k\mathbb{P}}, \widebar{k\mathbb{P}}) \cong U(\widebar{k\mathbb{P}})$$ 

In other words, 

+-- {: .un_thm}
######Theorem 
The category of (abstract) Schur functors is equivalent to the functor category $[\mathbb{P}^{op},FinVect_k]$. 
=-- 

We will accordingly call a species of the form $\mathbb{P}^{op} \to FinVect_k$ a **Schur object**. 

NB: This theorem refers only to the underlying category. In other words, this category certainy has linear tensor category structure as well, but this structure is not respected by Schur functor composition which we consider next. 

## Composition of Schur functors ##

Now we consider composition of Schur functors $U \to U$, or equivalently symmetric monoidal linear functors $\widebar{k\mathbb{P}} \to \widebar{k \mathbb{P}}$. Composition endows $[U, U]$ with a monoidal structure, and this monoidal structure transfers across the equivalence to a monoidal structure on the underlying category of Schur objects $\mathbb{P}^{op} \to FinVect_k$, which we proceed to analyze. 

It may be easier to do this in reverse. Start with a Schur object, i.e., a functor: 

$$1 \stackrel{F}{\to} [\mathbb{P}^{op}, FinVect_k].$$ 

This induces a symmetric monoidal functor, unique up to (unique) symmetric monoidal isomorphism: 

$$\mathbb{P} \stackrel{F^\sim}{\to} [\mathbb{P}^{op}, FinVect_k]: m \mapsto F^{\otimes m}$$ 

Here $F^{\otimes m}$ is a Day convolution product of $m$ copies of $F$. Finally, the functor $F^\sim$ is linearized and extended (uniquely) to the linear Cauchy completion, to give a symmetric monoidal linear functor on $\widebar{k \mathbb{P}}$. The efficient tensor product description is 

$$- \otimes_{\mathbb{P}} F^\sim: [\mathbb{P}^{op}, FinVect_k] \to [\mathbb{P}^{op}, FinVect_k]$$ 

as this manifestly preserves colimits in the blank argument and therefore all colimits needed for the Cauchy completion. (And since the extension to the Cauchy completion is unique, this formula must be correct!) 

In the language of species, this construction is called the _substitution product_, and is denoted $G \circ F$. Thus, 

$$G \circ F = G \otimes_{\mathbb{P}} F^\sim$$ 

In notation which looks slightly less abstract, this is the Schur object given by the formula 

$$(G \circ F)(n) = \bigoplus_{n \geq 0} G(n) \otimes_{S_n} F^{\otimes n}$$ 

although 

(To be continued.) 

There's a Schur functor from a symmetric monoidal category to itself for every $\mathbb{Z}[S_n]$ module $M$, given by 
$$S_M(X)=X^{\otimes n}\otimes_{\Z[S_n]}M.$$

The composition of these functors corresponds to a strange monoidal structure on $\oplus_n\mathbb{Z}[S_n]$-mod, given by plethysm:
$$M\boxtimes N=\mathrm{Ind}_{S_n\wr S_m}^{S_{mn}} M\wr N.$$

The Schur functors described above are those corresponding to irreducible modules over $\mathbb{Q}$. 

[[!redirects Schur functors]]