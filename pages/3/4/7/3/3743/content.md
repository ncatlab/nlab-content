# Rewriting
* table of contents
{: toc}


## Idea
Given an alphabet of letters and symbols (perhaps 'typed', so that certain symbols are declared to be 'symbols for functions', etc., e.g. '$+$ is a symbol for a binary operation), then one can form strings of letters to give words or more generally (well formed) formulae involving symbols of all types. 

In a rewriting system, one specifies a set of rules that describe valid replacements of subformulae by other ones. On some formulae of a rewriting system, the rewriting rules may produce conflicts, when two or more rules can be applied.


+-- {: .un_example}
####Example type
One type of example of a rewriting system is given by a [[group presentation]], $(X,R)$, where $X$ is a set of generators for a group $G$ and $R$ is a subset of pairs of elements in the free group on $X$.  As a definite example, take 
 
* $X = \{a,b\}$

* $R = \{(a a a,1),(b b,1),(a b a b,1)\}$

(and the group being presented is the symmetric group, $S_3$ on three symbols).
We think of $(a a a,1)$ as a 'rewrite rule': ''replace $a a a$ by 1'', often written $a a a\to 1$.
 
Working with the presentation, we can then  start generating words in the generators, for instance $a a a b a b$ and then see how that word can be 'rewritten' using the rewrite rules to $b a b$ using the first rule and to $a a$ using the last. There is thus a potential conflict between these rewritten forms of the word.  
=--
It is usual to choose a 'normal form' for each word.  In the example, in the symmetric group and the above presentation the elements of the group are often listed as $1,a,a^2,b,ab,a^2b$.  These might be our choice of normal forms for the elements. In other words any element has a unique representative in the form $a^ib^j$, and we _choose_ to label them that way. With the two uses of the rules applied to $a a a b a b$, the first did not gave a normal form, the second did.


In order to transform a rewriting system into a computation algorithm, one needs to apply the rules in a deterministic way, using a reduction strategy. We also need to know that there is a unique normal form that can be found for each word and that the 'algorithm' will _terminate_, that is it really _is_ an algorithm!. 

We therefore will need to discuss [[confluence]], [[termination]] and [[reduction strategy|reduction strategies]].


## References

For a general reference see

* wikipedia: [Rewriting](http://en.wikipedia.org/wiki/Rewriting)

A classical foundational paper is 

* Axel Thue,  Probleme &#252;ber Ver&#228;nderungen von Zeichenreihen nach gegebenen Regeln., Kristiania Vidensk. 
Selsk, Skr. (1914), no. 10, 493&#8211;524.

A key lemma is given in the beautiful paper:

* Maxwell Herman Alexander Newman, On theories with a combinatorial definition of "equivalence", Annals 
of Mathematics 43 (1942), no. 2, 223&#8211;243. 

For good references on word rewriting see

*  Ronald V. Book and Friedrich Otto, String-rewriting systems, Texts and Monographs in Computer Science, 
Springer-Verlag, 1993. 

 and on term rewriting

* Franz Baader and Tobias Nipkow, Term rewriting and all that, Cambridge University Press, 1998. 

and  

*   _Terese_, Term rewriting systems, Cambridge Tracts in Theoretical Computer Science, vol. 55, Cambridge University Press, 2003. 

Some recent results on rewriting are to be found in 
Tibor Beke's categorification of certain rewriting procedures of Knuth. It is of relevance for $n$lab as it contains a strong result on coherence theory:

* Tibor Beke, [Categorification, term rewriting and the Knuth-Bendix procedure](http://faculty.uml.edu/tbeke/knuth.pdf)

and for the higher dimensional forms of rewriting

 [[Yves Guiraud]] and [[Philippe Malbos]], _Identities among relations for higher-dimensional rewriting systems,   S&#233;minaires et Congr&#232;s, SMF, (to appear), [arXiv:0910.4538](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.4538v2.pdf). 

and [slides](http://ljk.imag.fr/membres/Dominique.Duval/CCS09/CCS09-Malbos.pdf)


[[!redirects rewriting]]
[[!redirects rewriting system]]
[[!redirects rewriting systems]]
[[!redirects rewriting procedure]]
[[!redirects rewriting procedures]]
