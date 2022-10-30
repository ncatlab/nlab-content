## Overview ##

If $C$ is a [[locally small category]], then we say a [[functor]] 

$$F: C^{op} \to Set$$ 

is **representable** if it is [[natural isomorphism|naturally isomorphic]] to a [[hom-functor]] $\hom_C(-, c): C^{op} \to Set$. The object $c$ is determined uniquely up to isomorphism, and is called a **representing object** for $F$. 

Representability is one of the most fundamental concepts of category theory, with close ties to the notion of [[adjoint functor]] and to the [[Yoneda lemma]]. It is the crucial concept underlying the idea of [[universal property]]; thus for example crucial concepts such as "[[limit]]", "[[colimit]]", "[[exponential]]", "[[Kan extension]]" and so on are naturally expressed in terms of representing objects. The concept permeates much of algebraic geometry and algebraic topology. 

## Discussion ## 

More precisely, given a functor $F: C^{op} \to Set$ (also called a [[presheaf]] on $C$), a **representation** of $F$ is a specified natural isomorphism 

$$\theta: \hom_C(-, c) \stackrel{\sim}{\to} F$$ 

By the Yoneda lemma, any such transformation $\theta$ (isomorphism or not) is uniquely determined by an element $\xi \in F(c)$. As above, the object $c$ is called a **representing object** (or often, **universal object**) for $F$, and the element $\xi$ is called a **universal element** for $F$. Again, it follows from the Yoneda lemma that...  WHAT?

Following the proof of the Yoneda lemma, representability means precisely this: given any object $x$ of $C$ and any element $\alpha \in F(x)$, there exists a unique morphism $f: x \to c$ such that the function $F(f)$ carries the universal element $\xi \in F(c)$ to $\alpha \in F(x)$. Such a dry formulation fails to convey the remarkable power of this concept, which can really only be appreciated through the myriad examples which illustrate it. 

### Example 1: limits ###

If $F:J\to C$ is a diagram in $C$, we can construct a diagram $\hom_C(-,F)$ in the [[functor category]] $Set^{C^{op}}$ as the composite of $F$ with the curried [[hom-functor]] $C\to\Set^{C^{op}}$.  The object-wise [[limit]] of this diagram in [[Set]], that is, the functor $C^{op}\to\Set$ sending on object $x$ to the set which is the limit of the diagram $\hom_C(x,F):J\to\Set$, is representable iff the diagram $F$ has a limit in $C$; in fact, a representing object for that limit functor is exactly $\lim F$, and we obtain a natural isomorphism

$$\lim\hom_C(-,F)\cong\hom_C(-,\lim F).$$

For an example in the case of [[categorical product]], let $c, d$ be objects of $C$, and consider the presheaf given by a product of [[hom-functor|hom-functors]]

$$\hom_C(-, c) \times \hom_C(-, d): C^{op} \to Set;$$ 

that is, the functor which takes an object $x$ of $C$ to the set $\hom_C(x, c) \times \hom_(x, d)$. A categorical product $c \times d$ is precisely a representing or universal object for this presheaf, where the universal element is precisely the pair of projection maps 

$$(\pi_c, \pi_d) \in \hom(c \times d, c) \times \hom(c \times d, d)$$ 

We leave it to the reader to check that the representability here means precisely that given a pair 
of maps 

$$(f, g) \in \hom(x, c) \times \hom(x, d)$$ 

there exists a unique element in $\hom(x, c \times d)$, denoted $langle f, g \rangle$, such that 

$$\pi_c \langle f, g \rangle = f \qquad \pi_d \langle f, g \rangle = g.$$

### Example 2: exponentials ### 

Suppose $C$ is a category which admits finite products; given objects $c, d$, consider the presheaf 

$$\hom_C(- \times c, d): C^{op} \to Set.$$ 

A representing or universal object for this presheaf is an exponential $d^c$; the universal element 

$$e \in \hom_C(d^c \times c, d)$$ 

is a morphism called the **evaluation** map $eval: d^c \times c \to d$. 

### Example 3: classifying bundles ### 

Consider a category $Top$ of 'nice' spaces (just to fix the discussion, let's say paracompact spaces, although this is a technical point), and a topological group $G$ therein, i.e., a group internal to $Top$. There is a presheaf 

$$G-Bund: Top^{op} \to Set$$ 

which assigns to each space $X$ the set of isomorphism classes of $G$-bundles over $X$, and assigns to each continuous map $f: X \to Y$ the function 

$$G-Bund(f): G-Bund(Y) \to G-Bund(X)$$ 

which carries a (class of a) G-bundle $E \to Y$ to the (class of the) pullback bundle $f^*E \to X$. It is well-known that the pullback construction is invariant with respect to homotopic deformations; that is, this presheaf descends to a functor on the homotopy category, 

$$G-Bund: Ho_{Top}^{op} \to Set.$$ 

A **[[classifying space]]** $B G$ is precisely a representing object for this functor; the universal element is the (class of the) classifying $G$-bundle $[\pi: E G \to B G]$. 

These general considerations are quite commonplace in algebraic topology, where they crop up for example in the connection between generalized cohomology theories and spectra; cf. Brown's representability theorem. 