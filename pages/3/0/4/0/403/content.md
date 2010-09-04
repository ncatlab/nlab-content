
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents
{:toc}

## Idea

The notion of a [[category]] can be formulated [[internalization|internal]] to any other category with enough [[pullback|pullbacks]]. By regarding [[group|groups]] as one-object [[groupoid|groupoids]], this generalizes the familiar way in which, for instance

 * topological groups are groups _internal to [[topological space]]s_
 
 * Lie groups are groups _internal to [[smooth manifold]]s_.

There is a more general notion of an [[internal category in a monoidal category]], where the pullbacks are replaced by cotensor products.

##Definition

Let $A$ be any category. A **category internal to $A$** consists of 

* an object of objects $C_0 \in A$;

* an object of morphisms $C_1 \in A$;

together with

* [[source]] and [[target]] morphisms $s,t: C_1 \to C_0$;

* an [[identity-assigning morphism]] $e: C_0 \to C_1$;

* a [[composition]] morphism $c: C_1 \times_{C_0} C_1 \to C_1$;

such that the following diagrams commute, expressing the usual category laws:

* laws specifying the source and target of identity morphisms:

$$
\array{
C_0 & \stackrel{e}{\to} & C_1 \\
{}  & 1\searrow         & \darr s \\
{}  & {}                & C_0
}
\quad\quad\quad\quad
\array{
C_0 & \stackrel{e}{\to} & C_1 \\
{}  & 1\searrow         & \darr t \\
{}  & {}                & C_0
}
$$

* laws specifying the source and target of composite morphisms:

$$
\array{
C_1 \times_{C_0} C_1 & \stackrel{c}{\to} & C_1 \\
{}^{p_1}\downarrow   & {}                & \downarrow^{s} \\
C_1                  & \stackrel{s}{\to} & C_0
}
\quad\quad\quad\quad
\array{
C_1 \times_{C_0} C_1 & \stackrel{c}{\to} & C_1 \\
{}^{p_2}\downarrow   & {}                & \downarrow^{t} \\
C_1                  & \stackrel{t}{\to} & C_0
}
$$

* the associative law for composition of morphisms:

$$
\array{
C_1 \times_{C_0} C_1 \times_{C_0} C_1 & \stackrel{c\times_{C_0} 1}{\to} & C_1 \times_{C_0} C_1 \\
{}^{1\times_{C_0}c}\downarrow         & {}                              & \downarrow^{c} \\
C_1 \times_{C_0} C_1                  & \stackrel{c}{\to}               & C_1
}
$$

* the left and right unit laws for composition of morphisms:

$$
\array{
C_0 \times_{C_0} C_1  & \stackrel{e \times_{C_0} 1}{\to} &
 C_1 \times_{C_0} C_1 & \stackrel{1 \times_{C_0} e}{\leftarrow} & C_1 \times_{C_0} C_0 \\
{}                    & {}^{p_2}\searrow                 & \downarrow^{c}       & \swarrow^{p_1}                          & {} \\
{}                    & {}                               & C_1                  & {}                                      & {}
}
$$

Here, the pullback $C_1 \times_{C_0} C_1$ is defined via the square
$$
\array{
C_1 \times_{C_0} C_1 & \stackrel{p_2}{\to} & C_1 \\
{}^{p_1}\downarrow   & {}                  & \downarrow^{s} \\
C_1                  & \stackrel{t}{\to}   & C_0
}
$$

Notice that inherent to this definition is the assumption that the pullbacks involved actually exist. This holds automatically when the [[ambient category]] $A$ has finite [[limit|limits]], but there are some important examples such as $A =\,$ [[Diff]] where this is not the case.  Here it is helpful to assume simply that $s$ and $t$ have all pullbacks; in the case of $Diff$ this occurs if they are submersions.

A [[groupoid]] internal to $A$ is all of the above 

 * such that the cartesian product $C_1 \times C_1$ exists

 * with a morphism
  $$
     C_1 \stackrel{i}{\to} C_1
  $$


 * such that
   $$
     \array{
        C_1 &\stackrel{diag}{\to}& C_1 \times C_1
        \\
        \downarrow^s && \;\;\;\;\;\;\;
           \downarrow^{c \circ (Id \times i)}
        \\
        C_0 &\stackrel{e}{\to}& C_1
     }
   $$

 * and
   $$
     \array{
        C_1 &\stackrel{diag}{\to}& C_1 \times C_1
        \\
        \downarrow^t && \;\;\;\;\;\;\;
           \downarrow^{c \circ (i \times Id)}
        \\
        C_0 &\stackrel{e}{\to}& C_1
     }
   $$

