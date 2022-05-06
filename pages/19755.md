
##Idea 

The set of [[permutations]] of a set, $X$, form a group, $S_X$, under composition.  This is especially clear if one thinks of the permutation as a [[bijection]] on $X$, where the multiplication / composition is just composition of functions. This group may be denoted $S_X$, $\Sigma_X$, $Sym(X)$, or $X!$.

When $X$ is [[the]] [[finite set]] $(n) = \{1,\dots,n\}$, then its symmetric group is a [[finite group]] of [[cardinality]] $n!$ = "$n$ [[factorial]]", and one typically writes $S_n$ or $\Sigma_n$. 

(We will make frequent use of the entry [[permutation]] for some key notation and concepts.)

We will concentrate on __finite symmetric groups__.

## Representation of elements.

We illustrate this by an example.

### Example : The symmetric group, $S_3$.

$S_3$ is the group of permutations of $(3)=\{1,2,3\}$.

One simple way to represent an element of $S_3$ is by listing the $(3)$ on the top row of an array with a second row denoting the image of each element under the permutation.  For instance, the element $sigma= (1\mapsto 2, 2\mapsto 1, 3\mapsto 3)$ can be written more compactly as 

$$\sigma= \left(\array{1&2&3\\2&1&3}\right).$$

We can also use, even more compactly, 'cycle notation', as explained in more detail at [[permutation]], in which successive images under the permutation, $\sigma$, are listed until you get back to where you started. Elements of (3), or more generally of (n),  are usually not listed as cycles of length 1, exept that (1) may be used too indicate the identity element. For the above permutation, this gives

$$\sigma = (12)$$

the _transposition_ exchanging the elements 1 and 2 and leaving 3 'unmoved'.  Whilst the 3-cycle, $(123)$, shifts every element to the right one position and then maps 3 to 1. 

Even in the simple example of $S_3$ one can see some patterns. 

* $(12)$ clearly has order 2, whilst $(123)$ as square $(132)$, and has order 3.

* $(123) = (12)(13)$, so transpositions generate the whole group.

This gives a listing of the elements of $S_3$ as 

$$\{ 1, (12),(13),(23),(123),(132)\}.$$

* $S_3$ has a [[group presentation|presentation]]

$$\langle a,b | a^3, b^2,(a b)^2 \rangle.$$

where $a$ corresponds to the 3-cycle, $(123)$, whilst $b$ corresponds to any transposition.  It also has a presentation in which the generatores correspond to the transpositions:

$$\langle \sigma_1,\sigma_2 | \sigma_1^2,\sigma_2^2, (\sigma_1\sigma_2)^3\rangle$$

It is easy to see that these relations imply that 

$$\sigma_1\sigma_2\sigma_1= \sigma_2\sigma_1\sigma2$$

which relates this symmetric group to the [[braid group]], **Br 3**, and to the [[trefoil knot|trefoil group]].  It is clear that there is an epimorphism $S_3\to Br_3$ obtained by making the two braid generators become the transpositions. 


##Related entries

* [[permutation]]

* [[braid group]]



##References

* [Symmetric group](https://en.wikipedia.org/wiki/Symmetric_group) in Wikipedia.




[[!redirects permutation group]]
[[!redirects permutation groups]]
[[!redirects symmetric  groups]]