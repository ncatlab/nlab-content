
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Simplicial groups model all [[∞-group]]s in [[∞Grpd]]. Accordingly  [[principal ∞-bundle]]s in [[∞Grpd]] should be modeled by [[Kan complex]]es $E \to X$ equipped with a principal [[action]] by a [[simplicial group]].


## Definition

+-- {: .un_def}
###### Definition
**(principal action)**

Let $G$ be a simplicial group. For $P$ a [[Kan complex]], an 
[[action]] of $G$ on $E$

$$
  \rho : E \times G \to E
$$

is called **principal** if it is degreewise principal, i.e. if for all $n \in \mathbb{N}$ the only elements $g \in G_n$ that have any fixed point $e \in E_n$ in that $\rho(e,g) = e$ are the neutral elements.

=--

+-- {: .un_example}
###### Example

The canonical action 

$$
  G \times G \to G
$$

of any simplicial group on itself is principal.

=--

+-- {: .un_def}
###### Definition
**(simplicial principal bundle)**

For $G$ a simplicial group, a morphism $P \to X$ of [[Kan complex]]es equipped with a $G$-[[action]] on $P$ is called a $G$-**simplicial principal bundle** if

* the action is principal;

* the base is isomorphic to the quotient $E/G := \lim_{\to}(E \times G \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to} E})$ by the action:

  $$
    E/G \simeq X
    \,.
  $$ 

=--


## Properties

+-- {: .un_prop}
###### Proposition

A simplicial $G$-principal bundle $P \to X$ is necessarly a [[Kan fibration]].

=--

+-- {: .proof}
###### Proof

This appears as Lemma 18.2 in [MaySimpOb](#MaySimplicialObjects).

=--


## The universal simplicial $G$-principal bundle

Recall from [[generalized universal bundle]] that a universal $G$-principal simplicial bundle should be a principal bundle $\mathbf{E}G \to \mathbf{B}G$ such that every other $G$-principal simplicial bundle $P \to X$ arises up to equivalence as the [[pullback]] of $\mathbf{E}G$ along a morphism $X \to \mathbf{B}G$.

A standard model for the [[delooping]] [[Kan complex]] $\mathbf{B}G$ for $G$ a simplicial group goes by the name 

$$
  \bar W G
  \,.
$$ 

This is described at <a href="http://ncatlab.org/nlab/show/simplicial%20group#Delooping">simplicial group - delooping</a>. The following establishes a model for the universal simplicial bundle over this model of $\mathbf{B}G$.

### Definition

+-- {: .un_def}
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

+-- {: .un_def}
###### Definition

We call $P_\bullet := X_\bullet \times^g W G$ the simplicial $G$-[[principal bundle]] corresponding to $g$.

=--

### Properties

+-- {: .un_prop}
###### Proposition

Let $\{\phi : X_n \to G_{(n-1)}\}$ be the [[twisting function]] corresponding to $g : X_\bullet \to \overline{W}G$ by the above discussion.

Then the simplicial set  $P_\bullet := X_\bullet \times_{g} W G$ is explicitly given by the formula called the [[twisted Cartesian product]] $X_\bullet \times^\phi G_\bullet$:

its cells are

$$
  P_n  = X_n \times G_n
$$

with face and degeneracy maps

*  $d_i (x,g) = (d_i x , d_i g) if $i \gt 0$

* $d_0 (x,g) = (d_0 x, \phi(x) d_0 g)$

* $s_i (x,g) = (s_i x, s_i g)$.

=--


## References 

Here are some pointers on where precisely in the literature the above statements can be found.

One useful reference is

* [[Peter May]], _Simplicial Objects in Algebraic Topology_ ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu)).

There the abbreviation PCTP ( _principal twisted cartesian product_ ) is used for what above we called just [[twisted Cartesian product]]s.

The fact that every PTCP $X \times_\phi G \to X$ defined by a [[twisting function]] $\phi$ arises as the pullback of $W G \to \overline{W}G$ along a morphjism of simplicial sets $X \to \overline{W}G$ can be found there by combining

1. the last sentence on p. 81 which asserts that pullbacks of PTCPs $X \times_\phi G \to X$ along morphisms of simplicial sets $f : Y \to X$ yield PTCPs corresponding to the composite of $f$ with $\phi$;

1. section 21 which establishes that $W G \to \bar W G$ is the PTCP for some universal twisting function $r(G)$.

1. lemma 21.9 states in the language of composites of twisting functions that every PTCP comes from composing a cocycle $Y \to \bar W G$ with the universal twisting function $r(G)$. In view of the relation to pullbacks in item 1, this yields the statement in the form we stated it above.

An explicit version of the statement that [[twisted Cartesian product]]s are nothing but pullbacks of a [[generalized universal bundle]] is on [page 148](http://ncatlab.org/timporter/files/menagerie10.pdf#page=148) of

* [[Tim Porter]], _[[timporter:crossed menagerie]]_

On [page 239](http://ncatlab.org/timporter/files/menagerie10.pdf#page=239) there it is mentioned that

$$
  G \to W G \to \overline{W}G
$$

is a model for the [[loop space object]] [[fiber sequence]]

$$
  G \to * \to \mathbf{B}G
  \,.
$$

One place in the literature where the observation that $W G $ is the [[decalage]] of $\overline{W}G$ is mentioned fairly explicitly is page 85 of

* [[John Duskin]], _Simplicial methods and the interpretation of "triple" cohomology_, number  163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc. (1975)


[[!redirects simplicial principal bundles]]

[[!redirects principal simplicial bundle]]
[[!redirects principal simplicial bundles]]
