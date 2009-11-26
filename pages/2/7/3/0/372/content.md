
#Contents#
* automatic table of contents goes here
{:toc}


## Definition ##

An **initial object** in a [[category]] $C$ is an [[object]] $\emptyset$ such that for any object $x$ of $C$, there is a unique [[morphism]] $!:\emptyset\to C$.  An initial object, if it exists, is unique up to unique [[isomorphism]], so we speak of [[the]] initial object.

An initial object may also be called _coterminal_, _universal initial_, _co-universal_, or simply _universal_.

Initial objects are the [[duality|dual]] concept to [[terminal object]]s: an initial object in $C$ is the same as a terminal object in $C^{op}$.  An object that is both initial and terminal is called a [[zero object]].


## Examples ##

* An initial object in a [[partial order|poset]] is a [[bottom]] element.

* The [[empty set]] is an initial object in [[Set]].

* Likewise, the empty category is an initial object in [[Cat]], the empty space is an initial object in [[Top]], and so on.

* The trivial group is the initial object (in fact, the zero object) of [[Grp]] and [[Ab]].

* The integers are the initial object of [[Ring]].


## Strict initial objects

An initial object $\emptyset$ is called **strict** if any morphism $x\to \emptyset$ must be an [[isomorphism]].  The initial objects of a poset, of $Set$, $Cat$, $Top$, and of any [[topos]] (in fact, any [[extensive category]]) are strict.  At the other extreme, a [[zero object]] is only a strict initial object if the category is trivial (equivalent to the [[terminal category]]).


[[!redirects initial]]
[[!redirects coterminal object]]