### Alternative definition

If $A$ has all pullbacks, then we can form the bicategory $Span(A)$ of [[span|spans]] in $A$.  A category in $A$ is precisely a [[monad]] in $Span(A)$.  The underlying 1-cell is given by the span $(s,t) : C_0 \leftarrow C_1 \to C_0$, and the pullback $C_1 \times_{C_0} C_1$ is the vertex of the composite span $(s,t) \circ (s,t)$.  The morphisms $e$ and $c$ are required to be morphisms of spans, which is equivalent to imposing the source and target axioms above.  Finally the unit and associativity axioms for monads imply those above.

This approach makes it easy to define the notion of [[internal profunctor]].


## Examples

A [[small category]] is a category internal to [[Set]].  In this case, $C_0$ is a set of objects and $C_1$ is a set of morphisms and the pullback is a subset of the [[Cartesian product]].

Historically, the motivating example was (apparently) the notion of [[Lie groupoids]]: a small Lie groupoid is a [[groupoid]] internal to the category [[Diff]] of [[smooth manifolds]]. This generalises immediately to a [[Lie category]]. Similarly, a [[topological groupoid]] is a groupoid internal to [[Top]]. (Warning: the term 'topological category' usually means a [[topological concrete category]], an unrelated notion. Sometimes a 'topological category' is defined to be a $Top$-[[enriched category]], which is a special case of the internal definition if it is interpreted [[strict category|strictly]] and the collection of objects is small.)  In these examples, $C_0$ is a "space of objects" and $C_1$ a "space of morphisms".

Further examples:
* A [[cocategory]] in $C$ is a category internal to $C^{op}$.
* A [[double category]] is a category internal to [[Cat]]. 
* A [[double bicategory]] is a category internal to [[Bicat]] (in a suitably weak sense).
* A [[crossed module]] is equivalent to a category internal to [[Grp]].
* A [[Baez-Crans 2-vector space]] is a category internal to [[Vect]].


## Internal functors

Functors between internal categories are defined in a similar fashion. See [[functor]].  But if the ambient category does not satisfy the [[axiom of choice]] it is often better to use [[anafunctor|anafunctors]] instead; this makes sense when $C$ is a [[superextensive site]].


## Internal nerve

The idea of the nerve of a small category can be generalised to give an *internal nerve* construction. Recall (from [[nerve]]), the basic idea is that, for a small category, $D$, its nerve, $N(D)$, is a simplicial set whose set of $n$-simplices is the set of sequences of composable morphisms of length $n$ in $D$. This set can be given by a (multiple) pullback of copies of $D_1$.  That description will carry across to give a nerve construction for an internal category.  

If $C$ is an internal category in some category $A$, (which thus has, at least, the pullbacks required for the constructions to make sense),its nerve $N(C)$ (or if more precision is needed $N_{int}(C)$, or similar) is the [[simplicial object]] in $A$ with 

 * $N(C)_0 = C_0$, the 'object of objects' of $C$;
 * $N(C)_1  = C_1$, the 'object of arrows' of $C$;
 * $N(C)_2 = C_1 \times_{C_0} C_1$ the object of [[composable pairs]] of arrows of $C$;
* $N(C)_3 = C_1 \times_{C_0} C_1\times_{C_0} C_1$, the object of composable triples of arrows;

and so on.  Face and degeneracy morphisms are induced from the structural moprhisms of $C$ in a fairly obvious way.

Internal functors between internal categories induce simplicial morphisms between the corresponding nerves.

###Example
A 2-group is an internal category in [[Grp]] and so has an internal nerve, which is a simplicial object in [[Grp]], that is  a [[simplicial group]].  If the 2-group corresponds to a [[crossed module]],$(C\stackrel{\delta}{\to}P)$, then the simplicial group nerve of $(C\stackrel{\delta}{\to}P)$ has [[Moore complex]] having $P$ in dimension 0, and $C$ in dimension 1, with the trivial group in all other dimensions. The only possible non-trivial boundary map from dimension 1 to dimension 0 is then the boundary $\delta$ of the crossed module. 

