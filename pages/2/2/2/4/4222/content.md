#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A two-sided bar construction is a [[simplicial object]] associated with the data of a left [[module]] and right module over a [[monad]]. 

## Definition ## 

### Left and right modules ###

Let $\mathbf{B}$ be a [[2-category]], and let $M: B \to B$ be a monad with multiplication $m: M M \to M$ and unit $u: 1_B \to M$. Recall that a **left module** over $M$ consists of a 1-cell $X: A \to B$ and a 2-cell $\alpha: M X \to X$ such that the diagrams 

$$\array{
M M X & \stackrel{M\alpha}{\to} & M X & & & X & \stackrel{1_X}{\to} & X \\
m X \downarrow & & \downarrow \alpha & & & u X \downarrow & & \downarrow 1_X\\
M X & \underset{\alpha}{\to} & X & & & M X & \underset{\alpha}{\to} & X 
}$$

commute. A **right module** over $M$ consists of a 1-cell $Y: B \to C$ and a 2-cell $\beta: Y M \to Y$ such that the diagrams 

$$\array{
Y M M & \stackrel{\beta M}{\to} & Y M & & & Y & \stackrel{1_Y}{\to} & Y \\
Y m \downarrow & & \downarrow \beta & & & Y u \downarrow & & \downarrow 1_Y\\
Y M & \underset{\beta}{\to} & Y & & & Y M & \underset{\beta}{\to} & Y 
}$$

commute. 

### Initial structure ### 

With the aid of string diagrams, one may easily visualize the structure $\mathbf{I}$ that is initial amongst 2-categories equipped with the data of monad and left and right modules over the monad. The 2-category has three 0-cells $0$, $1$, and $2$, 1-cells which are of the form 

$$m^{\circ n}: 1 \to 1 \qquad y m^{\circ n}: 1 \to 2 \qquad m^{\circ n} x: 0 \to 1 \qquad y m^{\circ n} x: 0 \to 2,$$

and the nonempty hom-categories $hom(i, j) = \mathbf{I}(i, j)$ may be described as follows: 

* $hom(1, 1)$ is isomorphic to the "algebraist's $\Delta_a$" (see [[simplex category]]): the category of finite ordinals and order-preserving maps; 

* $hom(1, 2)$ is isomorphic to $\Delta_{\bot}$: the category of nonempty finite ordinals and order-preserving maps that preserve the bottom element; 

* $hom(0, 1)$ is isomorphic to $\Delta_{\top}$: the category of nonempty finite ordinals and order-preserving maps that preserve the top element; 

* $hom(0, 2)$ is isomorphic to the "topologist's $\Delta^{op}$" (the usual simplex category), which is isomorphic to the category $\Delta_{\top, \bottom}$ of **finite intervals**, whose objects are finite ordinals with at least two elements, and whose morphisms are order-preserving maps that preserve both top and bottom. 

Note that the structure of $hom(1, 1)$ simply recapitulates the universal property of the algebraist's $\Delta_a$, as initial among strict monoidal categories equipped with a monoid $M$. This result is most easily understood in terms of string diagrams, and the structure of the other 
hom-categories is guided by similar string diagram considerations. 

### Two-sided bar construction ### 

Now we give the definition. Suppose given a 2-category $\mathbf{B}$ together with a monad $M: B \to B$ in $\mathbf{B}$, together with a left module $X: A \to B$ and a right module $Y: B \to C$. There is a unique 2-functor 

$$\mathbf{I} \to \mathbf{B}$$ 

which preserves the monad and module structures, and this induces a functor 

$$\Delta^{op} \cong \mathbf{I}(0, 2) \to \mathbf{B}(A, C)$$ 

This functor is the **two-sided bar construction**, denoted $B(Y, M, X)$. 

The structure of the two-sided bar construction may be given more concretely as follows: 

* The $n$-dimensional component of $B(Y, M, X)$ is 
$$B(Y, M, X)_n = Y M^{\circ n} X$$ 

* The $n+2$ face maps 
$$d_{n}^{i}: Y M^{n+1} X \to Y M^n X$$ 
are $\beta M^n X$ ($i = 0$), $Y M^{i-1} m M^{n-i} X$ ($1 \leq i \leq n$), and $Y M^n \alpha$ ($i = n+1$). 

* The $n+1$ degeneracy maps 
$$s_{n}^{i}: Y M^n X \to Y M^{n+1} X$$ 
are $Y M^i u M^{n-i} X$ ($0 \leq i \leq n$). 

## Examples ## 

Two-sided bar constructions encapsulate a surprising number of constructions, a few of which follow. 

### Classifying bundle ### 

Consider the cartesian monoidal category $Top$ as a 1-object bicategory $\Sigma Top$ (which we may strictify to a 2-category). A topological [[monoid]] $M$ is the same as a monad in $\Sigma Top$, and the usual meaning of left and right $M$-modules is preserved by thinking of them as modules over the monad. 

In particular, $M$ may be regarded as a left or right $M$-module, and the 1-point space $1$ carries a unique structure of left or right $M$-module. As a result we may consider the simplicial space 

$$B M = B(1, M, 1)$$ 

as base space, and the simplicial space 

$$E M = B(M, M, 1)$$ 

as total space, of a simplicial fibration 

$$B(\pi, M, 1): B(M, M, 1) \to B(1, M, 1)$$ 

