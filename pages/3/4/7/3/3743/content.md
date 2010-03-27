###Idea### 

An example of a rewriting system is given by a [[group presentation]], $(X,R)$, where $X$ is a set of generators for a group $G$ and $R$ is a subset of pairs of elements in the free group on $X$.  As a definite example, take 
 
* $X = \{a,b\}$

* $R = \{(aaa,1),(bb,1),(abab,1)\}$

(and the group being presented is the symmetric group, $S_3$ on three symbols).
We think of $(aaa,1)$ as a 'rewrite rule':''replace $aaa$ by 1'', often written $aaa\to 1$.
 
Working with the presentation, we can then  start generating words in the generators, for instance $aaabab$ and then see how that word can be 'rewritten' using the rewrite rules to $bab$ using the first rule and to $aa$ using the last. There is thus a potential conflict between these rewritten forms of the word.  In rewriting theory this sort of situation is studied in detail.

###References### 

* wikipedia: [Rewriting](http://en.wikipedia.org/wiki/Rewriting)

