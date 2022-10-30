
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 
 {#Idea}

A _net_ in a [[set]] $X$ is a [[function]] from a [[directed set]] $D$ to $X$. Special cases of nets are [[sequences]], for which $D = \mathbb{N}_{\leq}$ is the [[natural numbers]]. Regarded as a generalization of sequences, nets are used in [[topology]] for formalization of the concept of [[convergence]].

Nets are also called _Moore--Smith sequences_ and are equivalent (in a certain sense) to [[proper filters]] (def. \ref{Filter} below), their _[[eventuality filters]]_ (def. \ref{EventualityFilter} below).

The concept of nets is motivated from the fact that where plain [[sequences]] detect [[topology|topological]] properties in [[metric spaces]], in generally they fail to do so in more general [[topological spaces]]. 
For example [[sequentially compact metric spaces are equivalently compact metric spaces]], but for general [[topological spaces]] being [[sequentially compact space|sequentially compact]] neither implies nor is implied by being [[compact space|compact]] (see at _[[sequentially compact space]]_ [Examples and counter-examples](sequentially+compact+topological+space#Examples)). 

Inspection of these counter-examples reveals that the problem is that sequences indexed by the [[natural numbers]] may be "too short" in that they cannot go deep enough into uncountable territory, and they are "too slim" in that they proceed to their potential limiting point only from one direction, instead of from many at once. The use of general [[directed sets]] for nets in place of just the [[natural numbers]] for sequences fixes these two issues. 

And indeed, as opposed to sequences, nets do detect

1. the topology on general topological spaces (prop. \ref{TopologyDetectedByNets} below), 

1. the continuity of functions between them (prop. \ref{ContinuousFunctionsDetectedByNets} below), 

1. the [[Hausdorff topological space|Hausdorff]] property (prop. \ref{NetsDetectHausdorff} below);

1. [[compact topological space|compactness]] (prop. \ref{CompactSpacesEquivalentlyHaveConvergetSubnets} below).

While the concept of nets is similar to that of sequences, one gets a cleaner theory still by considering not the nets themselves but their "[[filters]] of [[subsets]] which they eventually meet" (def. \ref{EventuallyAndFrequently} below), called their _[[eventuality filters]]_ (def. \ref{EventualityFilter} below). For example equivalent filters are equal (in contrast to nets) and (unless in [[predicative mathematics]]) the set of filters on a set $X$ is [[small set|small]] (not a proper class).


## Definitions

### Directed sets
 {#DirectedSets}


+-- {: .num_defn #DirectedSet}
###### Definition
**([[directed set]])**

A _[[directed set]]_ is

* a [[preordered set]] $(D, \leq)$, hence a set $D$ equipped with a [[reflexive relation|reflexive]] and [[transitive]] [[relation]] $\leq$

such that

* every [[finite set|finite]] [[subset]] has an [[upper bound]], hence for any $a,b \in D$ there exists $c \in D$ with $a \leq c$ and $b \leq c$.

=--


+-- {: .num_example #DirectedSetOfNaturalNumbers}
###### Example
**([[directed set]] of [[natural numbers]])**

The [[natural numbers]] $\mathbb{N}$ with their canonical
lower-or-equal relation $\leq$ form a [[directed set]] (def. \ref{DirectedSet}).

=--

The key class of examples of nets, underlying their relation to [[topology]] ([below](#RelationToTopology)) is the following:

+-- {: .num_example #DirectedSetOfNeighbourhods}
###### Example
**([[directed set]] of [[neighbourhoods]])**

Let $(X, \tau)$ be a [[topological space]] and let $x \in X$ be an element of the underlying set. Then then set of $(Nbhd_X(x)_{\supset})$ [[neighbourhoods]] of $x$, ordered by _reverse_ inclusion, is a [[directed set]] (def. \ref{DirectedSet}).

=--

+-- {: .num_example #DirectedProductSet}
###### Example

Let $A_{\geq}$ and $B_{\geq}$ be two [[directed sets]] (def. \ref{DirectedSet}). Then the [[Cartesian product]] $A \times B$ of the underlying sets becomes itself a directed set by setting

$$
  \left(
    (a_1, b_1) \leq (a_2, b_2)
  \right)
  \,\coloneqq\,
  \left(
     \left( a_1 \leq a_2\right)
     \,\text{and}\,
     \left(
        b_1 \leq b_2
     \right)
  \right)
  \,.
$$ 

=--



### Nets
 {#Nets}


+-- {: .num_defn #Net}
###### Definition

For $X$ a [[set]], then a _net_ in $X$ is 

1. a [[directed set]] $A$ (def. \ref{DirectedSet}), called the _index set_,

1. a [[function]] $\nu \colon A \to X$ from (the underlying set of) $A$ to $X$.

We say that $A$ _indexes_ the net.  

=--

+-- {: .num_example #SequencesAreNets}
###### Example
**([[sequences]] are [[nets]])**

A [[sequence]] is a net (def. \ref{Net}) whose directed set of indices is the [[natural numbers]] $(\mathbb{N}, \leq)$ (example \ref{DirectedSetOfNaturalNumbers}).

=--

+-- {: .num_remark}
###### Remark

Although the index set $A$ in def. \ref{Net}, being a [[directed set]], is equipped with a [[preorder]], the function $\nu \colon A \to X$ is not required to preserve this in any way.  This forms an exception to the rule of thumb that a preordered set may be replaced by its quotient [[partial order|poset]].  

You can get around this if you instead define a net in $X$ as a [[multi-valued function]] from a partially ordered directed set $A$ to $X$.  Although there is not much point to doing this in general, it can make a difference if you put restrictions on the possibilities for $A$, in particular if you consider the definition of [[sequence]].  In some [[type theory|type-theoretic]] [[foundations]] of mathematics, you can get the same effect by defining a net to be an 'operation' (a [[prefunction]], like a function but not required to preserve [[equality]]).

=--

+-- {.num_defn #EventuallyAndFrequently}
###### Definition
**([[eventually]] and frequently)**

Consider [[net]] $\nu \colon A \to X$ (def. \ref{Net}), and given a [[subset]] $S \subset X$. We say that 

1. $\nu$ is _[[eventually]] in $S$_ if there exists $i \in A$ such that $\nu_j \in S$ for every $j \ge i$.  

1. $\nu$ is _frequently in $S$_ if for every index $i \in A$, then $\nu_j \in S$ for some $j \ge i$.  

=--

+-- {.num_remark}
###### Remark

Sometimes one says 'infinitely often' in place of 'frequently' in def. \ref{EventuallyAndFrequently} and even 'cofinitely often' in place of 'eventually'; these derive from the special case of sequences, where they may be taken literally.

=--

+-- {: .num_defn #Convergence}
###### Definition
**([[convergence]] of [[nets]])**

Let $(X,\tau)$ be a [[topological space]], and let $\nu \colon A \to X$ be a [[net]] in the underlying set (def. \ref{Net}).

We say that the net $\nu$ 

1. _[[convergence|converges]]_ to an element $x \in X$ if given any [[neighbourhood]] $U$ of $x$, $\nu$ is eventually in $U$ (def. \ref{EventuallyAndFrequently}); such $x$ is called a _[[limit point]]_ of the net;

1. _clusters_ at $x$ if, for every [[neighbourhood]] $U$ of $x$, $\nu$ is frequently in $U$ (also def. \ref{EventuallyAndFrequently}); such $x$ is called a _[[cluster point]]_ of the net.  

=--

+-- {: .num_remark}
###### Remark

Beware that [[limit points]] of nets, according to def. \ref{Convergence}, need not be unique. They are guaranteed to be unique in [[Hausdorff topological spaces|Hausdorff spaces]], see prop. \ref{NetsDetectHausdorff} below.

=--





### Subnets

The definition of the concept of _[[sub-nets]]_ of a net requires some care. The point of the definition is to ensure that prop. \ref{CompactSpacesEquivalentlyHaveConvergetSubnets} below becomes true, which states that [[compact spaces equivalently have converging subnet of every net|compact spaces are equivalently those for which every net has a converging subnet]].

There are several different definitions of '[[subnet]]' in the literature, all of which intend to generalise the concept of subsequences.  We state them now in order of increasing generality.  Note that it is Definition \ref{AA} which is correct in that it corresponds precisely to refinement of filters.  However, the other two definitions (def. \ref{Willard}, def. \ref{Kelley}) are sufficient (in a sense made precise by theorem \ref{EquivalenceOfDefinitionsOfSubnets} below) and may be easier to work with.


+-- {.num_defn #Willard}
###### Definition
(Willard, 1970).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

We have a [[function]] $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is monotone (that is, for every $\beta_1 \geq \beta_2 \in B$, $f(\beta_1) \geq f(\beta_2)$);
*  $f$ is cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that $f(\beta) \geq \alpha$).
=--

+-- {.num_defn #Kelley}
###### Definition
(Kelley, 1955).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

We have a [[function]] $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is strongly cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$, $f(\beta_1) \geq \alpha$).

=--

+-- {: .num_remark}
###### Remark

Notice that the function $f$ in definitions \ref{Willard} and \ref{Kelley} is _not_ required to be an [[injection]], and it need not be. As a result, a [[sequence]] regarded as a [[net]] in general has more sub-nets than it has sub-sequences.

=--


+-- {.num_defn #AA}
###### Definition
(Smiley, 1957; &#197;rnes & Anden&#230;s, 1972).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

The [[eventuality filter]] of $y$ (def. \ref{EventualityFilter}) refines the eventuality filter of $x$.  (Explicitly, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$ there is an $\alpha_1 \geq \alpha \in A$ such that $y_{\beta_1} = x_{\alpha_1}$.)
=--


The equivalence between these definitions is as follows:

+-- {.num_theorem #EquivalenceOfDefinitionsOfSubnets}
###### Theorem
([Schechter, 1996](#Schechter96)).

1.  If $y$ is a (\ref{Willard})-subnet of $x$, then $y$ is also a (\ref{Kelley})-subnet of $x$, using the same function $f$.
2.  If $y$ is a (\ref{Kelley})-subnet of $x$, then $y$ is also a (\ref{AA})-subnet of $x$.
3.  If $y$ is a (\ref{AA})-subnet of $x$, then there is some net $z$ such that
    *  $z$ is equivalent to $y$ in the sense that $y$ and $z$ are (\ref{AA})-subnets of each other, and
    *  $z$ is a (\ref{Willard})-subnet of $x$, using some function.
=--

So from the perspective of definition (\ref{AA}), there are enough (\ref{Willard})-subnets and (\ref{Kelley})-subnets, up to equivalence.



### Eventuality filters
 {#NetsAndFilters} 

Recall that: 

+-- {: .num_defn #Filter}
###### Definition
**([[filter]])**

Given a [[set]] $X$ then a [[set]] of [[subsets]] of $X$, hence a subset of the [[power set]]

$$
  \mathcal{F} \subset P(X)
$$

is called a _[[filter]]_ of subsets if it is closed under [[intersections]] and under taking supersets.

The filter $\mathcal{F}$ is called _proper_ if each set in it is [[inhabited subset|inhabited]].

=--

+-- {: .num_defn #EventualityFilter}
###### Definition
**([[eventuality filter]])**

Let $X$ be a [[set]] and let $\nu \colon D \to X$ be a net in $X$ (def. \ref{Net}).

The _[[eventuality filter]]_ $\mathcal{F}_\nu$ of the net $\nu$ is the [[filter]] (def. \ref{Filter}) onsisting of the subsets that $\nu$ is _eventually in_, according to def. \ref{EventuallyAndFrequently}.

$$
  \left(
    (U \subset X) \in \mathcal{F}_\nu
  \right)
   \,\Leftrightarrow\,
  \left(
    \nu \, \text{is eventually in}\, U
  \right)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark
**(equivalence of nets)**

Two nets are to be considered __equivalent__ if they have the same [[eventuality filter]] according to def. \ref{EventualityFilter}. 
By def. \ref{AA} and theorem \ref{EquivalenceOfDefinitionsOfSubnets}, this means equivalently that they are both subnets of each other.  

In particular, equivalent nets define the same logical quantifiers (see [below](#LogicOfNets)) and are therefore indeed equivalent for the application to [[topology]] (see [below](#RelationToTopology)).  

(Of course, it is possible to distinguish them by using the standard logical quantifiers instead.)

=--


Conversely,  every [[filter]] is the [[eventuality filter]] of some net:

+-- {: .num_defn #FilterNet}
###### Definition
**(nets from filters)**

Let $X$ be a [[set]] and let  $\mathcal{F} \subset P(X)$ be a [[filter]] of subsets of $X$ (def. \ref{Filter}).
Ss
Consider the [[disjoint union]] $\underset{U \in \mathcal{F}}{\sqcup}$ of subsets in  $\mathcal{F}$, hence the set whose elements are [[pairs]] of the form $(U,x)$, where $x \in U \in \mathcal{F}$. Equipped with the ordering 

$$ 
  \left(
    (U,x) \geq (V,y)  
  \right) 
  \,\Leftrightarrow\,
  \left(
    U \subset V
  \right)
  \phantom{AAA}
  \text{regardless of}\, x\, \text{and} \, y  
$$

the fact that $\mathcal{F}$ is a proper filter implies that this is a [[directed set]] according to def. \ref{DirectedSet}. (It is actually enough to use only a base of the filters).

Then the _filter net_ $\nu_F$ of $\mathcal{F}$ is the [[net]] on $X$ (def. \ref{Net}) given by

$$
  \array{
    \left(
      \underset{U \in \mathcal{F}}{\sqcup} U
    \right)_{\supset}
      &\overset{\nu_{\mathcal{F}}}{\longrightarrow}&
    X
    \\
    (U,x) &\overset{\phantom{AAA}}{\mapsto}& x
  }
  \,.
$$

=--


+-- {: .num_prop }
###### Proposition

Given a [[set]] $X$ and a [[filter]] of subsets $\mathcal{F} \subset P(X)$ (def. \ref{Filter}), then $\mathcal{F}$ is the [[eventuality filter]] (def. \ref{EventualityFilter}) of its filter net (def. \ref{FilterNet}).

=--



## Properties

### Relation to topology
 {#RelationToTopology}



+-- {: .num_prop #TopologyDetectedByNets}
###### Proposition
**(topology detected by nets)**

Using the [[axiom of choice]] then:

Let $(X, \tau)$ be a [[topological space]]. Then a [[subset]] $(U \subset X)$ is [[open subset|open]] in $X$ (is an element of $\tau \subset P(X)$) precisely if its [[complement]] $X \backslash S$ is a [[closed subset]] as seen not just by sequences but by nets, in that no [[net]] with elements in $X\backslash S$,  $\nu \colon A \to X\backslash S \hookrightarrow X$, [[converges]] to an element in $S$.


=--

+-- {: .proof}
###### Proof

In one direction, let $S \subset X$ be open, and consider a net $\nu \colon A \to X \backslash S \subset X$. We need to show that for every point $x \in S$, $x$ is not a limiting point of the net.

But by assumption then $S$ is a [[neighbourhood]] of $x$ which does not contain any element of the net, and so by definition of convergence it is not a limit of this net.

Conversely, let $S \subset X$ be a subset that is not open. We need to show that then there exists a net $\nu \colon A \to X\backslash S \subset X$ that converges to a point in $S$.

For $x \in X$, consider the [[directed set]] $Nbhd_X(x)_{\supset}$ of [[open neighbourhoods]] of this element (example \ref{DirectedSetOfNeighbourhods}).
Now the fact that the set $S$ is not open means that there exists an element $s \in S \subset X$ such that every [[open neighbourhood]] $U$ of $s$ intersects $X \backslash S$. This means that we may [[axiom of choice|choose]] elements $x_U \in U \cap (X \backslash S)$, and hence define a net

$$
  \array{
    Nbhds_X(s) &\overset{\nu}{\longrightarrow}& X \backslash S  \subset X
    \\
    U &\mapsto& x_U
  }
  \,.
$$

But by construction this net has the property that for every neighbourhood $V$ of $s$ there exists $U \in Nbhd_X(s)$ such that for all $U' \subset U$ then $x_{U'} \in V$, namely $U = V$. Hence the net converges to $s$.

=--

+-- {: .num_prop #ContinuousFunctionsDetectedByNets}
###### Proposition
**(continuous functions detected by nets)**

Assuming [[excluded middle]], then

Let $(X,\tau_X)$ and $(Y,\tau_Y)$ be two [[topological space]]. Then a [[function]] $f \colon X \to Y$ between their underlying sets is [[continuous function|continuous]] precisely if for every net $\nu \colon A \to X$ that [[convergence|converges]] to some [[limit point]] $x \in X$ (def. \ref{Convergence}), the image net $f\circ \nu$ converges to  $f(y)\in Y$.

=--

+-- {: .proof}
###### Proof

In one direction, suppose that $f \colon X \to Y$ is continuous, and that $\nu \colon A \to X$ converges to some $x \in X$. We need to show that $f \citc \nu$ converges to $f(y) \in Y$, hence that for every neighbourhood $U_{f(y)} \subset Y$ there exists $i \in A$ such that $f(\nu(j)) \in U_{f(y)}$ for all $j \geq i$.

But since $f$ is continuous, the [[pre-image]] $f^{-1}(U_{f(y)}) \subset X$ is an open neighbourhood of $x$, and so by the assumption that $\nu$ converges there is an $i \in A$ such that $\nu(j) \in f^{-1}(U_{f(y)})$ for all $j \geq i$. By applying $f$, this is the required statement.

Conversely, suppose that $f$ is not continuous, and that the net $\nu$ converges to some $x \in X$. We need to show that then $f \circ \nu$ does not converge to $f(x)$. (This is the [[contrapositive]] of the reverse implication, and by [[excluded middle]] equivalent to it.)

Now that $f$ is not continuous means that there exists an open subset $U \subset Y$ such that the pre-image $f^{-1}(U)$ is not open. By prop. \ref{TopologyDetectedByNets} this means that there exists a net $\nu$ in $X \backslash f^{-1}(U)$ that converges to an element $x \in f^{-1}(U)$. But this means that $f \circ \nu$ is a net in the $Y \backslash U$, which is a [[closed subset]] by the assumption that $U$ is open. Again by prop. \ref{TopologyDetectedByNets} this means that $f\circ \nu$ converges to an element in $Y \backslash U$, and hence not to $f(x) \in U$. 


=--

+-- {: .num_remark}
###### Remark

It is possible to define elementary conditions on this [[convergence]] relation that characterise whether it is topological (that is whether it comes from a topology on $X$), although these are a bit complicated.

By keeping only the simple conditions, one gets the definition of a [[convergence space]]; this is a more general concept than a topological space and includes many non-topological situations where we want to say that a sequence converges to some value (such as convergence in measure).  

=--

+-- {: .num_prop #NetsDetectHausdorff}
###### Proposition
**(Hausdorff property detected by nets)**

Assuming [[excluded middle]] and the [[axiom of choice]], then:

A [[topological space]] $(X,\tau)$ is [[Hausdorff topological space]] precisely if no [[net]] in $X$ (def. \ref{Net}) converges to two distinct [[limit points]] (def. \ref{Convergence}).

=--

+-- {: .proof}
###### Proof

In one direction, assume that $(X,\tau)$ is a Hausdorff space, and that $\nu \colon A \to X$ is a net in $X$ which has limits points $x_1, x_2 \in X$. We need to show that then $x_1 = x_2$.

Assume on the contrary that the two points were different, $x_1 \neq x_2$. By assumption of Hausdorffness, these would then have disjoint open neighbourhoods $U_{x_1}, U_{x_2}$, i.e. $U_1 \cap U_2 = \emptyset$. By definition of convergence, there would thus be $a_1, a_2 \in A$ such that $\nu_{a_1 \leq \bullet} \in U_{x_1}$ and $\nu_{a_2 \leq \bullet} \in U_{x_2}$. Moreover, by the definition of directed set, this would imply $a_3 \in A$ with $a_1, a_2 \leq a_3$, and hence that $x_{a_3 \leq \bullet} \in U_{x_1} \cap U_{x_2}$.  This is in contradiction to the emptiness of the intersection, and hence we have a [[proof by contradiction]].

Conversely, assume that $(X,\tau)$ is not a Hausdorff space. We need to show that then there exists a net $\nu$ in $X$ with two distinct limit points. 

That $(X,\tau)$ is not Hausdorff means that there are two distinct points $x_1, x_2 \in X$ such that every open neighbourhood of $x_1$ intersects every open neighbourhood of $x_2$. Hence we may [[axiom of choice|choose]] elements in these intersections

$$
  x_{U_{x_1}, U_{x_2}} \in U_{x_1}, U_{x_2}
  \,.
$$

Consider the directed neighbourhood sets $Nbhd_X(x_1)_{\supset}$ and $Nbhd_X(x_2)_{\supset}$ of these two points (example \ref{DirectedSetOfNeighbourhods}) and their directed Cartesian product set (example \ref{DirectedProductSet}) $Nbhd_X(x_1)_{\supset} \times Nbhd_X(x_2)_{\supset}$. The above elements then define a net

$$
  \array{
     Nbhd_X(x_1) \times Nbhd_X(x_2)
       &\overset{\nu}{\longrightarrow}&
     X
     \\
     (U_{x_1}, U_{x_2}) 
       &\overset{\phantom{AAA}}{\mapsto}&
     x_{U_1, U_2}
  }
  \,.
$$

We conclude by claiming that $x_1$ and $x_2$ are both limit points of this net. We show this for $x_1$, the argument for $x_2$ is directly analogous:


Let $U_{x_1}$ be an open neighbourhood of $x_1$. We need to find an element $(V_1, V_2) \in Nbhd_X(x_1) \times Nbhd_X(x_2)$ such that for all $(W_1, W_2) \subset (V_1, V_2)$ then $\nu_{(W_1, W_2)} \in U_{x_1}$.

Take $V_1 \coloneqq U_{x_1}$ and take $V_2 = X$. Then by construction 

$$
  \begin{aligned}
    \nu_{(W_1, W_2)} 
      & \in W_1 \cap W_2 
    \\
      & \subset V_1 \cap V_2
    \\
     & = U_{x_1} \cap X
    \\
     & = U_{x_1}
  \end{aligned}
  \,.
$$


=--


+-- {: .num_prop #CompactSpacesEquivalentlyHaveConvergetSubnets}
###### Proposition
**([[compact spaces equivalently have converging subnet of every net|compact spaces are equivalently those for which every net has a converging subnet]])**

Assuming [[excluded middle]] and the [[axiom of choice]], then:

A [[topological space]] $(X,\tau)$ is [[compact topological space|compact]] precisely if every [[net]] in $X$ (def. \ref{Net}) has a [[sub-net]] (def. \ref{Willard}) that [[convergence|converges]] (def. \ref{Convergence}).

=--

We break up the **proof** into that of lemmas \ref{InACompactSpaceEveryNetHasAConvergentSubnet} and \ref{IfEveryNetHasConvergentSubnetThenSpaceIsCompact}:

+-- {: .num_example #InACompactSpaceEveryNetHasAConvergentSubnet}
###### Lemma
**(in a compact space, every net has a convergent subnet)**

Let $(X,\tau)$ be a [[compact topological space]]. Then every net in $X$ has a convergent subnet.

=--

+-- {: .proof}
###### Proof

Let $\nu \colon A \to X$ be a net. We need to show that there is a subnet which converges.

For $a \in A$ consider the [[topological closures]] $Cl(S_a)$ of the sets $S_a$ of elements of the net beyond some fixed index:

$$
  S_a 
    \;\coloneqq\;
  \left\{
    \nu_b  \in X \;\vert\; b \geq a
  \right\}
  \subset X
  \,.
$$

Observe that the set $\{S_a \subset X\}_{a \in A}$ and hence also the set $\{Cl(S_a) \subset X\}_{a \in A}$ has the [[finite intersection property]], by the fact that $A$ is a [[directed set]]. Therefore [this prop. ](finite+intersection+property#CompactnessInTermsOfFiniteIntersectionProperty) implies from the assumption of $X$ being compact that the intersection of _all_ the $Cl(S_a)$ is non-empty, hence that there is an element

$$
  x \in \underset{a \in A}{\cap}  Cl(S_a)
  \,.
$$

In particular every [[neighbourhood]] $U_x$ of $x$ intersects each of the $Cl(S_a)$, and hence also each of the $S_a$. By definition of the $S_a$, this means that for every $a \in A$ there exists $b \geq a$ such that $\nu_b \in U_x$, hence that $x$ is a [[cluster point]] (def \ref{Convergence}) of the net.

We will now produce a [[sub-net]] 

$$
  \array{
     B && \overset{f}{\longrightarrow} && A
     \\
     & \searrow && \swarrow_{\nu}
     \\
     && X
  }
$$


that converges to this cluster point. To this end, we first need to build the domain directed set $B$. Take it to be the sub-directed set of the Cartesian product directed set (example \ref{DirectedProductSet}) of $A$ with the directed neighbourhood set $Nbhd_X(x)$ of $x$ (example \ref{DirectedSetOfNeighbourhods})

$$
  B \subset A_{\leq} \times Nbhd_X(x)_{\supset}
$$

on those pairs such that the element of the net indexed by the first component is is contained in the second component:

$$
  B 
    \;\coloneqq\;
  \left\{
     (a,U_x)  \,\vert \, \nu_a \in U_X
  \right\}
  \,.
$$

It is clear $B$ is a [[preordered set]]. We need to check that it is indeed directed, in that every pair of elements $(a_1, U_1)$, $(a_2, U_2)$ has a common upper bound $(a_{bd}, U_{bd})$. Now since $A$ itself is directed, there is an upper bound $a_3 \geq a_1, a_2$, and since $x$ is a cluster point of the net there is moreover an $a_{bd} \geq a_3 \geq a_1, a_3$ such that $\nu_{a_{bd}} \in U_1 \cap U_2$. Hence with $U_{bd} \coloneqq U_1 \cap U_2$ we have obtained the required pair.

Next take the function $f$ to be given by

$$
  \array{
     B &\overset{f}{\longrightarrow}& A
     \\
     (a, U) &\overset{\phantom{AAA}}{\mapsto}& a
  }
  \,.
$$

This is clearly order preserving, and it is cofinal since it is even a surjection. Hence we have defined a subnet $\nu \circ f$.

It now remains to see that $\nu \circ f$ converges to $x$, hence that for every open neighbourhood $U_x$ of $x$ we may find $(a,U)$ such that for all $(b,V)$ with $a \leq b$ and $U \supset V$ then $\nu(f(b,V)) = \nu(b) \in U_x$.  Now by the nature of $x$ there exists some $a$ with $\nu_a \in U_x$, and hence if we take $U \coloneqq U_x$ then nature of $B$ implies that with $(b, V) \geq (a,U_x)$ then $b \in V \subset U_x$.

=--

+-- {: .num_example #IfEveryNetHasConvergentSubnetThenSpaceIsCompact}
###### Lemma

Assuming [[excluded middle]], then:

Let $(X,\tau)$ be a [[topological space]]. If every [[net]] in $X$ has a [[subnet]] that [[convergence|converges]], then $(X,\tau)$ is a [[compact topological space]].

=--

+-- {: .proof}
###### Proof



By [[excluded middle]] we may equivalently prove the [[contrapositive]]: If $(X,\tau)$ is not compact, then not every net in $X$ has a convergent subnet.

Hence assume that $(X,\tau)$ is not compact. We need to produce a net without a convergent subnet.

Again by [[excluded middle]], then by [this prop.](finite+intersection+property#CompactnessInTermsOfFiniteIntersectionProperty) $(X,\tau)$ not being compact means equivalently that there exists a set $\{C_i \subset X\}_{i \in I}$ of [[closed subsets]] satisfying the [[finite intersection property]], but such that their intersection is empty: $\underset{i \in I}{\cap} C_i = \emptyset$.

Consider then $P_{fin}(I)$, the set of [[finite set|finite]] [[subsets]] of $I$. By the assumption that $\{C_i \subset X\}_{i \in I}$ satisfies the [[finite intersection property]], we may [[axiom of choice|choose]] for each $J \in P_{fin}(I)$ an element

$$
  x_J \in \underset{i \in J \subset I}{\cap} C_i
  \,.
$$



Now $P_{fin}(X)$ regarded as a [[preordered set]] under inclusion of subsets is clearly a [[directed set]], with an upper bound of two finite subsets given by their [[union]]. Therefore we have defined a net

$$
  \array{
     P_{fin}(X)_{\subset} &\overset{\nu}{\longrightarrow}& X
     \\
     J &\overset{\phantom{AAA}}{\mapsto}& x_J
  }
  \,.
$$

We will show that this net has no converging subnet.

Assume on the contrary that there were a subnet

$$
  \array{
     B && \overset{f}{\longrightarrow} && P_{fin}(X)
     \\
     & \searrow && \swarrow_{\nu}
     \\
     && X
  }
$$

which converges to some $x \in X$. 

By the assumption that $\underset{i \in I}{\cap} C_i = \emptyset$, there would exist an $i_x \in I$ such that $x \neq C_{i_x}$, and because $C_i$ is a [[closed subset]], there would exist even an [[open neighbourhood]] $U_x$ of $x$ such that $U_x \cap C_{i_x} = \emptyset$. This would imply that $x_J \neq U_x$ for all $J \supset \{i_x\}$.

Now since the function $f$ defining the subset is cofinal, there would exist $b_1 \in B$ such that $\{i_x\} \subset f(b_1)$. Moreover, by the assumption that the subnet converges, there would also be $b_2 \in B$ such that $\nu_{b_2 \leq \bullet} \in U_x$. Since $B$ is directed, there would then be an upper bound $b \geq b_1, b_2$ of these two elements. This hence satisfies both $\nu_{f(e)} \in U_x$ as well as $\{i_x\} \subset f(b_1) \subset f(b)$. But the latter of these two means that $\nu_{f(b)}$ is not in $U_x$, which is a contradiction to the former. Thus we have a [[proof by contradiction]].


=--


### Logic of nets 
 {#LogicOfNets}

A [[property]] of [[elements]] of a [[set]] $X$ (given by the [[subset]] $S \subset X$ of those elements of $X$ satisfying this property) may be applied to nets in $X$.  


Being eventually in $S$, def. \ref{EventuallyAndFrequently}, is a weakening of being always in $S$ (given by the [[universal quantifier]] $\forall_\nu$), while being frequently in $S$ is a strengthening of being sometime in $S$ (given by the [[particular quantifier]] $\exists_\nu$).  Indeed we can build a [[formal logic]] out of these.  Use $\ess\forall i, p[\nu_i]$ or $\ess\forall_\nu p$ to mean that a predicate $p$ in $X$ is eventually true, and use $\ess\exists i, p[\nu_i]$ or $\ess\exists_\nu p$ to mean that $p$ is frequently true.  Then we have:
$$\forall_\nu p \;\Rightarrow\; \ess\forall_\nu p \;\Rightarrow\; \ess\exists_\nu p \;\Rightarrow\; \exists_\nu p$$
$$\ess\forall_\nu (p \wedge q) \;\Leftrightarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \wedge q) \;\Rightarrow\; \ess\exists_\nu p \wedge \ess\exists_\nu q$$
$$\ess\forall_\nu (p \vee q) \;\Leftarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \vee q) \;\Leftrightarrow\; \ess\exists_\nu p \vee \ess\exists_\nu q$$
$$\ess\forall_\nu \neg{p} \;\Leftrightarrow\; \neg\ess\exists_\nu p$$
and other analogues of theorems from [[predicate logic]].  Note that the last item listed requires [[excluded middle]] even though its analogue from ordinary predicate logic does not.

A similar logic is satisfied by '[[almost everywhere]]' and its dual ('not almost nowhere' or 'somewhere significant') in [[measure spaces]].




## Related concepts

* [[limit of a net]]

* [Tychonoff theorem -- Proof via net convergence](Tychonoff+theorem#ProofViaNets)

## References

A textbook account is in 

* {#Schechter96} [[Eric Schechter]], sections 7.14--7.21 of _[[Handbook of Analysis and its Foundations]]_, Academic Press (1996)

Lecture notes include

* {#Vermeeren10} [[Stijn Vermeeren]], _Sequences and nets in topology_, 2010 ([pdf](http://stijnvermeeren.be/download/mathematics/nets.pdf))


[[!redirects net]]
[[!redirects nets]]

