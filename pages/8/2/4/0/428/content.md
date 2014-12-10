
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

The **bar construction** takes a [[monad]] $(T, \mu, \epsilon)$ equipped with an [[algebra over a monad|algebra-over-a-monad]] $(A, \rho)$ to the ([[augmented simplicial set|augmented]]) [[simplicial object]] whose structure maps are given by the structure maps of the monad and its action on its algebra:

$$
  \mathrm{B}(T,A)
  \coloneqq
  \left(
    \cdots
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    T T A
    \stackrel{\stackrel{\mu \cdot Id_A}{\longrightarrow}}{\stackrel{T \cdot \rho}{\longrightarrow}}
    T A \stackrel{\rho}{\longrightarrow} A
  \right)
    \,.
$$

This simplicial object can be viewed as a [[resolution]] of $A$, in a sense explained below. 

## Definition 

Let $\mathbf{E}$ be a [[category]] and let $(T, m: T T \to T, u: 1_{\mathbf{E}} \to T)$ be a [[monad]] on $\mathbf{E}$. We let $\mathbf{E}^T$ denote the [[Eilenberg-Moore category|category of]] $T$-[[algebra over a monad|algebras]], and $U: \mathbf{E}^T \to \mathbf{E}$ the [[forgetful functor]] which is [[monadic functor|monadic]], with [[left adjoint]] $F$. 

Recall that the ([[augmented simplicial set|augmented]]) [[simplex category]], viz. the category consisting of [[finite set|finite]] [[ordinals]][^fine1] and order-preserving maps, is the "[[walking structure|walking]] [[monoid]]", i.e., is [[initial object|initial]] among strict [[monoidal categories]] equipped with a [[monoid object]]. The monoidal product on $\Delta$ is ordinal addition $[m]+[n] = [m+n]$. If $[n]$ is the $n$-element ordinal, then the [[terminal object]] $[1]$ carries a unique monoid structure and represents the "generic monoid"[^fine2]. 

[^fine1]: N.B.: including the empty ordinal. 

[^fine2]: If $X: \Delta^{op} \to \mathbf{C}$ is a simplicial object, then $X([n])$ is what is usually denoted $X_{n-1}$, the object of cells in dimension $n-1$. Note that $X([0]) = X_{-1}$ is the augmented component. The $n$ can be thought of as the number of vertices of a simplex of dimension $n-1$. We choose the index $n$ over the geometric dimension $n-1$ as it is more convenient for our purposes. 

Similarly $\Delta^{op}$ is the walking [[comonoid]]. Since the [[comonad]] $F U$ on $\mathbf{E}^T$ can be regarded as a [[comonoid]] in the strict monoidal category of [[endofunctors]] $[\mathbf{E}^T, \mathbf{E}^T]$ (with endofunctor composition as monoidal product), there is a [[strong monoidal functor]] (or in fact a unique [[strict monoidal functor]]) 

$$\Delta^{op} \stackrel{Bar_T}{\to} [\mathbf{E}^T, \mathbf{E}^T]$$ 

that takes the generic monoid $[1]$ to $F U$ and generally $[n]$ to $(F U)^{\circ n}$. 

If furthermore $A$ is a $T$-algebra, there is an [[evaluation]] functor 

$$[\mathbf{E}^T, \mathbf{E}^T] \stackrel{eval_A}{\to} \mathbf{E}$$ 

and we have the following definition: 

+-- {: .num_defn} 
###### Definition 
The **bar construction** $Bar_T(A)$ is the simplicial $T$-algebra given by the composite functor 

$$\Delta^{op} \stackrel{Bar_T}{\to} [\mathbf{E}^T, \mathbf{E}^T] \stackrel{eval_A}{\to} \mathbf{E}.$$ 

The composite 

$$\Delta^{op} \stackrel{Bar_T(A)}{\to} \mathbf{E}^T \stackrel{U}{\to} \mathbf{E}$$ 

