
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $X$ any kind of [[space]] (or possibly a [[directed space]], viewed as some sort of [[category]] or higher dimensional analogue of one), its [[loop space object]]s $\Omega_x X$ canonically inherit a [[monoidal category|monoidal structure]], coming from concatenation of [[loops]].

If $x \in X$ is essentially unique, then $\Omega_x X$ equipped with this monoidal structure remembers all of the structure of $X$: we say $X \simeq B \Omega_x X$ call $B A$ the _[[delooping]]_ of the monoidal object $A$.

What all these terms ("loops" $\Omega$, "delooping" $B$ etc.) mean in detail and how they are _presented_ concretely depends on the given setup. We discuss some of these below in the section [Examples](#Examples).


## Examples
 {#Examples}

### For topological spaces and $\infty$-groupoids

There is an [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd_* 
    \stackrel{\overset{B}{\leftarrow}}{\underset{\Omega}{\to}}
  \infty Group
$$

between [[pointed object|pointed]] [[connected]] [[∞-groupoid]]s and [[∞-group]]s, where $\Omega$ forms [[loop space object]]s.

This is [[presentable (∞,1)-category|presented]] by a [[Quillen equivalence]] of [[model categories]]

$$
  sSet_* 
    \stackrel{\overset{\bar W}{\leftarrow}}{\underset{G}{\to}}
  sGrp  
$$

between the [[model structure on reduced simplicial sets]] and the [[transferred model structure]] on [[simplicial group]]s along the [[forgetful functor]] to the [[model structure on simplicial sets]].

(See [[groupoid object in an (infinity,1)-category]] for more details on this Quillen equivalence.)


### For parameterized $\infty$-groupoids ($\infty$-stacks / $(\infty,1)$-sheaves)

The following result makes precise for _parameterized [[∞-groupoid]]s_  -- for [[∞-stack]]s -- the general statement that $k$-fold [[delooping]] provides a correspondence between [[n-category|n-categories]] that have trivial [[k-morphism|r-morphism]]s for $r \lt k$ and  [[k-tuply monoidal n-category|k-tuply monoidal n-categories]].

+-- {: .num_defn}
###### Definition

An [[Ek-algebra]] object $A$ in an [[(∞,1)-topos]] $\mathbf{H}$ is called **groupal** if its [[homotopy groups in an (∞,1)-topos|connected components]] $\pi_0(A) \in \mathbf{H}_{\leq 0}$ is a [[group object]].

Write $Mon^{gp}_{\mathbb{E}[k]}(\mathbf{H})$ for the [[(∞,1)-category]] of groupal $E_k$-algebra objects in $\mathbf{H}$.

A groupal $E_1$-algebra -- hence an groupal [[A-∞ algebra]] object in $\mathbf{H}$ -- we call an _[[∞-group]]_ in $\mathbf{H}$. Write $\infty Grp(\mathbf{H})$ for the [[(∞,1)-category]] of [[∞-group]]s in $\mathbf{H}$.

=--

+-- {: .num_theorem}
###### Theorem (k-tuply monoidal $\infty$-stacks)

Let $k \gt 0$, let $\mathbf{H}$ be an [[(∞,1)-category of (∞,1)-sheaves]] and let $\mathbf{H}_*^{\geq k}$ denote the [[full subcategory]] of the category $\mathbf{H}_{*}$ of [[pointed objects]], spanned by those pointed objects thar are $k-1$-[[connected]] (i.e. their first $k$ [[homotopy groups in an (∞,1)-topos|homotopy sheaves]]) vanish. Then there is a canonical equivalence of [[(∞,1)-category|(∞,1)-categories]]

$$
  \mathbf{H}_*^{\geq k} \simeq Mon^{gp}_{\mathbb{E}[k]}(\mathbf{H}) \,.
$$

between the $(k-1)$-[[connected]] pointed objects and the groupal [[Ek-algebra]] objects in $\mathbf{H}$.

=--

This is ([Lurie, Higher Algebra, theorem 5.1.3.6](#LurieAlgebra)).


Specifically for $\mathbf{H} = $ [[Top]], this reduces to the classical theorem by [[Peter May]]

+-- {: .num_theorem}
###### Theorem (May recognition theorem)

Let $Y$ be a [[topological space]] equipped with an action of the [[little cubes operad]] $\mathcal{C}_k$ and suppose that $Y$ is grouplike. Then $Y$ is homotopy equivalent to a $k$-fold loop space $\Omega^k X$ for some pointed topological space $X$.

=--

This is [[Ek-Algebras|EkAlg, theorem 1.3.16.]]

+-- {: .num_remark #LoopingDeloopingDegree1InTopos}
###### Remark

For $k = 1$ we have a looping/delooping equivalence

$$
  \mathbf{H}_*
   \stackrel{\overset{\mathbf{B}}{\leftarrow}}{\underset{\Omega}{\to}}
  \infty Grpd(\mathbf{H})
$$

between pointed connected objects in $\mathbf{H}$ and grouplike [[A-∞ algebra]] objects in $\mathbf{H}$: [[∞-group]] objects in $\mathbf{H}$.

=--

+-- {: .num_remark}
###### Remark

If the ambient [[(∞,1)-topos]] has [[homotopy dimension]] 0 then every connected object $E$ admits a point $* \to E$. Still, the [[(∞,1)-category]] of pointed connected objects differs from that of unpointed connected objects (because in the latter the [[natural transformation]]s may have nontrivial components on the point, while in the former case they may not).

The connected objects $E$ which fail to be [[∞-group]]s by failing to admit a point are of interest: these are the _[[∞-gerbes]]_ in the [[(∞,1)-topos]].

=--

### For cohesive $\infty$-groupoids

A special case of the parameterized $\infty$-groupoids above are [[cohesive ∞-groupoid]]s. Looping and delooping for these is discussed at
[[cohesive (∞,1)-topos -- structures]] in the section <a href="http://www.ncatlab.org/nlab/show/cohesive%20%28infinity,1%29-topos%20--%20structures#InfinGroups">Cohesive ∞-groups</a>.

### For $(\infty,n)$-categories

See [[delooping hypothesis]].

## Relation to looping and suspension

For $A$ any monoidal [[space]], we may [[forgetful functor|forget]] its monoidal structure and just remember the underlying [[space]].  The formation of [[loop space object]]s composed with this [[forgetful functor]] has a [[left adjoint]] $\Sigma$ which forms _[[suspension objects]]_.


## Related concepts

* [[loop space object]], [[free loop space object]],

  * [[delooping]], **looping and delooping**

  * [[loop space]], [[free loop space]], [[derived loop space]]

* [[suspension object]]

  * [[suspension]], [[reduced suspension]]

[[!include k-monoidal table]]

## References

Section 6.1.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Section 5.1.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#LurieAlgebra}


[[!redirects looping]]
[[!redirects looping and delooping]]
