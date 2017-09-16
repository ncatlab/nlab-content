

#Definition#

The objects of the _augmented_ [[simplex category]] $\Delta_a$ can be identified with finite sets of cardinality $0$, $1$, $2$ .... The operation of addition of natural numbers extends to the structure of a [[monoidal category]] on $\Delta_a$:

Using the ordinary notation for the objects of the simplex category, this product acts as

$$
  \otimes_{join}: \Delta_a \times \Delta_a \to \Delta_a
$$
$$
  ([n], [m]) \mapsto [n + m + 1]
  \,,
$$

where $[n] := (0 \to 1 \to \cdots \to n)$, $n \in \mathbb{N}$  is the totally ordered set with $n$-elements, as usual. In this notation one writes $[-1]$ for the object of $\Delta_a$ given by the empty set. If instead we'd use the notation

$$
  (k) := [n-1]
$$

for the objects of $\Delta_a$, where the number $k$ directly gives the cardinality of the finite set in question, 
with $k \in \mathbb{N}$, then the join tensor product on $\Delta_a$ reads more naturally:

$$
  \otimes_{join} : ([k], [l]) \mapsto (k + l)
  \,.
$$


Now, via the general process of [[Day convolution]] the monoidal structure on $\Delta_a$ is lifted to a monoidal structure on presheaves on $\Delta_a$, i.e. to the the category [[ASSet]] of augmented [[simplicial set]]s. This is given by the [[end|coend]] formula

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

##Extension to a closed monoidal structure##

This join tensor product forms part of a [[closed monoidal category|closed monoidal structure]] on the category of
augmented simplicial sets, [[ASSet]] $ := Sets^{\Delta_a^{op}}$. The [[internal hom]] is given by
$$[X, Y ]_n =ASS(X; Dec^{n+1}Y )\,,$$
where $Dec$ is the [[decalage]] functor.


##Join of non-augmented simplicial sets##

The **join** of two ordinary (not augmented) [[simplicial set]]s $S$ and $S'$ is the join of their _trivial augmentation_ ($S_{-1} = S'_{-1} = pt$). This yields

$$
  (S \otimes_{join} S')_n =: (S \star S')_n := S_n \cup S'_n \cup 
   (\cup_{i+j = n-1} S_i \times S'_j)
  \,.
$$

In this form, the join is used
in [definition 1.2.8.1, p. 42](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=42) of

* J. Lurie, _Higher topos theory_ ([arXiv](http://arxiv.org/abs/math.CT/0608040))


##Some history## 

(please augment this?)

This join was studied by P. J. Ehlers, in his thesis

_Algebraic Homotopy in Simplicially Enriched Groupoids_, 1993, 
University of Wales Bangor, (see also the reference below),

but was there ascribed to Jack Duskin and Don van Osdol in some unpublished notes.  The main ideas were derived there from earlier work by Bill Lawvere.


#References#

* P. J. Ehlers and [[Tim Porter]], _Joins for (Augmented) Simplicial Sets_,  Jour. Pure Applied Algebra, 145 (2000) 37-44
([arXiv](http://arxiv.org/abs/math.CT/9904039)) .

A useful discussion emphasizing the Day convolution operation is also in section 3.1 of

* Dominic Verity, _Weak complicial sets I_ ([arXiv](http://arxiv.org/abs/math/0604414))

+--{: .query}
[[Tim Porter]]:  I find the initial definition given here VERY confusing. By saying the objects of $\Delta_a$ can be identified with finite sets of cardinality $0$, $1$, $2$ ... . Of course that is true, but by saying it, the ordinal property of the objects is lost.  No explicit mention of that property is made.  Perhaps I am missing something ??? The nature of the monoidal operation as being derived from 'ordinal sum' seems to be obscured here.  I have not tried to edit it as I fear that I might disturb some insight that is important from that other point of view.

[[Urs Schreiber|Urs]]: If I remember correctly I wrote this. No, there is no deeper insight hidden here, i think you are right and I should have mentioned the ordinal sum aspect. Do I understand you well that by saying "ordinal sum" we want to indicate how the tensor product acts on morphisms, is that the point you are making?

Please go ahead and edit this entry to a form that you find satisfactory. You are clearly the expert here.

=--