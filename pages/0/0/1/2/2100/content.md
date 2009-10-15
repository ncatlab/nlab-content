#Content#

* automatic table of contents goes here
{:toc}

# Idea #

This entry list details on concrete constructions for examples of [[geometric function theory|geometric function theories]], or closely related structures.

Recall the notion of _geometric function object_ from [[geometric function theory]]:

Given an [[(∞,1)-topos]] $\mathbf{H}$ of [[∞-stack]]s  -- in the simplest case just [[Top]] or [[∞-Grpd]] -- a _geometric function theory_ is some kind of assignment

$$
  C : \mathbf{H} \to (\infty,1)Cat
$$

such that for $X \in \mathbf{H}$ the object $C(X)$ behaves to some useful extent like a collection of "functions on $X$". 

More concretely, this will usually be taken to mean that $C$ satisfies properties of the following kind:

* **existence of pull-push** -- For every morphism $f : A \to B$ in $\mathbf{H}$ there is naturally (functorially) an [[adjunction]] $f_* : C(A) \stackrel{\leftarrow}{\to} C(B) : f^*$ with $f_*$ playing the role of push-forward of functions along $f$ and $f^*$ playing the role of pullback of functions along $f$;

* **respect for composition of spans** -- Pull-push through [[span]]s should be functorial: if 
  $$
    \array{
      &&&& Y_1 \times_{X_2} Y_2
      \\
      &&& {}^{p_1}\swarrow && \searrow^{p_2}
      \\
      && Y_1 &&&& Y_2
      \\
      & {}^t\swarrow && \searrow^u && {}^v\swarrow && \searrow^w
      \\
      X_1 &&&& X_2 &&&& X_4
    }
  $$
  is a composite of two [[span]]s, then the pull-push through both spans seperately should be equivalent to that through the total span

  $$
    w_* v^* u_* t^* 
    \simeq
    {w}_* {p_2}_* p_1^* t^* 
    \,.
  $$

  Of course this just means that the two ways to pull-push through the pullback diamond 

  $$
    \array{
      &&&& Y_1 \times_{X_2} Y_2
      \\
      &&& {}^{p_1}\swarrow && \searrow^{p_2}
      \\
      && Y_1 &&&& Y_2
      \\
      & && \searrow^u && {}^v\swarrow && 
      \\
      &&&& X_2 &&&& 
    }
  $$

  should coincide.

* **respect for fiber products** -- With respect to some suitable [[tensor product]] of geometric functions one has for each ([[homotopy pullback|homotopy]]) [[fiber product]] $X \times_Z Y$ in $\mathbf{H}$ that
  $$
   C(X \times_Z Y) \simeq C(X) \otimes_{C(Z)} C(Y)
   \,.
  $$


## over-categories and groupoidification ##

This first example is rather minimalistic and may feel a bit tautological, as compared to more involved constructions as discussed below. It does nevertheless have interesting applications and, due to its structural simplicity, should serve as a good model on which to study the structural aspects of geometric function theory.

So consider here the assignment

$$
  C := \mathbf{H}/(-) : \mathbf{H} \to (\infty,1)Cat
$$

that sends each object $X \in \mathbf{H}$ to its [[over category]] $\mathbf{H}/X$.

Checking that this assignment does satisfy a good deal of the properties of a geometric function object amounts to recalling the properties of  [[over category|over categories]].

So an [[object]] in $C(X)$ is a morphism $\psi : \Psi \to X$ in $\mathbf{H}$. A [[morphism]] $(\psi,\Psi) \to (\psi',\Psi')$ is a diagram

