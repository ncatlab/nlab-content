
# Presentations of groups
* table of contents
{: toc}

## Idea

In trying to study a [[group]] $G$, one way to proceed is to 

* look for a set of generating elements;

* look for 'relations' between those elements.

The problem is partially how one is to interpret this second part. To do this we need to look at words in the generators and hence at the [[free group]] on the set of generators.

For example, if we have the symmetric group $S_3$, or, isomorphically, the dihedral group (of symmetries of a triangle) which we will call $D_3$ (following the geometric convention (see the Wikipedia article on dihedral groups), then we have 6 elements, and they are all able to be got as products of a transposition and a three cycle (or alternatively as a reflection and a rotation).  If we call the three cycle $a$ and the transposition $b$, we have

$$S_3=\{1,a,a^2,b,a b,a^2b\}.$$

What about the other words: $ba$ for instance.  If one calculates $b a$ in $S_3$ and then looks up what you get you have $ba = a^2b$, so that there is a relation between these two words. This however is not all. What about $b a b a a b a a  a b b a a $? That is a word in the $a$s and $b$s so should represent something in $S_3$. in fact if you think in the geometric interpretation of $S_3$ as being the dihedral group, $D_3$, you can pick up  a triangle and interpret that word as a list of instructions for moving the triangle. You then find out what this word is out of the 6 possible given forms. 

For a presentation, you give a set of generators $X$, so there will be an epimorphism from $F(X)$ to $G$, and then you try to find a description for the kernel of that epimorphism, which we will denote by $N$.  The description of this normal subgroup $N$ is as the [[normal closure]] of a set $R$ of relations, i.e. words in the generators or, equally validly, elements in the free group on $X$.


## Definition

A presentation of a group, $G$, is a [[coequalizer|coequalizer diagram]] $F R \rightrightarrows F X \twoheadrightarrow G$, where $FX$ is the free group on a set of *generators*, and $FR$ one on a set of *relations* (or *relators*, depending on how the relations are specified).


This is not quite the usual `classical' form of the definition, so we will take it apart to show the relationship.

A  presentation is thus   given by a pair of sets, $X$ and $R$, written $\langle X: R\rangle$ such that setting $F=F(X)= \langle X\rangle =\langle X:\emptyset\rangle$ to be the [[free group]] on the set $X$ and $N$ the [[normal subgroup|normal closure]] of the set of relators $R$, there is a *specified* isomorphism from $F/N$ to $G$.

The specified isomorphism is often omitted, as often the set $X$ of generators is chosen as a subset of the set of elements of $G$.  In this case, the universal properties of free groups and quotients, there is a unique map $F\to G$ which restricts to the inclusion of $X$, and thereby at most one map $F/N \to G$ which does so; this map is then the one asserted to be an isomorphism.


In general it is necessary to proceed otherwise, however, and to give a specific function from a set $X$ to the set of elements of $G$.  This function then induces a group homomorphism from $F=\langle X\rangle$ to $G$, and if this is a surjection, then we can find some $N$ (generators for its kernel) to produce a presentation of $G$.  Without this extra data, certain of the manipulations of a group presntation look decidedly suspect, for instance a substitution which results in two copies of a generator being given. It is also much easier to work with morphisms of presentations if the full data is recorded.


## Examples of presentations

### The standard presentation

 A standard if somewhat trivial example of a presentation is given by the _standard presentation_ of a group, $G$.  We take $X= \{x_g\mid g\in G,g\neq 1\}$, to be a set in bijective correspondence with the underlying set of $G$. (You can take $X$ equal to that set if you like, but sometimes it is better to have a distinct set, for instance, it make for an easier notation for the description of certain morphisms.) The set of relations will be 

$$R =\{x_g.x_h= x_{gh}\mid g,h \in G\},$$ 

so as a _set_ is just a copy of $G\times G$ as the relations are indexed by pairs of elements of $G$.


### [[cyclic group|Cyclic groups]]

Cyclic group, $C_n$, of order $n$ has presentation $\langle a : a^n\rangle$.  There are many different functions from the (singleton) set of generators to  $C_n$ that will give a suitable presentation in the fuller sense.

### The [[symmetric group]] of order 6

  The group of permutations of three letters, $S_3$, has a presentation 

$$\langle a,b : a^3, b^2,(a b)^2 \rangle.$$

 Here $a$ corresponds to the 3-cycle, $(123)$, whilst $b$ corresponds to any transposition.

### [[knot group|Knot groups]] 

 The [[trefoil knot|trefoil]] [[knot group]] has two useful presentations:

  * $\langle a,b : a^3= b^2\rangle$, which displays the fact that the trefoil is a (2,3)-[[torus knot]]; and

  * $\langle x,y : x y x = y x y\rangle$, which shows the link between this group and the Artin [[braid group]], $Br3$.

### [[Coxeter groups]]

 At the entry on [[Coxeter groups]] one finds the following:

**Definition** A _Coxeter matrix_ over an index [[set]] $I$ is a symmetric [[matrix]] 

$$M \colon I \times I \to \{1, 2, 3, \ldots, \infty\}$$ 

such that $M(i, i) = 1$ for all $i \in I$, else $M(i, j) \gt 1$. Writing $m_{i,j} = M(i, j)$, the associated **Coxeter group** $W_M$ is the group presented as having generators $s_i$, $i \in I$, and relations 

$$(s_i s_j)^{m_{i, j}} = 1$$ 

for all $i, j \in I$, whenever $m_{i, j} \neq \infty$. In other words, $m_{i, j}$ is the order of $s_i s_j$ (as is easily shown), and these orders determine the group. 

We thus have an infinite family of group presentations.




## Discussion

*  *'Relations' and 'relators'*: In the discussion of $S_3$ above we had a **relation** $b a = a^2b$. so we are relating two words of $F(X)$. It is often the case that instead of relations we use **relators**, in other words a relation of form $r = 1$, where $r$ is a word in the generators. In the example $ b a = a^2b$ can be easily shown to imply and be implied by $ a b a b = 1$.


*  Given a group presentation as above, we have a 
short exact sequence,

$$1\to N \to F \to G \to 1,$$ 

where $F = F(X)$, the free group on the set $X$, $R$ is a 
subset of $F$ and $N = N(R)$ is the normal closure in $F$ of the set $R$.  The group 
$F$ acts on $N$ by conjugation: ${}^u c = ucu^{-1}, for  c\in N, u \in F$ and the 
elements of $N$ are words in the conjugates of the elements of $R$:

$$c = {}^{u_1}(r_1^{\varepsilon_1}){}^{u_2}(r_2^{\varepsilon_2})\ldots 
{}^{u_n}(r_n^{\varepsilon_n})$$

where each $\varepsilon_i$ is $ + 1$ or $ - 1$.  One also says such elements are **consequences** of 
$R$.  Heuristically an [[identity among the relations]] of $\mathcal{P}$ is such an element $c$ 
which equals 1. 


##Transformations of a group presentation##

Given a group presentation, it is natural to perform transformations using substitutions, say adding in one new symbol for a string of generators, and adjusting the presentation accordingly.  The valid transformations that do not change the group being presented are formalised as the [[Tietze transformation]]s.


## Combinatorial group theory

The study of group presentations, their transformations etc. forms part of [[combinatorial group theory]].

## Presentations of monoids and other algebraic and categorical structures.

The theory of group presentations generalises to that of presentations of monoids and then to general [[rewriting]] systems.



## References

A basic introduction to the theory of group presentations can be found in some standard texts, both on group theory itself and on related areas of low dimensional topology, for instance,


 * [[N. D. Gilbert]] and [[T. Porter]], Knots and Surfaces, Oxford U.P., 1994.


For more elementary or introductory texts, see, for instance,

* D. L. Johnson, Presentations of Groups (London Mathematical Society Student Texts 15) 1990, Cambridge Univ. Press,

or his earlier:

* D. L. Johnson, Topics in Theory of Group Presentations, London Mathematical Society Lecture notes series 42) 1980, Cambridge Univ. Press,

which have some very useful material in them.


For a deeper treatment of the area, more specialised sources are needed:

* [[Roger C. Lyndon]] and [[Paul E. Schupp]], _Combinatorial group theory_, Springer, 1977; [toc](http://elib.tu-darmstadt.de/tocs/94684782.pdf).


category: group theory

[[!redirects group presentation]]
[[!redirects group presentations]]

[[!redirects presentation of a group]]
[[!redirects presentations of a group]]
[[!redirects presentations of groups]]
