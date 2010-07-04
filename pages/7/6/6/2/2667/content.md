#Contents#
* automatic table of contents goes here
{:toc}


## Idea and definition ##

Classically, a **Schur functor** is a specific sort of [[functor]] 

$$F: FinVect \to FinVect$$ 

where [[FinVect]] is the category of finite-dimensional complex [[vector space|vector spaces]].  Namely, it is a functor where $F(V)$ is obtained by taking a [[tensor power]] of $V$, say $V^{\otimes n}$, and then picking out the subspace that transforms according to a particular [[irreducible representation]] of the [[symmetric group]] $S_n$, which acts on $V^{\otimes n}$ by permuting the tensor factors.  

For example:

* For each $n \geq 0$, the $n^{th}$ [[symmetric power]] $V \mapsto S^n(V)$ is a Schur functor. 

* For each $n \geq 0$, the $n^{th}$ [[alternating power]] $V \mapsto \Lambda^n(V)$ is a Schur functor. 

More generally, irreducible complex representations of $S_n$ correspond to $n$-box [[Young diagram|Young diagrams]], so Schur functors are usually described with the help of these.   An $n$-box Young diagram is simply a handy notation for a way of writing $n$ as a sum of natural numbers written in decreasing order.  For example, this 17-box Young diagram:

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

In general, the recipe is this:

* Given an $n$-box Young diagram and a vector space $V$, we form first the tensor power $V^{\otimes n}$.  We think of each factor in this tensor power as corresponding to a specific box of the Young diagram.  

* Then we pick out the subspace of $V^{\otimes n}$ consisting of tensors that are _unchanged_ by any permutation that interchanges two boxes in the same _row_.  

* Then we project this subspace onto the space of tensors that _change sign_ under any permutation that interchanges two boxes in the same _column_.  

The resulting subspace of $V^{\otimes n}$ is invariant under the action of $S_n$ --- and in fact, it is a direct sum of copies of a specific irreducible representation of $S_n$.  

It is easy to see from this description that:

* The tall skinny Young diagrams with one column and $n$ rows give the Schur functors $\Lambda^n$.

* The short fat Young diagrams with one row and $n$ columns give the Schur functors $S^n$.

We can also think of this relation between Young diagrams and Schur functors in a slightly more abstract way, using the [[group algebra]] of the symmetric group, $\mathbb{C}[S_n]$.  Given an $n$-box Young diagram $\lambda$, we can think of the operation 'symmetrize with respect to permutations of the boxes in each row' as an element $p^S_\lambda \in \mathbb{C}[S_n]$.  Similarly, we can think of the operation 'antisymmetrize with respect to permutations of the boxes in each column' as an element $p^A_\lambda \in \mathbb{C}[S_n]$.  By construction, each of these elements is [[idempotent]]:

$$ (p^A_\lambda)^2 = p^A_\lambda \, , \; \; (p^S_\lambda)^2 = p^S_\lambda  $$

Now, it is easy to see that the product of commuting idempotents is idempotent.   The elements $p_S$ and $p_A$ do not commute, but amazingly, their product 

$$ p_\lambda = p^A_\lambda p^S_\lambda $$

is still idempotent!  The reason is that $p_\lambda$ commutes with all permutations, so it lies in the [[center]] of the group algebra.  This ensures that

$$ p_\lambda^2 = p^A_\lambda p^S_\lambda p^A_\lambda p^S_\lambda =
p^A_\lambda p^A_\lambda p^S_\lambda p^S_\lambda = p_\lambda $$

Checking that $p_\lambda$ commutes with all permutations is a calculation that you must do for yourself someday.

This element $p_\lambda \in \mathbb{C}[S_n]$ is called the **Young symmetrizer** corresponding to the $n$-box Young diagram $\lambda$.  Since the group algebra $k[S_n]$ acts on $V^{\otimes n}$ by permuting the factors, the Young symmetrizer gives a projection

$$ p_\lambda : V^{\otimes n} \to V^{\otimes n} $$

whose range is a subspace called $S_\lambda(V)$.  Since $p_\lambda$ commutes with everything in $k[S_n]$, this subspace is invariant under the action of $S_n$, and --- as already mentioned --- it is a direct sum of copies of a specific irreducible representation of $S_n$.   But the point is this: there is a functor, called a **Schur functor**: 

$$  S_\lambda : FinVect \to FinVect $$

which has precisely this effect on objects:

$$    V \mapsto S_\lambda(V) $$

This is the beginning of a long and fascinating story connecting Schur functors with other objects that are named by Young diagrams: for example, elementary [[symmetric function|symmetric functions]] and [[characteristic classes]] for complex [[vector bundles]].  However, it is not really necessary to understand the details of Young diagrams, Young symmetrizers, or any of this other material, to begin understanding Schur functors.  As we shall see, one can go quite far simply noting that each irreducible representation of $S_n$ gives a functor from $FinVect$ to itself!

## The category of Schur functors

More generally, any finite direct sum of the Schur functors just described may also be called a **Schur functor**.   For example:

* For each $n \geq 0$, the $n^{th}$ [[tensor power]] $V \mapsto V^{\otimes n}$ is a Schur functor. 

* If $F$ and $G$ are Schur functors, of course the functor $V \mapsto F(V) \oplus G(V)$ is a Schur functor.

* If $F$ and $G$ are Schur functors, the functor $V \mapsto F(V) \otimes G(V)$ is also a Schur functor.

*  If $F$ and $G$ are Schur functors, the composite $V \mapsto F(G(V))$ is a Schur functor.  This way of constructing Schur functors is known as [[plethysm]].

There is a category $Schur$ with these more general Schur functors as objects and natural transformations between them as morphisms.  In this article we would like to give a conceputal explanation of this category and some of its generalizations.

