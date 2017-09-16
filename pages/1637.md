A **simplicial homotopy** is a [[homotopy]] in the classical [[model structure on simplicial sets]].

#Definition#

[[SSet]] has a [[cylinder functor]] given by [[cartesian monoidal category|cartesian]] product with the standard 1-[[simplex]] $I := \Delta^1$. 

Therefore for $f,g : X \to Y$ two morphisms of [[simplicial set]]s, a [[homotopy]] $\eta : f \Rightarrow g$ is a morphism $\eta : X \times \Delta^1 \to Y$ such that the diagram

$$
  \array{
    X \simeq X\times \Delta^0 &\stackrel{Id \times \delta^1}{\to}& X \times \Delta^1 \simeq Y
   &
   \stackrel{Id \times \delta^0}{\leftarrow}&
   Y \times \Delta^0
   \\
   &
    {}_f\searrow &\downarrow^\eta& \swarrow_{g}
   \\
   &&
   Y
  }
$$

commutes.

#Remarks#

* Since in the standard [[model structure on simplicial sets]] every simplicial set is cofibrant, this indeed defines left homotopies.

#Properties#

+-- {: .un_lemma}
###### Lemma

Precisely if $Y$ is a [[Kan complex]] is the relation 
$$
  (f \sim g) \Leftrightarrow 
  (\exists simplicial homotopy f \Rightarrow g : X \to Y )
$$
an [[equivalence relation]].

=--

+-- {: .proof}
###### Proof

Since [[Kan complex]]es are precisely the fibrant objects with respect to the standard [[model structure on simplicial sets]] this follows from general statements about [[homotopy]] in model categories.

The following is a direct proof.

We first show that the homotopy between points $x,y : \Delta^0 \to Y$ is an equivalence relation when $Y$ is a [[Kan complex]].

We identify in the following $x$ and $y$ with vertices in the image of these maps.

* -**reflexivity**- For every vertex $x \in Y_0$, the degenerate 1-simplex $s_0 x \in S_1$ has, by the [[simplicial identities]], 0-faces $d_0 s_0 x = x$ and $d_1 s_0 x = x$. 
  $$
    (d_1 s_0 x) \stackrel{s_0 x}{\to} (d_0 s_0 x)
  $$
  Therefore the morphism $\eta : \Delta^0 \times \Delta^1 \to Y$ that takes the unique non-degenerate 1-simplex in $\Delta^1$ to $s_0 x$ constitutes a homotopy from $x$ to itself.

* -**transitivity**- let $v_2 : x \to y$ and $v_0 : y \to z$ in $Y_1$ be 1-cells. Together they determine a map from the [[horn]] $\Lambda^2_1$ to $Y$, 
  $$
    (v_2, v_2) : \Lambda^2_1 \to Y
    \,.
  $$ 
  By the [[Kan complex]] property there is an extension $\theta$ of this morphism through the 2-[[simplex]] $Delta^2$
  $$
    \array{
      \Lambda^2_1 &\stackrel{(v_0,v_2)}{\to}& Y
      \\
      \downarrow & \nearrow_{\theta}
      \\
      \Delta^2
    }   
    \,.
  $$
  If we again identify $\theta$ with its image (the image of its unique non-degenerate 2-cell) in $Y_2$, then
  using the [[simplicial identities]] we find 
  $$
    \array{
       && (d_0 d_2 \theta) = (d_1 d_0 \theta)
       \\
       & {}^{d_2 \theta }\nearrow &
       \Downarrow \theta & \searrow^{d_0 \theta}
       \\
       (d_1 d_2 \theta) = (d_1 d_1 \theta) && \stackrel{d_1 \theta}{\to}  &&
       (d_0 d_1 \theta)
       =
       (d_0 d_1 \theta)
    }
  $$
 that the 1-cell boundary bit $d_1 \theta$ in turn has 0-cell boundaries
  $$
    d_0 d_1 \theta = d_0 d_0 \theta = z
  $$
  and
  $$
    d_1 d_1 \theta = d_1 d_2 \theta = x
    \,.
  $$
  This means that $d_1 \theta$ is a homotopy $x \to z$.

* -**symmetry**- In a similar manner, suppose that $v_2 : x \to y$ is a 1-cell in $Y_1$ that constitutes a homotopy from $x$ to $y$. Let $v_1 := s_0 x$ be the degenerate 1-cell on $x$. Since $d_1 v_1 = d_1 v_2$ together they define a map
$\Lambda^2_0 \stackrel{v_1, v_2}{\to} Y$ which by the Kan property of $Y$ we may extend to a map $\theta'$
  $$
   \array{
    \Lambda^2_0 &\stackrel{v_1, v_2}{\to}& Y
    \\
    \downarrow & \nearrow_{\theta'}
    \\
    \Delta^2
   }
  $$
  on the full 2-simplex. 

  Now the 1-cell boundary $d_0 \theta'$ has, using the [[simplicial identities]], 0-cell boundaries
  $$
    d_0 d_0 \theta' = d_0 d_1 \theta' = x
  $$
  and
  $$
    d_1 d_0 \theta' = d_0 d_2 \theta' = y
  $$
  and hence yields a homotopy $y \to x$. So being
  homotopic is a symmetric relation on vertices in a 
  Kan complex.

Finally we use the fact that [[SSet]] is a [[cartesian closed category]] to deduce from this statements about vertices the corresponding statement for all map: 

  a morphism $f : X \to Y$ is the Hom-[[adjunct]] of a morphism $\bar f : \Delta^0 \to [X,Y]$, and a homotopy $\eta : X \times \Delta^1 \to Y$ is the [[adjunct]] of a morphism $\bar \eta : \Delta^1 \to [X,Y]$. Therefore homotopies $\eta : f \Rightarrow g$ are in bijection with homotopies $\bar \eta : \bar f \to \bar g$.

=--



#References#

* Goerss, Jardine, _Simplicial homotopy theory_ ([ps](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi))