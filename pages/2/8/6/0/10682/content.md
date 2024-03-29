
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Urysohn's lemma_ (prop. \ref{UrysohnLemma} below) states that on a [[normal topological space]] disjoint [[closed subsets]] may be separated by [[continuous functions]] in the sense that a continuous function exists which takes value 0 on one of the two subsets and value 1 on the other (called an "Urysohn function", def. \ref{UrysohnFunction}) below. In fact the  existence of such functions is equivalent to a space being normal (remark \ref{Equivalence} below).

Urysohn's lemma is a key ingredient for instance in the proof of the [[Tietze extension theorem]] and in the proof of the existence of [[partitions of unity]] on [[paracompact topological spaces]].  See the list of implications [below](#Implications).

## Statement

+-- {: .num_defn #UrysohnFunction}
###### Definition
**(Urysohn function)**

Let $X$ be a [[topological space]], and let $A,B \subset X$ be disjoint [[closed subsets]]. Then an _Urysohn function_ for this situation is 

* a [[continuous function]] $f \colon X \to [0,1]$

to the [[closed interval]] equipped with its [[Euclidean space|Euclidean]] [[metric topology]], such that 

* it takes the value 0 on $A$ and the value 1 on $B$:

  $$
    f(A) = \{0\}
    \phantom{AAA}
    \text{and}
    \phantom{AAA}
    f(B) = \{1\}
    \,.
  $$ 

=--



+-- {: .num_prop #UrysohnLemma} 
###### Proposition
**(Urysohn's lemma)**

Assuming [[excluded middle]] then:

Let $X$ be a [[normal topological space|normal]] (or $T_4$) [[topological space]], and let $A,B \subset X$ be two disjoint [[closed subsets]] of $X$. Then there exists an Urysohn function (def. \ref{UrysohnFunction}).


=-- 

+-- {: .num_remark}
###### Remark

Beware that the function in prop. \ref{UrysohnLemma} may take the values 0 or 1 even outside of the two subsets. The condition that the function takes value 0 or 1, respectively, _precisely_ on the two subsets corresponds to _[[perfectly normal spaces]]_.

=--

+-- {: .num_remark #Equivalence}
###### Remark

It is immediate that, conversely, the existence of an Urysohn function (def. \ref{UrysohnFunction}) implies that the topological space is [[normal topological space|normal]]. For let $A, B \subset X$ be disjoint closed subsets, and consider a continuous function $f \colon X \to [0,1]$ with $f(A) = \{0\}$ and $f(B) = \{1\}$ then 

$$
  U_A \coloneqq f^{-1}([0,1/3)
  \phantom{AAA}
  U_B \coloneqq f^{-1}((2/3,1])
$$

are disjoint open neighbourhoods of these subsets. 

Hence Urysohn's lemma shows that a topological space being normal is _equivalent_ to it admitting Urysohn functions.

=--

## Proof
 {#Proof}

+-- {: .proof}
###### Proof
of Urysohn's lemma, prop. \ref{UrysohnLemma}


Set

$$
  C_0 \coloneqq A
  \phantom{AAA}
  U_1 \coloneqq X \backslash B
  \,.
$$

Since by assumption

$$
  A \cap B = \emptyset
  \,.
$$

we have 

$$
  C_0 \subset U_1
  \,.
$$

Notice that (by [this lemma](separation+axioms#T4InTermsOfTopologicalClosures)) if a space is normal then every open neighbourhood $U \supset C$ of a closed subset $C$ contains a smaller neighbourhood $V$ together with its closure $Cl(V)$

$$
  C \subset V \subset Cl(V) \subset U
  \,.
$$

Apply this fact successively to the above situation to obtain the following infinite sequence of nested open subsets $U_r$ and closed subsets $C_r$

$$
  \array{
    C_0 &&  &&  &&  &\subset&  &&  &&  && U_1
    \\
    C_0 &&  &\subset&  && U_{1/2} &\subset& C_{1/2} &&  &\subset&  && U_1
    \\
    C_0 &\subset& U_{1/4} &\subset& C_{1/4} &\subset& U_{1/2} &\subset& C_{1/2} &\subset& U_{3/4} &\subset& C_{3/4} &\subset& U_1
  }
$$

and so on, labeled by the [[dyadic rational numbers]] $\mathbb{Q}_{dy} \subset \mathbb{Q}$ within $(0,1]$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/UrysohnConstruction.png" width="400">
</div>


$$
 \{ U_{r} \subset X \}_{r \in (0,1] \cap \mathbb{Q}_{dy}}
$$

with the property 

$$
  \underset{r_1,r_2 \in (0,1] \cap \mathbb{Q}_{dy}}{\forall}
  \left(
    \left(
       r_1 \lt r_2
    \right)
     \Rightarrow
    \left(
      U_{r_1} \subset Cl(U_{r_1}) \subset U_{r_2}
    \right)
  \right)
  \,.
$$

Define then the function

$$
  f \;\colon\; X \longrightarrow [0,1]
$$

to assign to a point $x \in X$ the [[infimum]] of the labels of those open subsets in this sequence that contain $x$:

$$
  f(x) 
     \coloneqq
  \underset{U_r \supset \{x\}}{\lim} r
$$

Here the [[limit of a net|limit]] is over the [[directed set]] of those $U_r$ that contain $x$, ordered by reverse inclusion.


This function clearly has the property that $f(A) = \{0\}$  and $f(B) = \{1\}$. It only remains to see that it is continuous.

To this end, first observe that 

$$
  \array{
    (\star)
    &&
    \left( 
      x \in Cl(U_r) 
    \right)
      &\Rightarrow&
    \left(
       f(x) \leq r
    \right)
    \\
    (\star\star)
    &&
    \left(
      x \in U_r
    \right)
      &\Leftarrow&    
    \left(
      f(x) \lt r
    \right)
  }
  \,.
$$

Here it is immediate from the definition that $(x \in U_r) \Rightarrow (f(x) \leq r)$ and that $(f(x) \lt r) \Rightarrow (x \in U_r \subset Cl(U_r))$. For the remaining implication, it is sufficient to observe that
 
$$
  (x \in \partial U_r) \Rightarrow (f(x) = r)
  \,,
$$

where $\partial U_r \coloneqq Cl(U_r) \backslash U_r$ is the [[boundary]] of $U_r$.

This holds because the [[dyadic numbers]] are [[dense subset|dense]] in $\mathbb{R}$. (And this would fail if we stopped the above decomposition into $U_{a/2^n}$-s at some finite $n$.) Namely, in one direction, if $x \in \partial U_r$ then for every small positive real number $\epsilon$ there exists a dyadic rational number $r'$ with $r \lt r' \lt r + \epsilon$, and by construction $U_{r'} \supset Cl(U_r)$ hence  $x \in U_{r'}$. This implies that $\underset{U_r \supset \{x\}}{\lim} = r$.


{#PreimagesOfTheSubbaseOpens} Now we claim that for all $\alpha \in [0,1]$ then

1. $f^{-1}(\,(\alpha, 1]\,) = \underset{r \gt \alpha}{\cup} \left( X \backslash Cl(U_r) \right)$

1. $f^{-1}(\,[0,\alpha)\,) = \underset{r \lt \alpha}{\cup} U_r$

Thereby $f^{-1}(\,(\alpha, 1]\,)$ and $f^{-1}(\,[0,\alpha)\,)$ are exhibited as unions of open subsets, and hence they are open.


Regarding the first point: 

$$
  \begin{aligned}
     & x \in f^{-1}( \,(\alpha,1]\, )
     \\
     \Leftrightarrow\,
     & 
     f(x) \gt \alpha
     \\
     \Leftrightarrow\,
     &
     \underset{r \gt \alpha}{\exists} (f(x) \gt r)
     \\
     \overset{(\star)}{\Rightarrow}\,
     &
     \underset{r \gt \alpha}{\exists}
     \left( x \notin Cl(U_r) \right)
     \\
     \Leftrightarrow\,
     &
     x  \in \underset{r \gt \alpha}{\cup} \left(X \backslash Cl(U_r)\right)
  \end{aligned}
$$

and 

$$
  \begin{aligned}
     & x  \in \underset{r \gt \alpha}{\cup} \left(X \backslash Cl(U_r)\right)
     \\
     \Leftrightarrow\,
     &
     \underset{r \gt \alpha}{\exists}
     \left( x \notin Cl(U_r) \right)
     \\
     \Rightarrow\,
     &
     \underset{r \gt \alpha}{\exists}
     \left( x \notin U_r \right)     
     \\
     \overset{(\star \star)}{\Rightarrow}\,
     &
     \underset{r \gt \alpha}{\exists}
     \left(
       f(x) \geq r
     \right)
     \\
     \Leftrightarrow\,
     &
     f(x) \gt \alpha
     \\
     \Leftrightarrow\,
     &
     x \in f^{-1}(\, (\alpha,1] \,)
  \end{aligned}
  \,.
$$




Regarding the second point: 

$$
  \begin{aligned}
    & 
    x \in f^{-1}(\, [0,\alpha) \,)
    \\
    \Leftrightarrow\,
    &
    f(x) \lt \alpha
    \\
    \Leftrightarrow\,
    &
    \underset{r \lt \alpha}{\exists}( f(x) \lt r )
    \\
    \overset{(\star \star)}{\Rightarrow}\,
    &
    \underset{r \lt \alpha}{\exists }( x \in U_r )
    \\
    \Leftrightarrow\,
     &
    x \in \underset{r \lt \alpha}{\cup} U_r
  \end{aligned}
$$

and

$$
  \begin{aligned}
     &
    x \in \underset{r \lt \alpha}{\cup} U_r
    \\    
    \Leftrightarrow\,
    &
    \underset{r \lt \alpha}{\exists }( x \in U_r )
    \\
    \overset{}{\Rightarrow}\,
    &
    \underset{r \lt \alpha}{\exists }( x \in Cl(U_r) )   
    \\
    \overset{(\star)}{\Rightarrow}\,
     &
    \underset{r \lt \alpha}{\exists }( f(x) \leq r )       
    \\
    \Leftrightarrow\,
     &
    f(x) \lt \alpha
    \\
    \Leftrightarrow\,
    &
    x \in f^{-1}(\, [0,\alpha) \,)
  \end{aligned}
 \,.
$$

(In these derivations we repeatedly use that $(0,1] \cap \mathbb{Q}_{dy}$ is dense in $[0,1]$, and we use the [[contrapositions]] of $(\star)$ and $(\star \star)$, by [[excluded middle]].)


Now since the subsets $\{ [0,\alpha), (\alpha,1]\}_{\alpha \in [0,1]}$
form a [[topological subbase|sub-base]] for the Euclidean metric topology on $[0,1]$, it follows that all pre-images of $f$ are open, hence that $f$ is continuous.



=--




## Implications
 {#Implications}

Urysohn's lemma is key in the proof of many other theorems, for instance

* [[Tietze extension theorem]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]

## Related statements


* [[paracompact Hausdorff spaces are normal]]


## References

Due to [[Pavel Urysohn]].

* [[Terence Tao]], _[245B, Notes 12: Continuous functions on locally compact Hausdorff spaces](https://terrytao.wordpress.com/2009/03/02/245b-notes-12-continuous-functions-on-locally-compact-hausdorff-spaces/#more-1844)_

* [Proof at planetmath](http://planetmath.org/proofofurysohnslemma)

* Wikipedia, _[Urysohn's lemma](https://en.wikipedia.org/wiki/Urysohn%27s_lemma)_

Lectures notes include 

* Tarun Chitra, section 2.1 of _The Stone-Cech Compactification_ 2009 [pdf](httP://www.math.cornell.edu/~riley/Teaching/Topology2009/essays/chitra.pdf)

[[!redirects Urysohn's extension theorem]]
[[!redirects Urysohn's theorem]]
[[!redirects Urysohn theorem]]
[[!redirects Urysohn lemma]]

[[!redirects Urysohn function]]
[[!redirects Urysohn functions]]