For starters, we can replace the complex numbers by any field $k$ of characteristic zero, and everything in our discussion still works.   Even better, the resulting category $\Schur$ has has a nice description in terms of groupoid of finite sets and bijections.  We will find it convenient to work with a skeleton of this groupoid, namely the [[permutation groupoid]]:

$$ \mathbb{P} = \bigsqcup_{n \ge 0} S_n \, , $$

where objects are natural numbers, all morphisms are automorphisms, and the automorphisms of the object $n$ form the group $S_n$.   In these terms, $Schur$ is equivalent to the category where:

* objects are functors $F: \mathbb{P} \to FinVect$ such that $F(n) = \{0\}$ for all sufficiently large $n$;

* morphisms are natural transformations.

This allows us to think of $Schur$ as a subcategory of the category of **representations** of $\mathbb{P}$, by which we simply mean functors $F : \mathbb{P} \to \Vect$.  Every irreducible representation of $\mathbb{P}$ is finite-dimensional: it is really just an irreducible representation of some group $S_n$.  Every representation of $\mathbb{P}$ is a direct sum of these irreducibles.  $Schur$ may be identified with the full subcategory consisting of _finite_ direct sums of irreducibles.

The category of representations of any groupoid has many nice features: for example, it is a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]], meaning roughly that it has a well-behaved tensor product, direct sums, kernels, and cokernels.   It is easy to check that $Schur$ inherits these features.  This gives $Schur$ two monoidal structures, $\oplus$ and $\otimes$, defined by

$$ (F \oplus G)(V) = F(V) \oplus G(V) $$

and 

$$ (F \otimes G)(V) = F(V) \otimes G(V) $$

These make $Schur$ into a [[rig category]].

But the category of representations of a groupoid has even more nice features when the groupoid itself has a [[monoidal category|monoidal structure]]: then the representation category acquires a monoidal structure thanks to [[Day convolution]].  The groupoid $\mathbb{P}$ has, in fact, _two_ important monoidal structures, coming from the product $\times$ and disjoint union $+$ of finite sets.  Since $\times$ distributes over $+$, these make $\mathbb{P}$ into a [[rig category]].   Thanks to Day convolution, these give the category of representations of $\mathbb{P}$ two more monoidal structures, making it into a rig category in another way.  The same is true for the subcategory $Schur$.  

On top of all this, the composite of Schur functors is again a Schur functor.   This gives $Schur$ yet another monoidal structure, the **plethystic tensor product**.  Unlike the four previous monoidal structures, this one is not symmetric.   

Mathematicians often work with a decategorified version of $Schur$: its [[Grothendieck group]], also known as the ring of [[symmetric functions]].  The various structures that $Schur$ possesses endow this ring with corresponding structures.  Among other things, it is the free [[lambda-ring]] on one generator.   As we shall see, corresponds to the fact that $Schur$ is the free [[symmetric monoidal category|symmetric monoidal]] [[Cauchy complete category|Cauchy complete]] [[linear category]] on one object.

## Schur functors on more general categories ##

We have described Schur functors as special functors

$$  F: FinVect \to FinVect  $$

But in fact, functors such as the $n^{th}$ alternating power, $n^{th}$ symmetric power, etc. make sense in much wider contexts.   In fact they can be applied to any [[symmetric monoidal category|symmetric monoidal]] [[Cauchy complete category|Cauchy complete]] [[linear category]].  Here by **linear category** we mean a category enriched over $Vect$, the category of vector spaces over a fixed field $k$ of characteristic zero.  Such a category is **Cauchy complete** when:

* it has [[biproducts]], also known as [[direct sums]], and 

* [[idempotent|idempotents]] [[split idempotent|split]].

To illustrate the full breadth of this generalization, here are a few examples:

* the category [[Vect]], consisting of vector spaces over any field $k$ of characteristic zero

* the category [[FinVect]], consisting of finite-dimensional vector spaces over $k$

* the category of [[representation|representations]] of any [[group]] on vector spaces (or finite-dimensional vector spaces) over $k$

* the category of [[super vector space|super vector spaces]], [[graded vector space|graded vector spaces]] or [[chain complexes]] over $k$

* for $k = \mathbb{R}$ or $\mathbb{C}$, the category of finite-dimensional real or complex [[vector bundle|vector bundles]] over any [[topological space]], or smooth vector bundles over any smooth [[manifold]]

* the category of algebraic vector bundles over any [[algebraic variety]] (or more generally, [[scheme]] or [[algebraic stack]]) over $k$

* the category of [[coherent sheaves]] of vector spaces over any algebraic variety (or scheme or algebraic stack) over $k$

These examples can be hybridized, and thus they multiply indefinitely: for example, we could take coherent sheaves of chain complexes, or vector bundles equipped with a group action, and so on.  

In the following subsections, we explain how to define Schur functors on any category of this sort.  A somewhat novel feature of our treatment is that we _do not require the theory of Young diagrams_ to define and study Schur functors.  

Our strategy is as follows.  We fix a symmetric monoidal Cauchy complete linear category, $C$. The group algebra $k[S_n]$ begins life as a [[monoid]] in the symmetric monoidal category $FinVect$.   However, we shall explain how interpret it as living in $C$ by a "change of base" functor going from $FinVect$ to $C$.   This will let us use the Young symmetrizers $p_\lambda$ to construct idempotents on $V^{\otimes k}$ for any object $V \in C$.  Splitting these idempotents, we obtain the Schur functors $S_\lambda : C \to C$.

### Change of base ###

To achieve the desired change of base, let $Mat$ be the linear category whose objects are integers $m \geq 0$ and whose morphisms $m \to n$ are $m \times n$ matrices with entries in $k$. Because $C$ is Cauchy complete and in particular has finite biproducts (direct sums), there is an evident linear functor 

