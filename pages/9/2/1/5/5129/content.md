[[!redirects shuffles]]


#Contents#
* table of contents
{:toc}
 
##Idea

The term 'shuffle' conjures up the idea of shuffling a pack of cards. In fact the mathematical idea is nearer to shuffling two packs of cards one through the other. Suppose we have a pack of $p$ cards and a pack of $q$ cards and we build a pack of $p+q$ cards, whilst retaining the order on the two 'sub-packs'.  The result is a $(p,q)$-shuffle. 

## Definition

+-- {: .un_defn}
###### Definition

For $p,q \in \mathbb{N}$ two [[natural number]]s, a **$(p,q)$-shuffle** is a [[permutation]]

$$
  (\mu_1, \cdots, \mu_p, \nu_1, \cdots, \nu_q)
$$

of $(1,2, \cdots, p+q)$ subject to the condition that

$$  
  \mu_1 \lt \mu_2 \lt \cdots \lt \mu_p
$$

and

$$  
  \nu_1 \lt \nu_2 \lt \cdots \lt \nu_q
  \,.
$$

The **signature** of a $(p,q)$-shuffle is the [[signature of a permutation|signature]] of the corresponding permutation.

=--

## Applications 

### Products of simplices

Shuffles control the combinatorics of [[product]]s of [[simplices]]. See [[products of simplices]] for details.

### Eilenberg-Zilber map

Related to the product of simplices: shuffles control the [[Eilenberg-Zilber map]]. See there for details.


[[!redirects shuffles]]