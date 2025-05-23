
> This entry is about the notion of _frame_ in [[topos theory]]. For other notions, see [[frame (disambiguation)]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--




# Contents
* table of contents
{: toc}

## Idea

The notion of _frame_ is a generalization of the notion of [[category of open subsets]] of a [[topological space]]. A _frame_ is like a category of open subsets in a space possibly more general than a topological space: a [[locale]]. This in turn is effectively defined to be anything that has a collection of open subsets that behaves essentially like the open subsets of a topological space do.

## Definition

+-- {: .num_defn}
###### Definition

A **frame** $\mathcal{O}$ is 

* a [[partial order|poset]] 

* that has 

  * all [[small limit|small]] [[coproduct | coproducts]], called [[join|joins]] $\bigvee$

  * all [[finite limits]], called [[meet|meets]] $\wedge$

* and which satisfies the _infinite distributive law_:

  $$ 
    x \wedge (\bigvee_i y_i) \leq \bigvee_i (x\wedge y_i)
  $$

  for all $x, \{y_i\}_i$ in $A$

  (Note that the converse holds in any case, so we have equality.)

A _frame homomorphism_ is a homomorphism of posets that preserves finite meets and arbitrary joins. Frames and frame homomorphisms form the category [[Frm]].

The formal duals of frames, hence the objects in the [[opposite category]] [[Locale]] $:=$ [[Frm]]${}^{op}$ are called [[locale | locales]].

=--

+-- {: .num_remark}
###### Remark

The notation $\mathcal{O}$ to supposed to remind us that every frame is like a [[frame of opens]] of the corresponding [[locale]].

=--

+-- {: .num_remark}
###### Remark

So in particular a frame is a _[[lattice]]_ which has not only finite [[joins]] but all small joins. Being small itself, it is a [[suplattice]], and hence a [[complete lattice]]: it also has all (small) meets.

Furthermore, as the distributive law certainly holds when the joins in question are finite, it is a _[[distributive lattice]]_.

=--

## Properties

A useful way to understand frames and [[locales]] is as the simplest nontrivial special cases of [[(n,1)-topos | (n,1)-toposes]]. So we start in

* [As (0,1)-toposes](#As0Topos)

with some remarks on this, and only then turn to 

* [General properties](#GeneralProperties)

of frames, which should make more sense this way.

### As a $(0,1)$-topos
 {#As0Topos}

The notion of _frame_ -- or rather its formal dual, the notion of _[[locale]]_ -- is the special case of the notion of [[(n,1)-topos | (n,1)-toposes]] for $n = 0$: [[(0,1)-topos | (0,1)-toposes]].

The axioms on a frame are nothing but [[Giraud's axioms]] on [[sheaf topos | sheaf toposes]], restricted to [[(0,1)-categories]]:

given the existence of finite limits and arbitrary colimits, the _infinite distributive law_ expresses that a frame has [[universal colimits]]: they are stable under [[pullback]]. (For notice that in a poset [[pullback | pullbacks]] and [[product | products]] coincide.)

Then a morphism of frames is precisely (the [[inverse image]] of) a [[geometric morphism]]: a morphism preserving finite limits and arbitrary colimits. 


### General
 {#GeneralProperties}

+-- {: .num_prop}
###### Proposition

A frame is automatically a [[Heyting algebra]].  

=--

In [[category theory|category theoretic]] terms this means that it ia a [[cartesian closed category]], hence that

for every object $x \in \mathcal{O}$ the functor

$$
  x \wedge (-) : \mathcal{O} \to \mathcal{O}
$$

that forms the [[product]] with $x$ has a [[right adjoint]]

$$
  x \Rightarrow (-) : \mathcal{O} \to \mathcal{O}
$$

+-- {: .proof}
###### Proof


This exists by the [[adjoint functor theorem]], using that there is only a finite number of morphisms between any two objects (one or none) and that finite limits exist in $\mathcal{O}$.

=--

+-- {: .num_remark}
###### Remark

Therefore one may think of a of a frame as a [[cartesian closed category|cartesian closed]] [[suplattice]], or a cartesian [[quantale]].  

But notice that the frame [[homomorphism | homomorphisms]] are not required to preserve the Heyting implication.

=--

### As sites

A frame is naturally equipped with the structure of a [[site]]: 

a family of morphism $\{U_i \to U\}$ is [[covering]] precisely if $U$ is the [[union]] of the $U_i$

$$
  \bigvee_i U_i = U
  \,.
$$

For more on this see [[locale]].

## Formal duals: locales

The [[opposite category]] to the category [[Frm]] is the category [[Loc]] of [[locale | locales]] (possibly slightly generalized [[topological space | topological spaces]])

$$
  Loc := Frm^{op}
$$

Conversely, any [[topological space]] has a [[frame of opens|frame of open subsets]].  (In fact, one definition of a topological space is a set equipped with a subframe of its [[power set]].)

## Examples

\begin{example}
For $X$ a [[topological space]], the [[category of open subsets]] of $X$ is a frame: the [[frame of opens]].
\end{example}

\begin{example}
For $X$ a [[set]], the [[power set]] $\mathcal{P}(X)$ of $X$ is the [[frame of opens]] corresponding to the [[discrete topology]] on $X$. 
\end{example}

\begin{example}
The [[poset of truth values]] $\Omega$ is a [[frame]] equivalent to the [[frame of opens]] corresponding to the [[discrete topology]] on a [[singleton]]. 
\end{example}


\begin{example}
For $\mathcal{E}$ a [[geometric category]] and $X$ an [[object]] in $\mathcal{E}$, the [[subobject poset]] $\mathrm{Sub}(X)$ is a [[frame]]. 
\end{example}

\begin{example}
The [[category]] of [[boolean]]-indexed sets and [[surjection]]-preserving functions is a [[frame]] equivalent to the [[frame of truth values]]. 
\end{example}

\begin{example}
The [[category]] of [[total order|total]] [[Boolean algebras]] and [[Boolean algebra]] [[homomorphisms]] is a [[frame]] equivalent to the [[frame of truth values]]. 
\end{example}

\begin{proposition}
A [[sup-lattice|complete]] [[decidable equality|decidable]] [[linear order]] is a frame. 
\end{proposition}

\begin{proof}
For any $x$ and collection $y_i$, the inequality $\bigvee_i x \wedge y_i \leq x \wedge \bigvee_i y_i$ holds automatically. For the reverse inequality, we note this follows trivially in case $\bigvee_i y_i \leq x$, since in that case we have $y_i \leq x$ for all $i$, whence 

$$x \wedge \bigvee_i y_i = \bigvee_i y_i = \bigvee_i x \wedge y_i.$$ 

Otherwise we are in the case $x \lt \bigvee_i y_i$, where we must show the inequality 

$$x \wedge \bigvee_i y_i = x \leq \bigvee_i x \wedge y_i$$ 

But this inequality must hold, else $\bigvee_i x \wedge y_i \lt x$ which would imply $y_i \lt x$ for all $i$, whence $\bigvee_i y_i \leq x$, contradiction. 
\end{proof}

## Related concepts

* [[Heyting algebra]]
* [[Grothendieck topos]]
* [[coframe]]

## References

Frames in [[univalent foundations]]:

* Ayberk Tosun, _Formal Topology in Univalent Foundations_, ([pdf](https://odr.chalmers.se/handle/20.500.12380/301098), [slides](https://www.cs.bham.ac.uk/~axt978/talks/lab-lunch-formal-topology.pdf))

[[!redirects frames]]
[[!redirects morphism of frames]]
[[!redirects morphisms of frames]]
[[!redirects homomorphism of frames]]
[[!redirects homomorphisms of frames]]
[[!redirects frame homomorphism]]
[[!redirects frame homomorphisms]]
[[!redirects frame morphism]]
[[!redirects frame morphisms]]
