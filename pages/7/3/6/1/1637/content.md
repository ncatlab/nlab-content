
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **simplicial homotopy** is a [[homotopy]] in the classical [[model structure on simplicial sets]]. It can also be defined combinatorially; in that form one can define a homotopy 2-cell between morphisms of simplicial objects in any category $C$. 

##Definition via cylinders##

[[SSet]] has a [[cylinder functor]] given by [[cartesian monoidal category|cartesian]] product with the standard 1-[[simplex]] $I := \Delta^1$. (In fact, one can define simplicial  cylinders, $\Delta^1\odot X$, more generally, for example for $X$ being a simplicial object in an [[cocomplete category]] $C$,(see below).) 

Therefore for $f,g : X \to Y$ two morphisms of [[simplicial set]]s, a [[homotopy]] $\eta : f \Rightarrow g$ is a morphism $\eta : X \times \Delta^1 \to Y$ such that the diagram

$$
  \array{
    X \simeq X\times \Delta^0 &\stackrel{Id \times \delta^1}{\to}& X \times \Delta^1 
   &
   \stackrel{Id \times \delta^0}{\leftarrow}&
   X \times \Delta^0
   \simeq X
   \\
   &
    {}_f\searrow &\downarrow^\eta& \swarrow_{g}
   \\
   &&
   Y
  }
$$

commutes. 

Remark: Since in the standard [[model structure on simplicial sets]] every simplicial set is cofibrant, this indeed defines left homotopies.

##Combinatorial definition##

Given morphisms $f,g,:X\to Y$ of simplicial objects in any category $C$, a __simplicial homotopy__ is a family of morphisms $\eta_n:X_n\to Y_{n+1}$ $n = 0,1,2,\ldots$, such that $d_0 h_0 = f$, $d_{n+1} \eta_n = g$ and

$$ d_i h_j = \left\lbrace\array{
\eta_{j-1}d_i, & i\lt j \\
d_i \eta_{i-1}, &i=j\neq 0\\
\eta_j d_{i-1}, & i\gt j+1.
}\right.$$

$$ s_i h_j = \left\lbrace\array{
\eta_{j+1} s_i, & i\le j\\
\eta_j s_{i-1}, & i\gt j.
}\right.$$

##Commentary##
It is fairly easy to prove that the combinatorial definition of homotopy agrees with the one via the cylinder both for simplicial sets and for simplicial objects in any [[finitely cocomplete category]], $C$.  This uses the fact that the category of simplicial objects in a cocomplete category, $C$, has [[copower|copowers]] with finite simplicial sets and hence in articular with $\Delta[1]$. (As there are explicit formulae for the construction of [[copower|copowers]] ...)
+-- {: .query}
[[Tim Porter|Tim]]:  With only my own resources available, I was unable to find them so was hoping someone kind would come up with them. They derive from the coend formulae&#8203;/Kan extension formulae using some combinatorics to discuss the indexing sets. I think Quillen gave some form of them, but have not got a copy of HA. I needed them recently and could not find them in any of the usual sources, and did not manage to work them out using the Kan extension idea either (Help please anyone). We could do with those formulae or with a reference to them at least.
=--


In the case of the category of (not necessarily abelian) groups, the combinatorial definition equals the one via cylinder only if the role of "cylinder" for a group $G$ is played by a simplicial object in the category of groups which in degree $n$ equals the free product of $(n+2)$ copies of $G$, indexed by the set $\Delta[1]_n$ (noted by Swan and quoted in exercise 8.3.5 of Weibel: _Homological algebra_).

+--{: .query}
[[Tim Porter]]:   Perhaps we need an explicit description of [[copower|copowers]] in simplicial objects also. I pointed out in an edit above that the combinatorial description is much more general than just for  simplicial objects in an abelian category. 

Can specific references to Swan be given, anyone?

[[Zoran Škoda]]: I agree that one should talk about copowers etc. $\Delta^1$ in notation here is not the geometric realization of an interval, but the simplical set $\Delta[1]$.
=--

##Properties##

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

+-- {: .un_proposition}
###### Proposition

Let $A$ be an abelian category and $f,g : X\to Y$ homotopic morphisms of simplicial objects in $A$. Then the induced maps $f_*, g_* : N(X)\to N(Y)$ of their normalized chain complexes are chain homotopic. 

=--
+-- {: .un_proposition}
###### Proposition

Let $A$ be an abelian category. The morphisms of simplicial objects (variant: of unbounded chain complexes) in $A$, which are homotopic to zero, form an ideal. More precisely 

* being homotopic is an equivalence relation on the class of morphism,

* $f_1\sim 0$ and $f_2\sim 0$ implies $f_1+f_2 \sim 0$,

* if $f\circ h$ (resp. $h\circ f$) exists and if $f\sim 0$ then $f\circ h\sim 0$ (resp. $h\circ f\sim 0$). 
=--

##References##

* Goerss, Jardine, _Simplicial homotopy theory_ ([ps](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi))

Cylinder based homotopy is also discussed extensively in

* K. H. Kamps and T. Porter, _Abstract Homotopy and Simple Homotopy Theory_, World 
Scientific Publishing Co. Inc., River Edge, NJ.