
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Baer sum_ is the natural addition operation on [[abelian group extensions]]
as well on the extensions of $R$-modules, for fixed ring $R$. 

For $G$ a [[group]] and $A$ an [[abelian group]], the extensions of $G$ by $A$ are classified by the degree-2 [[group cohomology]] 

$$
  H^2_{Grp}(G,A) = H^2(\mathbf{B}G, A) = H(\mathbf{B}G, \mathbf{B}^2 A)
  \,.
$$

On [[cocycles]] $\mathbf{B}G \to \mathbf{B}^2 A$ there is a canonical addition operation coming from the additive structure of $A$, and the Baer sum is the corresponding operation on the extensions that these cocycles classify.


## Definition

Below are discussed several different equivalent ways to define the Baer sum

### On concrete cocycles

A [[cocycle]] in degree-2 [[group cohomology]] $H^2_{Grp}(G,A)$ is a [[function]]

$$
  c : G \times G \to A
$$

satisfying the cocycle property. 

+-- {: .num_defn }
###### Definition

Given two cocycles $c_1, c_2 : G \times G \to A$ their **sum** is the composite

$$
  (c_1 + c_2) : G \times G \stackrel{\Delta_{G \times G}}{\to} (G \times G) \times (G \times G) \stackrel{(c_1,c_2)}{\to} A \times A \stackrel{+}{\to} A
$$

of 

* the [[diagonal]] on $G\times G$;

* the [[direct product]] $(f,g)$;

* the group operation $+ \colon A \times A \to A$.

Hence for all $g_1, g_2 \in G$ this sum is the function that sends

$$
  (c_1 + c_2) : (g_1, g_2) \mapsto c_1(g_1,g_2) + c_2(g_1, g_2)
$$


=--



### On abstract cocycles
 
As discussed at [[group cohomology]], a cocycle $c \colon G \times G \to A$ is equivalently a morphism of [[2-groupoids]] from the [[delooping]] [[groupoid]] $\mathbf{B}G$ of $G$ to the double-delooping [[2-groupoid]] $\mathbf{B}^2 A$ of $A$:

$$
  c_1,c_2 : \mathbf{B}G \to \mathbf{B}^2 A
  \,.
$$

Since $A$ is an abelian group, $\mathbf{B}^2 A$ is naturally an abelian [[infinity-group|3-group]], equipped with a group operation $+ \colon (\mathbf{B}^2 A) \times (\mathbf{B}^A)\to \mathbf{B}^2 A $.

With respect to this the sum operation is 

$$
  c_1 + c_2 : \mathbf{B}G \stackrel{\Delta_{\mathbf{B}G}}{\to} \mathbf{B}G \times   \mathbf{B}G \stackrel{(c_1,c_2)}{\to} \mathbf{B}^2 A \times \mathbf{B}^2 A \stackrel{+}{\to} \mathbf{B}^2 A
$$

### On short exact sequences


In any category with products, for any object $C$ there is a [[diagonal]] morphism
$\Delta_C:C\to C\times C$; in a category with coproducts there is a codiagonal morphism $\nabla_C: C\coprod C\to C$ (addition in the case of modules). Every additive category is, in particular, a category with finite [[biproduct]]s, so both morphisms are there. Short exact sequences in
the category of $R$-modules, or in arbitrary abelian category $\mathcal{A}$, 
form an additive category (morphisms are commutative ladders of arrows) in which the biproduct
$0 \to A_i \to \hat H_{i} \to G_i \to 0$ for $i = 1,2$ is
$0\to A_1\oplus A_2 \to H_1\oplus H_2\to G_1\oplus G_2\to 0$. 

