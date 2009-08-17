
# Idea #

This entry list details on concrete constructions for examples of [[geometric function theory|geometric function theories]], or closely related structures.

Recall the notion of _geometric function object_ from [[geometric function theory]]:

Given an [[(∞,1)-topos]] $\mathbf{H}$ of [[∞-stack]]s  -- in the simplest case just [[Top]] or [[∞-Grpd]] -- a _geometric function theory_ is some kind of assignment

$$
  C : \mathbf{H} \to (\infty,1)Cat
$$

such that for $X \in \mathbf{H}$ the object $C(X)$ behaves to some useful extent like a collection of "functions on $X$". 

More concretely, this will usually be taken to mean that:

* **existece of pull-push** for every morphism $f : A \to B$ in $\mathbf{H}$ there is naturally (functorially) an [[adjunction]] $f_* : C(A) \stackrel{\leftarrow}{\to} C(B) : f^*$ with $f_*$ playing the role of push-forward of functions along $f$ and $f^*$ playing the role of pullback of functions along $f$;

* **respect for fiber products** with respect to some suitable [[tensor product]] of geometric functions one has for each ([[homotopy pullback|homotopy]]) [[fiber product]] $X \times_Z Y$ in $\mathbf{H}$ that
  $$
   C(X \times_Z Y) \simeq C(X) \otimes_{C(Z)} C(Y)
   \,.
  $$


## over-categories and groupoidification ##


Consider here the assignment

$$
  C := \mathbf{H}/(-) : \mathbf{H} \to (\infty,1)Cat
$$

that sends each object $X \in \mathbf{H}$ to its [[over category]] $\mathbf{H}/X$.

**Remarks**

* This is implicitly the notion of geometric ∞-functions that underlies [[John Baez]]' notion of [[groupoidification]] as well as the generalized sections that appear at ... 

* The definition seems to be disturbingly non-linearized, but this should be viewed in light of the possible nature of the $X$s considered here. If $X = E$ is, for instance, the [[groupoid]] incarnation of the total space of the [[vector bundle]] associated to a $G$-[[principal bundle]], then a choice of groupoid over $E$ picks a bunch of vectors in that bundle, hence picks a "distributional section" of that bundle.

... (have to interrupt)...
