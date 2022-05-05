
First observe that for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ two [[presheaves]], their [[Cartesian product]] is a [[colimit]] over [[representable presheaf|presheaves represented]] by Cartesian products in $\mathcal{C}$ as

$$
  \mathbf{X} \times \mathbf{Y}
  \;\simeq\;
  \int^{c_1,c_2 \in \mathcal{C}}
  y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
  \,.
$$

This is due to the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
    (\mathbf{X} \times \mathbf{Y})(c)
    & \simeq
    \left(
      \int^{c_1 \in \mathcal{C}}
      \mathcal{C}(c,c_1) \times \mathbf{X}(c_1)
    \right)
    \times
    \left(
      \int^{c_2 \in \mathcal{C}}
      \mathcal{C}(c,c_2) \times \mathbf{Y}(c_2)
    \right)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}}
    \int^{c_2 \in \mathcal{C}}
    \underset{
      \simeq \mathcal{c}(c, c_1 \times c_2)
    }{
    \underbrace{
      \mathcal{C}(c,c_1) \times \mathcal{C}(c,c_2)
    }}
    \times 
    \left( 
      \mathbf{X}(c_1) \times \mathbf{X}(c_2)
    \right)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}}
    \int^{c_2 \in \mathcal{C}}
    \mathcal{C}(c,c_1 \times c_2)
    \times 
       \mathbf{X}(c_1) \times \mathbf{X}(c_2)
  \end{aligned}
$$

where the first step expands out both presheaves as colimits of representables separately, via the [[co-Yoneda lemma]], the second step uses that the [[Cartesian product]] of presheaves is a [[left adjoint]] (by the [[closed monoidal structure on presheaves]]) and [[adjoints preserve (co-)limits|as such preserves colimits]] (in particular [[coends]]) and under the brace we use the defining [[universal property]] of the [[Cartesian products]], assumed to exist in $\mathcal{C}$.

Now observe that the [[colimit]] of a [[representable presheaf]] is the [[singleton]].

$$
  \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim} y(c)
  \;\simeq\;
  \ast
  \,.
$$

One way to see this is to regard the colimit as the [[left Kan extension]] along the unique functor $\mathcal{C}^{op} \overset{p}{\to} \ast$ to the [[terminal category]]. By the formula [there](Kan+extension#PointwiseByCoEnds), this yields

$$
  \begin{aligned}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    y(c)
    & \simeq
    \int^{c_1 \in \mathcal{C}} 
      \underset{const_\ast(c_1)}{\underbrace{\ast(-,p(c_1))}} \times y(c)(c_1)
    \\
    & \simeq
    \int^{c_1 \in \mathcal{C}} const_\ast(c_1) \times \mathcal{C}(c_1,c) 
    \\
    & \simeq const_\ast(c)
    \\
    & \simeq \ast
  \end{aligned}
$$

where we made explicit the [[constant functor]] $const_\ast \;\colon\; \mathcal{C} \to Set$, constant on the [[singleton]] set $\ast$, and then applied the [[co-Yoneda lemma]] in the last step.

Now we compute for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$:

$$
  \begin{aligned}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \left(
      \mathbf{X} \times \mathbf{Y}
    \right)
    & 
    \simeq 
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \int^{c_1,c_2 \in \mathcal{C}}
    y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
    \left(
      y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \right)
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \left(
      \underset{
        \simeq \ast
      }{
      \underbrace{
        \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim}
        y(c_1 \times c_2) 
      }}
    \right)
    \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \\
    & \simeq
    \int^{c_1,c_2 \in \mathcal{C}}
    \left( 
      \mathbf{X}(c_1) \times \mathbf{Y}(c_2)  
    \right)
    \\
    & \simeq
    \left(
      \int^{c_1\in \mathcal{C}}
      \mathbf{X}(c_1) 
    \right)
    \times 
    \left(
      \int^{c_2\in \mathcal{C}}
      \mathbf{Y}(c_2)  
    \right)
    \\
    & \simeq
    \left(
      \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
      \mathbf{X}
    \right)
    \times
    \left(
      \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
      \mathbf{Y}
    \right)
  \end{aligned}
$$