$$Mat \to C$$ 

which takes $m$ to $I^m$, the direct sum of $m$ copies of the tensor unit $I$. It is the unique linear functor taking $1$ to $I$, up to unique linear isomorphism. In the case $C = FinVect$, the linear functor 

$$Mat \to FinVect,$$ 

taking $1$ to $k$, is a linear equivalence (exhibiting $Mat$ as a [[skeleton]] of $C$). Because of this equivalence, we could equally well say that there is a linear functor 

$$i: FinVect \to C$$ 

which, up to unique linear isomorphism, is the unique linear functor taking $k$ to $I$. Notice that a [[symmetric monoidal functor]] of this form must take the tensor unit $k$ to $I$ (up to coherent isomorphism, as always), and in fact $i$ is symmetric monoidal, because there is a canonical isomorphism

$$I^m \otimes I^n \cong I^{m n},$$ 

using the fact that $\otimes$ preserves direct sums in each argument, and the fact that there is a canonical isomorphism $I \otimes I \cong I$. 

In summary, we have the following proposition. 

+-- {: .un_prop}
######Proposition 
There is exactly one symmetric monoidal linear functor 
$i: FinVect \to C$, up to symmetric monoidal linear isomorphism. 
=--

### The action of Young symmetrizers ###

Next we explain how given an object $X \in C$, any Young symmetrizer in $k[S_n]$ acts as an idempotent on $X^{\otimes n}$.   

For this we only need to know a little bit about the group algebra $k[S_n]$, which we recall here.  By Maschke's theorem, for any finite group $G$, the [[group algebra]] $k[G]$ decomposes as a direct sum of matrix algebras 

$$\bigoplus_{\lambda} hom(V_\lambda, V_\lambda)$$ 

where $\lambda$ ranges over isomorphism classes of irreducible representations of $G$.   The identity elements of these matrix algebras $hom(V_\lambda, V_\lambda)$ thus correspond to certain special elements $p_\lambda \in k[G]$.   Clearly these elements are [[idempotent]]:

$$ p_\lambda^2 = p_\lambda \, . $$

We are particularly interested in the case $G = S_n$.  In this case, we call the idempotents $p_\lambda$ are 'Young symmetrizers'.  However, we will not need the formula for these idempotents.

The key step is to apply base change to $k[S_n]$.   Here we exploit the fact that

$$   k[S_n] = \bigoplus_{\sigma \in S_n}  k $$

is a [[monoid]] in the monoidal category $FinVect$.  Since $i : FinVect \to C$ is a monoidal functor, it follows that $i$ carries $k[S_n]$ to a monoid in $C$, which we again call $k[S_n]$ by abuse of notation.  As an object of $C$, we have

\[  k[S_n] \cong \bigoplus_{\sigma \in S_n}  I  \label{sum} \]

There is a general concept of what it means for a monoid in a monoidal category to [[action|act]] on an object in that category.  In particular, if $X$ is an object of $C$, the monoid $k[S_n]$ acts on the tensor power $X^{\otimes n}$.  To see this, note that for each $\sigma \in S_n$, there is a corresponding symmetry isomorphism 

$$ \sigma : X^{\otimes n} \to X^{\otimes n} $$

Putting these together with the help of \eqref{sum} we obtain a morphism

$$k[S_n] \otimes X^{\otimes n} \to X^{\otimes n}$$ 

which is the desired action.

Finally, we would like to describe how each Young symmetrizer $p_\lambda \in k[S_n]$ acts on $X^{\otimes n}$.    Quite generally, any  element $x \in k[S_n]$ gives a linear map from $k$ to $k[S_n]$, namely the unique map sending $1$ to $x$.   Applying the functor $i$ to this, we obtain a morphism which by abuse of language we call

$$ x : I \to k[S_n]$$ 
 
This then yields an endomorphism 

$$ \widetilde{x}: X^{\otimes n} \to X^{\otimes n }$$

given as the composite

$$ X^{\otimes n} \stackrel{\cong}{\longrightarrow} I \otimes X^{\otimes n} \stackrel{x \otimes 1}{\longrightarrow} k[S_n] \otimes X^{\otimes n} \longrightarrow X^{\otimes n} $$

It is easy to check that for any $x,y \in k[S_n]$, 

$$ \widetilde{x y} = \widetilde{x} \widetilde{y} $$

Thus for any Young symmetrizer $p_\lambda$, the morphism

$$ \widetilde{p}_\lambda : X^{\otimes n} \to X^{\otimes n} $$

is idempotent, because $p_\lambda$ is. 

### Constructing Schur functors ###

By construction, the morphisms 

$$ \widetilde{p}_\lambda : X^{\otimes n} \to X^{\otimes n} $$

are the components of a natural transformation from the functor $X \mapsto X^{\otimes n}$ to itself.  Since idempotents split in $C$, we can form the cokernel of $1 - \widetilde{p}_\lambda$, or in other words, the coequalizer of the pair 

$$ X^{\otimes n} \stackrel{\widetilde{p}_\lambda}{1} X^{\otimes n} $$

+-- {: .un_def}
######Definition 
For any Young diagram $\lambda$, the **Schur functor** $S_\lambda: C \to C$ is defined as follows.  Given an object $X$ of $C$, let $S_\lambda(X)$ be the cokernel of $ \widetilde{p}_\lambda : X^{\otimes n} \to X^{\otimes n}$.  Given a morphism $f: X \to Y$ in $C$, let $S_\lambda(f)$ be the unique map $S_\lambda(X) \to S_\lambda(Y)$ such that 
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

