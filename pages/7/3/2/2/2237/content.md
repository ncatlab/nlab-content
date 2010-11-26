
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

Equivariant cohomology is [[cohomology]] of objects on which a [[group]] acts that takes the group action into account. 

There is some flexibility in interpreting precisely what this should mean, and accordingly there are various different flavors of equivariant cohomology theory, all closely related, but different.

Let $\mathbf{H}$ be the ambient [[(∞,1)-topos]] inside which we consider [[cohomology]], as described there. Let $G$ be a [[groupoid object in an (infinity,1)-category|group object]] in $\mathbf{H}$ and let $X \in \mathbf{H}$ be an object equipped with an [[action]] of $G$.

1. **Borel equivariant cohomology** We can form the [[action groupoid]] $X//G \in \mathbf{H}$ of the [[action]] of $G$ on $X$: the weak quotient of the action. Then for any coefficient object $A$ we may think of the [[cohomology]] of $X//G$ as being the $G$-equivariant cohomology of $X$. This definition is known _Borel equivariant cohomology_

   $$
     H_{Borel}(X,A) := \pi_0 \mathbf{H}(X//G, A)
     \,,
   $$ 

   This notion of equivariant cohomology captures notably the standard notion of equivariant $K$-[[principal bundle]]s for $A = \mathbf{B}K$ the [[delooping]] of the structure group $K$. If $X = {*}$ is the [[point]], then this reduces to the definition of [[group cohomology]] of the group $G$. Group cohomology is the Borel-equivariant cohomology of the point.

   This is described below in the section [Borel equivariant cohomology](#Borel).

1. **Equivariant multiplicative cohomology** For cohomology in $\mathbf{H} = Top$ with coefficient objects components of an [[E-∞-ring]] spectrum $E$ -- a [[multiplicative cohomology theory]] -- one finds that there is a _refinement_ of Borel equivariant cohomology that is of interest. 

   This is described below in the section [Multiplicative equivariant cohomology](#Multiplicative).


1. **Bredon equivariant cohomology** For $G$ a [[Lie group]], besides the [[action groupoid]]s of the form $X//G$, the group $G$ determines canonically its [[orbit category]] $O_G$. The [[(∞,1)-topos]] 
 
   $$
     \mathbf{H} = PSh_{(\infty,1)}(O_G)
   $$ 

   of [[(∞,1)-presheaf|(∞,1)-presheaves]] on $O_G$ has as objects [[topological space]]s/[[simplicial set]]s with a $G$-[[action]], whose [[homotopy n-type|homotopy type]] is determined on the subspaces of fixed points under the action of all closed [[subgroup]]s $K \subset G$.   Integer-graded _[[Bredon cohomology]]_ is the (abelian) [[cohomology]] inside this [[(∞,1)-topos]].  It can also be generalized to $RO(G)$-graded Bredon cohomology.  This is the kind of equivariant cohomology used mostly in [[equivariant stable homotopy theory]].

   This is described below in the section [Bredon equivariant cohomology](#Bredon).


## Borel equivariant cohomology {#Borel}

We first state the [[category theory|general abstract]] definition of _equivariant cohomology_ and then derive from it the more concrete formulations that are traditionally given in the literature.

+-- {: .standout}

Essentially, Borel equivariant cohomology is the [[cohomology]] of [[action groupoid]]s.

=--

For standard [[cohomology]] in the [[(∞,1)-topos]] $\mathbf{H} =$ [[Top]] these [[action groupoid]]s of a [[group]] $G$ acting on a [[topological space]] $X$ are traditionally known as the [[Borel construction]] $\mathcal{E}G \times_G X$.

Recall from the discussion at [[cohomology]] that in full generality we have a notion of cohomology of an object $X$ with coefficients in an object $A$ whenever $X$ and $A$ are objects of some [[(∞,1)-topos]] $\mathbf{H}$. The cohomology set $H(X,A)$ is the set of connected components in the [[hom-object]] [[∞-groupoid]] of maps from $X$ to $A$: $H(X,A) = \pi_0 \mathbf{H}(X,A)$.

Recall moreover from the discussion at [[space and quantity]] that objects of an [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-topos of (∞,1)-sheaves]] have the interpretation of [[∞-groupoid]]s with extra structure. For instance for $(\infty,1)$-sheaves on a [[site]] of  smooth test spaces such as [[Diff]] these objects have the interpretation of [[Lie ∞-groupoid]]s.

In this case, for $X$ some such [[∞-groupoid]] with structure, let $X_0  \hookrightarrow X$ be its 0-truncation, which is the [[space]] of [[object]]s of $X$, the [[discrete groupoid|categorically discrete groupoid]] underlying $X$. We think of the morphisms in $X$ as determining which points of $X_0$ are related under some kind of action on $X_0$, the 2-morphisms as relating these relations on some higher action, and so on. **Equivariance** means, roughly: functorial transformation behaviour of objects on $X_0$ with respect to this "action" encoded in the morphisms in $X$. This is the intuition that is made precise in the following

In the simple special case that one should keep in mind, $X$ is for instance the [[action groupoid]] $X = X_0//G$ of the [[action]], in the ordinary sense, of a [[group]] $G$ on $X_0$: its morphisms $x \to g(x)$ connect those objects of $X_0$ that are related by the action by some group element $g \in G$.

It is natural to consider the [[relative cohomology]] of the inclusion $X_0 \hookrightarrow X$. Equivariant cohomology is essentially just another term for relative cohomology with respect to an inclusion of a space into a ($\infty$-)groupoid.

+-- {: .un_defn}
###### Definition (equivariant cohomology)

In some [[(∞,1)-topos]] $\mathbf{H}$ the **equivariant cohomology** with coefficient in an object $A$ of a 0-truncated object $X_0$ with respect to an action encoded in an inclusion $X_0 \hookrightarrow X$ is simply the $A$-valued cohomology $H(X,A)$ of $X$.

More specifically, an **equivariant structure** on an $A$-cocycle $c : X_0 \to A$ on $X_0$ is a choice of extension $\hat c$

$$
  \array{
    X_0 &\to& A
    \\
    \downarrow & \nearrow_{\hat c}
    \\
    X
  }
  \,.
$$

i.e. a lift of $c$ through the projection $\mathbf{H}(X,A) \to \mathbf{H}(X_0,A)$.

=--




### Examples 

#### Group cohomology 

By comparing the definition of equivariant cohomology with that of [[group cohomology]] one sees that group cohomology can be equivalently thought of as being **equivariant cohomology of the point**.

#### Equivariant bundles

For $G$ some [[group]] let $G Bund$ be the [[stack]] of $G$-[[principal bundle]]s. Let $K$ be some finite group (just for the sake of simplicity of the example) and let $K \to Aut(X_0)$ be an action of $K$ on a space $X_0$. Let $X = X_0 // K$ be the corresponding [[action groupoid]].

Then a cocycle in the $K$-equivariant cohomology $H(X_0//K, G Bund)$ is

* a $G$-[[principal bundle]] $P \to X$ on $X$;

* for each $k \in K$ an [[isomorphism]] of $G$-principal bundles $\lambda_k : P \to k^* P$

* such that for all $k_1, k_2 \in K$ we have $\lambda_{k_2}\circ \lambda_{k_1} = \lambda_{k_2\cdot k_1}$.

#### Local systems -- flat connections

For $X_0$ a [[space]] and $X := P_n(X_0)$ a version of its [[path n-groupoid]] we have a canonical inclusion $X_0 \hookrightarrow P_n(X_0)$ of $X_0$ as the collection of constant paths in $X_0$.

Consider for definiteness $\Pi(X_0) := \Pi_\infty(X_0)$, the [[path ∞-groupoid]] of $X_0$. (All other cases are in principle obtaind from this by truncation and/or strictification).

Then for  $A$ some coefficient $\infty$-groupoid, a morphism $g : X_0 \to A$ can be thought of as classifying a $A$-[[principal ∞-bundle]] on the space $X_0$.

On the other hand, a morphism out of $P_n(X_0)$ is something like a flat [[connection on a bundle|connection]] (see there for more details) on this principal $\infty$-bundle, also called an $A$-[[local system]]. (More details on this are at [[schreiber:differential cohomology]]).

Accordingly, an extension of $g : X_0 \to A$ through the inclusion $X_0 \hookrightarrow \Pi(X)$ is the process of equipping a principal $\infty$-bundle with a flat connection.

Comparing with the above definition of eqivariant cohomology, we see that flat connections on bundles may be regarded as **path-equivariant structures** on these bundles.

This is therefore an example of equivariance which is not with respect to a global [[group]] action, but genuinely a [[groupoid]]al one.

### Remarks

When pairing equivariant cohomology with other variants of cohomology such as [[twisted cohomology]] or [[differential cohomology]] one has to exercise a bit of care as to what it really is that one wants to consider. A discussion of this is (beginning to appear) at [[schreiber:differential equivariant cohomology]].


## Equivariant abelian multiplicative cohomology {#Multiplicative}

A refinement of Borel equivariant cohomology. For the moment see

* [Equivariant multiplicative cohomology](http://ncatlab.org/nlab/show/A+Survey+of+Elliptic+Cohomology+-+A-equivariant+cohomology#equivariant)



## Bredon equivariant cohomology {#Bredon}

See also

* [[Bredon cohomology]]

### Preliminary remarks

According to the [[nPOV]] on [[cohomology]], if $X$ and $A$ are objects in an [[(∞,1)-topos]], the 0th cohomology $H^0(X;A)$ is $\pi_0(Map(X,A))$, while if $A$ is a [[groupoid object in an (∞,1)-category|group object]], then $H^1(X;A)= \pi_0(Map(X,B A))$.  More generally, if $A$ is $n$ times [[delooping|deloopable]], then $H^n(X;A) = \pi_0(Map(X, B^n A)$.  In [[Top]], this gives you the usual notions if $A$ is a (discrete) group, and in general, $H^1(X;A)$ classifies [[principal ∞-bundle]]s in whatever [[(∞,1)-topos]].

Now consider the $(\infty,1)$-topos $G Top$ of $G$-equivariant spaces, which can also be described as the [[(∞,1)-presheaf|(∞,1)-presheaves]] on the [[orbit category]] of $G$.  For any other group $\Pi$ there is a notion of a principal $(G,\Pi)$-bundle (where $G$ is the group of equivariance, and $\Pi$ is the structure group of the bundle), and these are classified by maps into a classifying $G$-space $B_G \Pi$.  So the principal $(G,\Pi)$-bundles over $X$ can be called $H^0(X;B_G \Pi)$.  If we had something of which $B_G \Pi$ was a [[delooping]], we could call the principal $(G,\Pi)$-bundles "$H^1(X;?)$", but there does not seem to be such a thing.  It seem sthat $B_G \Pi$ is not connected, in the sense that ${*}\to B_G \Pi$ is not an [[effective epimorphism]] and thus $B_G \Pi$ is not the quotient of a [[groupoid object in an (∞,1)-category|group object]] in $G Top$.

### $G$-equivariant spectra

If we have an object $A$ of our $(\infty,1)$-topos that can be delooped infinitely many times, then we can define $H^n(X;A)$ for any integer $n$ by looking at all the spaces $\Omega^{-n} A = B^n A$.  These integer-graded [[cohomology group]]s are closely connected to each other, e.g. they often have [[cup product]]s or [[Steenrod square]]s or [[Poincare duality]], so it makes sense to consider them all together as a _[[cohomology theory]]_ .  We then are motivated to put together all of the objects $\{B^n A\}$ into a [[spectrum object]], a single object which encodes all of the cohomology groups of the theory.  A general spectrum is a sequence of objects $\{E_n\}$ such that $E_n \simeq \Omega E_{n+1}$; the stronger requirement that $E_{n+1} \simeq B E_n$ restricts us to "connective" spectra, those that can be produced by successively delooping a single object of the $(\infty,1)$-topos.  In [[Top]], the most "basic" spectra are the [[Eilenberg-MacLane spectrum|Eilenberg-MacLane spectra]] produced from the input of an ordinary abelian group.

Now we can do all of this in $G Top$, and the resulting notion of spectrum is called a **naive $G$-spectrum**: a sequence of $G$-spaces $\{E_n\}$ with $E_n \simeq \Omega E_{n+1}$.  Any naive $G$-spectrum represents a cohomology theory on $G$-spaces.  The most "basic" of these are "Eilenberg-Mac Lane $G$-spectra" produced from **coefficient systems**, i.e. abelian-group-valued presheaves on the  [[orbit category]].  The cohomology theory represented by such an Eilenberg-Mac Lane $G$-spectrum is called an (integer-graded) [[Bredon cohomology]] theory.

It turns out, though, that the cohomology theories arising in this way are kind of weird.  For instance, when one calculates with them, one sees [[torsion]] popping up in odd places where one wouldn't expect it.  It would also be nice to have a [[Poincare duality]] theorem for $G$-manifolds, but that fails with these theories.  The solution people have come up with is to widen the notion of "[[loop space object|looping]]" and "[[delooping]]" and thereby the grading: 

instead of just looking at $\Omega^n = Map(S^n, -)$, we look at $\Omega^V = Map(S^V,-)$, where $V$ is a finite-dimensional [[representation]] of $G$ and $S^V$ is its [[one-point compactification]].  Now if $A$ is a $G$-space that can be [[delooping|delooped]] "$V$ times," we can define $H^V(X;A) = \pi_0(Map(X,\Omega^{-V} A)$.  If $A$ can be delooped $V$ times for all representations $V$, then our integer-graded cohomology theory can be expanded to an **$RO(G)$-graded cohomology theory**, with cohomology groups $H^\alpha(X;A)$ for all formal differences of representations $\alpha = V - W$.  The corresponding notion of spectrum is a **genuine $G$-spectrum**, which consists of spaces $E_V$ for all representations $V$ such that $E_V \simeq \Omega^{W-V} E_W$.  A naive Eilenberg-Mac Lane $G$-spectrum can be extended to a genuine one precisely when the coefficient system it came from can be extended to a [[Mackey functor]], and in this case we get an **$RO(G)$-graded Bredon cohomology theory** .

$RO(G)$-graded Bredon cohomology has lots of formal advantages over the integer-graded theory.  For instance, the torsion that popped up in odd places before can now be seen as arising by "shifting" of something in the cohomology of a point in an "off-integer dimension," which was invisible to the integer-graded theory.  Also there is a [[Poincare duality]] for $G$-manifolds: if $M$ is a $G$-manifold, then we can embed it in a representation $V$ (generally not a trivial one!) and by [[Thom space]] arguments, obtain a Poincare duality theorem involving a dimension shift of $\alpha$, where $\alpha$ is generally not an integer (and, apparently, not even uniquely determined by $M$!).  Unfortunately, however, $RO(G)$-graded Bredon cohomology is kind of hard to compute.




## References

* [[Matvei Libine]], _Lecture Notes on Equivariant Cohomology_ ([arXiv](http://arxiv.org/abs/0709.3615))

* [[Peter May]], _Equivariant homotopy and cohomology theory_ ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))

* B. Guillou, _A short note on models for equivariant homotopy theory_ ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf))

Parts of the above material is taken from a blog discussion between [[Mike Shulman|Mike]] and [[Urs Schreiber|Urs]] [here](http://golem.ph.utexas.edu/category/2010/01/the_sacred_and_the_profane.html#c031280).

* blog on [Localization techniques in Equivariant Cohomology](http://www.aimath.org/wiki/localization/index.php/Main_Page)