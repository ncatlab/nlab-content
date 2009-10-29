<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

We first state the [[category theory|general nonsense]] definition of _equivariant cohomology_ and then derive from it the more concrete formulations that are traditionally given in the literature.

+-- {: .standout}

Essentially, equivariant cohomology is the [[cohomology]] of [[groupoid]]s.

=--

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

# Examples #

## group cohomology ##

By comparing the definition of equivariant cohomology with that of [[group cohomology]] one sees that group cohomology can be equivalently thought of as being **equivariant cohomology of the point**.

## equivariant bundles ##

For $G$ some [[group]] let $G Bund$ be the [[stack]] of $G$-[[principal bundle]]s. Let $K$ be some finite group (just for the sake of simplicity of the example) and let $K \to Aut(X_0)$ be an action of $K$ on a space $X_0$. Let $X = X_0 // K$ be the corresponding [[action groupoid]].

Then a cocycle in the $K$-equivariant cohomology $H(X_0//K, G Bund)$ is

* a $G$-[[principal bundle]] $P \to X$ on $X$;

* for each $k \in K$ an [[isomorphism]] of $G$-principal bundles $\lambda_k : P \to k^* P$

* such that for all $k_1, k_2 \in K$ we have $\lambda_{k_2}\circ \lambda_{k_1} = \lambda_{k_2\cdot k_1}$.

## local systems -- flat connections ##

For $X_0$ a [[space]] and $X := P_n(X_0)$ a version of its [[path n-groupoid]] we have a canonical inclusion $X_0 \hookrigtharrow P_n(X_0)$ of $X_0$ as the collection of constant paths in $X_0$.

Consider for definiteness $\Pi(X_0) := \Pi_\infty(X_0)$, the [[path ∞-groupoid]] of $X_0$. (All other cases are in principle obtaind from this by truncation and/or strictification).

Then for  $A$ some coefficient $\infty$-groupoid, a morphism $g : X_0 \to A$ can be thought of as classifying a $A$-[[principal ∞-bundle]] on the space $X_0$.

On the other hand, a morphism out of $P_n(X_0)$ is something like a flat [[connection on a bundle|connection]] (see there for more details) on this principal $\infty$-bundle, also called an $A$-[[local system]]. (More details on this are at [[schreiber:differential cohomology]]).

Accordingly, an extension of $g : X_0 \to A$ through the inclusion $X_0 \hookrightarrow \Pi(X)$ is the process of equipping a principal $\infty$-bundle with a flat connection.

Comparing with the above definition of eqivariant cohomology, we see that flat connections on bundles may be regarded as **path-equivariant structures** on these bundles.

This is therefore an example of equivariance which is not with respect to a global [[group]] action, but genuinely a [[groupoid]]al one.

#Remarks#

When pairing equivariant cohomology with other variants of cohomology such as [[twisted cohomology]] or [[differential cohomology]] one has to exercise a bit of care as to what it really is that one wants to consider. A discussion of this is (beginning to appear) at [[schreiber:differential equivariant cohomology]].