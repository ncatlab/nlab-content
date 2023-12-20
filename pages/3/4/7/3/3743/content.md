

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

We therefore will need to discuss [[confluence]], [[normal form]], [[termination]] and [[reduction strategy|reduction strategies]].

## Related entries

* [[Globular]]

* [[abstract rewriting system]]

## References

### General

* Axel Thue,  Probleme &#252;ber Ver&#228;nderungen von Zeichenreihen nach gegebenen Regeln., Kristiania Vidensk. Selsk, Skr. (1914), no. 10, 493&#8211;524.

* [[Max H. A. Newman]], *On theories with a combinatorial definition of "equivalence"*, Annals of Mathematics **43** 2 (1942) 223-243 &lbrack;[doi:10.2307/1968867](https://doi.org/10.2307/1968867)&rbrack;

  > (proves [[Newman's lemma]])

*  Ronald V. Book, Friedrich Otto, _String-rewriting systems_, Texts and Monographs in Computer Science, 
Springer-Verlag, 1993. 


* [[Fabio Gadducci]], _On the algebraic approach to concurrent term rewriting_, PhD thesis (1996) &lbrack;[pdf](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=1277313dd2c4fce640780b7472221156579e392f), [[Gadducci-AlgebraicRewriting.pdf:file]]&rbrack;

* Franz Baader, Tobias Nipkow, _Term rewriting and all that_, Cambridge University Press (1998) &lbrack;[webpage](https://www21.in.tum.de/~nipkow/TRaAT/)&rbrack;


* [[Andrea Corradini]], [[Fabio Gadducci]], _An algebraic presentation of term graphs, via gs-monoidal categories_, Applied Categorical Structures **7** (1999) 299-331 &lbrack;[doi:10.1023/A:1008647417502](https://doi.org/10.1023/A:1008647417502)&rbrack;

  > (introducing [[gs-monoidal categories]] for term rewriting)

*   _Terese_, Term rewriting systems, Cambridge Tracts in Theoretical Computer Science, vol. 55, Cambridge University Press, 2003. 

See also:

* Wikipedia, *[Rewriting](http://en.wikipedia.org/wiki/Rewriting)*



On [[rewriting]] in [[group presentations]]:

* [[Nick Gilbert]], Emma Antonia Mcdougall, _Groupoids and the algebra of rewriting in group presentations_, Beitr&auml;ge zur Algebra und Geometrie **62** 3 (2021) 1-17 &lbrack;[doi:10.1007/s13366-020-00531-6](https://doi.org/10.1007/s13366-020-00531-6), [arXiv:1901.04348](https://arxiv.org/abs/1901.04348)&rbrack;


### Higher dimensional rewriting

For the higher dimensional forms of rewriting, one source is in the work of Guiraud and Malbos:

* [[Yves Guiraud]], [[Philippe Malbos]], _Identities among relations for higher-dimensional rewriting systems_, S&#233;minaires et Congr&#232;s, SMF, (to appear), [arXiv:0910.4538](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.4538v2.pdf); _Higher-dimensional categories with finite derivation type_, Theory Appl. Categ. __22__
(2009), No. 18, 420&#8211;478, [tac](http://www.tac.mta.ca/tac/volumes/22/18/22-18abs.html); pdf slides [Homotopical methods in polygraphic rewriting](http://ljk.imag.fr/membres/Dominique.Duval/CCS09/CCS09-Malbos.pdf), [n-Cat&#233;gories de type de d&#233;rivation fini](http://www.loria.fr/~guiraudy/exposes/ntdf-luminy.pdf).

This also includes emerging _homotopical theory of computation_ based on [[polygraph]]s (introduced by [[Albert Burroni]]) and polygraphic resolutions (introduced by [[François Métayer]]):

* Yves Lafont, _Algebra and geometry of rewriting_, Applied Categorical Structures
August __15__:4, 2007, pp 415-437  [doi](https://doi.org/10.1007/s10485-007-9083-6)



Again within the context of higher dimensional forms of rewriting, [[Tibor Beke]] has given a [[categorification]] of certain rewriting procedures of Knuth. This is of relevance here as it contains a strong result on coherence theory:

* [[Tibor Beke]], _Categorification, term rewriting and the Knuth-Bendix procedure_, J. Pure and Applied Algebra 215:5 (2011) 728-740 ([pdf](http://faculty.uml.edu/tbeke/knuth.pdf) at author's page) [doi:10.1016/j.jpaa.2010.06.019](https://doi.org/10.1016/j.jpaa.2010.06.019)

An approach via diagrammatic sets is in

* [[Amar Hadzihasanovic]], _Diagrammatic sets and rewriting in weak higher categories_, ([arXiv:2007.14505](https://arxiv.org/abs/2007.14505))

with slides (for GeoCat 2020), [here](https://www.irif.fr/~ahadziha/files/talk-geocat-rewriting.pdf).

* [[Samuel Mimram]], _Towards 3-dimensional rewriting theory_, ([arXiv:1403.4094](https://arxiv.org/abs/1403.4094))

See also:

* [[Neil Ghani]], C. Lüth, _Rewriting via coinserters_,  Nordic Journal of Computing 10 (2003) 290–312 [pdf](http://www.informatik.uni-bremen.de/~clueth/awe/papers/njc04b.pdf)

On the online proof assistant *[[Globular]]* for higher dimensional [[rewriting]] via [[semistrict]] [[globular set|globular]] [[higher categories]]:

* [[Krzysztof Bar]], [[Aleks Kissinger]], [[Jamie Vicary]], *Globular: an online proof assistant for higher-dimensional rewriting*,  Logical Methods in Computer Science **14** 1 (2018) &lbrack;[doi:10.23638/LMCS-14(1:8)2018](https://doi.org/10.23638/LMCS-14(1:8)2018), [arXiv:1612.01093](https://arxiv.org/abs/1612.01093)&rbrack;


See also:

* Nicolas Behr, [[Joachim Kock]], _Tracelet Hopf algebras and [[decomposition spaces]]_, [arXiv:2105.06186](https://arxiv.org/abs/2105.06186)

> Tracelets are the intrinsic carriers of causal information in categorical rewriting systems. In this work, we assemble tracelets into a symmetric monoidal decomposition space, inducing a cocommutative Hopf algebra of tracelets. This Hopf algebra captures important combinatorial and algebraic aspects of rewriting theory, and is motivated by applications of its representation theory to stochastic rewriting systems such as chemical reaction networks. 

The following [[machine learning]]-inspired rewriting systems for meta/hyper-graphs claim to be related to [[homotopy type theory]]

* [[Ben Goertzel]], _Reflective metagraph rewriting as a foundation for an AGI "Language of Thought"_, [arXiv:2112.08272](https://arxiv.org/abs/2112.08272)
* Xerxes D Arsiwalla, Jonathan Gorard, _Pregeometric spaces from Wolfram model rewriting systems as homotopy types_ [arXiv:2111.03460](https://arxiv.org/abs/2111.03460)

category: combinatorics, algebra, computer science, logic

[[!redirects rewriting]]
[[!redirects rewriting system]]
[[!redirects rewriting systems]]
[[!redirects rewriting procedure]]
[[!redirects rewriting procedures]]

[[!redirects rewrite rule]]
[[!redirects rewrite rules]]





