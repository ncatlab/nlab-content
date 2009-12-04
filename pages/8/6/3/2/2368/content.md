<div class="rightHandSide toc">

[[!include stable homotopy theory - contents]]

[[!include higher algebra - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[higher algebra]] and [[stable homotopy theory]] one is interested in  [[monoid in a monoidal (∞,1)-category|monoid objects]] in the [[stable (∞,1)-category of spectra]] -- 
called  [[A-∞ ring]]s -- and [[commutative monoid in an (infinity,1)-category|commutative monoid object]] -- called [[E-∞ ring]]s.
These monoid objects satisfy associativity, uniticity and, in the $E_\infty$-case, commutativity
up to coherent higher homotopies. 

For concretely working with these objects, it is often useful to have concrete 
[[category theory|1-categorical]] algebraic models 
for these intricate [[higher category theory|higher categorical]]/homotopical entities. 
The _symmetric monoidal smash product of spectra_
is a structure that allows to model [[A-infinity ring]]s as ordinary [[monoid]]s
and [[E-infinity ring]s as ordinray [[commutative monoid]]s
in a suitable [[category]].

As a first step one wants a [[model category]] $\mathcal{S}$ of spectra that 
[[presentable (infinity,1)-category|presents]] the
full [[(infinity,1)-category]] of [[spectrum|spectra]]. 
This allows to model the notion of equivalence
of spectra and of [[homotopy|homotopies]] between maps of spectra. Such a model category 
has been known 
for a long time: its [[homotopy category]] is the [[stable homotopy category]] $Ho \mathcal{S}$.

It was also known that there is a product functor 

$$
  \wedge : \mathcal{S} \times \mathcal{S} \to \mathcal{S}
  \,,
$$

called the **[[smash product of spectra]]**, which is itself neither associative nor unital nor
commutative, but which does induce on the [[stable homotopy category]] $Ho \mathcal{S}$
a [[tensor product]] which does enjoy all these properties and does induce
on $Ho \mathcal{S}$ the structure of a [[symmetric monoidal category]].

Ordinary [[monoid]]s in the [[symmetric monoidal category|symmetric monoidal]] 
[[stable homotopy category]] $Ho \mathcal{S}$ are called **[[ring spectrum|ring spectra]]** .

These can be understood as being [[monoid]]s in $\mathcal{S}$ up to possibly _incoherent_
homotopy: while associativity and uniticity do hold up to homotopy, these homotopies
are not specified and not required to satisfy higher coherence laws up to higher
homotopies themselves. 

But notice that an ordinary [[ring]] $R$ is not just a [[monoid]] in [[Set]] 
but in [[Ab]]: it may be understood as a [[module]] over the 
archetypical ring $\mathbb{Z}$ of integers, and the ring structure on it with
product operation $\cdot : R \otimes_\mathbb{Z} R \to R$ 
identifies $R$ with a [[monoid]] in the [[category]] $Mod_\mathbb{Z}$ of 
$\mathbb{Z}$-[[module]]s. This perspective turns out to have a useful generalization
from sets to [[spectrum|spectra]]:

in the world of [[E-infinity ring]]s the role of the archetypical [[ring]] $\mathbb{Z}$ is played
by the [[sphere spectrum]] $S$. There is a well known notion of a [[spectrum]] 
with the structure of an $S$-[[module]]. These
form a [[category]] $Mod_S$ of $S$-modules.

And it turns out that _this_ category does admit a version of the smash product of
spectra, now denoted 

$$
  \wedge_S : Mod_S \times Mod_S \to Mod_S
$$ 

which is associative, and commutative. Moreover, $Mod_S$ does admit 
the structure of a [[model category]] such that the
corresponding [[homotopy category]] is still the [[stable homotopy category]]

$$
  Ho Mod_S \simeq Ho \mathcal{S}
  \,.
$$

The image of $\wedge_S$ in that [[homotopy category]] is also unital.

This construction can be improved further: there is a slight variation of the smash product
$\wedge_S$, denoted $\star_S$, which is in addition unital: the [[tensor unit]] is the
[[sphere spectrum]] $S$, as it should be. 

>Question: is $(Mod_S, \star_S)$ then a [[symmetric monoidal category]]? With the 
above model strucvture, is it a [[monoidal model category]]?

The [[monoidal category]] $(Mod_S, \star_S)$ (or the almost-monoidal category $(Mod_S, \wedge_S)$) 
is therefore a natural context in which
to try to refine the notion of a [[ring spectrum]].

Indeed, it turns out that ordinary [[monoid]] objects in $(Mod_S, \wedge_S)$
are indeed equivalent to [[A-infinity ring]]s, and ordinary commutative monoid objects
in $(Mod_S, \wedge_S)$
are equivalent to [[E-infinity ring]]s: the way the smash product $\wedge_S$ works
it absorbs all the higher coherent homotopies. 

There is a generalization of this construction from [[A-infinity ring]]s to 
[[A-infinity algebra]]s: for $R$ any [[A-infinity ring]] possibly different from the
[[sphere spectrum]] $S$, there is a notion of $R$-[[module]] spectra forming a
category $Mod_R$. This $Mod_R$ in turn carries an associative and commutative
smash product over $R$, denoted $\wedge_R$ and there is a [[model category]]
structure on $Mod_R$ such that $\wedge_R$ becomes unital in the [[homotopy category]]. 
All this is such that an [[A-infinity algebra]] over $R$ is a [[monoid]] object in 
$(Mod_R, \wedge_R)$. Similarly [[E-infinity algebra]]s are commutative [[monoid]]
objects in  $(Mod_R, \wedge_R)$.

## Details

For defining the symmetric monoidal smash product of spectra it is necessary to use a model for the objects of the [[stable homotopy category]] that is a bit more refined than the notion of $\Omega$-[[spectrum]]. One uses [[coordinate-free spectrum|coordinate free spectra]].

...

## References

A survey of the general theory, also of its history, is

* A. Elmendorf, I. Kriz, [[Peter May|P. May]], _Modern foundations for stable homotopy theory_ 
([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

The definition of the symmetric monoidal category of spectra itself is compiled in the seminar notes

* [[Sander Kupers]], [[SymmetricSpectra.pdf:file]]
