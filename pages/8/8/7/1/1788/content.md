

Let $\mathbb{K} \,\in\, \big\{ \mathbb{R}, \mathbb{C}, \mathbb{H} \big\}$
and write

$$
  d
  \;\coloneqq\;
  dim_{\mathbb{R}}(\mathbb{K})
  \,.
$$

Given a a multiplicative cohomology theory $E$, let me write

$$
  G_d 
   \;\coloneqq\; 
  \Sigma^d (1^E) \;\;\,\in\, \widetilde E^d\big( S^d \big)
$$

for the $d$-fold suspension of the canonical generator.

Then given a $\mathbb{K}$-orientation $c^E$ on $E$, its "first extension stage" $c^{E,1}$, in the sense of the following square on the left, is equivalently a homotopy as shown on the right:

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{K}P^{2}
    &
    \overset{ c^{E,1} }{\longrightarrow}
    &
    E_d
    \\
    \big\uparrow
    &\mathclap{^{_{(hpo)}}}&
    \big\uparrow
    & 
    \nearrow \mathrlap{ {}_{ G_d  } }
    \\
    S^{ 2 d - 1 }
    &\underset{ h }{\longrightarrow}&
    \mathbb{K}P^1
  }
    \;\;\;\;\;\;
    \simeq
    \;\;\;\;\;\;
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    E_d
    \\
    \big\uparrow
    &
    {}_{  H  }
    \seArrow
    &
    \big\uparrow \mathrlap{ ^{_{ G_d }} }
    \\
    S^{2d - 1}
    &\underset{ h }{\longrightarrow}&
    \mathbb{K}P^1
    \,.
  }
$$

We may also choose a homotopy 

$$
  0 \overset{ G_{2d-1} }{\Rightarrow} G_d \cdot G_d
  \,,
$$

by degree-reasons. Combining this, we get a class 

$$
  H \cdot h^\ast G_d \,-\, h^\ast G_{2d-1}
  \;\;\;\in\;
  E^{2d-1}\big( S^{2d-1} \big)
  \,.
$$

When $E = H A$ is ordinary cohomology, then this class is the homotopy Whitehead integral formula for the Hopf invariant of $h$.

So for general $\mathbb{K}$-oriented $E$, we have an "$E$-Whitehead integral" formula induced from any choice of $\mathbb{K}$-orientation. I suppose. 

Has this been considered anywhere?

\linebreak







We regard this as a [[topological ring]] with respect to the canonical underlying [[topological space|topology]] of the [[Euclidean space]] $\mathbb{R}^{ dim_{_{\mathbb{R}}}(\mathbb{K}) }$.

For $n \in \mathbb{N}$, consider

$$
  \mathbb{K}P^n 
  \;\;
  \coloneqq
  \;\;
  \big(
    \mathbb{K}^{n+1} \setminus \{0\}
  \big) / \mathbb{K}^\times
$$

the $\mathbb{K}$-[[projective space]], i.e. the [[topological space|topological]] [[quotient space]] of the [[complement]] of zero in the $n+1$-fold [[Cartesian product]] of $\mathbb{K}$ by the right (say) [[multiplication]] [[action]] by the [[group of units]] $\mathbb{K}^\times \,=\, \mathbb{K} \setminus \{0\}$.

Notice the canonical [[topological subspace|subspace]] inclusion

$$
  \array{
    \mathbb{K}P^n
    &\hookrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big[
      z_0 \,:\, \cdots \,:\, z_n
    \big]
    &\mapsto&
    \big[
      z_0 \,:\, \cdots \,:\, z_n \,:\, 0
    \big]
    \,.
  }
$$

with induced [[complement]] $\mathbb{K}P^{n+1} \setminus \mathbb{K}P$ with [[topological boundary]]

$$
  \partial
  \big(
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P
  \big)
  \;\;
    \coloneqq
  \;\;
  \overline{
    \big(
      \mathbb{K}P^{n+1} \setminus \mathbb{K}P
    \big)
  }
  \setminus
  \big(
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P
  \big)
  \,.
