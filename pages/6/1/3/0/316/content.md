> This entry is mostly about cones in [[homotopy theory]] and [[category theory]]. For more geometric cones see at _[[cone (Riemannian geometry)]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In [[homotopy theory]], the _cone_ of a [[space]] $X$ is the space obtained by taking the $X$-shaped [[cylinder object|cylinder]] $X \times I$, where $I$ may be an [[interval object]], and squashing one end down to a point.  The eponymous example is where $X$ is the [[circle]], i.e. the [[topological space]] $S^1$, and $I$ is the standard interval $[0,1]$.  Then the [[cartesian product]] $X \times I$ really is a [[cylinder]], and the cone of $X$ is likewise a cone.

This notion also makes sense when $X$ is a [[category]], if $I$ is taken to be the [[interval category]] $\{ 0 \to 1 \}$, i.e. the [[ordinal]] $\mathbf{2}$.  Note that since the interval category is directed, this gives two different kinds of cone, depending on which end we squash down to a point.

Another, perhaps more common, meaning of 'cone' in category theory is that of a _cone over (or under) a [[diagram]]_.  This is just a [[diagram]] over the cone category, as above.  Explicitly, a cone over $F\colon J \to C$ is an [[object]] $c$ in $C$ equipped with a [[morphism]] from $c$ to each vertex of $F$, such that every *new* triangle arising in this way [[commutative triangle|commutes]].  A cone which is [[universal property|universal]] is a [[limit]].

In [[category theory]], the word _[[cocone]]_ is sometimes used for the case when we squash the other end of the interval; thus $c$ is equipped with a morphism *to* $c$ *from* each vertex of $F$ (but $c$ itself still belongs to $C$).  A cocone in this sense which is universal is a [[colimit]].  However, one should beware that in homotopy theory, the word [[mapping cocone|cocone]] is used for a different dualization.

This definition generalizes to [[higher category theory]]. In particular in [[(∞,1)-category theory]] a cone over an [[∞-groupoid]] is essentially a cone in the sense of [[homotopy theory]].


## Definition

### In homotopy theory

If $X$ is a space, then the cone of $X$ is the [[homotopy pushout]]
of the identity on $X$ along the unique map to the point:

$$
\array{
  X & \to & X \\
  \downarrow & & \downarrow \\
  * & \to & cone(X)
}\,.
$$

This homotopy pushout can be computed as the ordinary [[pushout]] $cone(X) := X\times I \amalg_X *$

$$
  \array{
    X &\stackrel{d_1}{\to} & X \times I
    \\
    \downarrow && \downarrow
    \\
    * &\to& cone(X)
  }
  \,.
$$

If $X$ is a [[simplicial set]], then the cone of $X$ is the [[join of simplicial sets|join]] of $X$ with the point.

The [[mapping cone]] (q.v.) of a morphism $f \colon X \to Y$ is then the pushout along $f$ of the inclusion $X \to cone(X)$.


### As a monad 

In contexts where [[intervals]] $I$ can be treated as [[monoid]] objects, the cone construction as quotient of a cylinder with one end identified with a point, 

$$C(X) = I \times X/(0 \times X) \sim p,$$ 

carries a structure of [[monad]] $C$. In such cases, the monoid has a multiplicative [[identity]] $1$ and an absorbing element $0$, where multiplication by $0$ is the constant map at $0$. In that case, a $C$-algebra consists of an object $X$ together with 

* An [[action]] of the monoid, $a: I \times X \to X$. 

* A constant or basepoint $x_0 \colon 1 \to X$ 

such that $a(0, x) = x_0$ for all $x$. This equation can be expressed in any category $\mathbf{C}$ with finite products and a suitable interval object $I$ as monoid (for example, $Top$, where $I = [0, 1]$ is a monoid under real multiplication, or under $min$ as multiplication). Under some reasonable assumptions (e.g., if the $\mathbf{C}$ has quotients, and these are preserved by the functor $I \times -$), the category of $C$-algebras will be monadic over $\mathbf{C}$ and the free $C$-algebra on $X$ will be $C(X)$ as described above. The category of $C$-algebras will also be monadic over the category of pointed $\mathbf{C}$-objects, $1 \downarrow \mathbf{C}$. 

These observations apply for example to $Top$, and also to $Cat$ where the [[interval category]] $\mathbf{2}$ is a monoid in $Cat$ under the $min$ operation (see below). 

If in addition the underlying category $\mathbf{C}$ is [[cartesian closed category|cartesian closed]], or more generally if $I$ is [[exponentiable object|exponentiable]], the monad $C$ on pointed $\mathbf{C}$-objects also has a [[right adjoint]] $P$ which can be regarded as a [[path space]] construction $P$, where we have a pullback 

$$\array{
P(X) & \to & 1 \\
\downarrow & & \downarrow \\
X^I & \stackrel{eval_0}{\to} & X.
}$$ 

For general abstract reasons, the right adjoint $P$ carries a comonad structure whereby $C$-algebras are equivalent to $P$-coalgebras. Considered over the category of simplicial sets, this is closely connected to [[decalage]]. 

### In category theory

If $C$ is a category, then the cone of $C$ is the [[cocomma category]] of the identity on $C$ and the unique map to the terminal category:

$$
\array{
  C & \to & C \\
  \downarrow & \Rightarrow  & \downarrow \\
  * & \to & cone(C)
}\,.
$$

Again, this may be computed as a pushout:

$$
  \array{
    C &\stackrel{d_1}{\to} & C \times \mathbf{2}
    \\
    \downarrow && \downarrow
    \\
    * &\to& cone(C)
  }
  \,.
$$

The cone of $C$ may equivalently be thought of, or defined, as the result of adjoining a new [[initial object]] to $C$.

### Cones over a diagram

A cone *in* a category $C$ is given by a category $J$ together with a [[functor]] $cone(J) \to C$.  By the [[universal property]] of the cocomma category, to give such a functor is to give an object $c$ of $C$, a functor $F \colon J \to C$, and a [[natural transformation]]
$$T: \Delta(c) \to F$$ 
where $\Delta(c):J\to C$ denotes the [[constant functor]] at the object $c$.  Such a transformation is called a _cone over the diagram_ $F$.

In other words, a cone consists of morphisms (called the **components** of the cone) 

$$T_j: c \to F(j),$$

one for each object $j$ of $J$, which are compatible with all the morphisms $F(f): F(j) \to F(k)$ of the diagram, in the sense that each diagram 
$$\array{
{}&{}&c&{}&{} \\
{}& \mathllap{\scriptsize{T_j}}\swarrow &{}& \searrow\mathrlap{\scriptsize{T_k}} &{}  \\
F(j) &{}&\stackrel{F(f)}{\longrightarrow} &{}& F(k) \\
}
$$
commutes.

It's called a cone because one pictures $c$ as sitting at the vertex, and the diagram itself as forming the base of the cone. 

A [[cocone]] in $C$ is precisely a cone in the [[opposite category]] $C^{op}$.


### Over a diagram in an $(\infty,1)$-category

For $F : D \to C$ a [[diagram]] of [[(∞,1)-categories]], i.e. an [[(∞,1)-functor]], the $(\infty,1)$-category of $(\infty,1)$-cones over $F$ is the [[over quasi-category]] denoted $C_{/F}$. Its objects are cones over $F$. Its [[k-morphism]]s are $k$-homotopies between cones. The [[limit in a quasi-category|(∞,1)-categorical limit]] over $F$ is, if it exists, the [[terminal object]] in $C_{/F}$.


## See also

These are shaped like the homotopy-theoretic cone, so maybe there is a deeper relationship:

* [[positive cone]] (in an [[ordered group]], such as an [[operator algebra]]),
* [[future cone]] (of an [[event]] in a [[Lorentzian manifold]], such as [[spacetime]]),
* [[convex cone]] (in a [[vector space]]).


[[!redirects cone]]
[[!redirects cones]]
