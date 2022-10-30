category: type theory

This entry is about the article [T. Streicher - a model of type theory in simplicial sets - a brief introduction to Voevodsky' s homotopy type theory](http://www.mathematik.tu-darmstadt.de/~streicher/sstt.pdf).

> The aim of this note is to describe in an accessible way how simplicial 
>sets organize into a model of Martin-L&#246;f type theory. Moreover, we explain 
>Voevodsky's Univalence Axiom which holds in this model and implements 
>the idea that isomorphic types are identical

The topos $sSet=:H$ contains a natural-numbers object. $H$ is equipped with the model structure $(C,W,F)$ (...).

Families of types are defined to be Kan fibrations. The class $F$ of Kan fibrations has the following properties:

* It is closed under composition, pullback along arbitrary morphisms and contains all isomorphisms.

* It is closed under $\Pi$; i.e. if $a:A\to I$ and $b:B\to A$ are in $F$ then $\Pi_a(b)$ is in $F$.

## Identity on $X$

Let $X\in H$ be an object. Let

$$X\xrightarrow{r_X}Id(X)\xrightarrow{p_X}X\times X$$

be a factorization of the diagonal $\delta_X : X \xrightarrow{}X\times X$ into an acyclic cofibration $r_X\in C\cap W$ followed by a fibration $p_X\in F$. We interpret the fibration $p_X$ as

$$x,y:X\vdash I_X(x,y)$$

Analogous, for a Kan fibration $f:A\to I$ we factor the diagonal $\delta_f:A\to A\times_I A$ of $f$ in this way. 

Now the problem ist that such a factorization is not stable under pullback. To solve this problem we introduce the notion of  _type theoretic universe_ / _Martin-L&#246;f universe.

## Universes in $sSet$ and lifting of Grothendieck universes into presheaf toposes

A _universe in $sSet$_ is defined to be a Kan fibration $p_U:\tilde U\to U$.

Such a universe in $sSet$ may be obtained by lifting a Grothendieck universe $\mathcal{U}\in Set$ to a type theoretic universe $p_U:\tilde U\to U$ in a presheaf topos $\hat C=Set^{C^{op}}$ on some site $C$ by exponentiating $\mathcal{U}$ with the component-wise dependent sum and then forming the generalized universal bundle. To be more precise this is done by defining

$$\label{1}
U(I)=\mathcal{U}^{(C/I)^{op}}
$$
$$\label{2}
U(\alpha)=\mathcal{U}^{\Sigma_\alpha^{op}}

$$

where for a morphism $\alpha$ the _dependent sum_ ${\Sigma_\alpha^{op}}=\alpha\circ (-)$ is given by postcomposition with $\alpha$. The idea behind this is that $\mathcal{U}^{(C/I)^{op}}$ is quivalent to the full subcategory of $\hat C/Y(I)$ on those maps whose fibers are $\mathcal{U}$-small. The presheaf $\tilde U$ is defined as

$$\label{3}\tilde U(I)=\{\langle A,a\rangle | A\in U(I)\,\text{ and }\,a\in A(id_I)\}$$

and

$$\label{4}\tilde U(\alpha)(\langle A,a\rangle)=\langle U(\alpha)(A),A(\alpha\to id_I)(a)\rangle$$

for $\alpha:J\to I$ in $C$. The map $p_U:\tilde U\to U$ sends $\langle A,a\rangle$ to $A$. $p_U$ is generic for maps with $\mathcal{U}$-small fibers. These maps are up to isomorphism precisely those which can be obtained as pullback of $p_U$ along some morphism in $\hat C$.

For $C=\Delta$ we apapt this idea in such a way that $p_U$ is generic for Kan fibrations with $\mathcal{U}$-small fibers. We redefine in this case

$$\label{formula5}U([n])=\{A\in \mathcal{U}^{\Delta/[n])^{op}} | P_A\,\text{ is a Kan fibration }\,\}$$

where $P_A:Elts(A)\to \Delta[n]$ is obtained from $A$ by the Grothendieck construction: For $A:\Delta[n]\to U$ it is the pullback $(P_A:Elts(A)\to \Delta[n]):=A^* p_U$ of $p_U$ along $A$. For morphisms $\alpha$ in $\Delta$ we define $U(\alpha)$ as above since Kan fibrations are stable under pullbacks. $\tilde U$ and $p_U$ are defined as above in (3) and (4) but with the modified $U$, formula (5).


