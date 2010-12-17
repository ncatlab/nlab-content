* tic
{: toc}

### Idea ###

On this page we shall record those aspects of the theory of Fr&#246;licher spaces that are particularly categorical in nature.

### Colimits ###

+-- {: .num_prop #colim}
###### Proposition
Every Fr&#246;licher space is functorially the colimit of a diagram of manifolds.  In fact, it is a colimit of a diagram in the full subcategory consisting of the single object $\mathbb{R}$.
=--

+-- {: .proof}
###### Proof
Let $(X,C,F)$ be a Fr&#246;licher space.  Let $\mathcal{C}$ be the category whose objects are the elements of $C$ and the morphisms $c \to c'$ correspond to the smooth functions $g \colon \mathbb{R} \to \mathbb{R}$ with $c' \circ g = c$.  Note that for a fixed curve $c'$ and a smooth function $g \colon \mathbb{R} \to \mathbb{R}$ then from the definition of a Fr&#246;licher space there is a curve $c \in C$ such that $g$ defines a morphism $c \to c'$ (take $c = c' \circ g$).

Define a functor $G \colon \mathcal{C} \to Fro$ by sending each object to $\mathbb{R}$ and sending each morphism $c \to c'$ to the corresponding smooth function.
We claim that $(X,C,F)$ is the colimit of this functor.  The morphism $G(c) \to (X,C,F)$ is simply $c$ (note that $C = Hom_{Fro}(\mathbb{R},X)$ so $c$ is a morphism in $Fro$).

Now suppose that we have suitable morphisms $g_c \colon G(c) \to (Y,C_Y,F_Y)$.  For each $x \in X$, there is a constant curve $c_x \colon \mathbb{R} \to X$ at $x$ (these are characterised by the fact that if $h \colon c \to c_x$ is a morphism in $\mathcal{C}$ then $c = c_x$).  Consider $g_{c_x} \colon \mathbb{R} \to Y$.  We shall show that this is a constant curve in $Y$.  Let $h \in C^\infty(\mathbb{R},\mathbb{R})$ and examine $g_{c_x} \circ h$.  As the $g_c$ are compatible, $g_{c_x} \circ h = g_{c_x \circ h}$.  But as $c_x$ is constant, $c_x \circ h = c_x$ so $g_{c_x} \circ h = g_{c_x}$ and thus $g_{c_x}$ is constant.

Define $h \colon X \to Y$ by $h(x) = g_{c_x}(0)$.  This is a set map, let us show that it lifts to Fr&#246;licher spaces.  To do this, we look at $h \circ c$ for a smooth curve $c \in C$.  Let $t \in \mathbb{R}$ and let $x = c(t)$ in $X$.  Then $(h \circ c)(t) = h(x) = g_{c_x}(0)$.  Let $f_t \colon \mathbb{R} \to \mathbb{R}$ be the constant function at $t$.  Then $c \circ f_t = c_x$ and so $g_c \circ f_t = g_{c_x}$.  Thus $g_{c_x}(0) = (g_c \circ f_t)(0) = g_c(t)$.  Hence $h \circ c = g_c$.  As $g_c \colon \mathbb{R} \to (Y,C_Y,F_Y)$ is a morphism in the category of Fr&#246;licher spaces with source $\mathbb{R}$, it is an element of $C_Y$.  Hence $h$ takes smooth curves in $X$ to smooth curves in $Y$ and so is a morphism of Fr&#246;licher spaces.

This also establishes $(X,C,F)$ as the colimit since we have the factorisation $g_c = h \circ c$.
=--