That is to say: if $G$ is a symmetric monoidal linear functor $C \to D$, then by definition $G$ preserves tensor products (at least up to coherent natural isomorphism), and $G$ will automatically preserve both direct sums (by linearity) as well as splittings of idempotents (as all functors do). Therefore, for a Schur functor $S_\lambda(X) = V_\lambda \otimes_{S_n} X^{\otimes n}$, we have natural isomorphisms 

$$\array{
S_{\lambda, D} (G X) = V_{\lambda, D} \otimes_{S_n} (G X)^{\otimes n} & \cong & V_{\lambda, D} \otimes_{S_n} G(X^{\otimes n}) \\
 & \cong & G(V_{\lambda, C}) \otimes_{S_n} G(X^{\otimes n}) \\
 & \cong & G(V_{\lambda, C} \otimes_{S_n} X^{\otimes n}) \\
 & \cong & G(S_{\lambda, C}(X))
}$$ 

where the first isomorphism uses the symmetric monoidal structure of $G$; the second uses the fact that $V_{\lambda, D} \cong G(V_{\lambda, C})$ because there is, up to isomorphism, only one symmetric monoidal linear functor $FinVect \to D$; the third uses the symmetric monoidal structure again and preservation of idempotent splittings. 

If $R$ is any representation, then by writing $R$ as a direct sum of irreducible representations $V_\lambda$ and using the fact that $G$ preserves direct sums, we have more generally 

$$S_{R, D} \circ G \cong G \circ S_{R, C}.$$

In summary, Schur functors $S_R$ transfer "naturally" across change of base functors $G: C \to D$. 

## Conceptual description of Schur functors ##

As we have seen, Schur functors $S_R$ are definable under fairly mild hypotheses: working over a field of characteristic zero, they can be defined on any symmetric monoidal linear category $C$ which is Cauchy complete.  So, for such $C$ we can define a Schur functor 

$$S_R: C \to C$$ 

and moreover, if $G: C \to D$ is a symmetric monoidal linear functor, the Schur functors on $C$ and $D$ are "naturally" compatible, in the sense that the diagram 

$$\array{
C & \stackrel{G}{\to} & D \\
S_{R, C} \downarrow & & \downarrow S_{R, D} \\
C & \underset{G}{\to} & D
}$$ 

commutes up to a canonical isomorphism $\phi_G: S_{R, D} \circ G \cong G \circ S_{R, C}$, and moreover these $\phi_G$ fit together sensibly when we compose symmetric monoidal linear functors. 

In this abstract framework, it may be wondered what significant role is played by the representations $R$ of the symmetric group. The natural isomorphisms $\phi_G$ which relate the Schur functors across change of base $G: C \to D$ are pleasant to observe, but surely this is just some piddling general nonsense in the larger story of Schur functors $S_R$, which are after all deeply studied and incredibly rich classical constructions? 

Let us put the question another way.  We have seen the Schur functors $S_R$ are constructed in a uniform (or "polymorphic") way across all symmetric monoidal Cauchy complete linear categories $C$, and this construction is natural with respect to symmetric monoidal change of base functors $G: C \to D$. Or rather: not natural in a strict sense, but _pseudonatural_ in the sense that naturality squares commute up to isomorphism $\phi_G$. Now pseudonaturality is a very general phenomenon in 2-category theory.  So the question is: among all such pseudonatural transformations $S$, what is special about the Schur functors $S_R$? What extra properties pick out exactly the Schur functors $S_R$ from the class of all pseudonatural transformations $S$? 

The perhaps surprising answer is: no extra properties! That is, the Schur functors $S_R$ are _precisely_ those functors that are defined on all symmetric monoidal Cauchy complete linear $C$ and that are pseudonatural with respect to change of base $G: C \to D$! 

Let us now make this precise. Schur functors are defined on certain symmetric monoidal linear categories, but they respect neither the symmetric monoidal structure nor the linear structure.  So, we have to forget some of the structure of the objects on which Schur functors are defined.   This focuses our attention on the 'forgetful' 2-functor

$$U: SymMonLinCauch \to Cat$$ 

where:

+-- {: .un_def}
######Definition 
**SymMonLinCauch** is the 2-category with

* small symmetric monoidal Cauchy complete linear categories as objects,

* symmetric monoidal linear functors as morphisms,

* symmetric monoidal linear natural transformations as 2-morphisms.
=--

As we shall see, Schur functors correspond to [[pseudonatural transformations]] from $U$ to itself, and morphisms between Schur functors correspond to [[modifications]] between these pseudonatural transformations.  For the reader unaccustomed to these 2-categorical concepts, we recall:

+-- {: .un_def} 
######Definition 
Given two 2-functors $U, V: S \stackrel{\to}{\to} C$ between 2-categories, a **pseudonatural transformation** $\phi: U \to V$ is a rule that assigns to each 0-cell $s$ of $S$ a 1-cell $\phi(s): U(s) \to V(s)$ of $C$, and to each 1-cell $f: r \to s$ of $S$ an invertible 2-cell $\phi(f)$ of $C$:  
$$\array{
U(r) & \stackrel{U(f)}{\to} & U(s) \\
\phi(r) \downarrow & \phi(f) \swArrow & \downarrow \phi(s) \\
V(r) & \underset{V(f)}{\to} & V(s)
}$$ 
such that the following pasting diagram equalities hold: 
$$\array{
U(r) & \stackrel{U(f)}{\to} & U(s) & \stackrel{U(g)}{\to} & U(t) & & U(r) & \stackrel{U(g f)}{\to} & U(t) & & \\
\phi(r) \downarrow & \phi(f) \swArrow & \downarrow \phi(s) & \phi(g) \swArrow & \downarrow \phi(t) & = & \phi(r) \downarrow & \phi(g f) \swArrow & \downarrow \phi(t) & & & \\
V(r) & \underset{V(f)}{\to} & V(s) & \underset{V(g)}{\to} & V(t) & & V(r) & \underset{V(g f)}{\to} & V(t) & & & 
}$$
and
$$\array{
 U(r) & \stackrel{U(1_r)}{\to} & U(r) & & \\
\phi(r) \downarrow & \phi(1_r) \swArrow & \downarrow \phi(r) & = & 1_{\phi(r)} \\
V(r) & \underset{V(1_r)}{\to} & V(r) & & 
}$$
=-- 