$$
  \array{
    \Psi &&\to&& \Psi'
    \\
    & {}_\psi\searrow && \swarrow_{\psi'}
    \\
    && X
  }
$$

in $\mathbf{H}$.

For $f : X \to Y$ a morphism in $\mathbf{H}$ the push-forward functor

$$
  f_* : C(X) \to C(Y)
$$

is simply given by postcomposition with $f$:

$$
  f_* \;\;:\;\; 
  \left(
    \array{
      \Psi
      \\
      \downarrow^\psi
      \\
      X
    }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
    \array{
      \Psi
      \\
      \downarrow^\psi
      \\
      X
      \\
      \downarrow^f
      \\
      Y
    }
  \right)
  \,.
$$

The pullback functor 

$$
  f^* : C(Y) \to C(X)
$$

is literally given by the ([[homotopy pullback|homotopy]]) [[pullback]] 

$$
  \array{
    f^* \Psi &\to& \Psi
    \\
    \downarrow^{f^* \psi} && \downarrow^\psi
    \\
    X &\stackrel{f}{\to}& Y
  }
$$

of a morphism $\psi : \Psi \to Y$ along $f$.

A quick way to check that pushforward $f_*$ and pullback $f^*$ defined this form a pair of  [[adjoint functor]]s is to notice the hom-isomorphism

$$
  Hom_{\mathbf{H}/X}(\Psi, f^* \Phi)
  \simeq
  Hom_{\mathbf{H}/X}(f_* \Psi, \Phi)
$$

which is established by the essential uniqueness of the universal morphism into the pullback

$$
  \array{
    \Psi &&\to&&
    \\
    & \searrow^{\exists ! \bar k} & && \downarrow^{k}
    \\
    \downarrow && f^* \Phi &\to& \Phi
    \\
    &\searrow& \downarrow^{f^* \psi} && \downarrow^\psi
    \\
    && X &\stackrel{f}{\to}& Y
  }
$$

Here the outer diagram exhibits a morphism $k : f_* \Psi \to \Phi$. The universal property of the [[pullback]] says that this essentially uniquely corresponds to the [[adjunct]]  morphism $\bar k : \Psi \to f^* \Phi$.

The fact that the pull-push respects composition of spans is a direct consequence of the way [[pullback]] diagrams compose under pasting: recall that in a diagram

$$
  \array{
    A &\to& B &\to& C
    \\
    \downarrow && \downarrow && \downarrow
    \\
    D &\to& E &\to& F
  }
$$

for which the left square is a pullback, the total rectangle is a pullback precisely if the right square is, too.

Apply this to the pull-push of an object $\left(\array{ \Psi \\ \downarrow^{\psi} \\ Y_1}\right) \in C(Y_1)$ through a pullback diamond (see the introduction above)

  $$
    \array{
      &&&& Y_1 \times_{X_2} Y_2
      \\
      &&& {}^{p_1}\swarrow && \searrow^{p_2}
      \\
      && Y_1 &&&& Y_2
      \\
      & && \searrow^u && {}^v\swarrow && 
      \\
      &&&& X_2 &&&& 
    }
    \,.
  $$

This is described by the diagram

  $$
    \array{
      && p_1^* \Psi
      \\
      & {}^{q_1}\swarrow && \searrow^{p_1^* \psi}
      \\
      \Psi&&&& Y_1 \times_{X_2} Y_2
      \\
      &\searrow^f && {}^{p_1}\swarrow && \searrow^{p_2}
      \\
      && Y_1 &&&& Y_2
      \\
      & && \searrow^u && {}^v\swarrow && 
      \\
      &&&& X_2 &&&& 
    }
    \,.
  $$

By the above definitions, the push-pull operation $v^* u_*$ is encoded in the pullback property of the total outer rectangle. On the other hand, the pull-push operation ${p_2}_* p_1^*$ is determined by the pullback property of the upper square. By the above fact both properties are equivalent. This means that indeed

$$
  v^* u_* \simeq {p_2}_* p_1^*
$$

and hence that the pull-push operations defined by over-categories are compatible with composition of [[span]]s.


Finally, there is a simple observation on the [[cartesian product]] on [[over category|over categories]]:

for 

$$
  \array{
     && Y
     \\
     && \downarrow^g
     \\
     X &\stackrel{f}{\to}& Z
  }
$$

a diagram in $\mathbf{H}$, notice that the objects in the [[fiber product]] of [[over category|over categories]]

$$
  (\mathbf{H}/X) \times_{\mathbf{H}/Y} \mathbf{H}/Y
$$ 

are those pairs $\psi : \Psi \to X$ and $\phi : \Phi \to Y$ such that we get a (homotopy) commutative diagram

$$
  \array{
     \Psi \simeq \Phi &\stackrel{\phi}{\to}& Y
     \\
     \downarrow^\psi && \downarrow^g
     \\
     X &\stackrel{f}{\to}& Z
  }
  \,.
$$

Again by the universal property of the pullback this is the same as maps

$$
  (\Psi \simeq \Phi) \to X \times_Z Y
$$

which are precisely the objects of $C(X \times_Z Y)$. So we get

$$
  C(X \times_Z Y) \simeq C(X) \times_{C(Z)} C(Y)
$$

### remarks ###

 * This is -- more or less implicitly -- the notion of geometric ∞-functions that underlies [[John Baez]]' notion of [[groupoidification]] as well as the generalized sections that appear at [these sigma-model notes](http://ncatlab.org/schreiber/show/Nonabelian+cocycles+and+their+sigma+model+QFTs).

* The definition seems to be disturbingly non-linearized, but this should be viewed in light of the possible nature of the $X$s considered here. If $X = E$ is, for instance, the [[groupoid]] incarnation of the total space of the [[vector bundle]] associated to a $G$-[[principal bundle]], then a choice of groupoid over $E$ picks a bunch of vectors in that bundle, hence picks a "distributional section" of that bundle.



## under-categories of $\infty$-quantities ##

By essentially simply applying [[Isbell duality]] for the case that the underlying [[site]] is [[CartSp]] to the above example one obtains the following example.

+-- {: .standout}

Tentative.

=--

Recall the notion of [[∞-quantity]]. Notice that by the discussion at [[models for ∞-stack (∞,1)-toposes]] every object $A \in \mathbf{H}$ may be modeled as a [[simplicial presheaf]]. Let $C^\infty(-)$ be the map that sends simplicial presheaves to cosimplicial copresheaves as described at [[∞-quantity]].

Then consider the assignment

$$
  C(-) : \mathbf{H} \to (\infty,1)Cat
$$

that sends every $X$ to the $(\infty,1)$-category of cosimplicial copresheaves  to the [[under category]]

$$
  C(X) = C^\infty(X)/CoSCoSh
$$

or

$$
  C(X) = C^\infty_{loc}(X)/CoSCoSh
  \,.
$$

From the discussion at [[∞-quantity]] and [[Lie-∞ algebroid representation]] we see that we can think of objects in $C(X)$ defines this way as representations of the [[Lie-∞ algebroid]] of $X$.

Now pullback is left adjoint and push-forward is right adjoint.


## quasicoherent sheaves ##

The choice $C(X) =$ the [[stable (∞,1)-category]] of [[quasicoherent sheaf|quasicoherent sheaves]] on a [[derived stack]] $X$ is discussed at 

* [[geometric ∞-function theory]].


[[!redirects examples for geometric function objects]]
[[!redirects example for geometric function objects]]
[[!redirects geometric function objects]]