A **strict epimorphism** in a [[category]] $C$ is a [[morphism]] which is the joint [[coequalizer]] of all parallel pairs that it coequalizes.  In other words, $f:B\to C$ is a strict epimorphism if it is the [[colimit]] of the (possibly large) diagram consisting of all [[parallel morphisms|parallel pairs]] $g,h:A \;\rightrightarrows\; B$ such that $f g = f h$.

If $C$ has [[pullback]]s, then any such $g,h$ factor uniquely through the [[kernel pair]] $r,s:ker(f) \;\rightrightarrows\; B$ of $f$, which is itself such a pair (that is, $f r = f s$).  Thus, for any $k:B\to D$, we have $k g = k h$ for all $g,h$ with $f g = f h$ if and only if $k r = k s$.  Therefore, $f$ is strict epi if and only if it is the coequalizer of its kernel pair, hence if and only if it is a [[regular epimorphism]].  For this reason, some sources define "regular epimorphism" in a category without pullbacks to mean what we have called a "strict epimorphism."

It is easy to see that in _any_ category, any regular epimorphism is strict.  In a category without pullbacks, it seems that not every strict epimorphism need be regular.  However, every strict epimorphism is [[strong epimorphism|strong]], and hence [[extremal epimorphism|extremal]], for the same reason that any regular epimorphism is.


+--{: .query}
[[David Roberts]]: I'm interested in a bicategorical version of this. You haven't happened to have done this Mike?

[[Mike Shulman]]: Not more than can be extracted from [[michaelshulman:2-congruence]] and [[michaelshulman:regular 2-category]].  What is there called an "eso" is the bicategorical version of a strong epi (which agrees with an extremal epi in the presence of pullbacks), and what is there called "the quotient of a 2-congruence" is the bicategorical version of a regular epi.  I've never thought about the bicategorical version of a strict epi; since strict epis agree with regular epis in the presence of finite limits I've never really had occasion to care about them independently.
=--
# References#

* [[Categories and Sheaves]], p115-116.