+-- {: .un_def} 
######Definition 
With notation as above, let $\phi, \psi: U \to V$ be two pseudonatural transformations. A **modification** $x: \phi \to \psi$ is a rule which associates to each 0-cell $s$ of $S$ a 2-cell $x(s): \phi(s) \to \psi(t)$ of $C$, such that the following compatibility condition holds:
=-- 

+-- {: style="text-align:center"}
[[tincan.png:pic]]
=--

We now propose our conceptual definition of Schur functor:

+-- {: .un_def} 
######Definition 
An (abstract) **Schur functor** is a pseudonatural transformation $S: U \to U$, where 
$$U: SymMonLinCauch \to Cat$$ 
is the forgetful 2-functor. A **morphism** of Schur functors is a modification between such pseudonatural transformations. 
=-- 

What this proposed definition makes manifestly obvious is that _Schur functors are closed under composition_. This provides a satisfying conceptual explanation of _plethysm_, as we will explore in the next two sections.  However, we should first check that this proposed definition gives a category of Schur functors equivalent to the category $Schur$ defined earlier!  

Before launching into the proof, it is worth pondering an easier problem where we replace categories by sets, and symmetric monoidal linear Cauchy-complete categories by commutative rings.  
So, instead of $Cat$ let us consider $Set$, and instead of $SymMonLinCauch$ let us consider $CommRing$.  There is a forgetful functor 

$$ U : CommRing \to Set \, . $$

What are the natural transformations from this functor to itself?  Any polynomial $P \in \mathbb{Z}[x]$
defines such a natural transformation, since for any commutative ring $R$ there is a function $P_R: U(R) \to U(R)$ given by

$$ P_R : x \mapsto P(x) $$

and this is clearly natural in $R$.  But in fact, the set of natural transformations from this functor turns out to be _precisely_ $\mathbb{Z}[x]$.  And the reason is that $\mathbb{Z}[x]$ is the free commutative ring on one generator!  

To see this, note that the forgetful functor

$$ U : CommRing \to Set  $$

has a left adjoint, the 'free commutative ring' functor

$$ F : Set \to CommRing \, . $$ 

The free commutative ring on a 1-element set is

$$ F(1) \cong \mathbb{Z}[x] $$

and homomorphisms from $F(1)$ to any commutative ring $R$ are in one-to-one correspondence with elements of the underlying set of $R$, since

$$ U(R) \cong hom(1, U(R)) \cong hom(F(1), R) \, . $$

So, we say $F(1)$ [[representable functor|represents]] the functor $U$.   This makes it easy to show that the set of natural transformations from $U$ to itself is isomorphic to the underlying set of $\mathbb{Z}[x]$, namely $U(F(1))$:

$$[U,U] \cong [hom(F(1), -), hom(F(1), -)] \cong hom(F(1), F(1)) \simeq U(F(1))$$ 

In the first step here we use the representability $U \cong hom(F(1), -)$; in the second we use the [[Yoneda lemma]], and in the third  we use the adjointness between $U$ and $F$.   

We shall carry out a categorified version of this argument to prove that $Schur$ is the category of endomorphisms of the 2-functor

$$U: SymMonLinCauch \to Cat$$ 

The key is that $Schur$ is the free symmetric monoidal linear Cauchy-complete category on one generator.  

+-- {: .query}

[[John Baez]]: I added explanatory remarks above.  Okay?
 
=-- 

## Representability ##

To build a bridge from abstract Schur functors as pseudonatural transformations to the more classical descriptions, we start with the following key result.  In what follows we use $k \mathbb{P}$ to denote the 'linearization' of the permutation groupoid: that is, the linear category formed by replacing the homsets in $\mathbb{P}$ by the free vector spaces on those homsets.  We use $\widebar{k \mathbb{P}}$ to denote the Cauchy completion of the linearization of $\mathbb{P}$.  As we shall see, $\widebar{k \mathbb{P}}$ is equivalent to the category of Schur functors.  But first:

+-- {: .un_thm}
######Theorem 
The underlying 2-functor 
$$U: SymMonLinCauch \to Cat$$ 
is represented by $\widebar{k \mathbb{P}}$.  In other words:

$$   U(-) \simeq hom(-, \widebar{k \mathbb{P}}) $$
 
=-- 

+-- {: .proof} 
######Proof (Sketch)

It is well-known that the permutation category $\mathbb{P}$, whose objects are integers $m \geq 0$ and whose morphisms are precisely automorphisms $m \to m$ given by permutation groups $S_m$, is the representing object for the underlying 2-functor 

$$U_0: SymMonCat \to Cat \, .$$

Let $SymMonLin$ denote the 2-category of small symmetric monoidal linear (but not necessarily Cauchy complete) categories, and let $Lin$ denote the 2-category of small linear categories. Let $k(-): Cat \to Lin$ denote linearization, given by change of base 

$$k \cdot - : Set \to Vect$$ 

