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

In [[categorical algebra]], the *bar construction* takes an [[algebra over a monad|algebra]] $A$ of a [[monad]] and systematically "puffs it up", replacing it with a [[simplicial object]] $Bar_T(A)$ in which all [[equations]] in the original algebra are replaced by [[1-simplices]], all equations between equations (called [[syzygies]]) are replaced by [[2-simplices]], and so on.  

More precisely, the bar construction takes an [[algebra over a monad|algebra]] $(A, \rho)$ of a [[monad]] $(T, \mu, \epsilon)$ on a [[category]] $C$ to an [[augmented simplicial object|augmented]] [[simplicial object]] $Bar_T(A)$ in the [[Eilenberg-Moore category]] $C^T$ of that monad.  The face and degeneracy maps of this augmented simplicial object are given by the structure maps of the monad and its action on the algebra $A$:

$$
  Bar_T(A)
  \coloneqq
  \left(
    \cdots
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    T T A
    \stackrel{\stackrel{\mu \cdot Id_A}{\longrightarrow}}{\stackrel{\phantom{A} T \cdot \rho \phantom{A}}{\longrightarrow}}
    T A \stackrel{\rho}{\longrightarrow} A
  \right)
    \,.
$$

If we apply the [[forgetful functor]] $U : C^T \to C$ to $Bar_T(A)$, we get an augmented simplicial object in $C$ called the **bar resolution** of $A$:

$$
  U Bar_T(A) = \left(
    \cdots
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    U T T A
    \stackrel{\stackrel{U (\mu \cdot Id_A)}{\longrightarrow}}{\stackrel{\phantom{A} U(T \cdot \rho) \phantom{A}}{\longrightarrow}}
    U T A \stackrel{U \rho}{\longrightarrow} U A
  \right)
    \,.
$$

This is called a [[resolution]] of $A$ because it is equipped with a [[simplicial homotopy equivalence]] to the underlying $C$-object $U A \in C$, in a sense clarified by the "acyclic structure" of Definition \ref{acyclic}.  Moreover the bar resolution of $A$ has a universal property: it is initial among resolutions of $A$, as explained in Theorem \ref{universal}. 

Here we distinguish between the bar construction and the bar resolution, although the terms are often used interchangeably. It is worth noting that the bar _construction_ $Bar_T(A)$ is not, in general, simplicially homotopy equivalent to $A$ in the category of simplicial objects in $C^T$.  Only after applying the forgetful functor $U \colon C^T \to C$ do we obtain a key feature of the bar _resolution_: the simplicial homotopy equivalence $U Bar_T(A) \simeq U A$.  

(Above we are identifying objects in a category, either $A \in C^T$ or $U A \in C$, with simplicial objects in that category that are "discrete".)

### Name

