
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The **join** $S \star T$ of two [[simplicial set]]s $S$ and $T$ is a new simplicial set that may geometrically be thought of as a [[cone]] over $T$ with tip of shape $S$. 

If the simplicial sets in question are [[quasi-categories]] the notion of join on them produces the notion of [[join of quasi-categories]] that underlies many constructions in [[higher category theory]] such as the definition of [[limit in a quasi-category]].

The join of [[simplicial set]]s extends that historically given for [[simplicial complex|simplicial complexes]], cf. for instance the description and discussion in [[Spanier|Spanier's classical text]] (page 109 and then pages 114 -116). 

The adaptation of this to simplicial sets reveals a neat link with some categorical structure in the category, $\Delta_a$, of finite ordinals (including the empty one).  


## Motivating examples

When $S = \Delta^0$ is the [[point]], then the join $S \star T$ is a genuine [[cone]] over $T$. Or if $S = 2$ is the discrete two-point space, the join is the [[suspension]] of $T$.

If you take two non-coplanar line segments in $\mathbb{R}^3$ (such as $A B$ and $C D$ in the picture below), then join every point in one to every point in the other, you get a 3-simplex (the tetrahedron in the picture). You can think of this as being the union of all the cones on the first segment, with cone points on the second one. We have that the join $\Delta[1]\star \Delta[1]$ is $\Delta[3]$.

![Picture](http://upload.wikimedia.org/wikipedia/commons/b/bc/SKT20093SimplexABCD.png)

<small markdown="1">[Picture from Wikimedia Commons](http://commons.wikimedia.org/wiki/File:SKT20093SimplexABCD.png)</small>


## Definition

The objects of the _augmented_ [[simplex category]] $\Delta_a$ can be identified with the finite [[total order|totally ordered]] [[set]]s, _including_ the [[empty set]], which we write in this context as

$$
  [-1] :=  \emptyset
$$

so that then

$$
  [0] = *
$$

is the singleton set, as usual and

$$
  [1] = \{ 0 \lt 1\}
$$

and so on, so that $[n] = \{ 0 \lt \ldots \lt n\}$

This counting is off by one compared to the [[cardinality]] of these sets. 



The monoidal structure on $\Delta_a$ that we are interested in now is, at the level of the sets, just union, but we have to consider the order on that 'union'. If we have $[n]$ and $[m]$, we form the union of the two sets, where we know the order on two elements we keep it, but it we have two elements one, $i$, say, from the $[n]$ and the other, $j$, from $[m]$ we put $i\lt j$.

As an example, consider $[1] = \{ 0 \lt 1\}$ and $[2] =  \{ \overline{0} \lt \overline{1} \lt \overline{2}\}$, where the overlines are just so that we can keep track of where the different elements come from. We form the union of the two sets and the rule says that anything without an overline is less than anything with one.  This gives a linear order
$$[1]+[2] = \{0 \lt 1\lt \overline{0} \lt \overline{1} \lt \overline{2}\},$$
which is isomorphic as a poset to $[4]$. Similarly $[1]+[1] = [3]$, which helps explain the picture above.

We can thus think of the operation as the **addition of cardinalities**, but must remember that $[n]$ has $n+1$ elements. In terms of the counting 'off-by-one', this reads

$$
  ([n], [m]) \mapsto [n + m + 1]
  \,,
$$

but remember there is also the order to keep track of.

This operation extends to give the **ordinal sum** structure  on $\Delta_a$ (for details see the discussion in the entry [[simplex category]]) making it a [[monoidal category]], whose product operation is

$$
  \otimes_{join}: \Delta_a \times \Delta_a \to \Delta_a
$$
$$
  ([n], [m]) \mapsto [n + m + 1]
  \,.
$$



Now, via the general process of [[Day convolution]], this monoidal structure on $\Delta_a$ is lifted to a monoidal structure on [[presheaf|presheaves]] on $\Delta_a$, i.e. to the the category [[ASSet]] of augmented [[simplicial set]]s. This is given by the [[end|coend]] formula

$$
  \otimes_{join} : ASSet \times ASSet \to ASSet
$$
$$
  (S \otimes_{join} S')_n
  :=
  \int^{[i],[j] \in \Delta_a}
    S_i \times S'_j \cdot \Delta([n],[i] \otimes_{join} [j])
  \,.
$$

### Extension to a closed monoidal structure

This join tensor product forms part of a [[closed monoidal category|closed monoidal structure]] on the category of
augmented simplicial sets, [[ASSet]] $ := Sets^{\Delta_a^{op}}$. The [[internal hom]] is given by
$$[X, Y ]_n =ASS(X; Dec^{n+1}Y )\,,$$
where $Dec$ is the [[decalage]] functor.


### Join of non-augmented simplicial sets

The **join** of two ordinary (not augmented) [[simplicial set]]s $S$ and $S'$ is the join of their _trivial augmentation_ ($S_{-1} = S'_{-1} = pt$). This yields

$$
  (S \otimes_{join} S')_n =: (S \star S')_n := S_n \cup S'_n \cup 
   (\cup_{i+j = n-1} S_i \times S'_j)
  \,.
$$

In this form, the join is used
in [definition 1.2.8.1, p. 42](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=42) of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

for the definition of the [[join of quasi-categories]]. 




## References

(please augment this?)

The join operation was studied by P. J. Ehlers, in his thesis

* _Algebraic Homotopy in Simplicially Enriched Groupoids_, 1993, 
University of Wales Bangor, (see also the reference below and the Menagerie notes available from [[Tim Porter]]'s homepage.),

but was there ascribed to [[Jack Duskin]] and [[Don van Osdol]] in some unpublished notes.  The main ideas were derived there from earlier work of [[Bill Lawvere]].

A useful published reference is

* P. J. Ehlers and [[Tim Porter]], _Joins for (Augmented) Simplicial Sets_,  Jour. Pure Applied Algebra, 145 (2000) 37-44
([arXiv](http://arxiv.org/abs/math.CT/9904039)) .

A useful discussion emphasizing the Day convolution operation is also in section 3.1 of

* [[Dominic Verity]], _Weak complicial sets I_ ([arXiv](http://arxiv.org/abs/math/0604414))

+--{: .query}
[[Tim Porter]]:  I find the initial definition given here VERY confusing. By saying the objects of $\Delta_a$ can be identified with finite sets of cardinality $0$, $1$, $2$ ... . Of course that is true, but by saying it, the ordinal property of the objects is lost.  No explicit mention of that property is made.  Perhaps I am missing something ??? The nature of the monoidal operation as being derived from 'ordinal sum' seems to be obscured here.  I have not tried to edit it as I fear that I might disturb some insight that is important from that other point of view.

[[Urs Schreiber|Urs]]: If I remember correctly I wrote this. No, there is no deeper insight hidden here, i think you are right and I should have mentioned the ordinal sum aspect. Do I understand you well that by saying "ordinal sum" we want to indicate how the tensor product acts on morphisms, is that the point you are making?

Please go ahead and edit this entry to a form that you find satisfactory. You are clearly the expert here.

[[Tim Porter|Tim]]:  Will do ... tomorrow. I am constrained by havng broken my glasses / spactacles which means typing is a pain (literally).
=--