applied to a $Set$-enriched category $(C_0, hom: C_0 \times C_0 \to Set)$ to yield a linear category $(C_0, C_0 \times C_0 \to Vect)$. $k(-): Cat \to Lin$ is left 2-adjoint to the underlying 2-functor $U_0: Lin \to Cat$.  For this, we use the fact that if $V$ is a nice closed category (here $Vect$) -- in particular cocomplete -- then the lax monoidal functor $\hom(I, -): V \to Set$ has a left adjoint $- \cdot I: Set \to V$ (here linearization) which is strong (symmetric) monoidal. This induces a 2-functor $Cat = Set$-$Cat \to V$-$Cat$ which is strong 2-symmetric monoidal.  It therefore sends symmetric pseudomonoids in $Set$-$Cat$ to symmetric pseudomonoids in $V$-$Cat$.  In other words, it sends symmetric monoidal categories to symmetric monoidal linear categories.  Therefore, the 2-adjunction $k(-) \dashv U_0$ between $Cat$ and $LinCat$ lifts to one between $SymMonCat$ and $SymMonLinCat$:  

$$(k(-): SymMonCat \to SymMonLin) \dashv (U_1: SymMonLin \to SymMonCat)$$ 

Finally, let $LinCauch$ denote the 2-category of small Cauchy complete linear categories. The linear Cauchy completion gives a 2-reflector $\widebar{(-)}: Lin \to LinCat$ which is left 2-adjoint to the 2-embedding $i: LinCauch \to Lin$, and again the 2-adjunction $\widebar{(-)} \dashv i$ lifts to the level of symmetric monoidal structure to give a 2-adjunction 

$$(\widebar{(-)}: SymMonLin \to SymMonLinCauch) \dashv (U_2: SymMonLinCauch \to SymMonLin)$$ 

For this, the key fact is that if $A \otimes B$ denotes the tensor product of two $V$-enriched categories, then there is a canonical enriched functor  $\overline{A} \otimes \overline{B} \simeq \overline{A \otimes B}$ making Cauchy completion into a lax 2-monoidal functor on $V$-$Cat$.  Even better, it is lax 2-symmetric monoidal.   So, it sends symmetric pseudomonoids to symmetric pseudomonoids.  In this case, then, it sends symmetric monoidal linear categories to symmetric monoidal linear Cauchy-complete categories.

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

[[John Baez]]: I took remarks from the query box here and used them to improve the proof above.  However, it could still use more improvement.  Could you polish it up a bit, Todd?

=--

### Structure of the representing object

Let us now calculate $\widebar{k \mathbb{P}}$. In general, the linear Cauchy completion of a linear category $C$ consists of the full subcategory of linear presheaves $C^{op} \to Vect$ that are obtained as retracts of finite direct sums of representables $C(-, c): C^{op} \to Vect$.  In the case $C = k\mathbb{P}$, these are the functors 

$$F: \mathbb{P}^{op} \to FinVect$$ 

where $F(n) = 0$ for large enough $n$.  For it is clear that this category contains the representables and is closed under finite direct sums and retracts. On the other hand, every polynomial $F$ is a sum of monomials $F(0) \oplus F(1) \oplus \cdots \oplus F(n)$, and by Maschke's theorem, each $S_j$-module $F(j)$ is the retract of a finite sum of copies of the group algebra $k[S_j]$ which corresponds to the representable $k\mathbb{P}(-, j)$. 

So, inspired by Joyal's work on [[combinatorial species]], we make the following definition:

+-- {: .un_def}
######Definition 
A **polynomial species** is a functor $F: \mathbb{P}^{op} \to FinVect$ where $F(n) = 0$ for all sufficiently large $n$.  A morphism of polynomial species is a natural transformation between such functors.

=--

As we have mentioned, the category of polynomial species inherits two monoidal structures from $\mathbb{P}$ via [[Day convolution]].  Most important is the one coming from the _additive_ monoidal structure on $\mathbb{P}$, which is given on the level of objects by adding natural numbers, and on the morphism level given by group homomorphisms 

$$S_m \times S_n \to S_{m+n}$$ 

which juxtapose permutations.  This can be linearized to give algebra maps 

$$k[S_m] \otimes k[S_n] \to k[S_{m+n}]$$ 

which give the monoidal category structure of $k\mathbb{P}$. This monoidal structure uniquely extends via [[Day convolution]] to the Cauchy completion $\widebar{k\mathbb{P}}$, which is intermediate between $k\mathbb{P}$ and the category of $Vect$-valued presheaves on $k\mathbb{P}$.  The general formula for the Day convolution product applied to presheaves $F, G: \mathbb{P}^{op} \to Vect$ is 

$$(F G)(n) = \sum_{j+k = n} (F(j) \otimes G(k)) \otimes_{S_j \times S_k} k[S_n]$$

+-- {: .query}

[[John Baez]]: Todd had written $S_n$ where I have put $k[S_n]$ here.  Okay?
 
=-- 

or, in other notation, 

$$(F G)(n) = \sum_{j+k = n} Ind_{S_j \times S_k}^{S_n} F(j) \otimes G(k)$$

and by restriction this formula gives a tensor product on polynomial species.  This tensor product is a kind of categorification of the usual definition of product of ordinary polynomials, where given 

$$F(x) = \sum_{0 \leq j \leq M} \frac{f_j x^j}{j!} \qquad G(x) = \sum_{0 \leq k \leq N} \frac{g_k x^k}{k!}$$

the $n^{th}$ Taylor coefficient of the product $F(x)G(x)$ is 

$$\sum_{j+k = n} \frac{n!}{j! k!} f_j g_k$$ 

So in summary: 

+-- {: .un_thm} 
######Theorem 
$\widebar{k \mathbb{P}}$ is equivalent to the symmetric monoidal category of polynomial species. 
=-- 

Now, having defined Schur functors abstractly as pseudonatural transformations $U \to U$, the representability theorem together with the 2-categorical Yoneda lemma means that the category of Schur functors is equivalent to the category of symmetric monoidal linear functors on $\widebar{k \mathbb{P}}$. Accordingly, we calculate 