## Higher internal category

One can also look at this in [[higher category theory]] and consider internal [[n-category|n-categories]]. See

* [[internal infinity-groupoid]].




## Literature

[...]

Jean Pradines, _In [[Ehresmann]]'s footsteps: from Group Geometries to Groupoid Geometries_ [	arXiv:0711.1608](http://arxiv.org/abs/0711.1608)

Baez & Crans, _[Higher-Dimensional Algebra VI: Lie 2-Algebras](http://arxiv.org/abs/math/0307263)_

[...]

## Discussion

Previous versions of this entry led to the following discussions

+--{: .query}
I think things are mutliply inconsistent in this entry.
I do not want to change as I do not know what the intentional notation to start with was. If $p_1; s = p_2; t$ that mean that target is read at the left-hand side (composition as o, not as ;), while the diagrams before that suggest left to right composition. Then finally the diagram for groupoids has $s$ both for source and inverse, and there is only for right inverse, and one should also check convention, once it is decided above.-Zoran

You\'re right; I think that I caught all of the inconsistencies now.  Incidentally, one needs only inverses on one side (as long as *all* such inverses exist), although it\'s probably best to put both in the definition.  (For groupoids, one also needs only identities on that same side too!  [This proof](http://en.wikipedia.org/wiki/Elementary_group_theory#Alternative_Axioms) generalises.)  ---Toby
=--


+--{: .query}

Question: I've looked at the definition of category in $A$ for a while and still haven't been able to absorb it. Could we walk through an explicit example, e.g. "This is exactly what $C_0$ is, this is exactly what $C_1$ is, this is exactly what $s,t,i$ are, and this is how it relates to the more familiar context"? For example, an [[algebra]] is a monoid in $Vect$. I'll try to step through it myself, but it will probably need some correcting. - [[Eric Forgy|Eric]]

Eric, one example to ponder is: how is an internal category in [[Grp]] the "same" as a [[crossed module]]? As a partial hint, try to convince yourself that given a internal category, part of whose data is $(C_1, C_0, s, t)$, the group $C_1$ of arrows can be expressed as a semidirect product with $C_0$ acting on $\ker(s)$. The full details of this exercise may take some doing, but it might also be enjoyable; if you get stuck, you can look at [Forrester-Barker](http://arxiv.org/PS_cache/math/pdf/0212/0212065v1.pdf). - [[Todd Trimble|Todd]]

_[[Urs Schreiber|Urs]]_: I don't know, but maybe Eric should first convince himself of what Todd may find too obvious: how the above definition of an internal category reproduces the ordinary one when one works internal to [[Set]]. Eric, is that clear? If not, let us know where you get stuck!

_[[Tim Porter|Tim]]_: I have just had a go at [[2-group]] and looked at the relationship between 2-groups and crossed modules in a little more detail, in the hope it will unbug the definition for those who have not yet 'groked' it.

_[[Eric Forgy|Eric]]_: Oh thanks guys. I will try to understand how a small category is a category internal to Set first and then move on to category in Grp and the stuff Tim wrote. I'm sure this is all obvious, but don't underestimate my ability to not understand the obvious :)

_[[Eric Forgy|Eric]]_: Ok. Duh. It is pretty obvious for Set EXCEPT for pullback. Pullbacks in Set are obvious, but what about other cases? Why is that important and what is an example where there are not pullbacks?  In other words, is there an a example of something that is ALMOST a category in some other category except it doesn't have pullbacks, so is not? 

_[[Tim Porter|Tim]]_: If I remember rightly the important case is when trying to work on 'smooth categories', that is, general internal categories in a category of smooth manifolds.  Unless you take care with the source and target maps, the pullback giving the space of composible pairs of arrows may not be a manifold. (I remember something like this being the case in Pradines work in the area.) The point is then that one works with internal categories with extra conditions on $s$ and $t$ to ensure the pullback is there when you need it.

_[[Toby Bartels|Toby]]_: Usually in the theory of Lie groupoids, they require $s$ and $t$ to be submersions, which guarantees that the pullback of *any* map along them exists.
=--


[[!redirects internal groupoid]]
[[!redirects internal categories]]
[[!redirects internal groupoids]]
[[!redirects category internal]]
[[!redirects groupoid internal]]
[[!redirects categories internal]]
[[!redirects groupoids internal]]