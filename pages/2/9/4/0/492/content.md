#Definition#

A _Kan fibration_ is a [[morphism]] $\pi : Y \to X$ of [[simplicial set|simplicia sets]] with the [[lifting property]] for all [[horn]] inclusions.

This means that for 

$$
 \array{
   \Lambda^k[n] &\to& Y
   \\
   \downarrow && \downarrow^\pi
   \\
   \Delta^n &\to& X
 }
$$

a commuting square, there always exists a lift

$$
 \array{
   \Lambda^k[n] &\to& Y
   \\
   \downarrow &\nearrow& \downarrow^\pi
   \\
   \Delta^n &\to& X
 }
 \,.
$$

#Quasi-fibration#

A _quasi-fibration_ of simplicial sets is defined as above, but with the lifting property only imposed in _inner horns_: $\Lambda^k[n]$ with $0 \lt k \lt (n-1)$.


#Relation to other concepts#

* Kan fibrations and quasi-fibrations are fibrations in two common [[model structure on simplicial sets|model structures on simplicial sets]].

* Recall that the [[horn]] $\Lambda^k[n]$ is the boundary of the $n$-[[simplex]] $\Delta^n$ with one face removed. If in the above definiion one replaces horns with the full boundaries of simplices, one obtaines the definition of a [[hypercover]], the acyclic fibrations in the classical [[model structure on simplicial sets]].

* A simplicial set $X$ for which the unique morphism $X \o pt$ to the [[terminal object|terminal simplicial set]] is a Kan fibration is called a [[Kan complex]].

* A simplicial set $X$ for which the unique morphism $X \o pt$ to the [[terminal object|terminal simplicial set]] is a weak Kan fibration is called a [[quasi-category]].