$$[U, U] \cong SymMonLinCauch(\widebar{k\mathbb{P}}, \widebar{k\mathbb{P}}) \cong U(\widebar{k\mathbb{P}})$$ 

In other words, 

+-- {: .un_thm}
######Theorem 
The category $Schur$ is equivalent to the category of polynomial species $\mathbb{P}^{op} \to FinVect$. 
=-- 

NB: This theorem refers only to the underlying category $U(\overline{k\mathbb{P}})$. In other words, this category certainly has linear tensor category structure as well, but this structure is not respected by Schur functor composition which we consider next. 

## Composition of Schur functors ##

Now we consider composition of Schur functors $U \to U$, or equivalently symmetric monoidal linear functors $\widebar{k\mathbb{P}} \to \widebar{k \mathbb{P}}$. Composition endows $[U, U]$ with a monoidal structure, and this monoidal structure transfers across the equivalence of the preceding theorem to a monoidal structure on the underlying category of Schur functors, or equivalently, polynomial species $\mathbb{P}^{op} \to FinVect$. We proceed to analyze this monoidal structure. 

It may be easier to do this in reverse.  Any Schur functor may regarded as a functor

$$1 \stackrel{F}{\to} \overline{k\mathbb{P}}  \, .$$ 

This induces a symmetric monoidal functor, unique up to (unique) symmetric monoidal isomorphism: 

$$\mathbb{P} \stackrel{F^\sim}{\to}\overline{k\mathbb{P}}: m \mapsto F^{\otimes m}$$ 

Here $F^{\otimes m}$ is a Day convolution product of $m$ copies of $F$. Finally, the functor $F^\sim$ is linearized and extended (uniquely) to the linear Cauchy completion, to give a symmetric monoidal linear functor on $\widebar{k \mathbb{P}}$. The efficient tensor product description is 

$$- \otimes_{\mathbb{P}} F^\sim: \overline{k\mathbb{P}} \to \overline{k\mathbb{P}}$$ 

as this manifestly preserves colimits in the blank argument and therefore all colimits needed for the Cauchy completion. (And since the extension to the Cauchy completion is unique, this formula must be correct! The only question is whether this functor is valued in $\overline{k\mathbb{P}}$.) 

In the language of species, this construction is called the _substitution product_, and is denoted $G \circ F$. This is morally correct because it is indeed an appropriate categorification of polynomial composition. However, to avoid overloading the symbol $\circ$ in ways that might be confusing, we will rename it $G \boxtimes F$. Thus, 

$$G \boxtimes F = G \otimes_{\mathbb{P}} F^\sim$$ 

In notation which looks slightly less abstract, this is the Schur object given by the formula 

$$(G \boxtimes F)(n) = \sum_{k \geq 0} G(k) \otimes_{S_k} F^{\otimes k}(n)$$ 

It should be noted that $(G \boxtimes F)(n)$ is indeed $0$ for $n \gt (deg G)(deg F)$, so that $G \boxtimes F$ is indeed a polynomial species. It is just the polynomial special case of the substitution product which is defined on general **linear species** $F, G: \mathbb{P}^{op} \to Vect$. 

+-- {: .un_prop}
######Proposition 
The product $\boxtimes$ makes the category of polynomial species into a monoidal category. The unit for this product is polynomial species $X$ given by the representable $\mathbb{P}(-, 1): \mathbb{P}^{op} \to FinVect$. 
=-- 

+-- {: .proof}
######Proof (Sketch)
The following proof is adapted from a similar argument due to Max Kelly [ref]: we exhibit an associativity isomorphism $\alpha: (- \boxtimes F) \boxtimes G \to - \boxtimes (F \boxtimes G)$ on the basis of universal properties. The point is that by the universal property of $\overline{k\mathbb{P}}$, the category of functors 
$$F: 1 \to \overline{k\mathbb{P}}$$ 
is equivalent to the category of symmetric monoidal linear functors 
$$H: \overline{k\mathbb{P}} \to \overline{k\mathbb{P}}$$ 
The correspondence in one direction takes $F$ to the symmetric monoidal functor $H = - \boxtimes F$, and in the other direction takes $H$ to $F = H(X)$. By the equivalence, we have a unit isomorphism $X \boxtimes F \cong F$. Also by this equivalence, symmetric monoidal linear transformations between symmetric monoidal linear functors of the form 
$$(- \boxtimes F) \boxtimes G \to - \boxtimes (F \boxtimes G)$$ 
are in natural bijection with morphisms $(X \boxtimes F) \boxtimes G \to X \boxtimes (F \boxtimes G)$, which by the unit isomorphism reduce to morphisms $F \boxtimes G \to F \boxtimes G$. Thus, corresponding to the identity on $F \boxtimes G$ we obtain an associativity map $\alpha: (- \boxtimes F) \boxtimes G \to - \boxtimes (F \boxtimes G)$. By similar arguments that appeal to the universal property of $\overline{k \mathbb{P}}$, we get all the required axioms: the invertibility of $\alpha$, the pentagon, etc. 
=--

To summarize: we have equivalences between 

* The category of pseudonatural transformations $U \to U$; 

* The category of symmetric monoidal linear functors $\overline{k\mathbb{P}} \to \overline{k \mathbb{P}}$; 

* The category $Schur = U(\overline{k\mathbb{P}})$. 

The equivalence $Schur \to SymMonLinCauch(\overline{k \mathbb{P}}, \overline{k \mathbb{P}})$ takes a polynomial species $F$ to $- \boxtimes F$. Moreover, the associativity isomorphism is precisely a structure 

$$(- \boxtimes G) \circ (- \boxtimes F) \to - \boxtimes (F \boxtimes G)$$ 

