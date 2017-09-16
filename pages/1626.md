A [[topological space]] $X$ is **connected** if 

$$hom(X, -): Top \to Set$$ 

preserves [[coproduct]]s. Equivalently, a space $X$ is connected if 

* It is nonempty, and 

* If $X \cong Y + Z$, where the right side is the coproduct of spaces $Y, Z$ (so that $Y, Z$ are identified with disjoint open subspaces of $X$), then one of $Y, Z$ is empty. Or again: if $K \subseteq X$ is **clopen** (closed and open), and $\exists_{x \in X} x \in K$, then $K = X$. 

Many authors drop the condition of nonemptiness, defining a space to be connected if it cannot be expressed as the union of two disjoint nonempty open subsets, thus allowing the empty space to be considered connected. However, many results come out more cleanly by disqualifying the empty space (much as one disqualifies $1$ when one defines the notion of 'prime number'). See also the discussion at [[empty set]]. 

## Basic results ## 

1. The [[image]] of a connected space $X$ under a continuous map $f: X \to Y$ is connected. 

1. (Wide) [[pushout]]s of connected spaces are connected. (This would of course be false if the empty space were considered to be connected.) This follows from the hom-functor definition of connectedness, plus the fact that coproducts in $Top$ commute with wide pullbacks. 

1. An arbitrary product of connected spaces is connected.  

1. The interval $[0, 1]$, as a subspace of $\mathbb{R}$, is connected. (This is the topological underpinning of the intermediate value theorem.) 

1. If $S \subseteq X$ is a connected subspace and $S \subseteq T \subseteq \overline{S}$ (i.e. if $T$ is between $S$ and its closure), then $T$ is connected. 

## Connected components ## 

Every topological space $X$ admits an equivalence relation $\sim$ where $x \sim y$ means that $x$ and $y$ belong to some subspace which is connected. The equivalence class $Conn(x)$ of an element $x$ is thus the union of all connected subspaces containing $x$; it follows readily from the basic results above that $Conn(x)$ is itself connected. It is called the **connected component** of $x$. It is closed, by one of the basic results above.  

Alternatively, observe that if $x \in C$ and $x \in K$, where $C$ is a connected subspace and $K$ is clopen, then $C \subseteq K$. Moreover, the intersection of all clopens containing $x$ is itself connected (because it cannot be further subdivided by a clopen). Hence 

$$Conn(x) = \bigcup_{clopen K: x \in K} K$$ 

**Warning:** It is not generally true that a space is the coproduct (in $Top$) of its connected components. For example, the connected components in Cantor space $2^{\mathbb{N}}$ (with its topology as a product of 2-point discrete spaces) are just the singletons, but the coproduct of the singleton subspaces carries the discrete topology. 

Indeed, a space is the coproduct of its connected components precisely when it is **locally connected** (meaning that every point has a connected neighborhood). This occurs for example if there are only finitely many connected components (because then each connected component will be both closed and open). 

## Path-connectedness ## 

An important variation on the theme of connectedness is path-connectedness. If $X$ is a space, define the path component $[x]$ to be the subspace of all $y \in X$ for which there exists a continuous map $h: [0, 1] \to X$ where $h(0) = x$, $h(1) = y$. We say $X$ is **path-connected** if it has exactly one path component. 

It follows easily from the basic results above that each path component $[x]$ is connected. However, it need not be closed (and therefore need not be the connected component of $x$). The **topologist's sine curve** 

$$\{(x, y) \in \mathbb{R}^2: (0 \lt x \leq 1 \wedge y = sin(1/x)) \vee (0 = x \wedge -1 \leq y \leq 1)\}$$ 

provides a classic example of this happenstance. However, the path components and connected components coincide if $X$ is **locally path-connected** (meaning each point has an open neighborhood which is path-connected). 

The basic categorical results 1., 2., and 3. above carry over upon replacing "connected" by "path-connected". (As of course does 4., trivially.) 

