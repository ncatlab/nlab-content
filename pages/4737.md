
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
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

For $\mathcal{G}$ a [[groupoid object in an (infinity,1)-category|groupoid object]] a _$\mathcal{G}$-principal bundle_ is a [[morphism]] $P \to X$ with an principal [[action]] of $\mathcal{G}$ on $P$.

## Definition

For $G$ a [[group object]] in some [[(∞,1)-topos]] $\mathbf{H}$ (for instance $\mathbf{H} = $ [[Smooth∞Groupoids]] for smooth [[Lie groupoid]]-bundles), and $\mathbf{B}G$ the corresponding [[delooping]] object, $G$-principal bundles are the [[(∞,1)-pullback]]s of the form

$$
  \array{
    P &\to& * 
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{B}G
  }
  \,.
$$

One equivalently (with non-negligible but conventional chance of confusion of terminology) calls such $P \to X$ a $\mathbf{B}G$-**groupoid principal bundle.

So more generally, for $\mathcal{G}$ any groupoid object with collection $\mathcal{G}_0$ of [[object]]s, the $(\infty,1)$-pullbacks

$$
  \array{
    P &\to& \mathcal{G}_0
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathcal{G}
  }
$$

are **groupoid principal bundles** .




## Examples

###Lie groupoid principal bundles

For $\mathbf{H}$ = $\infty LieGrpd$ and $G:=G_1 \Rightarrow G_0$ a [[Lie groupoid]], a $G$-principal bundle is locally of the form

$$
  U_i \times \mathcal{G}_{x_i}
$$

for $\mathcal{G}_{x_i}$ the target fiber over an object $x_i$, or equivalently of the form $U_i\times_{G_0} G_1$. 

More precisely, we have the following sub-definition for **Lie groupoid principal bundles**: Given a [[Lie groupoid]] $G=G_1 \Rightarrow G_0$,  a $G$-principal bundle over a manifold $M$ (with right $G$ action) is a surjective submersion $P\xrightarrow{\pi} M$ together with a moment map $P\xrightarrow{\rho} G_0$ (sometimes also called an anchor), such that there is a (right) **$G$-action** on $P$, that is, there is map $\Phi: P\times_{G_0} G_1 \to P$, such that 

* $\pi(\Phi(p, g))=\pi(p)$,

* $ \rho(\Phi(p,g))=s(g)$, 

* $\Phi(\Phi(p, g_1), g_2)=\Phi(p, g_1 g_2)$.

Moreover, we require the $G$-action to be free and proper, that is, 

* [free] $P\times_{G_0} G_1 \xrightarrow{id\times \Phi} P\times P$ is injective, 

* [proper]$P\times_{G_0} G_1 \xrightarrow{id\times \Phi} P\times P$ is a proper map , i.e. the preimage of a compact is compact.

These two conditions are equivalent to the fact that

$$ P\times_{G_0} G_1 \xrightarrow{id\times \Phi} P\times_M P$$

is an isomorphism.


## Applications

* Regarded as groupoid [[bibundles]], groupoid principal bundles serve as models for [[Morita morphisms]] between [[Lie groupoids]].

## Related concepts

* [[principal bundle]] / [[torsor]] / **groupoid principal bundle**

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]]

* [[higher differential geometry]]

## References

* [[Ieke Moerdijk]], [[Janez Mrcun]] _Introduction to Foliations and Lie Groupoids_, Cambridge Studies in Advanced Mathematics 91, Cambridge University Press, Cambridge, (2003) ([doi:10.1017/CBO9780511615450](https://doi.org/10.1017/CBO9780511615450))


[[!redirects groupoid principal bundles]]