of strong monoidal equivalence from $(Schur, \boxtimes)$ to the monoidal category $SymMonLinCauch(\overline{k\mathbb{P}}, \overline{k\mathbb{P}})$ under endofunctor composition. (The hexagonal coherence condition for a monoidal functor follows from the pentagon; one side of the hexagon is an identity since endofunctor composition is a strict monoidal product.) 

The tensor product $\boxtimes$ on $Schur$ goes by another name: it is the **plethystic tensor product**. 


## References ##

A nice quick introduction to Schur functors can be found here:

* William Fulton and Joe Harris, _Representation Theory: a First Course_, Springer, Berlin, 1991.

A good overall reference to Young diagrams is:

* William Fulton, _Young Tableaux, with Applications to Representation Theory and Geometry_, Cambridge U. Press, 1997.

Species were invented here:

* Andr&#233; Joyal, Une th&#233;orie combinatoire des s&#233;ries formelles, _Adv. Math_ **42** (1981), 1--82.

* Andr&#233;  Joyal: Foncteurs analytiques et esp&egrave;ces des structures, in _Combinatoire &#201;num&#233;rative_, Lecture Notes in Mathematics **1234**, Springer, Berlin, 1986, pp. 126--159.  

A standard reference is:

* Fran&#231;ois Bergeron, Gilbert Labelle, Pierre Leroux, _Combinatorial Species and Tree-like Structures_, Cambridge University Press, Cambridge 1998.


## Old Stuff ##

[[John Baez]]: this stuff should go somewhere, perhaps:

+-- {: .query}


The first thing that should be understood from the beginning is that a general Schur functor $F$ is _nonlinear_: the action on [[hom-set|hom-sets]] 

$$hom(V, W) \to hom(F(V), F(W))$$ 

is not assumed to respect the linear structure. In fact, linear Schur functors are rather uninteresting: because every finite-dimensional space is a finite [[direct sum]] of copies of the $1$-dimensional space $\mathbb{C}$, and because [[linear functor|linear functors]] preserve finite direct sums (that is, [[biproduct|biproducts]], it turns out that every linear Schur functor $F$ is [[representable functor|representable]] as $hom(X, -)$ where $X = F(\mathbb{C})$.  So, the category of linear Schur functors is equivalent to $FinVect$. 

=--

[[John Baez]]: This stuff should get worked into the discussion near the end of how Schur functors are like polynomials...

+-- {: .query}

### Modules over a bimonoid ###

Next we exploit the fact that, just like any [[group algebra]], $k[S_n]$ is a [[bialgebra]] --- or in fancier language, a  [[bimonoid]] in the symmetric monoidal category $FinVect_k$.  Since $i : FinVect_k \to C$ is a symmetric monoidal functor, this means that $i$ carries $k[S_n]$ to a  bimonoid in $C$.  As noted above, we call this bimonoid by the same name, $k[S_n]$.

The category of modules over a bimonoid is a monoidal category. More explicitly, in the case of the bimonoid $k[S_n]$ in $C$ with comultiplication 

$$\delta: k[S_n] \to k[S_n] \otimes k[S_n] \,,$$

the tensor product $V \otimes W$ of two $k[S_n]$-modules in $C$ carries a module structure where the action is defined by 

$$k[S_n] \otimes V \otimes W \stackrel{\delta \otimes 1_{V \otimes W}}{\to} k[S_n] \otimes k[S_n] \otimes V \otimes W \stackrel{1 \otimes \sigma \otimes 1}{\to} k[S_n] \otimes V \otimes k[S_n] \otimes W \stackrel{\alpha_V \otimes \alpha_W}{\to} V \otimes W$$ 

where $\sigma$ is a symmetry isomorphism and $\alpha_V$, $\alpha_W$ are the actions on $V$ and $W$. 

Now we consider a particular case of tensor product representations. If $X$ is an object of $C$, the symmetric group $S_n$ has a representation on $X^{\otimes n}$. (Indeed, for each $\sigma \in S_n$, there is a corresponding symmetry isomorphism $X^{\otimes n} \to X^{\otimes n}$. From this one may construct an action 

$$k[S_n] \otimes X^{\otimes n} \cong \bigoplus_{\sigma \in S_n} I \otimes X^{\otimes n} \to X^{\otimes n}$$ 

which is the required representation.) So, if $V_\nu$ is a Young tableau representation of $k[S_n]$ in $C$, we obtain a tensor product representation 

$$V_\nu \otimes X^{\otimes n}$$ 

of $k[S_n]$ in $C$. 

Consider next the **averaging operator** $e = \frac1{n!} \sum_{\sigma \in S_n} \sigma$: 

$$e: V_\nu \otimes X^{\otimes n} \to V_\nu \otimes X^{\otimes n}$$ 

This operator makes sense since $k$ has characteristic zero, and crucially, this operator is _idempotent_ (because $e = \sigma e$ for all $\sigma \in S_n$). Because we assume idempotents split in $C$, we have a (split) coequalizer 

$$V_\nu \otimes X^{\otimes n} \stackrel{\overset{e}{\to}}{\underset{1}{\to}} V_\nu \otimes X^{\otimes n} \to V_\nu \otimes_{S_n} X^{\otimes n}$$

This coequalizer is indeed the object of $S_n$-coinvariants of $V_\nu \otimes X^{\otimes n}$, i.e., the joint coequalizer of the diagram consisting of all arrows

$$V_\nu \otimes X^{\otimes n} \stackrel{\sigma \cdot-}{\to} V_\nu \otimes X^{\otimes n}$$

ranging over $\sigma \in S_n$ (it is the joint coequalizer because $e = \sigma e$ for all $\sigma$). 

We may now define the Schur functor $S_\nu$ on $C$ attached to a Young tableau $\nu$. 

=--


[[!redirects Schur functor]]
[[!redirects Schur functors]]
