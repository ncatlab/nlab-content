
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _local isomorphism_ in a [[presheaf]] category $PSh(S)$ is a morphism that becomes an [[isomorphism]] after passing to  [[sheaf|sheaves]] with respect to a given [[Grothendieck topology]] on $S$.

The collection of all local isomorphisms not only determines the [[Grothendieck topology]] but is precisely the collection of morphisms that are inverted when passing to sheaves. Hence local isomorphisms serve to understand [[sheaf|sheaves]] and [[sheafification]] in terms of the passage to a [[homotopy category]] of $PSh(S)$.

This is discussed in more detail at [[category of sheaves]]:

in terms of the discussion at [[geometric embedding]], local isomorphisms in $PSh(S)$ are precisely the [[calculus of fractions|multiplicative system]] $W$ that is sent to isomorphisms by the [[sheafification]] functor 

$$
  \bar{(-)} : PSh(S) \to Sh(S)
$$

which is left [[exact functor|exact]] [[left adjoint]] to the [[full and faithful functor|full and faithful]] inclusion

$$
  Sh(S) \hookrightarrow PSh(S)
  \,.
$$


## Axioms

A system of **local isomorphism**s on $PSh(S)$ is any collection of morphisms satisyfing

1. local isomorphisms are a system of [[category with weak equivalences|weak equivalences]] (i.e. every [[isomorphism]] is a local isomorphism and they satisfy 2-out-of-3);

2. a morphism is a local isomorphism if and only if its [[pullback]] along any morphism is 
$
  \array{
    U \times_X Y &\to& Y
    \\
    {}^{\mathllap{loc iso}}\downarrow
    &&
    \downarrow^{\mathrlap{\Leftrightarrow loc iso}}
    \\
    U &\to& X
  }
$


#Relation to Grothendieck topologies#

Systems of local isomorphisms on $PSh(S)$ are equivalent to [[Grothendieck topology|Grothendieck topologies]] on $S$.

The following indicates how choices of systems of local isomorphisms are equivalent to choices of systems of [[local epimorphisms]]. The claim follows by the discussion at [[local epimorphism]].

## Local epimorphisms from local isomorphisms ##

A system of [[local epimorphisms]] is defined from a system of local isomorphisms by declaring that $f : Y \to X$ is a [[local epimorphism]] precisely if $im(f) \to X$ is a local isomorphism.
 

## Local isomorphisms from local epimorphisms ##

Given a [[Grothendieck topology]] in terms of a system of [[local epimorphisms]], a system of local isomorphisms is constructed as follows.

A **local monomorphism** with respect to this topology is a morphism $f : A \to B$ in $[S^{op}, Set]$ such that the canonical morphism $A \to A \times_B A$ is a [[local epimorphism]].

A **local isomorphism** with respect to a Grothendieck topology is a morphism in $[S^{op}, Set]$ that is both a [[local epimorphism]] as well as a local monomorphism in the above sense.

#Relation to Lawvere-Tierney topologies#

Recall that [[Grothendieck topology|Grothendieck topologies]] on a [[small category]] $S$ are in bijection with [[Lawvere-Tierney topology|Lawvere-Tierney-topologies]] on $PSh(S)$ and that [[sheafification]] with respect to a [[Lawvere-Tierney topology]] is encoded in terms of monomorphisms in $PSh(S)$ which are _[[dense monomorphism|dense]]_ with respect to the [[Lawvere-Tierney topology]].

We have:

the [[dense monomorphisms]] are precisely the local isomorphisms which are also ordinary [[monomorphisms]].



#Properties#

* Local isomorphisms admit a left saturated [[calculus of fractions]].


# Sheafification #

The [[sheafification]] functor 
which sends a [[presheaf]] $F$ to its weakly 
equivalent [[sheaf]] $\bar F$
can be realized using a [[colimit]] over local
isomorphisms. See there.


#Characterization and relation to sieves#

Often one concentrates on the local isomorphisms whose codomain is a [[representable functor|representable presheaf]], i.e. those of the form

$$
  A \to Y(U)
  \,,
$$

where $U$ is an object in $S$ and $Y$ is the [[Yoneda embedding]]. These come from covering [[sieves]] of a [[Grothendieck topology]] on $S$: for $U \in S$ and $\{V_i \to U\}_i$ a covering [[sieve]] on $U$, the coresponding local isomorphism is the presheaf which is the [[image]] of the joint injection map

$$
  \sqcup_i Y(V_i) \to Y(U)
  \,.
$$

Using the fact that morphisms in a presheaf category are [[strict morphisms]], so that [[image]] and [[coimage]] coincide, it is useful, with an eye towards generalizations from [[sheaves]] to [[stacks]] and [[∞-stacks]] (see in particular [[descent for simplicial presheaves]]), to say this equivalently in terms of the [[coimage]]: the local isomorphism corresponding to the covering [[sieve]] $\{V_i \to U\}$ is

$$
  colim (
     (\sqcup_i Y(V_i))\times_{Y(U)}
     (\sqcup_i Y(V_i))
     \stackrel{\to}{\to}
     (\sqcup_i Y(V_i))
  )
  \to 
  Y(U)
$$

Notice that in general these are not _all_ the local isomorphism with representable codomain (more generally these are [[hypercovers]], where 
$(\sqcup_i Y(V_i))\times_{Y(U)} (\sqcup_i Y(V_i))$ is replaced in turn by one of its covers).


(...)


Notice that local isomorphism with codomain a representable already induce general local isomorphisms using the fact that every presheaf is a colimit of representables (the [[co-Yoneda lemma]]) and that local isomorphisms/sieves are stable under [[pullback]]:

+-- {: .un_prop}
###### Proposition

If $A \in PSh(S)$ is a [[local object]] with respect to local isomorphisms whose codomain is a representable, then every morphism $X \to Y$ of presheaves such that for every representble $U$ and every morphism $U \to Y$ the pullback
$X \times_Y U  \to U$ is a local isomorphism, the canonical morphism
$$
  Hom(Y,A) \to Hom(X,A)
$$
is an isomorphism.
=--

+-- {: .proof}
###### Proof

We may first rewrite trivially
$$
  X \simeq X \times_Y Y
$$
and then use the [[co-Yoneda lemma]] to write (suppressing notationally the Yoneda embedding)
$$
  Y \simeq colim_{U \to Y} U
$$
and hence rewrite $(X \to Y)$ as
$$
  X \times_Y (\colim_{U \to Y} U) \to colim_{U \to Y} U
  \,.
$$

Then using that colimits of presheaves are [[commutativity of limits and colimits|stable under base change]] this is
$$
  (\colim_{U \to Y}(X \times_Y U)) \to colim_{U \to Y} U
  \,.
$$

Recall that by assumption the components $X \times_Y U \to U$ of this are local isomorphisms. Hence
$$
  (Hom(Y,A) \to Hom(X,A))
  =
  lim_{U \to Y}
  Hom(U, A) \to 
  \lim_{U  \to Y}
  Hom(X \times_Y U, A)
$$
is a limit over isomorphisms, hence an isomorphism.
=--

#References#

This is in section 16.2 of

* Kashiwara-Schapira, _[[Categories and Sheaves]]_ .

See in particular exercise 16.5 there for the characterization of [[Grothendieck topology|Grothendieck topologies]] in terms of local isomorphisms.

[[!redirects local isomorphisms]]