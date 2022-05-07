

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _sphere fiber bundle_ is a [[fiber bundle]] whose [[fibers]] are [[spheres]] $S^n$ of some [[dimension]] $n$.

Often, but not always, this is considered in [[homotopy theory]] or even in [[stable homotopy theory]], hence for [[fibers]] which have the ([[stable homotopy type|stable]]) [[homotopy type]] of a sphere, in which case one speaks of _[[spherical fibrations]]_. See there for more.

## Properties
 {#Properties}

### Vertical tangent bundles of sphere bundles
 {#VerticalTangentBundlesOfSphereBundles}

The following appears in [[schreiber:Twisted Cohomotopy implies M5-brane anomaly cancellation|FSS 20, Sec. 3]] (somewhat implicit in v1, explicitly in v2):

\begin{prop}
  Let 
  \begin{tikzcd}[column sep=tiny]
    S^n \!/\!\!/ O(n+1)
    \ar[d]
    \ar[
      r,
      -,
      shift left=1pt
    ]
    \ar[
      r,
      -,
      shift right=1pt
    ]
    & 
    B O(n)
    \ar[
      d,
      "B i"
    ]
    \\
    B O(n+1)
    \ar[
      r,
      -,
      shift left=1pt
    ]
    \ar[
      r,
      -,
      shift right=1pt
    ]
    &
    B O(n+1)
  \end{tikzcd}
denote the universal $n$-[[spherical fibration]] over the [[classifying space]] of the [[orthogonal group]], where

  \begin{tikzcd}[row sep=0pt]
    O(n) 
    \ar[
      r,
      hook
    ]
    &
    O(n+1)
    \\
    A 
    \ar[
      r,
      phantom,
      "\mapsto"{
        description
      }
    ]
    & 
    \mathrm{diag}(1,A)
  \end{tikzcd}

is the canonical inclusion.

Then its [[homotopy fiber]] inclusion is the classifying map $\vdash Fr(S^n)$ of the orthonormal [[frame bundle]] of the [[n-sphere]]:

\begin{tikzcd}
  S^n
  \ar[
    rr,
    "
     \vdash \mathrm{Fr}(S^n)
    "
  ]
  \ar[d]
  \ar[
    drr,
    phantom,
    "\mbox{\tiny\rm(pb)}"{
      description
    }
  ]
  &&
  B O(n)
  \ar[d]
  \\
  \ast 
  \ar[
    rr
  ]
  &&
  B O(n+1)
\end{tikzcd}

\end{prop}
\begin{proof}
  By the [[pasting law]] we find that the [[homotopy fiber]] of the homotopy fiber inclusion, and hence (by the discssion at [[principal infinity-bundle]]) the total space of the bundle it classifies, is $\Omega B O(n+1) \simeq O(n+1)$:

\begin{tikzcd}
  O(n)
  \ar[
    r,
    hook,
    "i"
  ]
  \ar[d]
  \ar[
    dr,
    phantom,
    "\mbox{\tiny\rm(pb)}"{
      description
    }
  ]
  &
  O(n+1)
  \ar[
    r
  ]
  \ar[
    d
  ]
  \ar[
    dr,
    phantom,
    "\mbox{\tiny\rm(pb)}"{
      description
    }
  ]
  &
  \ast
  \ar[
    d
  ]
  \\
  \ast 
  \ar[r]
  &
  S^n
  \ar[
    r,
    "
     \vdash \mathrm{Fr}(S^n)
    "{
      description
    }
  ]
  \ar[d]
  \ar[
    dr,
    phantom,
    "\mbox{\tiny\rm(pb)}"{
      description
    }
  ]
  &
  B O(n)
  \ar[
    d,
    "B i"
  ]
  \\
  &
  \ast 
  \ar[
    r
  ]
  &
  B O(n+1)
\end{tikzcd}

Moreover, we have an evident [[isomorphism]]

\begin{tikzcd}
  O(n+1)
  \ar[
    out=180-66,
    in=66,
    looseness=3.5,
    "
    \scalebox{.77}{$
      \phantom{\cdot}
      \mathclap{
        O(n)
      }
      \phantom{\cdot}
    $}
    "{
      description
    },
    shift right=1
  ]
  \ar[
    rr,
    "\sim"
  ]
  &&
  \mathrm{Fr}(S^n)
  \ar[
    out=180-66,
    in=66,
    looseness=3.5,
    "
    \scalebox{.77}{$
      \phantom{\cdot}
      \mathclap{
        O(n)
      }
      \phantom{\cdot}
    $}
    "{
      description
    },
    shift right=1
  ]
