# Rewriting
* table of contents
{: toc}


## Idea
Given an alphabet of letters and sybols (perhaps 'typed', so that certain symbols are peprhaps declared to be 'symbols for functions', e.g. '$+$ is a symbol for a binary operation', then one can form strings of letters to give words or more generally (well formed) formulae involving symbols of all types. 

In a rewriting system, one specifies a set of rules that describe valid replacements of subformulae by other ones


+-- {: .un_example}
####Example type
One type of example of a rewriting system is given by a [[group presentation]], $(X,R)$, where $X$ is a set of generators for a group $G$ and $R$ is a subset of pairs of elements in the free group on $X$.  As a definite example, take 
 
* $X = \{a,b\}$

* $R = \{(a a a,1),(b b,1),(a b a b,1)\}$

(and the group being presented is the symmetric group, $S_3$ on three symbols).
We think of $(a a a,1)$ as a 'rewrite rule': ''replace $a a a$ by 1'', often written $a a a\to 1$.
 
Working with the presentation, we can then  start generating words in the generators, for instance $a a a b a b$ and then see how that word can be 'rewritten' using the rewrite rules to $b a b$ using the first rule and to $a a$ using the last. There is thus a potential conflict between these rewritten forms of the word.  In rewriting theory this sort of situation is studied in detail.
=--

## References

For a general reference see

* wikipedia: [Rewriting](http://en.wikipedia.org/wiki/Rewriting)

A classical foundational paper is 

* A. Thue,  Probleme &#252;ber Ver&#228;nderungen von Zeichenreihen nach gegebenen Regeln., Kristiania Vidensk. 
Selsk, Skr. (1914), no. 10, 493&#8211;524.

A key lemma is given in the beautiful paper:

* Maxwell Herman Alexander Newman, On theories with a combinatorial definition of "equivalence", Annals 
of Mathematics 43 (1942), no. 2, 223&#8211;243. 



Some recent results on rewriting are to be fund in Tibor Beke's categorification of certain rewriting procedures of Knuth. It is of relevance for $n$lab as it contains a strong result on coherence theory:

* Tibor Beke, [Categorification, term rewriting and the Knuth-Bendix procedure](http://faculty.uml.edu/tbeke/knuth.pdf)


[[!redirects rewriting]]
[[!redirects rewriting system]]
[[!redirects rewriting systems]]
[[!redirects rewriting procedure]]
[[!redirects rewriting procedures]]
