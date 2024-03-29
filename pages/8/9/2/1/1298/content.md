In noncommutative [[ring]] theory, particularly in the subject of noncommutative [[localization]] of rings, a __kernel functor__ is any left [[exact functor|exact]] additive [[subfunctor]] of the identity functor on the category ${}_R Mod$ of left modules over a ring $R$. There is a bijective correspondence between kernel functors and [[uniform filter]]s of ideals in $R$. A functor $\sigma: {}_R Mod\to {}_R Mod$ is __idempotent__ if $\sigma\sigma = \sigma$ and a preradical if it is additive subfunctor of the identity and $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$. 
A kernel functor $\sigma: {}_R Mod\to {}_R Mod$ is said to be an __idempotent kernel functor__ if $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$; it is idempotent as we see by calculating 

$$
\sigma \sigma M = \sigma Ker(M\to M/\sigma M) = Ker (\sigma M\to \sigma(M/\sigma M)) = Ker(\sigma M\to M/\sigma M) = \sigma M
$$

In the last step, we used that $\sigma$ is a subfunctor of the identity, hence the compositions $\sigma M\hookrightarrow M\to M/\sigma M$ and $\sigma M\to \sigma(M/\sigma M)\to M/\sigma M$ coincide. 

The basic reference is 

* O. Goldman, _Rings and modules of quotients_, J. Algebra __13__, 1969 10--47, [MR245608](http://www.ams.org/mathscinet-getitem?mr=245608), [doi](http://dx.doi.org/10.1016/0021-8693%2869%2990004-0)

which is clearly written from the point of view of a ring theorist. Unfortunately, it just creates another formalism in localization theory of the categories of modules over a ring for basically the same results as [[P. Gabriel]] succeeded by more categorical formulations in his thesis published 7 years earlier. Some of the methods from Goldman, and even more from Gabriel apply for more general [[Grothendieck category|Grothendieck categories]]. 

* Pascual Jara, Alain Verschoren, Conchi Vidal, _Localization and sheaves: a relative point of view_, Pitman Research Notes in Mathematics Series, 339. Longman, Harlow, 1995. xiv+235 pp.
* J. L. Bueso, P. Jara, A. Verschoren, _Compatibility, stability, and sheaves_, Monographs and Textbooks in Pure and Applied Mathematics, 185. Marcel Dekker, Inc., New York, 1995. xiv+265 pp. 
[[!redirects kernel functors]]