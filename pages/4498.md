
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

[[simplicial group|Simplicial groups]] model all [[∞-group]]s in [[∞Grpd]]. Accordingly  [[principal ∞-bundle]]s in [[∞Grpd]] (a [[discrete ∞-groupoid|discrete]] $\infty$-bundle) should be modeled by [[Kan complex]]es $E \to X$ equipped with a principal [[action]] by a [[simplicial group]]. It is suficient to assume the action to be strict. This yields the notion of _simplicial principal bundles_ .


## Definition

+-- {: .num_defn}
###### Definition
**(strict principal simplicial bundle)**

A strict simplicial principal bundle is...

=--

+-- {: .num_defn #WeaklyPrincipalSimplicialBundle}
###### Definition
**(weakly principal simplicial bundle)**

For $G$ a [[simplicial group]], a [[Kan fibration]] $P \to X$ of [[Kan complexes]] equipped with a $G$-[[action]] on $P$ over $X$ 

$$
  \array{
    P \times G 
    &&
    \overset{\rho}{\longrightarrow}
    && 
    P 
    \\
    & \searrow && \swarrow
    \\ 
    && 
    X
  }
$$

is a _weakly $G$-principal simplicial bundle_ if the _shear map_

$$
  P \times G
   \overset{ (p_1, \rho) }{\longrightarrow}
  P \times_X P
$$

(to the [[fiber product]] of $P$ with itself over $X$) is a [[simplicial weak equivalence]].

=--

(e.g. [NSS 12b, Def. 3.79](#NSS12b))


## Properties

### General

+-- {: .num_prop}
###### Proposition

A simplicial $G$-principal bundle $P \to X$ is necessarly a [[Kan fibration]].

=--

+-- {: .proof}
###### Proof

This appears as ([May, Lemma 18.2](#May)).

=--


### Twisted cartesian products

+-- {: .num_prop}
###### Proposition

Let $E \to B$ be a [[twisted cartesian product]] of the [[simplicial set]] $B$ with a [[simplicial group]] $G$. Then with respect to the canonical $G$-[[action]] this is a simplicial principal bundle.

=--

This is ([May, prop. 18.4](#May)).

+-- {: .num_remark}
###### Remark

It is simplicial principal bundles of this form that one is mainly interested in. These are the objects that are classified by the evident [[classifying space]] $\overline{W} G$. This is discussed [below](UniversalSimplicialBundle).

=--

## The universal simplicial $G$-principal bundle
 {#UniversalSimplicialBundle}

Recall from [[generalized universal bundle]] that a universal $G$-principal simplicial bundle should be a principal bundle $\mathbf{E}G \to \mathbf{B}G$ such that every other $G$-principal simplicial bundle $P \to X$ arises up to equivalence as the [[pullback]] of $\mathbf{E}G$ along a morphism $X \to \mathbf{B}G$.

A standard model for the [[delooping]] [[Kan complex]] $\mathbf{B}G$ for $G$ a simplicial group goes by the name 

$$
  \overline{W} G
  \,.
$$ 

This is described at <a href="http://ncatlab.org/nlab/show/simplicial%20group#Delooping">simplicial group - delooping</a>. The following establishes a model for the universal simplicial bundle over this model of $\mathbf{B}G$.

### Definition

+-- {: .num_defn}
###### Definition

For $G$ a simplicial group, define the [[simplicial set]] $W G$ to be the [[decalage]] of $\overline{W}G$

$$
  W G := Dec \overline{W}G
  \,.
$$

=--


By the discussion at [[homotopy pullback]] this means that for $X_\bullet$ any [[Kan complex]], an ordinary [[pullback]] diagram

$$
  \array{
    P_\bullet &\to& W G
    \\
    \downarrow && \downarrow
    \\
    X_\bullet &\stackrel{g}{\to}& \overline{W}G
  }
$$

in [[sSet]] exhibits $P_\bullet$ as the [[homotopy pullback]] in $sSet_{Quillen}$ / [[(∞,1)-pullback]] in [[∞Grpd]]

$$
  \array{
    P_\bullet &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    X_\bullet &\stackrel{g}{\to}& \overline{W}G
  }
  \,,
$$

i.e. as the [[homotopy fiber]] of the cocycle $g$.

+-- {: .num_defn}
###### Definition

We call $P_\bullet := X_\bullet \times^g W G$ the simplicial $G$-[[principal bundle]] corresponding to $g$.

=--

### Properties

+-- {: .num_prop}
###### Proposition

Let $\{\phi : X_n \to G_{(n-1)}\}$ be the [[twisting function]] corresponding to $g : X_\bullet \to \overline{W}G$ by the above discussion.

Then the simplicial set  $P_\bullet := X_\bullet \times_{g} W G$ is explicitly given by the formula called the [[twisted Cartesian product]] $X_\bullet \times^\phi G_\bullet$:

its cells are

$$
  P_n  = X_n \times G_n
$$

with face and degeneracy maps

*  $d_i (x,g) = (d_i x , d_i g)$ if $i \gt 0$

* $d_0 (x,g) = (d_0 x, \phi(x) d_0 g)$

* $s_i (x,g) = (s_i x, s_i g)$.

=--


## Related notions

* [[simplicial classifying space]]

* [[principal bundle]]

* [[torsor]] and [[heap]]

## References 

Here are some pointers on where precisely in the literature the above statements can be found.

One useful reference is

* [[Peter May]], _Simplicial Objects in Algebraic Topology_ ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu)).
 {#May}

There the abbreviation PCTP ( _principal twisted cartesian product_ ) is used for what above we called just [[twisted Cartesian product]]s.

The fact that every PTCP $X \times_\phi G \to X$ defined by a [[twisting function]] $\phi$ arises as the pullback of $W G \to \overline{W}G$ along a morphism of simplicial sets $X \to \overline{W}G$ can be found there by combining

1. the last sentence on p. 81 which asserts that pullbacks of PTCPs $X \times_\phi G \to X$ along morphisms of simplicial sets $f : Y \to X$ yield PTCPs corresponding to the composite of $f$ with $\phi$;

1. section 21 which establishes that $W G \to \bar W G$ is the PTCP for some universal twisting function $r(G)$.

1. lemma 21.9 states in the language of composites of twisting functions that every PTCP comes from composing a cocycle $Y \to \bar W G$ with the universal twisting function $r(G)$. In view of the relation to pullbacks in item 1, this yields the statement in the form we stated it above.

An explicit version of the statement that [[twisted Cartesian product]]s are nothing but pullbacks of a [[generalized universal bundle]] is on [page 148](http://ncatlab.org/timporter/files/menagerie10.pdf#page=148) of

* [[Tim Porter]], _[Crossed Menagerie](http://ncatlab.org/timporter/show/crossed+menagerie)_

On [page 239](http://ncatlab.org/timporter/files/menagerie10.pdf#page=239) there it is mentioned that
$$
  G \to W G \to \overline{W}G
$$
is a model for the [[loop space object]] [[fiber sequence]]
$$
  G \to * \to \mathbf{B}G.
$$

One place in the literature where the observation that $W G $ is the [[decalage]] of $\overline{W}G$ is mentioned fairly explicitly is page 85 of

* [[John Duskin]], _Simplicial methods and the interpretation of "triple" cohomology_, number  163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc. (1975)

Discussion of _topological_ simplicial principal bundles is in

* [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundle in parameterized spaces_ ([arXiv:1203.2460](http://arxiv.org/abs/1203.2460))
 {#RobertsStevenson}

* [[Danny Stevenson]], _Classifying theory for simplicial parametrized groups_ ([arXiv:1203.2461](http://arxiv.org/abs/1203.2461))
 {#Stevenson}

Discussion of principal simplicial bundles in more general [[categories of simplicial presheaves]] (presenting [[(infinity,1)-toposes]]):

* {#NSS12b} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Section 3.7.2 of: _[[schreiber:Principal ∞-bundles -- models and general theory|Principal $\infty$-bundles -- Presentations]]_, Journal of Homotopy and Related Structures, Volume 10, Issue 3 (2015), pages 565-622 ([doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4), [arXiv:1207.0249](http://arxiv.org/abs/1207.0249))



[[!redirects simplicial principal bundles]]

[[!redirects principal simplicial bundle]]
[[!redirects principal simplicial bundles]]

[[!redirects universal simplicial principal bundle]]
[[!redirects universal simplicial principal bundles]]