induced by the unique left module map $\pi: M \to 1$. This is the [[classifying bundle]] of the monoid $M$. 

### Cofibrant replacement ### 

If $M$ is a monad and $(X, \alpha: M X \to X)$ is a (left-sided) $M$-algebra, then with $M$ acting upon itself on the right, there is a simplicial object 

$$B(M, M, X)$$ 

which may be regarded as a _cofibrant replacement_ of $X$, a simplicial $M$-algebra which as a simplicial object is homotopy-equivalent to the constant simplicial object at $X$. (More should be added here.) See also [[bar construction]]. 

Rather more generally, if in addition $(Y, \beta: Y M \to Y$ is a right $M$-module, we may denote the coequalizer of the pair 

$$Y M X \stackrel{\overset{\beta X}{\to}}{\underset{Y \alpha}{\to}} Y X$$ 

(if it exists) by $Y \circ_M X$, and think of it as the _tensor product_ (over $M$) of $Y$ and $X$. The general principle is that the simplicial object $B(Y, M, X)$ is canonically augmented by $Y \circ_M X$, and serves as a cofibrant replacement of $Y \circ_M X$ when the latter is regarded as a constant simplicial object. See also homotopy colimits, below. 

### Canonical two-sided bar construction of an adjunction ### 

Suppose given any [[adjoint pair]] $(F: B \to A) \dashv (U: A \to B)$ in a 2-category $\mathbf{B}$, with counit $\varepsilon: F U \to 1_A$. There is an associated monad $M = U F: B \to B$, and a canonical left $M$-action on $U$: 

$$\alpha = U \varepsilon: U F U \to U,$$ 

and a canonical right $M$-action on $F$: 

$$\beta = \varepsilon F: F U F \to F.$$ 

We may then form the canonical simplicial object $B(F, M, U)$. By general abstract nonsense, the tensor product $F \circ_M U$ is $1_A$, so if we regard $1_A$ as a constant simplicial object $\Delta^{op} \to \mathbf{B}(A, A)$, the cofibrant replacement result above specializes as follows. 

+-- {: .un_prop}
######Proposition 
The canonical simplicial map $B(F, M, U) \to 1_A$ is a simplicial [[homotopy equivalence]]. 
=--

#### Delooping machines #### 

The classic application of this two-sided bar construction was given by Peter May, after work of Jon Beck. Let $\Omega = Top_{*}(S^1, -): Top_{*} \to Top_{*}$ be the loop space functor on pointed spaces, with left adjoint the suspension functor $S = S^1 \wedge -: Top_{*} \to Top_{*}$. For each $n \geq 1$, the adjunction $S^n \dashv \Omega^n$ induces a monad $\Omega^n S^n$ which acts (on the left) on $n$-fold loop spaces $\Omega^n X$, and acts on the right on $S^n$. 

+-- {: .un_prop}
######Proposition 
The canonical simplicial map $B(S^n, \Omega^n S^n, \Omega^n X) \to X$ is a simplicial [[homotopy equivalence]]. 
=--

So if $Y$ is an $n$-fold loop space, the two-sided bar construction $B(S^n, \Omega^n S^n, Y)$ provides its $n$-fold delooping. 

Continuing this train of thought: suppose given a monad $C_n$ equipped with a monad map $\phi: C_n \to \Omega^n S^n$ (which is [[mate]]d to an action $C_n \Omega^n \to \Omega^n$) such that $\phi$ is objectwise a homotopy equivalence. Then $\phi$ induces a homotopy equivalence 

$$B(S^n, \phi, \Omega^n): B(S^n, C_n, \Omega^n) \to B(S^n, \Omega^n S^n, \Omega^n)$$ 

The classic example of this is where $C_n$ is the little $n$-cubes operad, which acts canonically on $\Omega^n = Top_{*}(S^n, -)$. The advantage is that the monad $C_n$ is much more tractable than $\Omega^n S^n$. 

Continuing this thought still further, we have the following recognition theorem of May: 

+-- {: .un_thm}
######Theorem 
Suppose $Y$ is a connected space with a $C_n$-action. Then $Y$ is homotopy equivalent to an $n$-fold loop space, and indeed there is a canonical span 
$$\Omega^n B(S^n, C_n, Y) \leftarrow B(\Omega^n S^n, C_n, Y) \to B(\Omega^n S^n, \Omega^n S^n, Y) \simeq Y$$
where each of the arrows is a homotopy equivalence. 
=-- 

+--{.query}
I'm going on sheer memory here of May's Geometry of Iterated Loop Spaces, and it's quite possible that I'm missing hypotheses in some directions and that hypotheses could be weakened in other directions, e.g., replacing the connectedness assumption with a group completion assumption. This is in need of expert attention.
=--

### Homotopy colimits ### 

Suppose that $C$ is a small category and $F: C \to Top$ is a functor. We may regard $C$ as a monad $C: C_0 \to C_0$ in the bicategory of [[span]]s in $Top$, where $C_0$ is the set of objects with the discrete category, and we may regard $F$ as a left module over the monad $C$. 

As always, the terminal object $1$ carries a unique right module structure. The usual colimit, $colim F$, may be described as the tensor product 

$$colim F \cong 1 \circ_C F$$ 

As a result, we have the cofibrant replacement $B(1, C, F)$ of $colim F$. The geometric realization of the simplicial space $B(1, C, F)$ is none other than the **[[homotopy colimit]]** of $F$. 
