
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $\{U_i \to X\}$ a [[cover]] of a [[space]] $X$, the corresponding **&#268;ech groupoid** is the [[internal groupoid]]

$$
  C(\{U_i\}) = (\coprod_{i j} U_i \cap U_j \rightrightarrows \coprod_i U_i)
$$

whose set of objects is the [[disjoint union]] $\coprod_i U_i$ of the covering patches, and the set of morphisms is the disjoint union of the [[intersections]] $U_i \cap U_j$ of these patches.

This is the $2$-[[coskeleton]] of the full [[Čech nerve]]. See there for more details.

If we speak about [[generalized element|generalized points]] of the $U_i$ (which are often just ordinary points, in applications), then 

* an [[object]] of $C(\{U_i\})$ is a pair $(x,i)$ where $x$ is a point in $U_i$;

* there is a unique [[morphism]] $(x,i) \to (x,j)$ for all pairs of objects labeled by the same $x$ such that $x \in U_i \cap U_j$;

* hence the composition of morphism is of the form

  $$
    \array{
       && (x,j)
       \\
       & \nearrow &=& \searrow
       \\
      (x,i) &&\to&& (x,k)
    }
    \,.
  $$

## Definition
 {#Definition}



+-- {: .num_defn #CechGroupoid}
###### Definition
**(Cech groupoid)**

Let $\mathcal{C}$ be a [[site]], and $X \in \mathcal{C}$ an [[object]] of that site. For each [[covering]] family $\{ U_i \overset{\iota_i}{\to} X\}$ of $X$ in the given [[coverage]], the _[[Cech groupoid]]_ is the [[presheaf of groupoids]]

$$
  C(\{U_i\}) 
    \;\in\; 
  [\mathcal{C}^{op}, Grpd]
  \;\simeq\;
  Grpd\left( [\mathcal{C}^{op}, Set]  \right)
$$

which, regarded as an [[internal category]] in the [[category of presheaves]] over $\mathcal{C}$, has as [[presheaf]] of [[objects]] the [[coproduct]]

$$
  Obj_{C(\{U_i\})} \;\coloneqq\; \underset{i}{\coprod}  y(U_i)
$$

of the [[representable presheaf|presheaves represented]] (under the [[Yoneda embedding]]) by the [[covering]] objects $U_i$, and as [[presheaf]] of [[morphisms]] the [[coproduct]] over all [[fiber products]] of these:

$$
  Mor_{C(\{U_i\})} 
    \;\coloneqq\; 
  \underset{i,j}{\coprod}  y(U_i) \times_{y(X)} y(U_j)
  \,.
$$

This means that for any $V \in \mathcal{C}$ the [[groupoid]] assigned by $C(\{U_i\})$ has as set of objects [[pairs]] consisting of an index $i$ and a morphism $V \overset{\kappa_i}{\to} U_i$ in $\mathcal{C}$, and there is a unique morphism between two such objects 

$$
  \kappa_i \longrightarrow \kappa_j
$$

precisely if 

\[
  \label{CechMatchingCondition}
  \iota_i \circ \kappa_i
  \;=\;
  \iota_j \circ \kappa_j
  \phantom{AAAAAAAA}
  \array{
    && V
    \\
    & {}^{\mathllap{\kappa_i}}\swarrow && \searrow^{\mathrlap{\kappa_j}}
    \\
    U_i && && U_j
    \\
    & {}_{\mathllap{\iota_i}}\searrow && \swarrow_{\mathrlap{\iota_j}}
    \\
    && X
  }
\]


=--

## Properties

### Codescent
 {#Codescent}

We discuss (Prop. \ref{CechGroupoidCoRepresents} below) how the Cech groupoid co-represents _[[matching families]]_ as they appear in the definition of [[sheaves]]. 

For reference, we first recall that definition:

+-- {: .num_defn #CompatibleElements}
###### Definition
**([[matching family]] -- [[descent object]])**

Let $\mathcal{C}$ be a [[small category]] equipped with a [[coverage]], hence a [[site]] and consider a [[presheaf]] $\mathbf{Y} \in [\mathcal{C}^{op}, Set]$ (Example \ref{CategoryOfPresheaves}) over $\mathcal{C}$.

Given an [[object]] $X \in \mathcal{C}$ and a [[covering]] $\left\{ U_i \overset{\iota_i}{\to} X \right\}_{i \in I}$ of it  we say that a _[[matching family]]_ (of probes of $\mathbf{Y}$) is a [[tuple]] $(\phi_i \in \mathbf{Y}(U_i))_{i \in I}$ such that for all $i,j \in I$ and [[pairs]] of [[morphisms]] $U_i \overset{\kappa_i}{\leftarrow} V \overset{\kappa_j}{\to} U_j$ satisfying

\[
  \label{MatchingCondition}
  \iota_i \circ \kappa_i
  \;=\;
  \iota_j \circ \kappa_j
  \phantom{AAAAAAAA}
  \array{
    && V
    \\
    & {}^{\mathllap{\kappa_i}}\swarrow && \searrow^{\mathrlap{\kappa_j}}
    \\
    U_i && && U_j
    \\
    & {}_{\mathllap{\iota_i}}\searrow && \swarrow_{\mathrlap{\iota_j}}
    \\
    && X
  }
\]

we have 

\[
  \label{GluingCondition}
  \mathbf{Y}(\kappa_i)(\phi_i)
  \;=\;
  \mathbf{Y}(\kappa_j)(\phi_j)
  \,.
\]

We write

\[
  \label{SetOfMatching}
  Match\big( 
    \{U_i\}_{i \in I}
    \,,\,
    \mathbf{Y}
  \big)
  \subset
  \underset{i}{\prod} \mathbf{Y}(U_i)
  \;\in\;
  Set
\]

for the set of [[matching families]] for the given presheaf and covering. 

This is also called the _[[descent object]]_ of $\mathbf{Y}$ for _[[descent]]_ along the [[covering]] $\{U_i \overset{\iota_i}{\to}X\}$.

=--


+-- {: .num_example #CechGroupoidCoRepresents}
###### Proposition
**([[Cech groupoid]] co-represents [[matching families]] -- [[codescent]])**

For [[Grpd]] regarded as a [[cosmos]] for [[enriched category theory]], via its [[cartesian closed category]]-structure, and $\mathcal{C}$ a [[site]], let

$$
  \mathbf{Y} \in [\mathcal{C}^{op}, Set] \hookrightarrow [\mathcal{C}^{op}, Grpd]
$$

be a [[presheaf]] on $\mathcal{C}$, regarded as a [[Grpd]]-[[enriched presheaf]], let $X \in \mathcal{C}$ be any [[object]] and $\{U_i \overset{\iota_i}{\to} X\}_i$ a [[covering]] family with induced [[Cech groupoid]] $C(\{U_i\}_i)$ (Def.\ref{CechGroupoid}).

Then there is an [[isomorphism]]

$$
  [\mathcal{C}^{op},Grpd]
  \left(
    C\left(\{U_i\}_i\right), \, \mathbf{Y}
  \right)
  \;\simeq\;
  Match\left( \{U_i\}_i, \, \mathbf{Y} \right)
$$

between the [[hom-object|hom-groupoid]] of [[Grpd]]-[[enriched presheaves]]  and the set of [[matching families]] (Def. \ref{CompatibleElements}).

Since therefore the Cech-groupoid co-represents the [[descent object]], it is sometimes called the _[[codescent object]]_ along the given covering.

Moreover, under this identification the canonical morphism $C\left( \{U_i\}_i \right) \overset{p_{\{U_i\}_i}}{\longrightarrow} X$ induces the comparison morphism

$$
  \array{    
    [\mathcal{C}^{op}, Grpd]\left( X, \, \mathbf{Y} \right)
    & \simeq &
    \mathbf{Y}(X) 
    \\
    {}^{
      \mathllap{
        [\mathcal{C}^{op}, Grpd](p_{\{U_i\}_i}, \mathbf{Y})
      }
    }\downarrow && \downarrow
    \\
    [\mathcal{C}^{op},Grpd]
    \left(
      C\left(\{U_i\}_i\right), \, \mathbf{Y}
    \right)
    &\simeq&
    Match\left( \{U_i\}_i, \, \mathbf{Y} \right)
  }
  \,.
$$

In conclusion, this means that the [[presheaf]] $\mathbf{Y}$ is a [[sheaf]] (Def. \ref{Sheaf}) precisely if homming Cech groupoid projections into it produces an isomorphism.

=--

+-- {: .proof}
###### Proof

The hom-groupoid is computed as the [[end]]

$$
  [\mathcal{C}^{op},Grpd]
  \left(
    C\left(\{U_i\}_i\right), \, \mathbf{Y}
  \right)
  \;=\;
  \int_{V \in \mathcal{C}}
  \left[
    C\left(\{U_i\}_i\right)(V), \, \mathbf{Y}(V)
  \right]
  \,,
$$ 

where the "integrand" is the [[functor category]] (here: a [[groupoid]]) from the [[Cech groupoid]] at a given $V$ to the set (regarded as a groupoid) assigned by $\mathbf{Y}$ to $V$.

Since $\mathbf{Y}(V)$ is just a set, that functor groupoid, too, is just a set, regarded as a groupoid. Its elements are the [[functors]] $C\left(\{U_i\}_i\right)(V) \longrightarrow \mathbf{Y}(V)$, which are equivalently those  [[functions]] on sets of objects

$$
  \underset{i}{\coprod} y(U_i)(V)
  =
  Obj_{C\left(\{U_i\}_i\right)(V)} 
    \longrightarrow 
  Obj_{\mathbf{Y}(V)}
  =
  \mathbf{Y}(V)
$$

which respect the [[equivalence relation]] induced by the morphisms in the Cech groupoid at $V$. 

Hence the hom-groupoid is a subset of the [[end]] of these [[function sets]]:

$$
  \begin{aligned}
    \int_{V \in \mathcal{C}}
    \left[
      C\left(\{U_i\}_i\right)(V), \, \mathbf{Y}(V)
    \right]
    & \hookrightarrow
    \int_{V \in \mathcal{C}}
    \left[
      \underset{i}{\coprod} y(U_i)(V), \, \mathbf{Y}(V)
    \right]
    \\
    & \simeq
    \int_{V \in \mathcal{C}}
    \underset{i}{\prod}
    \left[
       y(U_i)(V), \, \mathbf{Y}(V)
    \right]
    \\
    & \simeq
    \underset{i}{\prod}
    \int_{V \in \mathcal{C}}
    \left[
       y(U_i)(V), \, \mathbf{Y}(V)
    \right]
    \\
    & \simeq
    \underset{i}{\prod}
    \mathbf{Y}(U_i)
  \end{aligned}
$$

Here we used: first that the [[internal hom]]-functor turns colimits in its first argument into limits (see at _[[internal hom-functor preserves limits]]_), then that [[limits commute with limits]], hence that in particular [[ends]] commute with [[products]] , and finally the [[enriched Yoneda lemma]], which here comes down to just the plain [[Yoneda lemma]] . The end result is hence the same [[Cartesian product]] set that also the set of matching families is defined to be a subset of, in (eq:SetOfMatching).

This shows that an element in 
$ \int_{V \in \mathcal{C}}
    \left[
      C\left(\{U_i\}_i\right)(V), \, \mathbf{Y}(V)
    \right]
$ is a [[tuple]] $(\phi_i \in \mathbf{Y}(U_i))_i$, subject to some condition. This condition is that for each $V \in \mathcal{C}$ the assignment 

$$
  \array{
    C\left(\{U_i\}_i\right)(V) 
      & \longrightarrow & 
    \mathbf{Y}(V)
    \\
    (V \overset{\kappa_i}{\to} U_i)
    &\mapsto&
    \kappa_i^\ast \phi_i
    =
    \mathbf{Y}(\kappa_i)(\phi_i)
  }
$$

constitutes a [[functor]] of [[groupoids]].

By definition of the [[Cech groupoid]], and since the [[codomain]] is a just [[set]] regarded as a [[groupoid]], this is the case precisely if

$$
  \mathbf{Y}(\kappa_i)(\phi_i)
  \;=\;
  \mathbf{Y}(\kappa_j)(\phi_j)
  \phantom{AAAA}
  \text{for all}\, i,j
  \,,
$$

which is exactly the condition (eq:GluingCondition) that makes $(\phi_i)_i$ a matching family.

=--

## Examples

For $X$ a [[smooth manifold]] and $\{U_i \to X\}$ an [[atlas]] by [[coordinate chart]]s, the &#268;ech groupoid is a [[Lie groupoid]] which is equivalent to $X$ as a Lie groupoid:
$C(\{U_i\}) \stackrel{\simeq}{\to} X$

For $\mathbf{B}G$ the Lie groupoid with one object coming from a [[Lie group]] $G$ morphisms of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
$$

are also called [[anafunctor]]s from $X$ to $\mathbf{B}G$. They correspond to smooth $G$-[[principal bundle]]s on $X$.

## Related concepts

* [[Cech nerve]]

## References

For instance 

* {#Jardine06} [[J. F. Jardine]], Example 5 in: _Homotopy classification of gerbes_ ([arXiv:math/0605200](https://arxiv.org/abs/math/0605200))

[[!redirects Cech groupoid]]
[[!redirects Cech groupoids]]
[[!redirects Čech groupoids]]
