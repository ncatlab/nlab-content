
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $X$ any kind of [[space]] (possibly a [[directed space]], hence a [[category]]) its [[loop space object]]s $\Omega_x X$ canonically inherit a [[monoidal category|monoidal structure]], coming from composition of loops. 

If $x \in X$ is essentially unique, then $\Omega_x X$ equipped with this monoidal structure remembers all of the structure of $X$: we say $X \simeq B \Omega_x X$ and call $B A$ the _[[delooping]]_ of the monoidal object $A$.

## Examples

### For topological spaces and $\infty$-groupoids

There is an [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd_* 
    \stackrel{\overset{B}{\leftarrow}}{\underset{\Omega}{\to}}
  \infty Group
$$

between [[pointed object|pointed]] [[∞-groupoid]]s and [[∞-group]]s, where $\Omega$ forms [[loop space object]]s.

This is [[presentable (∞,1)-category|presented]] by a [[Quillen equivalence]] of [[model categories]]

$$
  sSet_* 
    \stackrel{\overset{\bar W}{\leftarrow}}{\underset{G}{\to}}
  sGrp  
$$

between the [[model structure on reduced simplicial sets]] and the [[transferred model structure]] on [[simplicial group]]s along the [[forgetful functor]] to the [[model structure on simplicial sets]].

(See [[groupoid object in an (infinity,1)-category]] for more details on this Quillen equivalence.)


### For parameterized $\infty$-groupoids ($\infty$-stacks / $(\infty,1)$-sheaves)

The following result makes precise for _parameterized [[∞-groupoid]]s_  -- for [[∞-stack]]s -- the general statement that $k$-fold [[delooping]] provides a correspondence betwen [[n-category|n-categories]] that have trivial [[k-morphism|r-morphism]]s for $r \lt k$ and  [[k-tuply monoidal n-category|k-tuply monoidal n-categories]].

+-- {: .un_theorem}
###### Theorem (k-tuply monoidal $\infty$-stacks)

Let $k \gt 0$, let $\mathcal{X}$ be an [[∞-stack]] [[(∞,1)-topos]] and let $\mathcal{X}_*^{\geq k}$ denote the [[full subcategory]] of the category $\mathcal{X}_{*}$ of pointed objects, spanned by those pointed objects thar are $k-1$-[[connected]] (i.e. their first $k$ [[homotopy groups in an (∞,1)-topos|∞-stack homotopy groups]]) vanish. Then there is a canonical equivalence of [[(∞,1)-category|(∞,1)-categories]]

$$
  \mathcal{X}_*^{\geq k} \simeq Mon^{gp}_{\mathbb{E}[k]}(\mathcal{X}) \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Ek-Algebras|EKAlg, theorem 1.3.6.]].

=--

Specifically for $\mathcal{X} = Top$, this reduces to the classical theorem by [[Peter May]]

+-- {: .un_theorem}
###### Theorem (May recognition theorem)

Let $Y$ be a [[topological space]] equipped with an action of the [[little cubes operad]] $\mathcal{C}_k$ and suppose that $X$ is grouplike. Then $Y$ is homotopy equivalent to a $k$-fold loop space $\Omega^k X$ for some pointed topological space $X$.

=--

+-- {: .proof}
###### Proof

This is [[Ek-Algebras|EkAlg, theorem 1.3.16.]]

=--


### For $(\infty,n)$-categories

See [[delooping hypothesis]].

## Relation to looping and suspension

For $A$ any monoidal [[space]], we may [[forgetful functor|forget]] its monoidal structure and just remember the underlying [[space]].  The formation of [[loop space object]]s composed with this [[forgetful functor]] has a [[left adjoint]] $\Sigma$ which forms _[[suspension objects]]_ .

## Related concepts

* [[loop space object]], [[free loop space object]],

  * [[delooping]], **looping and delooping**

  * [[loop space]], [[free loop space]], [[derived loop space]]

* [[suspension object]]

  * [[suspension]], [[reduced suspension]]


