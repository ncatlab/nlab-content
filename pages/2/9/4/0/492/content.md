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


#Relation to other concepts#

* Recall that the [[horn]] $\Lambda^k[n]$ is the boundary of the $n$-[[simplex]] $\Delta^n$ with one face removed. If in the above definiion one replaces horns with the full boundaries of simplices, one obtaines the definition of a [[hypercover]].

* A simplicial set $X$ for which the unique morphism $X \o pt$ to the [[terminal object|terminal simplicial set]] is a Kan fibration is called a [[Kan complex]].
---
The geometric realization of a Kan fibration is a Serre fibration. Proved by Quillen in a very short paper.

nLab page on [[nlab:Kan fibration]]