$$


Prop. We have a [[pushout diagram]] in [in topological spaces](Top#UniversalConstructions) of the form

$$
  \array{
    \overline{
      \mathbb{K}P^{n+1}
      \setminus
      \mathbb{K}P^n
    }
    &\longrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big\uparrow
    &{}_{^{(po)}}&
    \big\uparrow
    \\
    \partial
    \big(
      \mathbb{K}P^{n+1}
      \setminus
      \mathbb{K}P^n
    \big)
    &\longrightarrow&
    \mathbb{K}P^n
  }
  \;\;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;\;
  \array{
    D^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) }
    &\longrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big\uparrow
    &{}_{^{(po)}}&
    \big\uparrow
    \\
    S^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) - 1 }
    &\longrightarrow&
    \mathbb{K}P^n
  }
$$

exhibiting $\mathbb{K}P^{n+1}$ as the result of an $(n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K})$-[[cell attachment]] to $\mathbb{K}P^{n}$ with [[attaching map]] the canonical projection

$$
  \array{
     S^{(n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K})-1}
     \;\simeq\;
     \big(
       \mathbb{K}^{n+1} \setminus \{0\}
     \big) / \mathbb{R}_+^\times
     &\longrightarrow&
     \big(
       \mathbb{K}^{n+1} \setminus \{0\}
     \big) / \mathbb{K}^\times
     \;\simeq\;
     \mathbb{K}P^n
  }
$$

Proof.

Just to observe the [[homeomorphism]]

$$
  \array{
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P^n
    &\overset{\;\;\;\simeq\;\;\;}{\longrightarrow}&
    Int
    \big(
      D^{(n+1) dim_{{}_{\mathbb{R}}}(\mathbb{K})}
    \big)
    \,\simeq\,
    \left\{
      (y_0, \cdots, y_n, r)
      \,\left\vert\,
      \array{
         r \in (0,1] \subset \mathbb{R}\,,
         \\
         \left\vert \vec y \right\vert^2 + r^2  = 1 
      }
      \right.
    \right\}
    & 
    \subset 
    \mathbb{K}^{n+2}
    \\
    \big[
      z_0
      \,\colon\,
      \cdots
      \,\colon\,
      z_n
      \,\colon\,
      z_{n+1}
    \big]
    &\mapsto&
    \tfrac{1}{\left\vert \vec z\right\vert}
    \Big(
      z_0
      \cdot
      \tfrac{ z^\ast_{n+1} }{ \left\vert z_{n+1}\right\vert }
      \,,\,
      \cdots
      \,,\,
      z_n
      \cdot
      \tfrac{ z^\ast_{n+1} }{ \left\vert z_{n+1}\right\vert }
      \,,\,
      \left\vert z_{n+1}\right\vert
    \Big)
  }
$$

in terms of which the [[topological boundary]] on the left corresponds to the subspace with $r = 0$ on the the right;.



\linebreak

\linebreak

Equivalently this means that a complex orientation $c_1^E$ in $E$-theory is an [[extension]] (in the [[classical homotopy category]]) of the map $\Sigma^2 1 \,\colon\, \mathbb{C}P^1 \longrightarrow \Omega^\infty E$ (which classifies the suspended identity in the cohomology ring) along the canonical inclusion of [[complex projective spaces]] 

\[
  \label{ComplexOrientationAsExtension}
  \array{
     \mathbb{C}P^1
     &
     \overset{
       \Sigma^2 1_E
     }{
       \longrightarrow
     }
     &
     \Omega^{\infty - 2} E
     \\
     \big\downarrow
     &
     \nearrow \mathrlap{ {}_{c_1^E} }
     \\
     \mathbb{C}P^\infty
  }
\]

Notice that the [[complex projective spaces]] form a [[cotower]]