\end{tikzcd}

given by acting with $O(n+1)$ on the canonical [[orthonormal basis]] $(v_0, v_1, \cdots, v_n)$ of $\mathbb{R}^{n+1}$, regarded as a point $v_0$ on $S^n = S(\mathbb{R}^{n+1})$ equipped with a frame $(v_1, \cdots, v_n)$ of its [[tangent space]] $T_{v_0} S(\mathbb{R}^{n+1})$.

This isomorphism is manifestly $O(n)$-equivariant, and its quotient on both sides is manifestly $S^n$, so that this is actually an isomorphism of $O(n)$-principal bundles.
\end{proof}

In parametrized generalization of this situation, it follows that:

\begin{corollary}\label{OnceStabilizedVerticalTangentBundlesOfSphereBundlesArePulledBackFromBase}
**(once-[[stable tangent bundle|stabilized]] [[vertical tangent bundles]] to [[sphere-fiber bundles]] are [[pullback bundle|pulled back]] from base)**
  Let 
  $
    S(p) \colon S(\mathcal{V}) \to X
  $ 
  be an $n$-[[spherical fibration]], associated to an [[orientation|oriented]] [[real vector bundle]] $p \colon \mathcal{V} \to X$, 
hence fitting into a [[homotopy pullback]]-diagram as shown here:
  \begin{tikzcd}[column sep=small]
    S(\mathcal{V})
    \ar[
      rrr, 
      bend left=15pt,
      "\vdash T_{S(p)} S(\mathcal{V})"
    ]
    \ar[
      rr
    ]
    \ar[
      d,
      "
        S(p)
      "{
        left
      }
    ]
    \ar[
      drr,
      phantom,
      "\mbox{\tiny\rm(pb)}"
    ]
    &
    {\phantom{AA}}
    &
    S^n /\!\!/ O(n+1)
    \ar[
      r,
      -,
      shift left=1pt
    ]
    \ar[
      r,
      -,
      shift right=1pt
    ]
    \ar[d]
    & 
    B O(n)
    \ar[
      dl,
      "
        \;\;
        B i
      "{
        right
      }
    ]
    \\
    X 
    \ar[
      rr,
      "
        \vdash \mathcal{V}
      "{
        above
      }
    ]
    &&
    B O(n+1)
  \end{tikzcd}
Then: 

1. the top map shown classifies the [[vertical tangent bundle]] $T_{S(p)} S(\mathcal{V})$;

1. hence the homotopy-commutativity of the diagram says that the  once-[[stable tangent bundle|stabilized]] vertical tangent bundle is the [[pullback bundle|pullback]] of the original bundle on the base:

   $$
     T_{S(p)}
     S(\mathcal{V})
     \times \mathbb{R}
     \;\simeq_{{}_{X}}\;
     S(p)^\ast 
     \big(
       \mathcal{V}
     \big)
     \,.
   $$

\end{corollary}


### Tangent bundles of sphere bundles

