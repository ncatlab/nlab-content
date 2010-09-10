
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


* [[principal bundle]] / [[torsor]]

* [[principal 2-bundle]] / [[gerbe]] / **bundle gerbe**

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]]

***




#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _bundle gerbe_ is a special model for the total space [[Lie groupoid]] of a $\mathbf{B}U(1)$-[[principal 2-bundle]] for $\mathbf{B}U(1)$ the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle 2-group</a>.

More generally, for $G$ a more general [[Lie 2-group]] (often taken to be the [[automorphism 2-group]] $G = AUT(H)$ of a [[Lie group]] $H$), a [[nonabelian bundle gerbe]] for $G$ is a model for the total space groupoid of a $G$-[[principal 2-bundle]].

The definition of _bundle gerbe_ is not in fact a special case (nor a generalization) of the definition of [[gerbe]], even though there are equivalences relating both concepts.

## Definition

A **bundle gerbe'* over a [[smooth manifold]] $X$ is 

* a [[surjective submersion]]

  $$
      \array{
          Y
          \\
          \downarrow^{\mathrlap{\pi}}
          \\
          X
      }
    $$

* together with a $U(1)$-[[principal bundle]]

  $$
      \array{
           L
           \\
           \downarrow^{\mathrlap{p}}
           \\
           Y \times_X Y
        }
    $$

  over the [[fiber product]] of $Y$ with itself, i.e.

  $$
    \array{
          L
          \\
          \downarrow^{\mathrlap{p}}
          \\
          Y \times_X Y &\stackrel{\overset{\pi_1}{\rightarrow}}{\underset{\pi_2}{\rightarrow}}& Y
          \\
          && \downarrow^{\mathrlap{\pi}}
          \\
          && 
          X
      }
     \,,
  $$

* an [[isomorphism]]

   $$
     \mu : 
     \pi_{12}^*L \otimes
     \pi_{23}^*L 
     \to 
     \pi_{13}^* L
   $$

   of $U(1)$-bundles on $Y \times_X Y \times_X Y$

* such that this satisfies the evident associativity condition on
  $Y\times_X Y \times_X Y \times_X Y$.

Here $\pi_{12}, \pi_{23}, \pi_{13}$ are the three maps

$$
  Y^{[3]} \stackrel{\stackrel{\rightarrow}{\rightarrow}}{\rightarrow}
   Y^{[2]}
$$

in the [[Cech nerve]] of $Y \to X$.

In a [[nonabelian bundle gerbe]] the bundle $L$ is generalized to a [[bibundle]].


## Interpretation {#Interpretation}

A bundle gerbe may be understood as a specific model for the total space [[Lie groupoid]] of a [[principal 2-bundle]]. 

We first describe this Lie groupoid in

