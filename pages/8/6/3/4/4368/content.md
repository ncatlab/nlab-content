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

* Peter Gabriel and Friedrich Ulmer, _Lokal Praesentierbare Kategorien_, Springer Lecture Notes in Mathematics **221**, Berlin, 1971. 

For some nice general treatments of Gabriel--Ulmer duality and its generalizations, see:

* C. Centazzo and E. M. Vitale, A duality relative to a limit doctrine.  ([web](http://www.tac.mta.ca/tac/volumes/10/20/10-20.pdf))

* Stephen Lack and John Power, Gabriel--Ulmer duality and Lawvere Theories enriched over a general base.  ([web](http://www.scm.uws.edu.au/~stevel/papers/jfp.pdf))


[[!redirects Gabriel-Ulmer duality]]
[[!redirects Gabriel–Ulmer duality]]
[[!redirects Gabriel--Ulmer duality]]
