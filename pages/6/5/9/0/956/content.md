
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

A (binary) [[relation]] $\sim$ on a [[set]] $A$ is __connected__ if any two [[elements]] that are related in neither order are [[equality|equal]]:
$$ \forall (x, y: A),\; x \nsim y \;\wedge\; y \nsim x \;\Rightarrow\; x = y .$$
This is a basic property of [[strict total orders]].

Every [[tight relation]] is a connected relation. Every connected [[symmetric relation]] is a tight relation. 

## Constructive aspects

Using [[excluded middle]], it is equivalent to say that every two elements are related in some order or equal:
$$ \forall (x, y: A),\; x \sim y \;\vee\; y \sim x \;\vee\; x = y .$$
However, this version is too strong for the intended applications to [[constructive mathematics]].  (In particular, $\lt$ on the located Dedekind [[real numbers]] satisfies the first definition but not this one.)

On the other hand, there is a stronger notion that may be used in [[constructive mathematics]], if $A$ is already equipped with a [[tight apartness]] $\#$.  In that case, we say that $\sim$ is __strongly connected__ if any two distinct elements are related in one order or the other:
$$ \forall (x, y: A),\; x \# y \;\Rightarrow\; x \sim y \;\vee\; y \sim x .$$
Since $\#$ is connected itself, every strongly connected relation is connected; the converse holds with [[excluded middle]] (through which every set has a unique tight apartness).

We can do a similar thing if $A$ is equipped with any [[inequality]] $\#$, except that in the general case, this is not necessarily stronger than being connected, and so we should call it __$\#$-connected__.

## In dependent type theory

In dependent type theory, an [[irreflexive relation]] $\sim$ with terms $a:A \vdash \mathrm{irr}(a):(a \sim a) \to \emptyset$ is connected if the canonical function 
$$\mathrm{idtosymnotrel}(a, b):(a =_A b) \to (((a \sim b) \to \emptyset) \times ((b \sim a) \to \emptyset))$$
inductively defined by 
$$\beta(a):\mathrm{idtosymnotrel}(a, a)(\mathrm{refl}_A(a)) =_{((a \sim a) \to \emptyset) \times ((a \sim a) \to \emptyset)} (\mathrm{irr}(a), \mathrm{irr}(a))$$
is an [[equivalence of types]]
$$\mathrm{conn}(a, b):\mathrm{isEquiv}(\mathrm{idtosymnotrel}(a, b))$$

## See also

* [[strict total order]]
* [[tight relation]]

[[!redirects connected relation]]
[[!redirects connected relations]]

[[!redirects strongly connected relation]]
[[!redirects strongly connected relations]]
