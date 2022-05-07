
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Connected relations
* table of contents
{: toc}

## Definitions

A (binary) [[relation]] $\sim$ on a set $A$ is __connected__ (or sometimes __linear__) if any two elements that are related in neither order are [[equality|equal]]:
$$ \forall (x, y: A),\; x \nsim y \;\wedge\; y \nsim x \;\Rightarrow\; x = y .$$
This is a basic property of [[linear orders]].

An [[apartness relation]] (or indeed any [[inequality]]) is usually called __tight__ if it is connected, in which case [[equality]] is its [[negation]].  Since these are [[symmetric relation|symmetric]], one can use a simpler definition:
$$ \forall (x, y: A),\; x \nsim y \;\Rightarrow\; x = y .$$
Thus, one could in principle distinguish _connected_ from _tight_ relations in the nonsymmetric case (with tightness stronger than connectedness), but it\'s not clear that anybody does this.  (That is, it may be that the term 'tight' is only ever applied to symmetric relations.)


## Constructive aspects

Using [[excluded middle]], it is equivalent to say that every two elements are related in some order or equal:
$$ \forall (x, y: A),\; x \sim y \;\vee\; y \sim x \;\vee\; x = y .$$
However, this version is too strong for the intended applications to [[constructive mathematics]].  (In particular, $\lt$ on the located Dedekind [[real numbers]] satisfies the first definition but not this one.)

On the other hand, there is a stronger notion that may be used in [[constructive mathematics]], if $A$ is already equipped with a [[tight apartness]] $\#$.  In that case, we say that $\sim$ is __strongly connected__ if any two distinct elements are related in one order or the other:
$$ \forall (x, y: A),\; x \# y \;\Rightarrow\; x \sim y \;\vee\; y \sim x .$$
Since $\#$ is connected itself, every strongly connected relation is connected; the converse holds with [[excluded middle]] (through which every set has a unique tight apartness).

We can do a similar thing if $A$ is equipped with any [[inequality]] $\#$, except that in the general case, this is not necessarily stronger than being connected, and so we should call it __$\#$-connected__.


[[!redirects connected relation]]
[[!redirects connected relations]]
[[!redirects linear relation]]
[[!redirects linear relations]]
[[!redirects tight relation]]
[[!redirects tight relations]]

[[!redirects strongly connected relation]]
[[!redirects strongly connected relations]]