The 'bar complex' got its name because the first authors introducing it ([[Samuel Eilenberg]] and [[Saunders MacLane]] in [(Eilenberg-MacLane '53)](#EM53)) denoted its elements using a notation involving vertical bars in lieu of $\otimes$ for tensors ([Ginzburg](#Ginzburg)). Thus 'bar' does not need to be capitalized.

## Definition 

Let $\mathbf{E}$ be a [[category]] and let $(T, m: T T \to T, u: 1_{\mathbf{E}} \to T)$ be a [[monad]] on $\mathbf{E}$. We let $\mathbf{E}^T$ denote the [[Eilenberg-Moore category|category of]] $T$-[[algebra over a monad|algebras]], and $U: \mathbf{E}^T \to \mathbf{E}$ the [[forgetful functor]] which is [[monadic functor|monadic]], with [[left adjoint]] $F$. 

Recall that the [[augmented simplicial set|augmented]] [[simplex category]] $\Delta_a$, viz. the category consisting of [[finite set|finite]] [[ordinals]][^fine1] and order-preserving maps, is the "[[walking structure|walking]] [[monoid]]", i.e., is [[initial object|initial]] among strict [[monoidal categories]] equipped with a [[monoid object]]. The monoidal product on $\Delta_a$ is ordinal addition $[m]+[n] = [m+n]$. If $[n]$ is the $n$-element ordinal, then the [[terminal object]] $[1]$ carries a unique monoid structure and represents the "generic monoid"[^fine2]. 

[^fine1]: N.B.: including the empty ordinal. 

[^fine2]: If $X: \Delta_a^{op} \to \mathbf{C}$ is a simplicial object, then $X([n])$ is what is usually denoted $X_{n-1}$, the object of cells in dimension $n-1$. Note that $X([0]) = X_{-1}$ is the augmented component. The $n$ can be thought of as the number of vertices of a simplex of dimension $n-1$. We choose the index $n$ over the geometric dimension $n-1$ as it is more convenient for our purposes. 

Similarly $\Delta_a^{op}$ is the walking [[comonoid]]. Since the [[comonad]] $F U$ on $\mathbf{E}^T$ can be regarded as a [[comonoid]] in the strict monoidal category of [[endofunctors]] $[\mathbf{E}^T, \mathbf{E}^T]$ (with endofunctor composition as monoidal product), there is a [[strong monoidal functor]] (or in fact a unique [[strict monoidal functor]]) 

$$\Delta_a^{op} \stackrel{Bar_T}{\to} [\mathbf{E}^T, \mathbf{E}^T]$$ 

that takes the generic monoid $[1]$ to $F U$ and generally $[n]$ to $(F U)^{\circ n}$. 

If furthermore $A$ is a $T$-algebra, there is an [[evaluation]] functor 

$$[\mathbf{E}^T, \mathbf{E}^T] \stackrel{eval_A}{\to} \mathbf{E}^T$$ 

and we have the following definition: 

+-- {: .num_defn} 
###### Definition 
The **bar construction** $Bar_T(A)$ is the simplicial $T$-algebra given by the composite functor 

$$\Delta_a^{op} \stackrel{Bar_T}{\to} [\mathbf{E}^T, \mathbf{E}^T] \stackrel{eval_A}{\to} \mathbf{E}^T.$$ 

The composite 

$$\Delta_a^{op} \stackrel{Bar_T(A)}{\to} \mathbf{E}^T \stackrel{U}{\to} \mathbf{E}$$ 

will here be called the **bar resolution** of $A$. 
=-- 

In the notation of [[two-sided bar constructions]], the bar construction would be written as $Bar_T(A) = B(F, T, A)$, and the bar resolution as $B(T, T, A)$. 

## D&#233;calage and resolutions 

### D&#233;calage 

To explain the sense in which $U Bar_T(A)$ is a *resolution* of (the constant simplicial object) $A$, we recall the fundamental [[décalage]] construction. Very simply, putting 

$$D = [1] + (-): \Delta_a^{op} \to \Delta_a^{op}$$ 

the d&#233;calage functor on simplicial objects $C^{\Delta_a^{op}}$ (valued in a category $\mathbf{C}$) is the functor 

$$P: \mathbf{C}^{\Delta_a^{op}} \stackrel{\mathbf{C}^D}{\to} \mathbf{C}^{\Delta_a^{op}}.$$ 

Note that $D$ has a comonad structure (inherited from the comonoid structure on $[1]$ in $\Delta_a^{op}$, see also at _[d&#233;calage -- comonad structure](decalage#DecalageComonad)_), and therefore $P$ also carries a comonad structure. Notice also that there is a comonad map $D \to [1]\circ !$ (where $[1]: 1 \to \Delta_a^{op}$ is left adjoint to $!: \Delta_a^{op} \to 1$ since $[1]$ is initial in $\Delta_a^{op}$), induced by the evident natural inclusion $[1]+i: [1]+[0] \to [1]+[m]$ in $\Delta_a$. This in turn induces a comonad map $P X \to {|X|}$ where 
${|-|}$ is the composite ("discretization"): 

$$C^{\Delta_a^{op}} \stackrel{ev_{[1]}}{\to} C \stackrel{diag}{\to} C^{\Delta_a^{op}}.$$

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
An **acyclic structure** on a simplicial object $X: \Delta_a^{op} \to C$ is a $P$-coalgebra structure $X \to P X$. 
=-- 

Here a $P$-coalgebra structure on $X$ is the same as a *right* $D$-coalgebra (or $D$-comodule) structure, given by a simplicial map $h: X \to X \circ D$ satisfying evident equations. In more nuts-and-bolts terms, it consists of a series of maps $h_n: X([n]) \to X([n+1])$ satisfying suitable equations. 

The map $h: X \to X D$ may be viewed as a homotopy. Again, turning to the topological analogue for intuition, the corresponding $h: X \to P X$ is a homotopy (or rather, the composite $X \to P X \to X^I$ can be turned into a homotopy $I \times X \to X$). The coalgebra structure $h: X \to P X$ has a retraction given by the counit $\varepsilon: P X \to X$, so $X$ becomes a retract of an acyclic space, hence acyclic itself. 

+-- {: .num_remark #rem}
###### Remark 
Definition \ref{acyclic} gives an *absolute* notion of acyclicity, in the sense that if $X: \Delta_a^{op} \to \mathbf{C}$ carries an acyclic structure $h: X \to X D$ and $G: \mathbf{C} \to \mathbf{C}'$ is any functor, then $G X$ automatically carries an acyclic structure $G h: G X \to G X D$. (For example, $G X$ becomes acyclic in a standard model category sense under any functor $G: \mathbf{C} \to Set$.) 
=-- 

### Resolutions 

Returning now to the bar resolution $U Bar_T(A)$: there is a canonical [[natural isomorphism]] $T \circ U Bar_T \cong U Bar_T \circ D$ obtained as the following 2-cell pasting (where $U Bar_T$ abbreviates the top and bottom horizontal composites) 

$$\label{strong}\array{
\Delta_a^{op} & \stackrel{Bar_T}{\to} & [\mathbf{E}^T, \mathbf{E}^T] & \stackrel{[id, U]}{\to} & [\mathbf{E}^T, \mathbf{E}] \\ 
 _\mathllap{D = [1] + (-)} \downarrow & \cong & _\mathllap{[id, F U]} \downarrow & \cong & \downarrow_\mathrlap{[id, U F] = [id, T]} \\ 
\Delta_a^{op} & \underset{Bar_T}{\to} & [\mathbf{E}^T, \mathbf{E}^T] & \underset{[id, U]}{\to} & [\mathbf{E}^T, \mathbf{E}],
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

Because $Bar_T: \Delta_a^{op} \to [\mathbf{E}^T, \mathbf{E}^T]$ is a strong monoidal functor (see the left isomorphism in (eq:strong)), the squares in 

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

We now state and prove a [[universal property]] of the bar construction $Bar_T(A)$. 

+-- {: .num_defn} 
###### Definition 
Let $(T, m: T T \to T, u: 1 \to T)$ be a monad on a category $\mathbf{E}$. A $T$-**algebra resolution** is a simplicial object $Y: \Delta_a^{op} \to \mathbf{E}^T$ together with an acyclic structure on $U Y: \Delta_a^{op} \to \mathbf{E}$. A morphism between $T$-algebra resolutions is a natural transformation $\phi: Y \to Y'$ such that $U\phi: U Y \to U Y'$ is a $P$-coalgebra map. 
=-- 

Let $AlgRes_T$ be the category of $T$-algebra resolutions. There is a forgetful functor 

$$G: AlgRes_T \to \mathbf{E}^T$$ 

that takes an algebra resolution $Y$ to its augmentation component $Y[0]$. 

+-- {: .num_theorem #universal}
###### Theorem 
The functor $\hom_{\mathbf{E}^T}(A, G-): AlgRes_T \to Set$ is represented by $Bar_T(A)$; i.e., $Bar_T(-): \mathbf{E}^T \to AlgRes_T$ is [[left adjoint]] to $G$. 
=-- 

The proof is distributed over two lemmas. 

+-- {: .num_lemma #unique} 
###### Lemma 
Given a $T$-algebra resolution $Y$ and a $T$-algebra map $f: A \to Y[0]$, there is at most one $T$-algebra resolution map $\phi: Bar_T(A) \to Y$ such that 
$\phi[0] = f$. 
=-- 

+-- {: .proof} 
###### Proof 
The $P$-coalgebra structure $h: U Bar_T(A) \to U Bar_T(A) \circ D$ is defined on components $U Bar_T(A)[n] = T^n A$ by $h[n] = u T^n(A): T^n(A) \to T^{n+1}(A)$. Thus in order that $U\phi$ be a $P$-coalgebra map, we must have that the diagram 

$$\array{
T^n A & \stackrel{u T^n A}{\to} & U F T^n(A) \\ 
 _\mathllap{U\phi[n]} \downarrow & & \downarrow_\mathrlap{U\phi[n+1]} \\ 
U Y[n] & \underset{h_Y[n]}{\to} & U Y[n+1]
}$$ 

commutes. Here $\phi[n]: T^n (A) \to Y[n]$ determines a unique $T$-algebra map $g: F T^n(A) \to Y[n+1]$ such that 

$$U(g) \circ u T^n(A) = h_Y[n] \circ U\phi[n]$$ 

since $F$ is left adjoint to $U$. Thus, starting with $\phi[0] = f$ as given, each algebra map $\phi[n]$ uniquely determines its successor $\phi[n+1] = g$. 
=-- 

+-- {: .num_remark #simp} 
###### Remark 
The preceding proof does not show that the $\phi[n]$ fit together to form a map $\phi$ of simplicial $T$-algebras (i.e., to respect faces and degeneracies); it merely shows at most one such $T$-algebra resolution map is possible. But once we show that $\phi$ respects faces and degeneracies, the proof of Theorem \ref{universal} will be complete. 
=-- 

+-- {: .num_lemma #exist} 
###### Lemma 
Given a $T$-algebra resolution $Y$ and an algebra map $f: X \to Y[0]$, there is at least one $T$-algebra resolution map $\phi: Bar_T(X) \to Y$ with $\phi[0] = f$. 
=-- 

+-- {: .proof} 
###### Proof 
It is enough to produce such a map $\phi: Bar_T(Y[0]) \to Y$ in the case $f = 1_{Y[0]}$, since the case for general $f: X \to Y[0]$ is then given by a composite 

$$Bar_T(X) \stackrel{Bar_T(f)}{\to} Bar_T(Y[0]) \stackrel{\phi}{\to} Y.$$ 

We will do something slightly more general. For any category $\mathbf{C}$, the endofunctor category $[\mathbf{C}^{\Delta_a^{op}}, \mathbf{C}^{\Delta_a^{op}}]$ has a comonoid object $P = - \circ D$, so that there is an induced strong monoidal functor 

$$\Delta_a^{op} \stackrel{\tilde{P}}{\to} [\mathbf{C}^{\Delta_a^{op}}, \mathbf{C}^{\Delta_a^{op}}]$$ 

which, upon evaluating at an object $Y$ of $\mathbf{C}^{\Delta_a^{op}}$, gives a functor 

$$B(Y, D, D) \coloneqq eval_Y \circ \tilde{P}: \Delta_a^{op} \to \mathbf{C}^{\Delta_a^{op}}$$ 

with $B(Y, D, D)[n] = Y D^n$, so that $B(Y, D, D)$ is a double simplicial object. Taking $\mathbf{C} = \mathbf{E}^T$ and taking $Y$ to be a $T$-algebra resolution with acyclic structure $h: Y \to Y D$, we will produce a (double) simplicial map 

$$\Phi: B(T, T, Y) \to B(Y, D, D)$$ 

where $\Phi[n]: T^n Y \to Y D^n$ is defined recursively as in the proof of Lemma \ref{unique}, by setting $\Phi[0] = 1_Y$ and taking $\Phi[n+1]: T^{n+1} Y \to Y D^{n+1}$ the unique simplicial $T$-algebra map such that 

$$\array{
T^n Y & \stackrel{u T^n Y}{\to} & T^{n+1} Y \\ 
 _\mathllap{\Phi[n]} \downarrow & & \downarrow_\mathrlap{\Phi[n+1]} \\ 
Y D^n & \underset{h D^n}{\to} & Y D^{n+1}
}$$ 

commutes for all $n$. Once we verify the claim that $\Phi$ respects faces and degeneracies, the same will be true for $\phi[n] = \Phi[n][0]: (T^n Y)[0] = T^n(Y[0]) \to (Y D^n)[0] = Y[n]$, whence the proof will be complete by Remark \ref{simp}. 

The claim is proved by induction on $n$. Let $\epsilon: D \to 1_{\Delta_a^{op}}$ be the counit and $\delta: D \to D D$ be the comultiplication. We have face maps 

$$T^j m T^{n-j-1} Y: T^{n+1} Y \to T^n Y, \qquad Y D^j \epsilon D^{n-j}: Y D^{n+1} \to Y D^n$$ 

for $j = 0$ to $n$, under the special convention that $m T^{-1}Y: T Y \to Y$ denotes the action $\alpha: T Y \to Y$. We also have degeneracy maps 

$$T^j u T^{n-j} Y: T^n Y \to T^{n+1} Y, \qquad Y D^{j-1} \delta D^{n-j}: Y D^n \to Y D^{n+1}$$ 

for $j = 1$ to $n$. We proceed as follows. 

* To check preservation of face maps, we treat separately the cases where $j = 0$ and $j \geq 1$. 
  * For $j = 0$, we must check commutativity of the square in 
$$\array{
T^n Y & \stackrel{u T^n Y}{\to} & T^{n+1} Y & \stackrel{\Phi[n+1]}{\to} & Y D^{n+1} \\ 
 & _\mathllap{id} \searrow & \downarrow_\mathrlap{m T^{n-1} Y} & & \downarrow_\mathrlap{Y\epsilon D^n} \\ 
 & & T^n Y & \underset{\Phi[n]}{\to} & Y D^n.
}$$ 
Since all the maps are algebra maps and $u T^n Y: T^n Y \to T^{n+1} Y$ exhibits $T^{n+1} Y$ as the free algebra on $T^n Y$, it suffices to check commutativity around the perimeter. (N.B.: the triangle commutes, even in the case where $n=0$ which we need to start the induction.) By definition of $\Phi[n+1]$, commutativity of the perimeter boils down to commutativity of 
$$\array{
T^n Y & \stackrel{u T^n Y}{\to} & T^{n+1} Y & \stackrel{\Phi[n+1]}{\to} & Y D^{n+1} \\ 
 & _\mathllap{\Phi[n]} \searrow & & \nearrow_\mathrlap{h D^n} & \downarrow_\mathrlap{Y\epsilon D^n} \\ 
 & & Y D^n & \underset{id}{\to} & Y D^n 
}$$ 
where the triangle commutes by one of the acyclic structure equations. 
  * For $j \geq 1$, the commutativity of the right square in 
$$\array{
T^n Y & \stackrel{u T^n Y}{\to} & T^{n+1} Y & \stackrel{\PhiY[n+1]}{\to} & Y D^{n+1} \\ 
 _\mathllap{T^{j-1}m T^{n-j-1} Y} \downarrow & nat. & \downarrow_\mathrlap{T^j m T^{n-j-1} Y} & & \downarrow_\mathrlap{Y D^j \epsilon D^{n-j}} \\ 
T^{n-1} Y & \underset{u T^{n-1} Y}{\to} & T^n Y & \underset{\Phi[n]}{\to} & Y D^n \\ 
 & _\mathllap{\Phi[n-1]} \searrow & & \nearrow_\mathrlap{h D^{n-1}} & \\ 
 & & Y D^{n-1} & & 
}$$ 
is again by appeal to a freeness argument where we just need to check commutativity of the perimeter, noting commutativity of the left square by naturality and that of the bottom quadrilateral by the recursive definition of $\Phi[n]$. But the perimeter commutes by examining the diagram 
$$\array{
T^n Y & \stackrel{u T^n Y}{\to} & T^{n+1} Y & \stackrel{\Phi[n+1]}{\to} & Y D^{n+1} \\ 
_\mathllap{T^{j-1}m T^{n-j-1} Y} \downarrow & _\mathllap{\Phi[n]} \searrow & & \nearrow_\mathrlap{h D^n} & \downarrow_\mathrlap{Y D^j \epsilon D^{n-j}} \\ 
T^{n-1} Y & ind. & Y D^n & nat. & Y D^n \\ 
 & _\mathllap{\Phi[n-1]} \searrow & \downarrow & \nearrow_\mathrlap{h D^{n-1}} & \\ 
 & & Y D^{n-1} & & 
}$$ 
(where the middle vertical arrow is $Y D^{j-1} \epsilon D^{n-j}$) using the inductive hypothesis in the bottom left parallelogram. 

* To check preservation of degeneracy maps, we treat separately the cases $j=1$ and $j \geq 2$. 
  * For $j = 1$, the commutativity of the top right square in 
$$\array{
T^{n-1} Y & \stackrel{u T^{n-1} Y}{\to} & T^n Y & \stackrel{\Phi[n]}{\to} & Y D^n \\ 
 _\mathllap{u T^{n-1} Y} \downarrow & nat. & \downarrow _\mathrlap{T u T^{n-1} Y} & & \downarrow_\mathrlap{Y \delta D^{n-1}} \\ 
T^n Y & \underset{u T^n Y}{\to} & T^{n+1} Y & \underset{\Phi[n+1]}{\to} & Y D^{n+1} \\ 
 & _\mathllap{\Phi[n]} \searrow & & \nearrow_\mathrlap{h D^n} & \\ 
 & & Y D^n & & 
}$$ 
is by appeal to a freeness argument where we just need to check commutativity of the perimeter (the special case $n=1$ being used to start the induction). But this boils down to commutativity of the diagram 
$$\array{
T^{n-1} Y & \stackrel{u T^{n-1} Y}{\to} & T^n Y & \stackrel{\Phi[n]}{\to} & Y D^n \\ 
 _\mathllap{u T^{n-1} Y} \downarrow & \searrow_\mathrlap{\Phi[n-1]} & & _\mathllap{h D^{n-1}} \nearrow & \downarrow_\mathrlap{Y \delta D^{n-1}} \\ 
T^n Y & & Y D^{n-1} & & Y D^{n+1} \\ 
 & _\mathllap{\Phi[n]} \searrow & \downarrow_\mathrlap{h D^{n-1}} & \nearrow_\mathrlap{h D^n} & \\ 
 & & Y D^n & & 
}$$ 
where the bottom right quadrilateral commutes by one of the acyclic structure equations. 
  * For $j \geq 2$, the commutativity of the top right square in 
$$\array{
T^{n-1} Y & \stackrel{u T^{n-1} Y}{\to} & T^n Y & \stackrel{\Phi[n]}{\to} & Y D^n \\ 
 _\mathllap{T^{j-1} u T^{n-j} Y} \downarrow & nat. & \downarrow _\mathrlap{T^j u T^{n-j} Y} & & \downarrow_\mathrlap{Y D^{j-1} \delta D^{n-j}} \\ 
T^n Y & \underset{u T^n Y}{\to} & T^{n+1} Y & \underset{\Phi[n+1]}{\to} & Y D^{n+1} \\ 
 & _\mathllap{\Phi[n]} \searrow & & \nearrow_\mathrlap{h D^n} & \\ 
 & & Y D^n & & 
}$$
is once again by appeal to a freeness argument where we just need to check commutativity of the perimeter. Here it boils down to commutativity of 
$$\array{
T^{n-1} Y & \stackrel{u T^{n-1} Y}{\to} & T^n Y & \stackrel{\Phi[n]}{\to} & Y D^n \\ 
 _\mathllap{T^{j-1} u T^{n-j} Y} \downarrow  & \searrow_\mathrlap{\Phi[n-1]} & & _\mathllap{h D^{n-1}} \nearrow & \downarrow_\mathrlap{Y D^{j-1} \delta D^{n-j}} \\ 
T^n Y & ind. & Y D^{n-1} & nat. & Y D^{n+1} \\ 
 & _\mathllap{\Phi[n]} \searrow & \downarrow & \nearrow_\mathrlap{h D^n} & \\ 
 & & Y D^n & & 
}$$ 
where the middle vertical arrow is $Y D^{j-2} \delta D^{n-j}$. 

This completes the proof. 
=-- 

## Special cases

### The classifying space and universal bundle of a group
 {#UniversalPrincipalBundle}

There is a monad $T$ on [[Set|$Set$]] whose algebras are left [[G-set|$G$-sets]], given by

$$ 
  T X \,=\, G \times X
  \,.
$$

The [[terminal object|terminal]] $G$-set $1$, namely the [[singleton set]] equipped with the [[trivial action]] of $G$, is an [[algebra over a monad|algebra for this monad]] $T$.    

Now recalling that the bar construction takes any algebra of any monad and turns it into a simplicial object in the category of algebras of that monad, write $Bar_T(1)$ for the augmented simplicial set obtained by applying this to $1 \in G Set$.  

By Theorem \ref{universal}, its [[underlying]] [[simplicial set]] $U Bar_T(1)$ is [[contractible homotopy type|contractible]].  This simplicial set is often denoted $E G$ (and as such known as the [[universal principal bundle|universal]] [[simplicial principal bundle|simplicial]] $G$-[[principal bundle]]) or $W G$ (see [here](simplicial+classifying+space#WGInComponents) at *[[simplicial classifying space]]*).

Working through the details, we see that the set of $n$-simplices of $E G$ is $G^{n+1}$, and all the face maps $\partial_i \colon G^{n+1} \to G^n$ are given by multiplying successive entries in the $(n+1)$-tuple, except for the last face map, which encodes the trivial action of $G$ on $1$:

$$  
  \partial_i (g_0, g_1, \dots, g_n) 
   \;=\; 
  (g_0, \dots, g_i g_{i+1}, \dots, g_n) 
$$

for $i = 0, \dots, n-1$, while

$$ 
  \partial_n (g_0, g_1, \dots, g_n) 
    \;=\; 
  (g_0, g_1, \dots, g_{n-1})
  \,. 
$$

The [[quotient]] $B G \coloneqq (E G)/G$ is known as the [[simplicial classifying space]] of $G$ (also denoted $\overline{W}G$), and its [[topological realization]] is a [[topological space|topological]] [[classifying space]] for $G$-[[principal bundles]]. Finally the topological realization of the quotient map $E G \to B G$ is the "[[universal principal bundle|universal]] $G$-[[principal bundle]]".  

The simplicial set $B G$ is also the [[simplicial nerve]] of the *[[delooping groupoid]]* of $G$.

### For modules over an algebra

Let $A$ be a commutative [[associative algebra]]s over some [[ring]] $k$. Write $A Mod$ for the category of right [[module]]s over $A$.

For $M$ a right module, also $M \otimes_k A$ is canonically a right module. This construction extends to a functor

$$
  T = (-) \otimes_k A : 
    A Mod 
      \to 
    A Mod 
  \,.
$$

The [[monoid]] structure on $A$ makes $T$ into a [[monad]] on $A Mod$: the monad product and unit are given by the product and unit in $A$.

For any right $A$-module $M$, the action $\rho \colon M \otimes A \to M$ makes $M$ into an algebra of the monad $T$.  The bar construction $Bar_T(A)$ is then the simplicial $A$-module

$$
  \cdots
  \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
  M \otimes_k A \otimes_k A \stackrel{\overset{Id \otimes \mu}{\longrightarrow}}{\underset{\rho \otimes Id}{\longrightarrow}} M \otimes_k A
  \,.
$$

Under the [[Moore complex]] functor of the [[Dold-Kan correspondence]], this simplicial $A$-module is identified with a [[chain complex]] of $A$-modules whose [[differential]] is given by the alternating sums of the face maps indicated above. 

This chain complex is what originally was called the **bar complex** in [[homological algebra]].

This chain complex provides a free resolution of $A$, which can be used to compute the [[Tor]] group

$$
  Tor(M, A \times A)
  \,.
$$

This gives the [[Hochschild homology]] of $A$. See there for more details.

### For differential graded (Hopf) algebras

See [[bar and cobar construction]].

### For $E_\infty$-algebras

See ([Fresse](#Fresse)).

##Related entries

* [[simplicial resolution]]; this is essentially the same concept but from a slightly different perspective.

* [[homotopy coherent nerve]]

* [[canonical resolution]]

* [[monadic cohomology]] 

## References and Literature

The original reference for bar constructions in the generality of monads is

* {#Godement58} [[Roger Godement]], *Topologie algébrique et theorie des faisceaux*, Actualités Sci. Ind. **1252**, Hermann, Paris (1958) &lbrack;[webpage](https://www.editions-hermann.fr/livre/topologie-algebrique-et-theorie-des-faisceaux-roger-godement), [[Godement-TopologieAlgebrique.pdf:file]]&rbrack;

whereas in the homological context the first appearance is:

* {#EM53} [[Samuel Eilenberg]], [[Saunders MacLane]], *On the groups of $H(\Pi, n)$ I*, Annals of Mathematics, Second Series, 58: 55–106, (1953), ([doi:10.2307/1969820](https://doi.org/10.2307/1969820))


A general discussion of bar construction for monads is at

* {#Trimble} [[Todd Trimble]], _On the Bar Construction_ ([blog](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html))

Textbook accounts can be found at:

* [[Saunders Mac Lane]], section IV.5 of _Homology_

* [[Charles Weibel]], section 8.6 of _[[An Introduction to Homological Algebra]]_ (1994)

The bar complex of a bimodule is reviewed for instance in 

* {#Ginzburg} [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603))


around page 16.

The bar complex for [[E-infinity algebra]]s is discussed in

* [[Benoit Fresse]], _The bar complex of an E-infinity algebra_, Advances in Mathematics Volume 223, Issue 6, 1 April 2010, Pages 2049-2096 
{#Fresse}


The compositional structure of the bar construction of several monads, as well as its interpretation in terms of [[partial evaluation|partial evaluations]] is studied in

* [[Carmen Constantin]], [[Tobias Fritz]], [[Paolo Perrone]] and [[Brandon Shapiro]], _Partial evaluations and the compositional structure of the bar construction_. ([arXiv](https://arxiv.org/abs/2009.07302))


[[!redirects bar constructions]]
[[!redirects bar complex]]
[[!redirects bar resolution]]
[[!redirects bar resolutions]]