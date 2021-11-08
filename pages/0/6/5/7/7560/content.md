
# Ordinal sums
* table of contents
{: toc}

## Idea

In [[ordinal arithmetic]], the ordinal sum is a natural addition on ordered sets.  This is particularly well behaved when considering _finite_ ordinals and so provides a useful tool when manipulating [[simplicial sets]]. With infinite ordinals as well the properties are subtler and so care has to be taken.

The basic idea is that in ordinal sum you 'first put one of the two ordinals and then the other', so that the elements of the second ordinal are all bigger than those in the first one.

Restricted to $\Delta_a$ and thus to finite ordinals, the ordinal sum induces the operation of [[join of simplicial sets]] endowing the category, $sSet_+$, of augmented simplicial sets with the structure of a [[monoidal category]]. 

##Recall: Finite ordinals as simplicial sets

The objects of the _augmented_ [[simplex category]] $\Delta_a$ can be identified with the finite [[total order|totally ordered]] [[set]]s, _including_ the [[empty set]], which we write in this context as

$$
  [-1] \coloneqq \emptyset
$$

so that then

$$
  [0] = *
$$

is the singleton set, as usual and

$$
  [1] = \{ 0 \lt 1\}
$$

and so on, so that $[n] = \{ 0 \lt \cdots \lt n\}$

This counting is off by one compared to the [[cardinality]] of these sets. 

 

(We will restrict for the moment to finite ordinals and thus to the category $\Delta_a$.)

The monoidal structure on $\Delta_a$  is, at the level of the sets, just the [[disjoint union]], but we  consider the order on that union. 

##The definition (initially for finite ordinals)

If we have $[n]$ and $[m]$, we form the union of the two sets, where we know the order on two elements we keep it, but if we have two elements one, $i$, say, from the $[n]$ and the other, $j$, from $[m]$ we put $i \lt j$.

###Example 

As an example, consider $[1] = \{ 0 \lt 1\}$ and $[2] =  \{\overline{0} \lt \overline{1} \lt \overline{2}\}$, where the overlines are just so that we can keep track of where the different elements come from. We form the union of the two sets and the rule says that anything without an overline is less than anything with one.  This gives a linear order
$$[1] \oplus [2] = \{0 \lt 1 \lt \overline{0} \lt \overline{1} \lt \overline{2}\},$$
which is [[isomorphic]] as a [[poset]] to $[4]$. Similarly $[1] \oplus [1] = [3]$, which helps explain the picture of the related [[join of simplicial sets]] given there.

We can thus think of the operation as the **addition of cardinalities**, but must remember that $[n]$ has $n + 1$ elements. In terms of the counting 'off-by-one', this reads

$$
  ([n], [m]) \mapsto [n + m + 1]
  \,,
$$

but must remember there is also the order to keep track of.

This operation extends to give the **ordinal sum** structure  on $\Delta_a$ (for details see the discussion in the entry [[simplex category]]) making it a [[monoidal category]], whose monoidal product is the $\oplus$ operation described above.  Note however that $[m]\oplus [n]$ and $[n]\oplus [m]$, although isomorphic are not _naturally_ so.


##Ordinal sum in general
If we consider ordinals that may not be finite then clearly the idea of ordinal sum generalises, so, for ordinals, $\alpha$ and $\beta$,  $\alpha\oplus \beta$ is the set  $\alpha\sqcup \beta$ with total order in which elements in either part are ordered as originally, but where any $a\in \alpha$ is less than and $b\in \beta$. 

If either ordinal is infinite, this may lead to $\alpha\oplus \beta$ and $\beta\oplus \alpha$ not being isomorphic.  For instance, $[0]\oplus\omega$ is isomorphic to $\omega$ itself, but $\omega\oplus [0]$ has a greatest element, i.e. the $0$ in $[0]$-summand, so clearly there can be no isomorphism between the two ordinals.  

We thus give a *warning*: 
the [[monoidal structure]] given by ordinal sum is not a symmetric monoidal category structure even when restricted to  the subcategory of finite ordinals. If one extends to consider infinite ordinals, there may even be no order preserving maps at all from $[i] \oplus [j]$ to $[j] \oplus [i]$ for $i \neq j$, let alone isomorphisms.

## Ordinal sum of categories

In "Ordinal Sums and Equational Doctrines", Lawvere defines the **ordinal sum $A +_\sigma B$ of two categories** $A$ and $B$ as the [[pushout]]

$$
 \array{
 A \times |2| \times B &\to& A \times 2 \times B \\
 \downarrow & & \downarrow \\
 A + B &\to & A +_\sigma B
 }
$$

where $A+B$ is the [[coproduct]] of $A$ and $B$, 2 is the [[interval category]], $|2|$ is its underlying discrete category of objects, and the left vertical arrow is defined by

$$
\lang a,i,b\rang = \begin{cases}a & i = 0 \\ b & i = 1\end{cases}
$$

Concretely, $A +_\sigma B$ may be described as the category $A + B$ together with exactly one arrow $a \to b$ adjoined for every object $a \in A, b \in B$ (in other words, as the [[cograph of a profunctor|collage]] of $A$ and $B$ along the terminal profunctor). 

Equivalently, $A +_\sigma B$ may be described as the colimit of the diagram 

$$\array{
 & & A \times B & & & & A \times B & & \\
 & \mathllap{\pi_1}\; \swarrow & & \searrow \; \mathrlap{i_0} & & \mathllap{i_1}\; \swarrow & & \searrow \; \mathrlap{\pi_2} & \\ 
A & & & & A \times 2 \times B & & & & B. 
}$$

##Related entries

* [[join of categories]]

* [[join of simplicial sets]]

## References

* [[William Lawvere]], Ordinal sums and equational doctrines. In ''Seminar on Triples and Categorical Homology Theory'', LNM 80 (1969), pp. 141-155.

[[!redirects ordinal sum]]
[[!redirects ordinal sums]]
[[!redirects ordinal sum of categories]] 
[[!redirects ordinal sums of categories]]