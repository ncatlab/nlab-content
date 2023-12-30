
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A basic example of [[limits commuting with colimits]] in [[category theory]] is that [[colimits]] over [[opposite categories]] of categories with [[finite products]] preserves [[finite products]]. One says equivalently that categories with [[finite products]] are _[[cosifted categories]]_.


## Statement

+-- {: .num_example #CategoriesWithFiniteProductsAreCosifted}
###### Example
**([[categories with finite products are cosifted]])**

Let $\mathcal{C}$ be a [[small category]] which has [[finite products]]. Then $\mathcal{C}$ is a _[[cosifted category]]_, equivalently its [[opposite category]] $\mathcal{C}^{op}$ is a _[[sifted category]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] are _[[sifted colimits]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] _[[limits commuting with colimits|commute]] with [[finite products]]_, as follows:

For $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ to [[functors]] on the [[opposite category]] of $\mathcal{C}$ (hence two [[presheaves]] on $\mathcal{C}$) we have a [[natural isomorphism]]

$$
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
  \left(
    \mathbf{X} \times \mathbf{Y}
  \right)
  \;\simeq\;
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{X}
  \right)
  \times
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{Y}
  \right)
  \,.
$$ 

=--

+-- {: .proof}
###### Proof


First observe that for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ two [[presheaves]], their [[Cartesian product]] is a [[colimit]] over [[representable presheaf|presheaves represented]] by Cartesian products in $\mathcal{C}$. Explicity, using [[coend]]-notation, we have:

\[
  \label{OnSiteWithProductsExpandProductOfPresheaves}
  \mathbf{X} \times \mathbf{Y}
  \;\simeq\;
  \int^{c_1,c_2 \in \mathcal{C}}
  y(c_1 \times c_2) \times \mathbf{X}(c_1) \times \mathbf{Y}(c_2)
  \,,
\]

where $y \;\colon\; \mathcal{C} \hookrightarrow [\mathcal{C}^{op}, Set]$ denotes the [[Yoneda embedding]].

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
    \,,
  \end{aligned}
$$

where the first step expands out both presheaves as colimits of representables separately, via the [[co-Yoneda lemma]], the second step uses that the [[Cartesian product]] of presheaves is a two-variable [[left adjoint]] (by the [[symmetric monoidal category|symmetric]] [[closed monoidal structure on presheaves]]) and [[adjoints preserve (co-)limits|as such preserves colimits]] (in particular [[coends]]) in each [[variable]] separately, and under the brace we use the defining [[universal property]] of the [[Cartesian products]], assumed to exist in $\mathcal{C}$.

Now observe that the [[colimit]] of a [[representable presheaf]] is the [[singleton]].

\[
  \label{ColimitOfRepresentableIsSingleton}
  \underset{\underset{\mathcal{D}^{op}}{\longrightarrow}}{\lim} y(c)
  \;\simeq\;
  \ast
  \,.
\]

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

where we made explicit the [[constant functor]] $const_\ast \;\colon\; \mathcal{C} \to Set$, constant on the [[singleton]] set $\ast$, and then applied the [[co-Yoneda lemma]].

Using this, we compute for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ the following sequence of [[natural isomorphisms]]:

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

Here the first step is (eq:OnSiteWithProductsExpandProductOfPresheaves), the second uses that [[colimits commute with colimits]], the third uses again that the [[Cartesian product]] respects colimits in each variable separately, the fourth is (eq:ColimitOfRepresentableIsSingleton), the last step is again the respect for colimits of the Cartesian product in each variable separately.

=--


## Applications

* In the definiton of _[[cohesive site]]_ and _[[infinity-cohesive site]]_, the assumption that the site has finite products (more generally: is [[cosifted category|cosifted]]) is what guarantees that the induced [[shape modality]] preserves finite products, as (usually) required for a [[cohesive topos]] or [[cohesive (infinity,1)-topos]]

## Related concepts

* [[commutativity of limits and colimits]]
