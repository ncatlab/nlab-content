

The lead-in to this entry might be more informative, thinking of readers who really don't know yet.

Maybe something like this:

The [[category]] [[TopSp]] of all [[topological spaces]] serves in the foundations of many subfields of [[mathematics]], as reflected in the widely (but not universally) accepted convention that "space" in [[mathematics]] means "[[topological space]]", by default. However, the great flexibility of the notion of topological spaces also has its drawbacks, as, without further qualification, it tends to be a little too general for usage in any given sub-field.  At the same time, the relevant further conditions typically required on topological spaces in any given application varies, sometimes considerably, and many further such conditions have been and are being introduced. Hence what counts as a well-behaved ("nice") topological spaces strongly depends on context, and the main point to be aware of is the existence of key *classes* of possible extra conditions on topological spaces. 

The foremost among these are certainly the *[[separation axioms]]*, which may be understood as prescribing how exotic (pathological) a topological space is allowed to be, locally, as compared to the archetypical example of *[[Euclidean space]]* (which, it may be good to remember, was the default meaning of "space" for most of human history). In consequence, [[separation conditions]] are typically required of  topological spaces if and to the extent that these are used as models for *space* in the original sense of [[geometry]]. Probably the most prominent among the separation axioms is the [[Hausdorff space|Hausdorff]]-condition "[[T2-space|$T_2$]]", and many authors will by default mean "[[Hausdorff topological space]]" when saying "topological space".

Another class of nicety conditions on topological spaces are not primarily motivated by the look of the individual spaces, but by ensuring that the [[full subcategory]] of spaces satisfying these conditions has good [[category theory|category theoretic]] properties, such as [[cartesian closed category|cartesian closure]].
Such *[[convenient categories of topological spaces]]* are of foundational importance in [[algebraic topology]] where it is tolerable to change the [[homeomorphism]]-type of a space as long as its [[homotopy type]] is retained. Prominent examples of classes of topological spaces which are "nice" in a way that their categories are "convenient", in this sense, are the "[subcategory-generated spaces](convenient+category+of+topological+spaces#CategoriesOfColimitsOfGeneratingSpaces)", namely those that may be obtained as [[colimits]] of a given [[full subcategories]] of building blocks. For example, if these building blocks are taken to be all [[compact spaces]] then one speaks of *[[compactly generated topological spaces]]*, while if they are taken to be all [[Euclidean spaces]] one speaks of [[Delta-generated topological spaces]].

Further in this vein of [[algebraic topology]] and [[homotopy theory]] are conditions on a topological space which ensure that it is a good model for its ([[weak homotopy type|weak]]) [[homotopy type]]. For example, the condition that a topological space be a [[CW-complexes]] (hence  [[cofibrant object|cofibrant]] in the [[classical model structure on topological spaces|classical model structure]]) ensures that [[continuous functions]] out of it model all [[homotopy classes]] of morphisms out of the homotopy type (as witnessed by [[Whitehead's theorem]]), while the condition that a [[topological group]] be *[[well-pointed topological group|well-pointed]]* ensures that the [[geometric realization of simplicial topological spaces|topological realization]] of its [[nerve]] has the expected [[homotopy type]]. It is this last condition which leads over to the notion of [[nice simplicial topological spaces]].





${}^o\searrow_c \swarrow^v$
$\overset{o}{}\searrow\overset{}{c} \swarrow^v$

 $$
    \{x,y\} \hookrightarrow  {X} 
    \;\;\;\,\rightthreetimes\,\;\;\;
     \{\overset{x}\underset{\searrow}\underset{x'}{\swarrow}\overset{X}{}{\searrow}\overset{}{y'}{\swarrow}\overset{\boxed{y}}{}\} 
    \longrightarrow  \{\boxed{x=x'=X=y'=y}\}
   $$


$\boxed{ \overset{ \boxed{ \boxed{u} \;\; \, \,\,\,\, \;\; \boxed{v}} }{ \underset{ c_1 \,\,\, c_2 } { \searrow \;\,\,\,\, \swarrow } } }$

$
  \boxed{
    \overset{
              \boxed{u}\,}{
        \underset{
           \,c
        }
        {
         \,\, \searrow \,\, 
        }
      }
  }  
$


$  \boxed{
    \overset{
      \boxed{
        \boxed{u}
        \;\;
        \,
        
           }
      }{
        \underset{
           c
        }
        {
          \searrow 
        }
      }
  }  
$

$\box$


$\perp$

\begin{prop}
 For $A$ a [[pointed homotopy type]], hence an [[∞-groupoid]] equipped with a base point $\ast \xrightarrow{ pt_A } A$,
then for $n \,\in\, \mathbb{N}$, the [[iterated loop space|n-fold loop space]] of $A$ is the [[homotopy fiber]] of basepoint-[[evaluation map]] on the [[mapping space]] from the [[homotopy type]] of the [[n-sphere]]:
$$
  \Omega^n A
  \xrightarrow{ hofib(ev_{\ast}) }
  Maps
  \big( 
    &#643; S^d 
    ,\,
    A
  \big)
  \xrightarrow{ ev_\ast }
  A
$$
\end{prop}
\begin{proof}
  We may [[presentable (infinity,1)-category]] the sequence in the [[classical model structure on topological spaces]] or the [[classical model structure on simplicial sets]], in the latter case we may assume that $A$  is presented by a [[Kan complex]].

Then the respective canonical model for the [[iterated loop space]] is evidently the ordinary [[1-category]]-theoretic [[fiber]] of the [[evaluation map]] out of the [[internal hom]]:
$$
  \Omega^n A
  \xrightarrow{ ev_\ast }
  Maps( S^d ,\, A )
  \xrightarrow{ ev_\ast }
  A
  \,.
$$
Moreover, the evaluation map is equivalently the image of the point inclusion under the [[internal hom]]-functor
$$
  ev_\ast 
  \;=\;
  Maps( \ast \to S^d ,\, A )
  \,.
$$
Since either model category is a [[Cartesian closed monoidal category|Cartesian closed]] [[monoidal model category|monoidal model]], hence an [[enriched model category]] over itself
and since $\ast \to S^d$ is a [[cofibration]] in either case, 


\end{proof}
Hence the [[homotopy groups]] of the mapping space form a [[long exact sequence]] with thos of $A$, of the following form:
\begin{tikzcd}[column sep=10pt]
    \cdots
    \ar[r]
    &
    \pi_{\bullet + 1}(A)
    \ar[rr]
    &&
    \pi_{\bullet+d}(A)
    \ar[
      rr
    ]
    &&
    \pi_{ \bullet }
    \big(
      \mathrm{Maps}
      ( 
        S^d 
        \,
         A 
      )
    \big)
    \ar[
      rr
    ]
    &&
    \pi_{\bullet}(A)
    \ar[
      rr
    ]
    &&
    \pi_{\bullet + d-1}(A)
    \ar[r]
    &
    \cdots
\end{tikzcd}