* [As a groupoid extension](#AsGroupoidExtension)

and then describe how this is the total space of a principal 2-bundle in

* [As the total space of a 2-bundle](#AsTotalSpace).

### As a groupoid extension {#AsGroupoidExtension}

Give a surjective submersion $\pi : Y \to X$, write 

$$
  C(Y) := \left(
    Y \times_X Y \stackrel{\to}{\to} Y
  \right)
$$ 

for the corresponding [[Cech groupoid]]. Notice that this is a [[resolution]] of the [[smooth manifold]] $X$ itself, in that the canonical projection is a weak equivalence (see [[infinity-Lie groupoid]] for details)

$$
  \array{
     C(Y)
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
  \,.
$$

The data of a bundle gerbe $(Y,L,\mu)$ induces a [[Lie groupoid]] $P_{(Y,L,\mu)}$ which is a $\mathbf{B}U(1)$-extension of $C(Y)$, exhibiting a [[fiber sequence]]

$$
  \mathbf{B}U(1) \to P_{(Y,L,\mu)} \to X
  \,.
$$


This Lie groupoid is the groupoid whose space of morphisms is the total space $L$ of the $U(1)$-bundle

$$
  P_{(Y,L,\mu)} = 
  \left(
    L \stackrel{\overset{\pi_1 \circ p}{\to}}{\underset{\pi_2 \circ p}{\to}} Y
  \right)
$$

with composition given by the composite

$$
  L \times_{s,t} L
  \stackrel{\simeq}{\to}
  \pi_{12}^* L \times \pi_{23}^3* L
  \stackrel{}{\to}
  \pi_{12}^* L \otimes \pi_{23}^3* L
  \stackrel{\mu}{\to}
  \pi_{13}^* L
  \to
  L
  \,.
$$


### As the total space of a principal 2-bundle {#AsTotalSpace}

+-- {: .un_prop}
###### Proposition

The Lie groupoid $P_{(Y,L,\mu)}$ defined by a bundle gerbe is in [[?LieGrpd]] the [[(∞,1)-pullback]]

$$
  \array{
     P_{(Y,L,\mu)} &\to& *
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow
     \\
     X &\stackrel{g}{\to}& \mathbf{B}^2 U(1)
  }
$$

of a [[cocycle]] $[g] \in H(X,\mathbf{B}^2 U(1)) \simeq H^3(X,\mathbb{Z})$. 

=--

In fact a somewhat stronger statement is true, as shown in the following proof.

+-- {: .proof}
###### Proof

We can assume without restriction that the bundle $L$ in the data of the bundle gerbe is actually the trivial $U(1)$-bundle $L = Y \times_X Y \times U(1)$ by refining, if necessary, the surjective submersion $Y$ by a [[good open cover]]. In that case we may identify $\mu$ with a $U(1)$-valued function

$$
  \mu : Y \times_X Y \times_X Y  \to U(1)
$$

which in turn we may identify with a smooth 2-[[anafunctor]]

$$
  \array{
    C(U) &\stackrel{\mu}{\to}& \mathbf{B}^2 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
  \,.
$$

From here on the computation is a special case of the general theory of [[groupoid cohomology]] and the extensions classified by it.

Then recall from [[universal principal infinity-bundle]] that we model the $(\infty,1)$-pullbacks that defines principal $\infty$-bundles in terms of ordinary pullbacks of the universal $\mathbf{B}U(1)$-principal 2-bundle $\mathbf{E}\mathbf{B}U(1) \to \mathbf{B}^2 U(1)$.

We may model all this in the case at hand in terms of [[strict omega-groupoid|strict 2-groupoip]]s. Then using an evident cartoon-notation we have

$$
  \mathbf{B}^2 U(1)
  = 
  \left\{
    \array{
       & \nearrow \searrow
       \\
       \bullet &\Downarrow^{\mathrlap{c \in U(1)}}& \bullet
       \\
       & \searrow \nearrow
    }
  \right\}
$$

and $\mathbf{E}\mathbf{B}U(1)$ is the 2-groupoid whose _morphisms_ are diagrams

$$
  \array{
      && \bullet
      \\
      & \nearrow &\swArrow_{c}& \searrow
     \\
     \bullet &&\to&& \bullet
  }
$$

in $\mathbf{B}^2 U(1)$ with composition given by horizontal [[pasting]]

$$
  \array{
     &&& \bullet
     \\
     & \swarrow &\swArrow_{c_1} & \downarrow &\swArrow_{c_2}& \searrow
    \\
    \bullet &\to&& \bullet &&\to& \bullet
  }
$$

and 2-morphisms are paper-cup diagrams

$$
  \array{
      && \bullet
      \\
      & \nearrow &\swArrow_{c}& \searrow
     \\
     \bullet &&\to&& \bullet
     \\
     & \searrow &\swArrow_{k}& \swarrow
     \\
     && \bullet
  }
  \;\;\;\;\;
  =
  \;\;\;\;\;
  \array{
      && \bullet
      \\
      & \nearrow &\swArrow_{c k}& \searrow
     \\
     \bullet &&\to&& \bullet
  }
  \,.
$$

So $\mathbf{E}\mathbf{B}U(1)$ is the Lie 2-groupoid with a single object, with  $U(1)$ worth of 1-morphisms and unique 2-morphism between these.

From this we read of that 

$$
  \array{
    P_{(Y,L,\mu)} &\to& \mathbf{E} \mathbf{B}U(1)
    \\
    \downarrow && \downarrow
    \\
    C(U) &\stackrel{\mu}{\to}& \mathbf{B}^2 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

is indeed a [[pullback]] square (in the category of [[simplicial presheaves]] over [[CartSp]]). The morphisms of the pullback Lie groupoid are pairs of diagrams

$$
  \array{
      && \bullet
      \\
      & \nearrow &\swArrow_{c}& \searrow
     \\
     \bullet &&\to&& \bullet
     \\
     \\
     (x,i) &&\to&& (x,j)
  }
$$

hence form a trivial $U(1)$-bundle over the morphisms of $C(U)$, and the 2-morphims are pairs consisting of 2-morphisms 

$$
  \array{
     && (x,j)
     \\
     & \nearrow &\swArrow& \searrow
     \\
     (x,i) &&\to&& (x,k)
  }
$$


in $C(U)$ and paper-cup diagrams of the form

$$
  \array{
     &&& \bullet
     \\
     & \swarrow &\swArrow_{c_1} & \downarrow &\swArrow_{c_2}& \searrow
    \\
    \bullet &\to&& \bullet &&\to& \bullet
    \\
    & \searrow &&\swArrow_{\mu_{i j k}(x)}&&& \swarrow
  }
  \;\;\;\;
  =
  \;\;\;\;
  \array{
      && \bullet
      \\
      & \nearrow &\swArrow_{c_1 c_2 \mu_{i j k}(x)}& \searrow
     \\
     \bullet &&\to&& \bullet
   }
$$

in $\mathbf{B}^2 U(1)$, which exhibits indeed the composition operation in $P_{(Y,L,\mu)}$.

=--

## Connections on bundle gerbes

See [[connection on a bundle gerbe]].

## Related entries

* [[transgression of bundle gerbes]]

##References##

The notion of _bundle gerbe_ as such was introduced in

* [[Michael Murray]], _Bundle gerbes_ ([arXiv:dg-ga/9407015](http://arxiv.org/abs/dg-ga/9407015))


[[!redirects bundle gerbes]]