Now if $0\to M\to N\to P\to 0$ is any extension, call it $E$, 
and $\gamma:P_1\to P$ a morphism, 
then there is a morphism $\Gamma' = (id_M,\beta_1,\gamma)$ from an
extension $E_1$ of the form $0\to M\to N_1\to P_1\to 0$ to $E$, where the pair $(E_1,\Gamma_1)$ is unique up to isomorphism of extensions, 
and it is called $E\gamma$. In fact, the diagram
$$\array{
N_1&\to &P_1\\
\downarrow\beta_1 && \downarrow\gamma\\
N&\to &P
}$$
is a pullback diagram. Every morphism of abelian extensions $(\alpha,\beta,\gamma):E\to E'$ in a unique way decomposes as
$$
E\stackrel{(\alpha,\beta_a,id)}\longrightarrow E\gamma \stackrel{(id,\beta_ 1,\gamma)}\longrightarrow E'
$$
for some $\beta_a$ with $\beta_1$ as above. In short, the morphism of extensions factorizes through $E\gamma$.

Dually, for any morphism $\alpha:M\to M_2$, there is a morphism $\Gamma_2 = (\alpha,\beta_2,id_P)$ to an extension $E_2$ of the form
$0\to M_2\to N_2\to P$; the pair $(E_2,\Gamma_2)$ is unique up to isomorphism of
extensions and it is called $\alpha E$. 

In fact, the diagram
$$\array{
M&\to &N\\
\downarrow\alpha && \downarrow\beta_2\\
M_2&\to &N_2
}$$
is a pushout diagram. Every morphism of abelian extensions $(\alpha,\beta,\gamma):E\to E''$ in a unique way decomposes as
$$
E\stackrel{(\alpha,\beta_a,id)}\longrightarrow \alpha E \stackrel{(id,\beta_ 2,\gamma)}\longrightarrow E''
$$
for some $\beta_a$, with $\beta_2$ as above. In short, the morphism of extensions factorizes through $\alpha E$.

There are the following isomorphisms of extensions: $(\alpha E)\gamma\cong \alpha (E\gamma)$, $id_M E \cong E$, $E id_P \cong P$, 
$(\alpha'\alpha)E\cong\alpha' (\alpha E)$, $(E\gamma)\gamma' \cong E(\gamma\gamma')$.

The Baer's sum of two extensions $E_1,E_2$ of the form $0\to M\to N_i\to P\to 0$
(i.e. with the same $M$ and $P$) is given by $E_1+E_2 = \nabla_M (E_1\oplus E_2) \Delta_P$; this gives the structure of the abelian group on $Ext(P,M)$ and $Ext:\mathcal{A}^{op}\times\mathcal{A}\to Ab$ is a biadditive (bi)functor. This is also related to the isomorphisms of extensions
$\alpha (E_1+E_2)\cong \alpha E_1+\alpha E_2$, $(\alpha_1+\alpha_2) E \cong \alpha_1 E+ \alpha_2 E$, $(E_1+E_2)\gamma \cong E_1\gamma + E_2\gamma$, $E(\gamma_1+\gamma_2)\cong E\gamma_1 + E\gamma_2$.

In different notation, if $0 \to A \to \hat G_{i} \to G \to 0$ for $i = 1,2$ 
are two [[short exact sequences]] of [[abelian groups]], their **Baer sum** is 

$$
  \hat G_1 + \hat G_2
  \coloneqq
  +_* \Delta^* \hat G_1 \times \hat G_2
$$

The first step forms the [[pullback]] of the short exact sequence along the diagonal on $G$:

$$
  \array{
    A \oplus A &\to& A \oplus A
    \\
    \downarrow && \downarrow
    \\
    \Delta^* (\hat G_1 \oplus \hat G_2) &\to& \hat G_1 \oplus \hat G_2
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{\Delta_G}{\to}&  G\oplus G
  }
$$

The second forms the [[pushout]] along the addition map on $A$:

$$
  \array{
    A \oplus A &\stackrel{+}{\to}& A
    \\
    \downarrow && \downarrow
    \\
    \Delta^* (\hat G_1 \oplus \hat G_2) &\to& +_* \Delta^*(\hat G_1 \oplus \hat G_2)
    \\
    \downarrow && \downarrow
    \\
    G &\to&  G
  }
$$


## Related concepts

* [[cup product]]

## References

* S. MacLane, _Homology_, 1963

* Patrick Morandi, _Ext groups and Ext functors_ ([pdf](http://sierra.nmsu.edu/morandi/oldwebpages/math683fall2002/Ext.pdf))

[[!redirects Baer sums]]
[[!redirects Baer's sum]]
