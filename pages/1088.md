#Idea#

A _local isomorphism_ in a [[presheaf]] category $PSh(S)$ is a morphism that becomes an [[isomorphism]] after passing to  [[sheaf|sheaves]] with respect to a given [[Grothendieck topology]] on $S$.

The collection of all local isomorphisms not only determines the [[Grothendieck topology]] but is precisely the collection of morphisms that are inverted when passing to sheaves. Hence local isomorphisms serve to understand [[sheaf|sheaves]] and [[sheafification]] in terms of the passage to a [[homotopy category]] of $PSh(S)$.

This is discussed in more detail at [[category of sheaves]].

#Axioms#

A system of **local isomorphism**s on $PSh(S)$ is any collection of morphisms satisyfing

1. local isomorphisms are a system of [[category with weak equivalences|weak equivalences]] (i.e. every [[isomorphism]] is a local isomorpphism and they satisfy 2-out-of-3);

2. a morphism is a local isomorphism if and only if its [[pullback]] along any morphism is 
$
  \array{
    U \times_X Y &\to& Y
    \\
    \downarrow^{loc iso}
    &&
    \downarrow^{\Leftrightarrow loc iso}
    \\
    U &\to& X
  }
$


#Relation to Grothendieck topologies#

Systems of local isomorphisms on $PSh(S)$ are equivalent to [[Grothendieck topology|Grothendieck topologies]] on $S$.

The following indicates how choices of systems of local isomorphisms are equivalent to choices of systems of [[local epimorphism]]s. The claim follows by the discussion at [[local epimorphism]].

## Local epimorphisms from local isomorphisms ##

A system of [[local epimorphism]]s is defined from a system of local isomorphisms by declaring that $f : Y \to X$ is a [[local epimorphism]] precisely if $im(f) \to B$ is a local isomorphism.
 

## Local isomorphisms from local epimorphisms ##

Given a [[Grothendieck topology]] in terms of a system of [[local epimorphism]]s, a system of local isomorphisms is constructed as follows.

A **local monomorphism** with respect to this topology is a morphism $f : A \to B$ in $[S^{op}, Set]$ such that the canonical morphism $A \to A \times_B A$ is a [[local epimorphism]].

A **local isomorphism** with respect to a Grothendieck topology is a morphism in $[S^{op}, Set]$ that is both a [[local epimorphism]] as well as a local monomorphism in the above sense.

#Relation to Lawvere-Tierney topologies#

Recall that [[Grothendieck topology|Grothendieck topologies]] on a [[small category]] $S$ are in bijection with [[Lawvere-Tierney topology|Lawvere-Tierney-topologies]] on $PSh(S)$ and that [[sheafification]] with respect to a [[Lawvere-Tierney topology]] is encoded in terms of monomorphisms in $PSh(S)$ which are _[[dense monomorphism|dense]]_ with respect to the [[Lawvere-Tierney topology]].

We have:

the [[dense monomorphism]]s are precisely the local isomorphisms which are also ordinary [[monomorphism]]s.



#Properties#

* Local isomorphisms form a left saturated [[multiplicative system]].


# Sheafification #

The [[sheafification]] functor 
which sends a [[presheaf]] $F$ to its weakly 
equivalent [[sheaf]] $\bar F$
can be realized using a [[colimit]] over local
isomorphisms. See there.


#Characterization and relation to sieves#

(...)




#References#

This is in section 16.2 of

* Kashiwara-Schapira, [[Categories and Sheaves]] .

See in particular exercise 16.5 there for the characterization of [[Grothendieck topology|Grothendieck topologies]] in terms of local isomorphisms.