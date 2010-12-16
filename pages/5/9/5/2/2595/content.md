
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Since a [[topos]] is a [[cartesian monoidal category]] the notion of a unital [[ring]], and commutative unital ring can be defined [[internalization|internal]] to it.

A _ringed topos_ $(X,\mathcal{O}_{X})$ is a topos $X$ equipped with a choice of ring object $\mathcal{O}$. If $X$ is a [[sheaf topos]] over a [[site]] $C$ then $\mathcal{O}_X$ is a [[sheaf]] or rings on $C$: a [[structure sheaf]].

The notion of ringed topos makes sense for the theory of rings replaced by any [[Lawvere theory]]. Moreover, it makes sense for higher toposes such as [[(∞,1)-topos]]es. This is described at [[structured (∞,1)-topos]].

## Definition


+-- {: .un_defn}
###### Definition

A **ringed topos** is a [[topos]] $X$ with a distinguished unital ring object $\mathcal{O}_X \in X$, usually, (commutative or not, depending on convention). 

If all [[stalk]]s of $\mathcal{O}_X$ are [[local ring]]s, $(X, \mathcal{O}_X)$ is a called a **locally ringed topos**.

=--

More generally:

+-- {: .un_defn}
###### Definition

For $T$ a [[Lawvere theory]], a $T$-ringed topos is a [[topos]] $X$ together with a [[product]]-preserving [[functor]] $\mathcal{O}_X : T \to X$.

=--

In order to say what _locally_ $T$-ringed means, one needs the extra structure of a [[geometry (for structured (infinity,1)-toposes)|geometry]] on $T$. See there for details.


## Examples

* A [[ringed space]] $(X,\mathcal{O})$ induces the ringed [[localic topos]] $(Sh(X),\mathcal{O})$ of [[sheaf|sheaves]] on the [[category of open subsets]] of the [[topological space]] $X$. 

  Similarly but more generally a  [[ringed site]] $(S, \mathcal{O})$ induces the ringed [[Grothendieck topos]] $(Sh(S), \mathcal{O})$.

* In some applications the ringed topos is refined to a [[lined topos]] when instead of a [[ring]] object an [[algebra]]-object is required.


## Related concepts

* [[ringed space]], [[ringed site]],  **ringed topos**

* [[structured (∞,1)-topos]]

## References

* [[SGA]] IV 

* M. Hakim, *Topos annel&#233;s et sch&#233;mas relatifs*, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 64, Springer, Berlin, New York (1972). 

[[!redirects ringed toposes]]