+-- {: .num_theorem #1}
###### Theorem
The simplicial set $U$, formula (5) is a Kan complex
=--

+-- {: .proof}
###### Proof
V. Voevodsky some draft papers and Coq files - www.math.ias.edu/&#8764;vladimir/Site3/Univalent Foundations.html
=--

+-- {: .num_theorem #2}
###### Theorem
For the simplicial set $U$, formula (5), the morphism $p_U:\tilde U\to U$ is universal for morphisms with $\mathcal{U}$-small fibers in that every morphisms with $\mathcal{U}$-small fibers arises as a pullback of $p_U$ along some morphism in $H$.
=--

+-- {: .proof}
###### Proof
$p_U$ is a Kan fibration since if

$$\array{
\Lambda_k[n]&\xrightarrow{a}&\tilde U
\\
\downarrow^{i_k^n}&&\downarrow^{p_U}
\\\Delta[n]&\xrightarrow{A}&U
}$$
 is commutative, the pullback of $p_U$ along $A$ is by definition the Kan fibration $P_A:Elts(A)\to \Delta[n]$. This gives a lift $\Delta[n]\to Elts(A)$ which composed with the projection $Elts(A)\to \tilde U$ provides the searched diagonal filler $\Delta[n]\to \tilde U$.

$p_U$ is universal since a Kan fibration $a:A\to I$ with $\mathcal{U}$-small fibers is the pullback of $p_U$ along the morphism $A:I\to U$ sending $x\in I([n])$ to an $\mathcal{U}$-valued presheaf on $\Delta/[n]$ which is isomorphic to $x^* a$ by the Grothendieck construction.

$$\array{
A_x&\to&A&\to&\tilde U
\\
\downarrow^{x^* a}&&\downarrow^a&&\downarrow^{p_U}
\\
* &\xrightarrow{x}&I&\xrightarrow{A}&U
}$$
=--

+-- {: .num_cor}
###### Corollary
The type theoretic universe $p_U:\tilde U\to U$, Theorem \ref{2}, is closed under dependent sums, products and contains the natural-numbers object $N:=\Delta(\mathbb{N})$.
=--

## Identity types in the lifted Grothendieck universe $U$

We consider the factorization $\tilde U\xrightarrow{r_{\tilde U}}Id_{\tilde U}\xrightarrow{p_{\tilde U}}\tilde U\times_U \tilde U$ of the diagonal $\delta_{p_{\tilde U}}$ of $p_{\tilde U}$ into an acyclic cofibration $r_{\tilde U}\in C\cap W$ followed by a fibration $p_{\tilde U}\in F$.

### Interpretation of the eliminator for identity types

For interpreting the eliminator $J$ for $Id$-types we pull back the whole situation along the projection

$$\Gamma:=(C:Id_{\tilde U}\xrightarrow{U}U^* U, d:\Pi_U(r^*_{\tilde U} C))$$

(...)

## Voevodsky' s univalence axiom

Now we will see that Voevodsky's univalence axiom holds in the model described above.

Fix the following notation

$iscontr(X :Set) := (\Sigma_x :X )(\Pi_y:Y ) Id_X (x, y)$ 

$hfiber(X, Y :Set)(f :X \to Y )(y:Y ) := (\Sigma_x :X ) Id_Y (f (x), y)$

$isweq(X, Y :Set)(f :X \to Y ) := (\Pi_y:Y ) iscontr(hfiber(X, Y , f , y))$

$Weq(X, Y :Set) := (\Sigma_f :X \to Y ) isweq(X, Y , f )$

The eliminator $J$ for identity types induces a canonical map

$$eqweq(X,Y:Set)isweq(eqweq(X,Y))$$

The univalence axiom claims then that all maps $eqweq(X,Y)$ are themselves weak equivalences, i.e.

+-- {: .num_defn}
###### Definition
$$UnivAx:(\Pi X, Y:Set)isweq(eqweq(X,Y))$$
=--

+-- {: .num_remark}
###### Remark
The univalence axiom implies the _function extensionality principle_: for $f,g:X\to Y$ we have

$$(\Pi x:X)Id_Y(fx,gx))\to Id_{X\to Y}(f,g)$$
=--

Even without the univalence axiom we have the following result corresponding to the fact that in $sSet$ a morphism to a Kan complex is a weak equivalence iff it is a homotopy equivalence.

+-- {: .num_remark}
###### Remark

$isweq(X,Y)(f)$ is equivalent to

$$isiso(X,Y)(f):=(\Sigma g :Y\to X)((\Pi x:X)Id_X(g(fx),x))\times ((\Pi y:Y)Id_Y(f(gy),y))$$
=--