$$
  \ast 
  \,=\,
  \mathbb{C}P^0
  \hookrightarrow
  \mathbb{C}P^1
  \hookrightarrow
  \mathbb{C}P^2
  \hookrightarrow
  \mathbb{C}P^3
  \hookrightarrow
  \cdots
  \hookrightarrow
  \mathbb{C}P^\infty
  \,=\,
  \underset{\longrightarrow}{\lim}
  \mathbb{C}P^\bullet
$$

where each inclusion stage is (by [this Prop.](complex+projective+space#CellComplexStructureOnComplexProjectiveSpace)) the coprojection of a [[pushout]] [of topological spaces](Top#UniversalConstructions) (of [[pointed topological spaces]]) of the form

$$
  \array{
    D^{2n+2}
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{C}P^{n+1}
    \\
    \big\uparrow
    &\mathclap{^{_{(po)}}}&
    \big\uparrow
    \\
    S^{2n+1}
    &\underset{h^{2n+1}_{\mathbb{C}}}{\longrightarrow}&
    \mathbb{C}P^n
  }
$$

(where $h^{2n+1}_{\mathbb{C}}$ is the [[complex Hopf fibration]] in dimension $2n+1$) hence of a [[homotopy pushout]] of [[classical model structure on topological spaces|underlying homotopy types]] (rather: [[classical model structure on pointed topological spaces|of pointed homotopy types]]) of this form:

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{C}P^{n+1}
    \\
    \big\uparrow
    &\mathclap{^{_{(hpo)}}}&
    \big\uparrow
    \\
    S^{2n+1}
    &\underset{h^{2n+1}_{\mathbb{C}}}{\longrightarrow}&
    \mathbb{C}P^n
  }
$$

Therefore, a complex orientation by extension (eq:ComplexOrientationAsExtension) is equivalently the homotopy colimiting map out of a sequence

$$
  \big(
    \Sigma^2 1 
      \,=\, 
    c_1^{E,0}
    ,\,
    c_1^{E,1}
    ,\,
    c_1^{E,2}
    ,\,
    \cdots
    ,\,
    c_1^{E,\infty}
    \,=\,
    c_1^E
  \big)
$$

of finite-stage extensions

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{C}P^{n+1}
    &
    \overset{ c_1^{E,n+1} }{\longrightarrow}
    &
    \Omega^{\infty -2} E
    \\
    \big\uparrow
    &\mathclap{^{_{(hpo)}}}&
    \big\uparrow
    & 
    \nearrow \mathrlap{ {}_{c_1^{E,n}} }
    \\
    S^{2n+1}
    &\underset{h^{2n+1}_{\mathbb{C}}}{\longrightarrow}&
    \mathbb{C}P^n
    \,.
  }
$$

Moreover, by the defining [[universal property]] of the [[homotopy pushout]], the extension $c_1^{E,n+1}$ of $c_1^{E,n}$ is equivalently a choice of [[homotopy]] which trivializes the pullback of $c_1^{E,n}$ to the [[n-sphere|2n+1-sphere]]:

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \Omega^{\infty - 2} E
    \\
    \big\uparrow
    &
    {}_{  c_1^{E,n+1}  }
    \seArrow
    &
    \big\uparrow \mathrlap{ ^{_{ c_1^{E,n} }} }
    \\
    S^{2n+1}
    &\underset{ h^{2n+1}_{\mathbb{C}} }{\longrightarrow}&
    \mathbb{C}P^n
    \,.
  }
$$

This means, first of all, that the non-triviality of the pullback class

$$
  \big( 
    h^{2n+1}_{\mathbb{C}}
  \big)^\ast 
  ( c_1^{E,n} )
  \;\in\;
  \widetilde E^2
  \big(
    S^{2n+1}
  \big)
  \;\simeq\;
  E_{2n-1}
$$

is the [[obstruction]] to the existence of the extension/orientation at this stage. 

It follows that if these obstructions all vanish, then a complex $E$-orientation does exist.  A sufficient condition for this is, evidently, that the reduced $E$-cohomology of all odd-dimensional spheres vanishes, hence, that the [[graded-commutative ring|graded]] $E$-[[cohomology ring]] $E_\bullet$ is trivial in odd degrees.


