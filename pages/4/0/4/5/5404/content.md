* tic
{: toc}

### Idea ###

On this page we shall record those aspects of the theory of Fr&#246;licher spaces that are particularly categorical in nature.

### Limits and Colimits ###

+-- {: .num_prop #colimlim}
###### Proposition
Every Fr&#246;licher space is functorially the limit and colimit of a diagram of manifolds.  In fact, is a limit or colimit of a diagram in the full subcategory consisting of the single object $\mathbb{R}$.
=--

+-- {: .proof}
###### Proof
Let $(X,C,F)$ be a Fr&#246;licher space.  Let $\mathcal{C}$ be the category whose objects are the elements of $C$ and the morphisms $c \to c'$ correspond to the smooth functions $g \colon \mathbb{R} \to \mathbb{R}$ with $c' g = c$.  Define a functor $G \colon \mathcal{C} \to Fro$ by sending each object to $\mathbb{R}$ and sending each morphism $c \to c'$ to the corresponding smooth function.

We claim that $(X,C,F)$ is the colimit of this functor.  The morphism $G(c) \to (X,C,F)$ is simply $c$ (note that $C = Hom_{Fro}(\mathbb{R},X)$ so $c$ is a morphism in $Fro$).  Given a sink $g \colon G \to (Y,C_Y,F_Y)$, we define a morphism $(X,C,F) \to (Y,C_Y,F_Y)$ as follows.  Let $x \in X$.  Then there is a curve $c_x \in C$ which is the constant curve at $x$.  Then $g_{c_x} \colon \mathbb{R} \to (Y,C_Y,F_Y)$ is a constant curve in $Y$, so defines a point in $Y$.

*... to be continued ...*


=--