The following generalizes Cor. \ref{OnceStabilizedVerticalTangentBundlesOfSphereBundlesArePulledBackFromBase} to the full [[tangent bundle]] of sphere-fiber bundles, now assuming that the base is a [[smooth manifold]] and giving a more traditional [[differential geometry|differential-geometric]] [[proof]] (
the statement appears without proof as [Crowley-Escher 03, Fact. 3.1](#CrowleyEscher03), apparently reading between the lines in [Milnor 56, p. 403](#Milnor1956)):

\begin{prop}\label{StableTangentBundleOfUnitSphereBundle}
**([[stable tangent bundle]] of [[unit sphere bundle]])** \linebreak
  The once-[[stable tangent bundle|stabilized]] [[tangent bundle]] of a [[unit sphere bundle]] $S(\mathcal{V})$ in a [[real vector bundle]] $\mathcal{V} \overset{p}{\longrightarrow} M$ (Example \ref{UnitSphereBundles}) over a [[smooth manifold]] $M$ is [[isomorphism|isomorphic]] to the [[pullback bundle|pullback]]  of the [[direct sum of vector bundles|direct sum]] of the [[stable tangent bundle]] of the base manifold with that vector bundle:

$$
  T S(\mathcal{V}) \times \mathbb{R}
  \;
  \simeq
  \;
  S(p)^\ast
  \big(
    T M 
    \oplus_M
    \mathcal{V}
  \big)
  \,.
$$
\end{prop}

\begin{proof}\label{ProofOfStableTangentBundleOfUnitSphereBundle}
  Consider first the actual [[tangent bundle]] but to the [[open ball]]/[[disk]]-[[fiber bundle]] $D(\mathcal{V})$ that fills the given sphere-fiber bundle: By the standard splitting ([this Prop.](vertical+vector+field#SplittingOfTotalSpaceTangentBundle)) this is the [[direct sum of vector bundles|direct sum]]

$$
  T 
  \big(
   D(\mathcal{V})
  \big)
  \;\simeq\;
  \big(
     D(p)^\ast T M
  \big)
  \oplus_M
  T_p D(\mathcal{V})
  \,,
$$

where $T_p D(\mathcal{V})$ is the [[vertical tangent bundle]] of the disk bundle. But, by definition of disk bundles, this is the restriction of the vertical tangent bundle of the vector bundle $\mathcal{V}$ itself, and that is just the pullback of that vector bundle along itself (by [this Example](vertical+vector+field#SplittingOfTotalSpaceTangentBundle)):

$$
  \begin{aligned}
  \cdots
  & 
  \simeq\;
  \big(
    D(p)^\ast T M
  \big)
  \oplus_M
  \big(
    D(p)^\ast \mathcal{V}
  \big)
  \\
  & \simeq\;
  D(p)^\ast
  \big(
    T M \oplus_M \mathcal{V}
  \big)
  \,.
  \end{aligned}
$$

To conclude, it just remains to observe that the [[normal bundle]] of the [[n-sphere]]-boundary inside the $(n+1)$-ball is manifestly [[trivial bundle|trivial]], so that the restriction of the tangent bundle of $D(\mathcal{V})$ to $S(\mathcal{V})$ is the [[stable tangent bundle]] of $S(\mathcal{V})$.
\end{proof}


## Examples

### Unit sphere bundles

\begin{example}\label{UnitSphereBundles}
A key example of sphere fiber bundles are the _unit sphere bundles_ inside of [[real vector bundles]] that are equipped with [[orthogonal structure]]: the bundles whose [[fibers]] are the [[unit spheres]] in the corresponding fiber of the given [[real vector bundle]].
\end{example}


These appear in the discussion of [[Thom spaces]] and hence of [[Thom spectra]], as well as in the discussion of [[wave front sets]].


## Related concepts

* [[Sullivan model of a spherical fibration]]

## References

With focus on [[3-sphere]]-fiber bundles over the [[4-sphere]] and the construction of [[exotic 7-spheres]]:

* {#Milnor1956} [[John Milnor]], _On manifolds homeomorphic to the 7-sphere_, Annals of Mathematics 64 (2): 399&#8211;405 (1956) ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/exotic.pdf), [doi:10.1142/9789812836878_0001](https://doi.org/10.1142/9789812836878_0001))

* {#CrowleyEscher03} [[Diarmuid Crowley]], [[Christine Escher]], _A classification of $S^3$-bundles over $S^4$_, Differential Geometry and its Applications Volume 18, Issue 3, May 2003, Pages 363-380 (<a href="https://doi.org/10.1016/S0926-2245(03)00012-3">doi:10.1016/S0926-2245(03)00012-3</a>))


[[!redirects sphere fiber bundles]]

[[!redirects sphere bundle]]
[[!redirects sphere bundles]]


[[!redirects unit sphere fiber bundle]]
[[!redirects unit sphere fiber bundles]]

[[!redirects sphere-fiber bundle]]
[[!redirects sphere-fiber bundles]]

[[!redirects unit sphere bundle]]
[[!redirects unit sphere bundles]]