will here be called the **bar resolution** of $A$. 
=-- 

In the notation of [[two-sided bar constructions]], the bar construction would be written as $Bar_T(A) = B(T, T, A)$. 

## D&#233;calage and resolutions 

### D&#233;calage 

To explain the sense in which $U Bar_T(A)$ is an *acyclic resolution* of (the constant simplicial object) $A$, we recall the fundamental [[décalage]] construction. Very simply, putting 

$$D = [1] + (-): \Delta^{op} \to \Delta^{op}$$ 

the d&#233;calage functor on simplicial objects $C^{\Delta^{op}}$ (valued in a category $\mathbf{C}$) is the functor 

$$P: \mathbf{C}^{\Delta^{op}} \stackrel{(\mathbf{C})^D}{\to} \mathbf{C}^{\Delta^{op}}.$$ 

Note that $D$ has a comonad structure (inherited from the comonoid structure on $[1]$ in $\Delta^{op}$, see also at _[d&#233;calage -- comonad structure](decalage#DecalageComonad)_), and therefore $P$ also carries a comonad structure. Notice also that there is a comonad map $D \to [1]\circ !$ (where $[1]: 1 \to \Delta^{op}$ is left adjoint to $!: \Delta^{op} \to 1$ since $[1]$ is initial in $\Delta^{op}$), induced by the evident natural inclusion $[1]+i: [1]+[0] \to [1]+[m]$ in $\Delta$. This in turn induces a comonad map $P X \to {|X|}$ where 
${|-|}$ is the composite ("discretization"): 

$$C^{\Delta^{op}} \stackrel{ev_{[1]}}{\to} C \stackrel{diag}{\to} C^{\Delta^{op}}.$$

The notation $P$ is chosen because d&#233;calage is essentially a kind of [[path space]] construction, i.e., in the case $\mathbf{C} = Set$ it is a [[simplicial sets]] analogue of a topological pullback 

$$\array{
P X & \to & X^I & \stackrel{ev_1}{\to} X \\ 
\downarrow & & \downarrow_\mathrlap{ev_0} & \\ 
{|X|} & \underset{id}{\to} & X
}$$ 

where $id: {|X|} \to X$ is the identity inclusion of the underlying set with the discrete topology. $P X$ is essentially a sum of spaces of based paths $(\alpha: (I, 0) \to (X, x_0)$ over all possible choices of basepoint $x_0$, fibered over $X$ by taking $\alpha$ to $\alpha(1)$. Each space of based paths is contractible and therefore $P X$ is acyclic. 

The following definition names a nonce expression; this author (Todd Trimble) does not know how this is (or might be) referred to in the literature: 

+-- {: .num_defn #acyclic} 
###### Definition 
An **acyclic structure** on a simplicial object $X: \Delta^{op} \to C$ is a $P$-coalgebra structure $X \to P X$. 
=-- 

Here a $P$-coalgebra structure on $X$ is the same as a *right* $D$-coalgebra (or $D$-comodule) structure, given by a simplicial map $h: X \to X \circ D$ satisfying evident equations. In more nuts-and-bolts terms, it consists of a series of maps $h_n: X([n]) \to X([n+1])$ satisfying suitable equations. 

The map $h: X \to X D$ may be viewed a homotopy. Again, turning to the topological analogue for intuition, the corresponding $h: X \to P X$ is a homotopy (or rather, the composite $X \to P X \to X^I$ can be turned into a homotopy $I \times X \to X$). The coalgebra structure $h: X \to P X$ has a retraction given by the counit $\varepsilon: P X \to X$, so $X$ becomes a retract of an acyclic space, hence acyclic itself. 

+-- {: .num_remark #rem}
###### Remark 
Definition \ref{acyclic} gives an *absolute* notion of acyclicity, in the sense that if $X: \Delta^{op} \to \mathbf{C}$ carries an acyclic structure $h: X \to X D$ and $G: \mathbf{C} \to \mathbf{C}'$ is any functor, then $G X$ automatically carries an acyclic structure $G h: F X \to F X D$. (For example, $G X$ becomes acyclic in a standard model category sense under any functor $G: \mathbf{C} \to Set$.) 
=-- 

### Resolutions 

Returning now to the bar resolution $U Bar_T(A)$: there is a canonical [[natural isomorphism]] $T \circ U Bar_T \cong U Bar_T \circ D$ obtained as the following 2-cell pasting (where $U Bar_T$ abbreviates the top and bottom horizontal composites) 

$$\label{strong}\array{
\Delta^{op} & \stackrel{Bar_T}{\to} & [\mathbf{E}^T, \mathbf{E}^T] & \stackrel{[id, U]}{\to} & [\mathbf{E}^T, \mathbf{E}] \\ 
 _\mathllap{D = [1] + (-)} \downarrow & \cong & _\mathllap{[id, F U]} \downarrow & \cong & \downarrow_\mathrlap{[id, U F] = [id, T]} \\ 
\Delta^{op} & \underset{Bar_T}{\to} & [\mathbf{E}^T, \mathbf{E}^T] & \underset{[id, U]}{\to} & [\mathbf{E}^T, \mathbf{E}],
}$$ 

whence there is a homotopy 

$$h = (U Bar_T \stackrel{u U Bar_T}{\to} T U Bar_T \cong U Bar_T D).$$ 

+-- {: .num_prop} 
###### Proposition 
The map $h$ is an acyclic structure, def. \ref{acyclic}, i.e., a right $D$-coalgebra structure. 
=-- 

+-- {: .proof} 
###### Proof 
We verify the coassociativity condition for the coaction $h: U Bar_T \to U Bar_T D$; the counit condition is checked along similar lines. The comultiplication of the comonad $F U$ is $\delta \coloneqq F u U$, and putting $\eta = u U: U \to U F U$ for a right $F U$-coaction, the coassociativity of $\eta$ follows from a naturality square 

$$\array{
U & \stackrel{\eta}{\to} & U F U \\ 
 _\mathllap{\eta} \downarrow & & \downarrow_\mathrlap{U\delta} \\ 
U F U & \underset{\eta F U}{\to} & U F U F U.
}$$

Apply $[id_{\mathbf{E}^T}, -]$ to this coassociativity square to get another coassociativity, this time for the comonad $K \coloneqq [id_{\mathbf{E}^T}, F U]$ on $[\mathbf{E}^T, \mathbf{E}^T]$ (with comultiplication denoted $\delta_K$) and coaction $H \coloneqq [id, \eta]: [id, U] \to [id, U] \circ K$. Thus there is an equalizing diagram 

$$[id, U] \stackrel{H}{\to} [id, U]K \stackrel{\overset{[id, U]\delta_K}{\to}}{\underset{H K}{\to}} [id, U]K K.$$ 

Because $Bar_T: \Delta^{op} \to [\mathbf{E}^T, \mathbf{E}^T]$ is a strong monoidal functor (see the left isomorphism in (eq:strong)), the squares in 

$$\array{
[id, U] Bar_T & \stackrel{H Bar_T}{\to} & [id, U]K Bar_T & \stackrel{\overset{[id, U]\delta_K Bar_T}{\to}}{\underset{H K Bar_T}{\to}} & [id, U]K K Bar_T \\ 
 & _\mathllap{h}{\searrow} & \downarrow_\mathrlap{\cong} & & \downarrow_\mathrlap{\cong} \\ 
 & & [id, U] Bar_T D & \stackrel{\overset{[id, U]Bar_T \delta_D}{\to}}{\underset{h D}{\to}} & [id, U]Bar_T D D 
}$$ 

commute serially, with the triangle commuting by definition of $h$. This completes the verification. 
=-- 

By Remark \ref{rem}, it follows that $U Bar_T(A)$, obtained by applying evaluation at a $T$-algebra $A$, carries an acyclic structure as well. In this sense we may say that $U Bar_T(A)$ (which has $A$ as its augmented component in dimension $-1$) is an acyclic resolution of the constant simplicial $T$-algebra at $A$ that carries a $T$-algebra structure. 

## Properties

### Universal property

We now state a [[universal property]] of the bar resolution $B(T, A) = U Bar_T(A)$. 

+-- {: .num_defn} 
###### Definition 
Let $T$ be a monad on a category $\mathbf{E}$. A $T$-**algebra resolution** is a simplicial object $Y: \Delta^{op} \to \mathbf{E}^T$ together with an acyclic structure on $U Y: \Delta^{op} \to \mathbf{E}$. A morphism between $T$-algebra resolutions is a natural transformation $\phi: Y \to Y'$ such that $U\phi: U Y \to U Y'$ is a $P$-coalgebra map. 
=-- 

Let $AlgRes_T$ be the category of $T$-algebra resolutions. There is a forgetful functor 

$$G: AlgRes_T \to \mathbf{E}^T$$ 

that takes an algebra resolution $Y$ to its augmentation component $Y([0])$. 

+-- {: .num_theorem}
###### Theorem 
The functor $\hom_{\mathbf{E}^T}(A, G-): AlgRes_T \to Set$ is represented by $Bar_T(A)$. In other words, $Bar_T(-): \mathbf{E}^T \to AlgRes_T$ is [[left adjoint]] to $G$. 
=-- 

+-- {: .proof} 
###### Proof 
To be filled in. 
=-- 

## Special cases

### For modules over an algebra

Let $A$ be a commutative [[associative algebra]]s over some [[ring]] $k$. Write $A Mod$ for the category of [[connective chain complex|connective]] [[chain complex]]es of [[module]]s over $A$.

For $N$ a right module, also $N \otimes_k A$ is canonically a module. This construction extends to a functor

$$
  A \otimes_k (-) : 
    A Mod 
      \to 
    A Mod 
  \,.
$$

The [[monoid]]-structure on $A$ makes this a [[monad]] in [[Cat]]: the monad product and unit are given by the product and unit in $A$.

For $N$ a module its right action $\rho :N \otimes A \to N$ makes the module an [[algebra over a monad|algebra over this monad]].

The bar construction $\mathrm{B}(A,N)$ is then the simplicial module

$$
  \cdots
  \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
  N \otimes_k A \otimes_k A \stackrel{\overset{Id \otimes \mu}{\longrightarrow}}{\underset{\rho \otimes Id}{\longrightarrow}} N \otimes_k A
  \,.
$$

Under the [[Moore complex]] functor of the [[Dold-Kan correspondence]] this is identified with a [[chain complex]] whose [[differential]] is given by the alternating sums of the face maps indicated above. 

This chain complex is what originally was called the **bar complex** in [[homological algebra]]. Because the first authors denoted its elements using a notation involving vertical bars ([Ginzburg](#Ginzburg))!!

This chain complex provides a resolution that computes the [[Tor]]

$$
  Tor(N, A \times A)
  \,.
$$

This gives the [[Hochschild homology]] of $A$. See there for more details.

### For differential graded (Hopf) algebras

See [[bar and cobar construction]].

### For $E_\infty$-algebras

See ([Fresse](#Fresse)).

## References

A general discussion of bar construction for monads is at

* [[Todd Trimble]], _On the Bar Construction_ ([blog](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html))
{#Trimble}

The bar complex of a bimodule is reviewed for instance in 

* [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603))
{#Ginzburg}

around page 16.

The bar complex for [[E-infinity algebra]]s is discussed in

* [[Benoit Fresse]], _The bar complex of an E-infinity algebra_ Advances in Mathematics Volume 223, Issue 6, 1 April 2010, Pages 2049-2096 
{#Fresse}


[[!redirects bar constructions]]

[[!redirects bar complex]]