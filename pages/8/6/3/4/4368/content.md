# Gabriel--Ulmer duality
* table of contents
{: toc}


## The idea

**Gabriel--Ulmer duality** says that there is an [[equivalence of categories|equivalence]] of [[2-categories]] (or in other words, a [[biequivalence]]) 

$$ 
\begin{matrix}
Lex^{op} & \to &  LFP \\
  C      & \mapsto & Lex(C, Set) 
\end{matrix}
$$

where [[Lex]] is the 2-category of:

* small [[finitely complete categories]], 

* finite limit preserving functors, and 

* natural transformations, 

and LFP is the 2-category of 

* [[locally finitely presentable categories]], 

* finitary right adjoint functors and 

* natural transformations.

The idea is that an object $C \in Lex$ can be thought of as an [[essentially algebraic theory]], which has a category of [[model|models]] $Lex(C,Set)$.  Gabriel--Ulmer duality says that this category of models is locally finitely presentable, all LFP categories arise in this way, and we can recover the theory $C$ from its category of models.


## References

The original source is:

* Peter Gabriel, Friedrich Ulmer, _Lokal Praesentierbare Kategorien_, Springer Lecture Notes in Mathematics **221**, Berlin, 1971. 

Some other general treatments of Gabriel--Ulmer duality (and generalizations to other [[doctrine|doctrines]]):

* C. Centazzo, E. M. Vitale, _A duality relative to a limit doctrine_, Theory and Appl. of Categories __10__, No. 20, 2002, 486&#8211;497, [pdf](http://www.tac.mta.ca/tac/volumes/10/20/10-20.pdf)

* [[Stephen Lack]], John Power, _Gabriel--Ulmer duality and Lawvere Theories enriched over a general base_, [pdf](http://www.scm.uws.edu.au/~stevel/papers/jfp.pdf)

* M. Makkai, A. Pitts, _Some results on locally finitely presentable categories_, Trans. Amer. Math. Soc. __299__ (1987), 473-496, [MR88a:03162](http://www.ams.org/mathscinet-getitem?mr=869216), [doi](http://dx.doi.org/10.2307/2000508), [pdf](http://www.ams.org/journals/tran/1987-299-02/S0002-9947-1987-0869216-2/S0002-9947-1987-0869216-2.pdf)

For a 2-dimensional analogue see the slides from a 2010 talk by Makkai: [pdf](http://www.math.mcgill.ca/makkai/scans/2010Washington0001.pdf)

For a connection to Tannaka theory see

* ncafe discussion [here](http://golem.ph.utexas.edu/category/2011/07/doctrinal_and_tannakian_recons.html)
* [[Brian Day]], _Enriched Tannaka duality_, JPAA __108__ (1996) 17-22

[[!redirects Gabriel-Ulmer duality]]
[[!redirects Gabriel–Ulmer duality]]
[[!redirects Gabriel--Ulmer duality]]
