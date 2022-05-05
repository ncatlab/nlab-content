
+-- {: .num_prop #InitialObjectIsLimitOverIdentityFunctor}
###### Example
**([[initial object]] is [[limit]] over [[identity functor]])**

Let $\mathcal{C}$ be a [[category]], and let $\emptyset \in \mathcal{C}$ be an [[object]]. The following are equivalent:

1. $\emptyset$ is an [[initial object]] of $\mathcal{C}$;

1. $\emptyset$ is the [[limit]] of the [[identity functor]] on $\mathcal{C}$.

=--

+-- {: .proof}
###### Proof

First let $\emptyset$ be an [[initial object]]. Then, by definition, it is the tip of a unique [[cone]] over the identity functor

\[
  \label{InitialObjectCone}
  \array{
    const_{\emptyset}&\phantom{AA}& && \emptyset
    \\
    {}^{\mathllap{i^{\emptyset}}}\Downarrow && & {}^{\mathllap{i^{\emptyset}_{c_1}}}\swarrow && \searrow^{\mathrlap{i^{\emptyset}_{c_2}}}
    \\
    id_{\mathcal{C}} && c_1 && \underset{f}{\longrightarrow} && c_2
  }
\]

We need to show that that every other cone $i^x$

$$
  \array{
    const_{x}&\phantom{AA}& && x
    \\
    {}^{\mathllap{\mathllap{i^x}}}\Downarrow && & {}^{i^x_{c_1}}\swarrow && \searrow^{\mathrlap{i^x_{c_2}}}
    \\
    id_{\mathcal{C}} && c_1 && \underset{f}{\longrightarrow} && c_2
  }
$$

factors uniquely through $i^\emptyset$. 

First of all, since the cones are over the identity functor, there is the component $i^x_{\emptyset} \;\colon\; x \to \emptyset$, and it is a morphism of cones. 

To see that this is the unique morphism of cones, consider any morphism of cones $j^x_\emptyset$, hence a morphism in $\mathcal{C}$ such that $i^x_c = i^\emptyset_c  \circ j^x_\emptyset $ for all $c \in \mathcal{C}$. Taking here $c = \emptyset$ yields

$$
  \begin{aligned}
    i^x_\emptyset 
      & = 
    \underset{ = id_\emptyset }{\underbrace{i^\emptyset_{\emptyset}}} \circ j^x_{\emptyset}
    \\
    & = j^x_\emptyset
    \,,
  \end{aligned}
$$

where under the brace we used that $\emptyset$ is initial. This proves that $i^\emptyset$ is the limiting cone.

For the converse, assume now that $i^\emptyset$ is a limiting cone over the identity functor, with labels as in (eq:InitialObjectCone). We need to show that its tip $\emptyset$ is an initial object. 

Now the cone condition applied for any object $x \in \mathcal{C}$ over the morphims $f \coloneqq i^\emptyset_x$ says that 

$$
  i^{\emptyset}_x \circ i^\emptyset_\emptyset = i^\emptyset_x
$$

which means that $i^\emptyset_\emptyset$ constitutes a morphism of cones from $i^\emptyset$ to itself. But since $i^\emptyset$ is assumed to be a limiting cone, and since the [[identity morphism]] on $\emptyset$ is of course also a morphism of cones from $i^\emptyset$ to itsely, we deduce that

\[
  \label{iemptyemptyIsIdempty}
  i^\emptyset_\emptyset 
   \;=\;
  id_{\emptyset}
  \,.
\]

Now consider any morphism of the form $\emptyset \overset{f}{\to} x$. Since we already have the morphism $\emptyset \overset{i^\emptyset_x}{\to} x$, to show initiality of $\emptyset$ we need to show that $f = i^\emptyset_x$.

Indeed, the cone condition of $i^\emptyset_x$ applied to $f$ now yields

$$
  \begin{aligned}
    i^\emptyset_x
    & = 
    f \circ \underset{ = id_{\emptyset} }{\underbrace{i^\emptyset_\emptyset}}
    \\
    & =
    f\,,
  \end{aligned}
$$

where under the brace we used (eq:iemptyemptyIsIdempty).

=--

