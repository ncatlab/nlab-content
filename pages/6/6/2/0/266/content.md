For $F : C \to D$ a functor and 
$$
 \array{
  C
  \\
  \downarrow^p
  \\
  E
 }
$$
another functor, the left (right) _Kan extension_ of $F$ along $p$ is the "push-forward" of $F$ along $p$ (left/rightadjoint to the pullback: the precomposition with $p$), namely the functor $Lan_p F$ which is universal with the property that it fits into a diagram

$$
  \array{
     C & \stackrel{F}{\to} && D
     \\
     \downarrow^p &\Downarrow& \nearrow_{Lan_p F}
     \\
     E
  }
  \,.
$$

#References#

Chapter 4 of

* G.M. Kelly, _Basic Concepts of Enriched Category Theory_, 
 Cambridge University Press, Lecture Notes in Mathematics 64, 1982,  Republished in:
Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))


I once tried to summarize some basic ideas (with pointers to pages and formulas in Kelly's book) at a blog comment [here](http://golem.ph.utexas.edu/category/2008/03/limits_and_pushforward.html#c016093).
---
For homotopy Kan extensions, see Dwyer et al: The A-complexity of a space

See also [Kan lift](http://www.ncatlab.org/nlab/show/Kan+lift) in nLab

&lt;http://www.ncatlab.org/nlab/show/Kan+extension>

nLab page on [[nlab:Kan extension]]
