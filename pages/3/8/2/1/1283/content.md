
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


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

## Connections

As bundle gerbes are a [[vertical categorification|categorification]] of transitions in fiber bundles,
bundle gerbes with connection are a categorification of transitions in
fiber bundles with connection.

Like a connection on a locally trivialized bundle is encoded in a 
Lie algebra-valued connection $1$-form on $Y$, the connection on a bundle gerbe 
gives rise to a Lie-algebra valued $2$-form on $Y$ (this shift in degree
is directly related to the step from second to third integral cohomology). This $2$-form
is sometimes addressed as the _curving $2$-form_ of a bundle gerbe.

But there is more data necessary to describe a connection on a bundle gerbe.
The details of the definition -- which is evident for line bundle gerbes but more
involved for principal bundle gerbes -- can be naturally derived from a functorial
concept of parallel surface transport, just like connection $1$-forms on bundles
can be derived from parallel line transport.

###Definitions###



####for line bundle gerbes####

A connection (also known as "connection and curving") on a line bundle gerbe
$$
  B \stackrel{p}{\to} Y^{[2]} \stackrel{\to}{\to} Y \stackrel{\pi}{\to} X
$$ 
is

* a 2-form on $Y$
    $$
      B \in \Omega^2(Y)
    $$

* a connection $\nabla$ on the line bundle $B \to Y^{[2]}$

* such that
   $$
      \pi_1^*B \; -\;  p_2^*B \;=\; F_\nabla
   $$

* together with an extension of the bundle gerbe product $\mu$ to an isomorphism
    $$
        \mu_\nabla \;:\; p_{12}^* (B,\nabla) \;\; \otimes p_{23}^* (B,\nabla) \;\to\; p_{13}^* (B,\nabla)
    $$
    of line bundles with connection.



Notice that this condition ensures that $d B$ is a $3$-form on $Y$ which agrees on
double intersections
$$
  p_1^* d B \;\; = \;\; p_2^* d B
  \,.
$$
This means that $d B$ actually descends to a 3-form on $X$.

The __curvature__ associated with the connection on a line bundle gerbe 
is the unique 3-form on $X$
$$
  H \in \Omega^3(X)
$$
such that
$$
  \pi^* H = d B
  \,.
$$

The deRham class $[H]$ of this 3-form is the image in real cohomology of the class in integral coholomology classifying the bundle gerbe.

#### for principal bundle gerbes ####

A connection on a $G$-principal bundle gerbe is

* a $\mathrm{Lie}(G)$-valued 2-form on $Y$
    $$
       B \in \Omega^2(Y,\mathrm{Lie}(G))
    $$

* together with a $\mathrm{Lie}(\mathrm{Aut}(G))$-valued 1-form on $Y$
    $$
       A \in \Omega^1(Y,\mathrm{Lie}(\mathrm{Aut}(G)))
    $$

* and a certain twisted notion of connection on the $G$-bundle $B$


* satisfying a couple of conditions that reduce to those described above in the case $G = U(1)$.

For the case that $F_{A} + \mathrm{ad} B = 0$, these conditions are nothing but
a tetrahedron law on a 2-functor from 2-paths in $Y$ to the category 
$\Sigma(G\mathrm{BiTor})$. This is discussed in
[math.DG/0511710](http://arxiv.org/abs/math.DG/0511710).

For the more general case a choice for these conditions that harmonizes with the
conditions found for (proper) gerbes with connection by Breen &amp; Messing in
[math.AG/0106083](http://arxiv.org/abs/math.AG/0106083) has
been given by Aschieri, Cantini &amp; Jur&ccaron;o in  
[hep-th/0312154](http://arxiv.org/abs/hep-th/0312154).

###Surface transport###

From a line bundle gerbe with connection one obtains a notion of [[parallel transport]] along surfaces in a way that generalizes the procedure for locally trivialized fiber bundles with connection.

Recall that in the case of fiber bundles, the holonomy associated to a based loop $\gamma$ is obtained by

* choosing a triangulation of the loop (i.e., a decomposition into intervals) such that each vertex sits in a double intersection $U_{ij}$ and such that each edge sits in a patch $U_i$ 

* choosing for each edge a lift into $Y = \sqcup_i U_i$

* choosing for each vertex a lift into $Y^{[2]} = \sqcup_{ij} U_i\cap U_j$

* assigning to each edge lifted to $U_i$ the transport computed from the connection 
    1-form $a_i$

* assigning to each vertex  lifted to $U_i \cap U_j$ the value of the transition function
    $g_{ij}$ at that point

* multiplying these data in the order given by $\gamma$ .

For bundle gerbes this generalizes to a procedure that assigns a triangulation to a closed surface, that lifts faces, edges, and vertices to single, double and triple intersections,
respectively, and which assigns the exponentiated integrals of the 2-form over faces, of the connection 1-form over edges, and assigns the isomorphism $\mu_{ijk}$ to vertices.

For the abelian case (line bundle gerbes) this procedure has been first described in

* K. Gawedzki &amp; N. Reis, _WZW branes and Gerbes_
([arXiv](http://arxiv.org/abs/hep-th/0205233))

based on

* O. Alvarez, _Topological quantization and cohomology_
Commun. Math. Phys. 100 (1985), 279-309.

Further discussion can be found in 

* A. Carey, S. Johnson &amp; M. Murray, _Holonomy on D-branes_, ([arXiv](http://arxiv.org/abs/hep-th/0204199))

Gawedzki and Reis showed this way that the Wess-Zumino term in the WZW-model is nothing but the surface holonomy of a (line bundle) gerbe.

In terms of string physics this means that the string (the $2$-particle) couples to the Kalb-Ramond field -- which hence has to be interpreted as the connection ("and curving") of a gerbe -- in a way that categorifies the coupling of the electromagnetically charged ($1$-)particle to a line bundle.

The necessity to interpret the Kalb--Ramond field as a connection on a gerbe was originally discussed in

* D. Freed and E. Witten
_Anomalies in string theory with D-branes_, Asian J. Math. 3 (1999), 819-851 ([arXiv](http://arxiv.org/abs/hep-th/9907189))


Underlying the Gawedzki--Reis formula is a general mechanism of transition of transport $2$-functors, described in

* U. Schreiber, K. Waldorf, _Connections on non-abelian gerbes and their holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923))

and similarly in 

* Joao Faria Martins, Roger Picken, _A Cubical Set Approach to 2-Bundles with Connection and Wilson Surfaces_ ([arXiv](http://arxiv.org/abs/0808.3964))


 This applies to more general situations than ordinary line bundle gerbes with connection.

The generalization to unoriented surfaces (hence to type I strings) was given in

* K. Waldorf, C. Schweigert &amp; U. S., _Unoriented WZW Models and Holonomy of Bundle Gerbes_ ([arXiv](http://arxiv.org/abs/hep-th/0512283))

## Related entries

* [[transgression of bundle gerbes]]

##References##

The notion of _bundle gerbe_ as such was introduced in

* [[Michael Murray]], _Bundle gerbes_ ([arXiv:dg-ga/9407015](http://arxiv.org/abs/dg-ga/9407015))


[[!redirects bundle gerbes]]