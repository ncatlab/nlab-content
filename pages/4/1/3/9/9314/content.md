
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

### Traditional

Given a right [[principal bundle|principal]] $G$-bundle $\pi: P\to X$ and a left $G$-[[action]] on some $F$, all in a sufficiently strong category $C$ (such as [[Top]]), one can form the [[quotient object]] $P \times_G F = (P\times F)/{\sim}$, where $P \times F$ is a [[product]] and $\sim$ is the smallest [[congruence]] such that (using [[generalized element]]s) $(p g,f)\sim (p,g f)$; there is a canonical projection $P\times_G F\to X$ where the class of $(p,f)$ is mapped to $\pi(p)\in X$, hence making $P\times_G F\to X$ into a fibre bundle with typical fiber $F$, and the transition functions belonging to the action of $G$ on $F$. We say that  $P\times_G F\to X$ is the __associated bundle__ to $P\to X$ with fiber $F$. 

### In geometric homotopy theory
 {#InGeometricHomotopyTheory}

In the context of [[higher topos theory]] there is an elegant and powerful definition and construction of associated bundles. We discuss here some basics and how this recovers the traditional definition. For more see at _[[associated infinity-bundle]]_ and at _[[geometry of physics -- representations and associated bundles]]_.

At _[[geometry of physics -- principal bundles]]_ in the section _[Smooth principal bundles via smooth groupoids](geometry%20of%20physics%20--%20principal%20bundles#PrincipalBundlesViaSmoothGroupoids)_ is discussed how smooth [[principal bundles]] for a [[Lie group]] $G$ over a [[smooth manifold]] $X$ are equivalently the [[homotopy fibers]] of morphisms of [[smooth groupoids]] ([[smooth stacks]]) of the form

$$
  X \stackrel{}{\longrightarrow} \mathbf{B}G
  \,.
$$

Now given an [[action]] $\rho$ of $G$ on some [[smooth manifold]] $V$, and regarding this action via its [[action groupoid]] projection $p_\rho \colon V//G \to \mathbf{B}G$ as discussed [above](#ActionsOf1Groups), then we may consider these two morphisms into $\mathbf{B}G$ jointly

$$
  \array{
    && V//G
    \\
    && \downarrow^{\mathrlap{p_\rho}}
    \\
    X &\stackrel{g}{\longrightarrow}& \mathbf{B}G
  }
$$

and so it is natural to construct their [[homotopy fiber product]]. 

We now discuss that this is equivalently the [[associated bundle]] which is associated to the principal bundle $P \to X$ via the action $\rho$.

+-- {: .num_prop}
###### Proposition

For $G$ a [[smooth group]] (e.g. a [[Lie group]]), $X$ a [[smooth manifold]], $P \to X$ a smooth $G$-[[principal bundle]] over $X$ and $\rho$ a smooth [[action]] of $G$ on some [[smooth manifold]] $V$, then the [[associated bundle|associated]] $V$-[[fiber bundle]] $P \times_G V\to X$ is equivalently (regarded as a [[smooth groupoid]]) the [[homotopy pullback]] of the [[action groupoid]]-projection $p_\rho \colon V//G \to \mathbf{B}G$ along a morphism $g \colon X\to\mathbf{B}G$ which [[modulating morphism|modulates]] $P$

$$
  \array{
    P\times_G V &\longrightarrow& V//G
    \\
    \downarrow && \downarrow^{\mathrlap{p_\rho}}
    \\
    X &\stackrel{g}{\longrightarrow}& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion at _[[geometry of physics -- principal bundles]]_ in the section _[Smooth principal bundles via smooth groupoids](geometry%20of%20physics%20--%20principal%20bundles#PrincipalBundlesViaSmoothGroupoids)_, the morphism $g$ of smooth groupoids is presented by a morphism of pre-smooth groupoids after choosing an [[open cover]] $\{U_i \to X\}$ over wich $P$ trivialize and choosing a trivialization, by the [[zig-zag]]

$$
  \array{
    C(\{U_i\})_\bullet &\stackrel{g_\bullet}{\longrightarrow}& (\mathbf{B}G)_\bullet
    \\
    \downarrow^{\mathrlap{\simeq_{lwe}}}
    \\
    X
  }
$$

where the top morphism is the [[Cech cohomology|Cech cocycle]] of the given local trivialization regarded as a morphism out of the [[Cech groupoid]] of the given cover.

Moreover, by [this proposition](geometry+of+physics+--+representations+and+associated+bundles#MapFromActionGroupoidOnSetBackToBG) the morphism $(p_\rho)_\bullet$ is a global fibration of pre-smooth groupoids, hence, by the discussion at _[[geometry of physics -- smooth homotopy types]]_, the homotopy pullback in question is equivalently computed as the ordinary pullback of pre-smooth groupoids of $(p_\rho)_\bullet$ along this $g_\bullet$

$$
  \array{
    C(\{U_i\})_\bullet \underset{(\mathbf{B}G)_\bullet}{\times} (V//G)_\bullet &\longrightarrow& (V//G)_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(p_\rho)_\bullet}}
    \\
    C(\{U_i\})_\bullet &\stackrel{g_\bullet}{\longrightarrow}&
    (\mathbf{B}G)_\bullet
    \\
    \downarrow^{\mathrlap{\simeq_{lwe}}}
    \\
    X
  }
  \,.
$$

This pullback is computed componentwise. Hence it is the pre-smooth groupoid whose morphisms are pairs consisting of a morphism $(x,i)\to (x,j)$ in the Cech groupoid as well as a morphism $s \stackrel{g}{\to} \rho(s)(g)$ in the action groupoid, such that the group label $g$ of the latter equals the cocycle $g_{i j}(x)$ of the cocycle on the former. Schematically:

$$
  C(\{U_i\})_\bullet \underset{(\mathbf{B}G)_\bullet}{\times} (V//G)_\bullet
  =
  \left\{
     ((x,i),s) \stackrel{g_{i j}(x)}{\longrightarrow} ((x,j),\rho(s)(g))
  \right\}
  \,.
$$

This means that the pullback groupoid has at most one morphism between every ordered pair of objects. Accordingly this groupoid is [[equivalence of groupoids]] equivalent to the [[quotient]] of its space of objects by the [[equivalence relation]] induced by its morphisms:

$$
  \cdots \simeq
  \left(
    \underset{i}{\coprod} U_i \times V
  \right)/_\sim
  \,.
$$

This is a traditional description of the associated bundle in question.

=--



## Examples

* [[adjoint bundle]]

* [[tractor bundle]]

## Related concepts

* [[associated infinity-bundle]]

[[!redirects associated bundles]]


## References

* [[Norman Steenrod]], _The topology of fibre bundles_, Princeton Mathematical Series __14__, 1951. viii+224 pp. [MR39258](http://www.ams.org/mathscinet-getitem?mr=39258); reprinted 1994 

* [[Dale Husemöller]], _Fibre bundles_, McGraw-Hill 1966 (300 p.); Springer Graduate Texts in Math. __20__, 2nd ed. 1975 (327 p.), 3rd. ed. 1994 (353 p.) 


* [[Glen Bredon]], Section II.2 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN:9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](https://jfdmath.sitehost.iu.edu/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))



[[!redirects associated bundles]]

[[!redirects associated fiber bundle]]
[[!redirects associated fiber bundles]]


