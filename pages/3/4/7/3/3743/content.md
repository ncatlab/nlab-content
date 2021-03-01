# Rewriting
* table of contents
{: toc}

## Idea

Given an alphabet of letters and symbols (perhaps '[[type]]d', so that certain symbols are declared to be 'symbols for functions', etc., e.g. '$+$' is a symbol for a binary operation), then one can form [[list|strings]] of letters to give words or more generally (well formed) formulae involving symbols of all types. 

In a _rewriting system_, one specifies a set of rules that describe valid replacements of subformulae by other ones. On some formulae of a rewriting system, the rewriting rules may produce conflicts, when two or more rules can be applied.


+-- {: .un_example}
###### Example type
One type of example of a rewriting system is given by a [[group presentation]], $(X,R)$, where $X$ is a set of generators for a group $G$ and $R$ is a subset of pairs of elements in the free group on $X$.  As a definite example, take 
 
* $X = \{a,b\}$

* $R = \{(a a a,1),(b b,1),(a b a b,1)\}$

(and the group being presented is the symmetric group, $S_3$ on three symbols).
We think of $(a a a,1)$ as a 'rewrite rule': ''replace $a a a$ by 1'', often written $a a a \rightsquigarrow 1$ (or just $a a a \to 1$).
 
Working with the presentation, we can then  start generating words in the generators, for instance $a a a b a b$ and then see how that word can be 'rewritten' using the rewrite rules to $b a b$ using the first rule and to $a a$ using the last. There is thus a potential conflict between these rewritten forms of the word.  
=--

It is usual to choose a '[[normal form]]' for each word.  In the example, in the symmetric group and the above presentation the elements of the group are often listed as $1, a, a^2, b, a b, a^2 b$.  These might be our choice of normal forms for the elements. In other words any element has a unique representative in the form $a^i b^j$, and we _choose_ to label them that way. With the two uses of the rules applied to $a a a b a b$, the first did not gave a normal form, the second did.


In order to transform a rewriting system into a computation [[algorithm]], one needs to apply the rules in a deterministic way, using a reduction strategy. We also need to know that there is a unique normal form that can be found for each word and that the 'algorithm' will _terminate_, that is it really _is_ an algorithm!. 

We therefore will need to discuss [[confluence]], [[termination]] and [[reduction strategy|reduction strategies]].


## References

* wikipedia: [Rewriting](http://en.wikipedia.org/wiki/Rewriting)

A classical foundational paper is 

* Axel Thue,  Probleme &#252;ber Ver&#228;nderungen von Zeichenreihen nach gegebenen Regeln., Kristiania Vidensk. Selsk, Skr. (1914), no. 10, 493&#8211;524.

A key lemma is given in the beautiful paper:

* [[Max Newman|Maxwell Herman Alexander Newman]], _On theories with a combinatorial definition of "equivalence"_, Annals of Mathematics __43__ (1942), no. 2, 223&#8211;243. 

For good references on word rewriting see

*  Ronald V. Book, Friedrich Otto, _String-rewriting systems_, Texts and Monographs in Computer Science, 
Springer-Verlag, 1993. 

 and on term rewriting

* Franz Baader, Tobias Nipkow, _Term rewriting and all that_, Cambridge University Press, 1998. 

*   _Terese_, Term rewriting systems, Cambridge Tracts in Theoretical Computer Science, vol. 55, Cambridge University Press, 2003. 


For the higher dimensional forms of rewriting, one source is in the work of Guiraud and Malbos:

* [[Yves Guiraud]], [[Philippe Malbos]], _Identities among relations for higher-dimensional rewriting systems_, S&#233;minaires et Congr&#232;s, SMF, (to appear), [arXiv:0910.4538](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.4538v2.pdf); _Higher-dimensional categories with finite derivation type_, Theory Appl. Categ. __22__
(2009), No. 18, 420&#8211;478, [tac](http://www.tac.mta.ca/tac/volumes/22/18/22-18abs.html); pdf slides [Homotopical methods in polygraphic rewriting](http://ljk.imag.fr/membres/Dominique.Duval/CCS09/CCS09-Malbos.pdf), [n-Cat&#233;gories de type de d&#233;rivation fini](http://www.loria.fr/~guiraudy/exposes/ntdf-luminy.pdf).

This also includes emerging _homotopical theory of computation_ based on [[polygraph]]s (introduced by [[Albert Burroni]]) and polygraphic resolutions (introduced by [[François Métayer]]):

* Yves Lafont, _Algebra and geometry of rewriting_, Applied Categorical Structures
August __15__:4, 2007, pp 415-437  [doi](http://dx.doi.org/10.1007/s10485-007-9083-6
)


Again within the context of higher dimensional forms of rewriting, [[Tibor Beke]] has given a categorification of certain rewriting procedures of Knuth. This is of relevance here as it contains a strong result on coherence theory:

* [[Tibor Beke]], _Categorification, term rewriting and the Knuth-Bendix procedure_, J. Pure and Applied Algebra 215:5 (2011) 728-740 ([pdf](http://faculty.uml.edu/tbeke/knuth.pdf) at author's page) [doi:10.1016/j.jpaa.2010.06.019](https://doi.org/10.1016/j.jpaa.2010.06.019)

There is a preprint by [[Samuel Mimram]]

* _Towards 3-Dimensional Rewriting Theory_, ([arXiv:1403.4094](https://arxiv.org/abs/1403.4094))

An approach via diagrammatic sets is in

* [[Amar Hadzihasanovic]], _Diagrammatic sets and rewriting in weak higher categories_, ([arXiv:2007.14505](https://arxiv.org/abs/2007.14505))

with slides (for GeoCat 2020), [here](https://www.irif.fr/~ahadziha/files/talk-geocat-rewriting.pdf).

* N. Ghani, C. Lüth, _Rewriting via coinserters_,  Nordic Journal of Computing 10 (2003) 290–312 [pdf](http://www.informatik.uni-bremen.de/~clueth/awe/papers/njc04b.pdf)

category: combinatorics, algebra, computer science, logic
[[!redirects rewriting]]
[[!redirects rewriting system]]
[[!redirects rewriting systems]]
[[!redirects rewriting procedure]]
[[!redirects rewriting procedures]]
