# Rewriting
* table of contents
{: toc}


## Idea

An example of a rewriting system is given by a [[group presentation]], $(X,R)$, where $X$ is a set of generators for a group $G$ and $R$ is a subset of pairs of elements in the free group on $X$.  As a definite example, take 
 
* $X = \{a,b\}$

* $R = \{(a a a,1),(b b,1),(a b a b,1)\}$

(and the group being presented is the symmetric group, $S_3$ on three symbols).
We think of $(a a a,1)$ as a 'rewrite rule': ''replace $a a a$ by 1'', often written $a a a\to 1$.
 
Working with the presentation, we can then  start generating words in the generators, for instance $a a a b a b$ and then see how that word can be 'rewritten' using the rewrite rules to $b a b$ using the first rule and to $a a$ using the last. There is thus a potential conflict between these rewritten forms of the word.  In rewriting theory this sort of situation is studied in detail.


## References

* wikipedia: [Rewriting](http://en.wikipedia.org/wiki/Rewriting)

One of the strongest results on rewriting is Tibor Beke's categorification of certain rewriting procedures of Knuth. It is of great relevance for $n$lab as it contains a strong result on coherence theory:

* Tibor Beke, [Categorification, term rewriting and the Knuth-Bendix procedure](http://faculty.uml.edu/tbeke/knuth.pdf)


[[!redirects rewriting]]
[[!redirects rewriting system]]
[[!redirects rewriting systems]]
[[!redirects rewriting procedure]]
[[!redirects rewriting procedures]]
