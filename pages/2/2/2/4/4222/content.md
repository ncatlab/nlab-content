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

and the nonempty hom-categories $hom(i, j) = \mathbf{B}(i, j)$ may be described as follows: 

* $hom(1, 1)$ is isomorphic to the "algebraist's $\Delta$" (see [[simplex category]]): the category of finite ordinals and order-preserving maps; 

* $hom(1, 2)$ is isomorphic to $\Delta_{\bot}$: the category of nonempty finite ordinals and order-preserving maps that preserve the bottom element; 

* $hom(0, 1)$ is isomorphic to $\Delta_{\top}$: the category of nonempty finite ordinals and order-preserving maps that preserve the top element; 

* $hom(0, 2)$ is isomorphic to the "topologist's $\Delta^{op}$", which is isomorphic to the category $\Delta_{\top, \bottom}$ of **finite intervals**, whose objects are finite ordinals with at least two elements, and whose morphisms are order-preserving maps that preserve both top and bottom. 

Note that the structure of $hom(1, 1)$ simply recapitulates the universal property of the algebraist's $\Delta$, as initial among strict monoidal categories equipped with a monoid $M$. This result is most easily understood in terms of string diagrams, and the structure of the other 
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
$$d_{n}^{i}: Y M^{n+1} X \to Y m^N X$$ 
are $\beta M^n X$ ($i = 0$), $Y M^{i-1} m M^{n-i} X$ ($1 \leq i \leq n$), and $Y M^n \alpha$ ($i = n+1$). 

* The $n+1$ degeneracy maps 
$$s_{n}^{i}: Y M^n X \to Y M^{n+1} X$$ 
are $Y M^i u M^{n-i} X$ ($0 \leq i \leq n$). 

## Examples ## 

### Classifying bundle ### 

Consider the cartesian monoidal category $Top$ as a 1-object bicategory $\Sigma Top$ (which we may strictify to a 2-category). A topological monoid $M$ is the same as a monad in $\Sigma Top$, and the usual meaning of left and right $M$-modules is preserved by thinking of them as modules over the monad. 

In particular, $M$ may be regarded as a left or right $M$-module, and the 1-point space $1$ carries a unique structure of left or right $M$-module. As a result we may consider the simplicial space 

$$B M = B(1, M, 1)$$ 

and the simplicial space 

$$E M = B($$ 

I've been kicked off the computer. I will return as soon as I can. 
