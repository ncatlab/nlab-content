
\tableofcontents

## Definition

### In unsorted set theory

In [[unsorted set theory]], a **reflexive set** is a set that belongs to itself:
$$ X \in X .$$
Equivalently, $X$ is reflexive iff it equals its [[successor]] $X \cup \{X\}$.  Compare [[transitive sets]].

If the [[axiom of foundation]] holds in a set theory, then there are no reflexive sets.  In non-well-founded set theory, however, there may be many reflexive sets.

A __Quine atom__ is a minimally reflexive set:
$$ X = \{X\} .$$

### In two-sorted set theory

In [[two-sorted set theory]] with [[element reflection]], a **reflexive set** is a set whose element reflection belongs to itself:
$$\mathrm{asElem}(X) \in X$$
Similarly, in a [[two-sorted set theory]] with [[set reflection]], a **reflexive element** is an element which belongs to its set reflection:
$$X \in \mathrm{asSet}(X)$$

## Examples

In [[Peter Aczel]]\'s ill-founded set theory, there is a unique Quine atom.  On the other hand, by exempting Quine atoms (and only Quine atoms) from the axiom of foundation, one obtains a theory of pure sets equivalent to well-founded material sets with [[urelements]].

### Fully formal ETCS

Take any [[single-sorted definition of a category|single-sorted definition]] of a [[well-pointed topos]] $\mathcal{E}$, such as [[fully formal ETCS]], which by definition has a [[morphism]] $1$ representing the [[terminal object]], the [[identity morphism]] of the terminal object, and the single [[global element]] of the terminal object. Sets are represented by morphisms with [[codomain]] $1$, and elements are represented by morphisms with [[domain]] $1$. Thus, we define the [[predicates]] $\mathrm{set}(f) \coloneqq \mathrm{codom}(f) = 1$ and $\mathrm{element}(f) \coloneqq \mathrm{dom}(f) = 1$. The codomain and domain of general functions are then defined as usual to be sets, $\mathrm{set}(\mathrm{codom}(f))$ and $\mathrm{set}(\mathrm{dom}(f))$. We define the membership relation $a \in b$ as requiring the morphism $a$ to be an [[element]], the morphism $b$ to be a [[set]], and the codomain of $a$ to be $b$:

$$a \in b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(b) \wedge \mathrm{codom}(a) = b$$

The terminal object $1$ is then a [[Quine atom]] with respect to $\in$. 

## See also

* [[unsorted set theory]]
* [[fully formal ETCS]]

[[!redirects reflexive set]]
[[!redirects reflexive sets]]

[[!redirects reflexive element]]
[[!redirects reflexive elements]]

[[!redirects Quine atom]]
[[!redirects Quine atoms]]
