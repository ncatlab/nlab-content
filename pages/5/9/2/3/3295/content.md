
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
* table of contents
{:toc}

## Idea

Where _[[cohomology]]_ classifies [[cocycles]] on a space $X$ with coefficients in some object $A$, _relative cohomology_ for a map of spaces $Y \to X$ classifies cocycles on $X$ that satisfy some condition when pulled back to $Y$, such as being trvializable there.

## Definition

We first give a general abstract definition and then reduce to certain special cases.

### General definition

Recall the general abstract definition of _[[cohomology]]_, as discussed there: 

for $\mathbf{H}$ an [[(∞,1)-topos]], and $X, A \in \mathbf{H}$ two [[objects]], a _cocycle on $X$ with coefficients in $A$_ is a morphism $X \to A$, the [[∞-groupoid]] of cocycles, [[coboundaries]] and higher coboundaries is the [[(∞,1)-categorical hom space]] $\mathbf{H}(X,A)$ and the _cohomology_ classes themselves are the connected components / homotopy classes in there

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$

+-- {: .num_defn}
###### Definition

Let $i : Y \to X$ and $f : B \to A$ be two [[morphisms]] in $\mathbf{H}$. Then the **relative cohomology** of $X$ with coefficients in $A$ relative to these morphisms is the connected components of the $\infty$-groupoid of relative cocycles

$$
  H_{Y}^B(X,A) := \pi_0 \mathbf{H}^I(Y \stackrel{i}{\to} X\;,\; B \stackrel{f}{\to} A)
  \,,
$$

where $\mathbf{H}^I$ the [[arrow category]] of $\mathbf{H}$, hence the [[(∞,1)-category of (∞,1)-functors]] $I \to \mathbf{H}$, where $I$ is the [[interval category]].


=--

+-- {: .num_remark}
###### Remark

Often relative cohomology is considered for the special case where $A$ is a [[pointed object]], $B = *$ is the [[terminal object]] and $B \simeq *  \to A$ is the point inclusion. In this case we may write just

$$
  H_Y(X,A) := H_Y^*(X,A)
  \,.
$$


=--

+-- {: .num_prop #AsAPullback}
###### Remark

The $\infty$-groupoid of relative cocycles is the [[(∞,1)-pullback]] in 

$$
  \array{
    \mathbf{H}^I(Y \to X, B \to A)
    &\to&
    \mathbf{H}(Y, B)
    \\
    \downarrow && \downarrow^{\mathrlap{f_*}}
    \\
    \mathbf{H}(X, A) &\stackrel{i^*}{\to}& \mathbf{H}(Y,A)
  }
  \,.
$$

This makes manifest the interpretation of relative cocycles as $A$-cocycles on $X$ whose restriction to $Y$ is equipped with a coboundary to a $B$-cocycle on $Y$.

If $B$ is the point then this means: $A$ cocycles on $X$ which are equipped with a trivialization on $Y$.

=--


+-- {: .num_remark #RelationToTwistedCohomology}
###### Remark

If we fix an $A$-cocycle $\mathbf{c}$ on $X$, then we may consider the relative cohomology just of this cocycle, hence the [[homotopy fiber]] of the $\infty$-groupoid of relative cocycles over $\mathbf{c}$

$$
  \array{
    \mathbf{H}^I_{\mathbf{c}}(i,f) &\to& \mathbf{H}^I(i,f)
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{\mathbf{c}}{\to}& \mathbf{H}(X,A)
  }
  \,.
$$

By the [[pasting law]] it follows that this fiber is equivalently given by the following [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}^I_{\mathbf{c}}(i,f) &\to& \mathbf{H}(Y,B)
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{f_*\mathbf{c}}{\to}& \mathbf{H}(Y,A)
  }
  \,.
$$

Comparison shows that this identifies $\mathbf{H}^I_{\mathbf{c}}(i,f)$ as the cocycle $\infty$-groupoid of the $[f_*\mathbf{c}]$-[[twisted cohomology]] of $Y$ with coefficients in the [[homotopy fiber]] of $f$.

See for instance the example of [twisted bundles on D-branes](#TwistedBundlesOnDBranes) below.

=--

### In chain complexes

A special case of the general definition of [[cohomology]] is _[[abelian sheaf cohomology]]_, obtained by taking the coefficient objects $A$ and $B$ to be in the image of [[chain complexes]] under the [[Dold-Kan corresponence]].

If moreover we restrict attention to the case that $B = *$, then by remark \ref{AsAPullback} the relative cohomology is given by the [[homotopy fiber]] of a morphism of cochain complexes $C^\bullet(X,A) \to C^\bullet(Y,A)$, presenting the morphism $\mathbf{H}(X, A) \to \mathbf{H}(Y,A)$. Such homotopy fibers are given for instance by dual [[mapping cone]] complexes. Accordingly, in the abelian case the $A$-cohomology on $X$ relative to $Y$ is the [[cochain cohomology]] of this mapping cone complex. This is the definition one finds in much traditional literature.

## Examples

### Twisted bundles on D-branes
 {#TwistedBundlesOnDBranes}

We consider an example of relative cohomology for the general case where $B \to A$ is not the point inclusion, but exhibits an additional twist, according to \ref{RelationToTwistedCohomology}.

This example is motivated from the [[physics]] of [[D-branes]] in [[type II string theory]], as well as from [[twisted K-theory]].

Let the ambient [[(∞,1)-topos]] be $\mathbf{H} := $ [[Smooth∞Grpd]]. For any $n \in \mathbb{N}$ consider the sequence of [[Lie groups]]

$$
  U(1) \to U(n) \to PU(n)
  \,,
$$

exhibiting the [[unitary group]] as a [[central extension of groups]] of the [[projective unitary group]]. The [[fiber]] sequence on [[delooping]] [[smooth ∞-groupoids]] induced by this is 

$$
  \mathbf{B}U(1) \to \mathbf{B}U(n) \to \mathbf{B} PU(n) \stackrel{f}{\to} \mathbf{B}^2 U(1)
  \,.
$$

For $Y$ a [[smooth manifold]], the $f$-[[twisted cohomology]] of $X$ is classifies $U(n)$-principal [[twisted bundles]] on $Y$, as discussed there. These appear in [[string theory]]/[[twisted K-theory]], where the twist is a [[B-field]]/[[circle n-bundle with connection|circle 2-bundle]]/[[bundle gerbe]] classified by $Y \to \mathbf{B}^2 U(1)$.

But in these applications, this 2-bundle is the restriction of an ambient 2-bundle classified by $\mathbf{c} : X \to \mathbf{B}^2 U(1)$ on a [[spacetime]] $X$ along an embedding $Y \hookrightarrow X$ of the [[D-brane]] [[worldvolume]]. Therefore the [[moduli stack]] of total field configurations consisting of the ambient [[B-field]] and the [[gauge field]] on the D-brane (see [[Freed-Witten anomaly]] for the details of this mechanism) is the $infty$-groupoid of $(Y \hookright X)$-relative cocycles with coefficients in $(\mathbf{B}PU \to \mathbf{B}^2 U(1))$.

