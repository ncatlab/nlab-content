
# Heaps
* table of contents
{: toc}

## Idea

A _heap_ is an algebraic structure which is basically equivalent to a [[group]] when one forgets about which element is the [[identity element|unit]].  Similar notions are [[affine space]], [[principal homogeneous space]] and so on. However, the notion of a heap has a directness and simplicity in the sense that it is formalized as an algebraic structure with only one ternary operation satisfying a short list of axioms. If we start with a group the ternary operation is defined via $(a,b,c)\mapsto a b^{-1}c$.  We can interpret that operation as shifting $a$ by the (right) translation in the group which translates $b$ into $c$.  There is also a dual version, [[quantum heap]].

Heaps in the sense of algebra should not be confused with [heaps](http://en.wikipedia.org/wiki/Heap) in the sense of theoretical computer science.  There are also a number of synonyms for the term 'heap'; below we consider 'torsor' in this light.  In Russian one term for a heap is 'груда' ('gruda') meaning a heap of soil; this is a pun as it is parallel to the russian word 'группа' ('gruppa') meaning a group: forgetting the unit element is sort of creating an amorphous version.  This term also appears in English as 'groud'. In universal algebra the standard name is __associative Malcev algebra__ (in various spellings, including Mal'cev, Mal'tsev and Maltsev), other names include __herd__.


## Definition

A __heap__ $(H,t)$ is a [[inhabited set|nonempty]] set $H$
equipped with a ternary operation $t : H \times H \times H\to H$ satisfying the relations

$$ t(b,b,c) = c = t(c,b,b)$$

$$ t(a,b,t(c,d,e)) = t(t(a,b,c),d,e) $$

More generally, a ternary operation in some [[variety of algebras]] satisfying the first pair of equations is called a [[Mal'cev operation]].  A Mal'cev operation is  called _associative_ if it also satisfies the latter equation (i.e. it makes its domain into a heap).

A **heap homomorphism**, of course, is a function that preserves the ternary operations.  This defines a category $Heap$ of heaps.


## Automorphism group

As suggested above, if $G$ is a group and we define $t(a,b,c) = a b^{-1} c$, then $G$ becomes a heap.  This construction defines a functor $Prin:Grp\to Heap$.  In fact, up to isomorphism, all heaps arise in this way; to every heap is associated a group $Aut(H)$ called its _automorphism group_, unique up to isomorphism.  There are a number of ways to define $Aut(H)$ from $H$.

1. If we choose an arbitrary element $e\in H$, then we can define a multiplication on $H$ by $a b = t(a,e,b)$.  It is straightforward to verify that this defines a group structure on $H$, whose underlying heap structure is the original one.

2. We can define $Aut(H)$ to be the set of pairs $(a,b)\in H\times H$, modulo the [[equivalence relation]] $(a,b)\sim (a',b')$ iff $t(a,a',b')=b$.  (We think of $(a,b)$ as representing $a^{-1} b$.)  We then define multiplication by $(c,d)(a,b) = (c,t(d,a,b))$; the inverse of (the [[equivalence class]] of) $(a,b)$ is (the equivalence class of) $(b,a)$ and the identity element is (the equivalence class of) $(a,a)$ (for any $a$).

3. We can also define $Aut(H)$ as an actual subgroup of the [[symmetric group]] of $H$, analogously to [[Cayley's theorem]] (see [Wikipedia](http://en.wikipedia.org/wiki/Cayley's_theorem)) for groups.  We take the elements of $Aut(H)$ to be set bijections
of the form $t(-,a,b): H \rightarrow H$
where $a,b \in H$, with composition as the group operation.  Note that
\[ t(-,c,d) \cdot_{Aut(H)} t(-, a,b) =
 t(t(-,c,d),a,b) = t(-,c,t(d,a,b)), \]
 so $Aut(H)$ is closed under this operation.  The first axiom of a  heap shows that $Aut(H)$ contains the identity $t(-,x,x)$ for any  $x$), and the inverse of $t(\cdot,a,b)$ is $t(\cdot,b,a)$; thus  $Aut(H)$ is a subgroup of the symmetric group of $H$.

Note that in both the second and third constructions, the elements of $Aut(H)$ are determined by pairs of elements of $H$, modulo some equivalence relation.  The following theorem shows that the two equivalence relations are the same.

+-- {: .un_theorem}
###### Theorem

The following are equivalent

1. bijections $t(\cdot,a,b)$ and $t(\cdot,a',b')$ are
the same maps,

2. $t(a,a',b') = b$,

3. $t(b,b',a') = a$.
=--

+-- {: .proof}
###### Proof

(ii) follows from (i) and $t(a,a,b) = b$.

(iii) follows from (ii) by applying $t(\cdot,b',a')$ on the
right. Similarly (ii) follows from (iii).

(i) follows from (ii) by the calculation:
\[ t(x,a',b') = t(t(x,a,a),a',b')= t(x,a,t(a,a',b'))
 = t(x,a,b).\]
=--

The composition laws are also easily seen to agree, so the second two constructions of $Aut(H)$ are canonically isomorphic.  To compare them to the first construction, observe that for a fixed $e\in H$, any equivalence class contains a unique pair of the form $(e,a)$.  (If $(b,c)$ is in the equivalence class, then $a$ is determined by $a = t(e,b,c)$.)  This sets up a bijection between the first two constructions, which we can easily show is an isomorphism.

The second two constructions are clearly functorial, so we have a functor $Aut:Heap\to Grp$.  Note that we have $Aut(Prin(G))\cong G$ for any group $G$, and $Prin(Aut(H))\cong H$ for any heap $H$, but while the first isomorphism is natural, the second is not.  In particular, the categories $Heap$ and $Grp$ are not [[equivalence of categories|equivalent]].


## Heaps and torsors

Note that $Aut(H)$ comes equipped with a canonical action on $H$ (this is most clear from the third definition).  This action is transitive
(by $t(a,a,b) = b$) and  free (if $t(a,b,c) = a$ then
by the previous statement $t(x,b,c) = x$ for each $x$, and in particular $t(b,b,c) = b$ and also $t(b,b,c) = c$).  Therefore, $H$ is an $Aut(H)$-[[torsor]] (over a point).  Conversely, a torsor $H$ over any group $G$ can be made into a heap, by defining $t(a,b,c) = g\cdot c$, where $g\in G$ is the unique group element such that $g\cdot b = a$.

In fact, the category $Heap$ is equivalent to the following category $Tors$: its objects are pairs $(G,H)$ consisting of a group $G$ and a $G$-torsor $H$, and its morphisms are pairs $(\phi,f):(G,H)\to (G',H')$ consisting of a group homomorphism $\phi:G\to G'$ and a $\phi$-equivariant map $f:H\to H'$.


## The empty heap {#empty}

If we wish $Heap$ to be an [[algebraic category]], then we must remove the clause that the underlying set of a heap must be nonempty.  Then the [[empty set]] becomes a heap in a unique way.  However, in this case, the various theorems relating heaps to groups above all break down.  For this reason, one usually requires a heap to be inhabited.

On the other hand, we could generalize the notion of [[group]] to allow for an empty group.  This even remains a purely algebraic notion: we can define a group as a (traditionally inhabited) [[semigroup]], with the semigroup operation denoted by [[concatenation]], equipped with a unary operation $a \mapsto a^{-1}$ satisfying these laws:

* $a a^{-1} b = b$,
* $a^{-1} a b = b$,
* $b a^{-1} a = b$,
* $b a a^{-1} = b$,

Then any possibly-empty-group is a possibly-empty-heap, and every possibly-empty-heap arises in this way from its automorphism possibly-empty-group (defined by either method (2) or (3)); the category of possibly-empty-heaps is equivalent to the category of possibly-empty-groups equipped with torsors over the point; etc.

This is even [[constructive mathematics|constructive]]; the theorems can be proved uniformly, rather than by treating the empty and inhabited cases separately. (This rather trivial method is obvious to a classical mathematician, but it\'s not constructively valid, since a possibly-empty-group/heap as defined here can\'t be constructively proved empty or inhabited; it can only be proved empty iff not inhabited.  Indeed, taking any group $G$ and any [[truth value]] $P$, the possibly-empty-subgroup $\{x \in G \;|\; P\}$ is empty or inhabited iff $P$ is false or true.)


## References and remarks

* [[Christopher D. Hollings]], [[Mark V. Lawson]], _Wagner’s Theory of Generalised Heaps_, 2017, Springer.  [doi](http://dx.doi.org/10.1007/978-3-319-63621-4)

* [[A. K. Sushkevich]], _Theory of Generalised Groups_, DNTVU, Kharkov-Kiev (1937) (in Russian).
[[А. К. Сушкевич]], _Теория обобщенных групп_, Государственное научно-техническое издательство Украины, 1937.

* G.M. Bergman, A.O. Hausknecht,
_Cogroups and co-rings in categories of associative rings_, 
Ch.IV, paragraph 22, p.95ff  -- Providence, R.I. : AMS 1996.

* Z. &#352;koda, _Quantum heaps, cops and heapy categories_, Mathematical Communications 12, No. 1, pp. 1--9 (2007); arXiv:[math.QA/0701749](http://arxiv.org/abs/math.QA/0701749)

* Thomas Booker, [[Ross Street]], _Torsors, herds and flocks_, J. Algebra 330 (2011) 346–374 [pdf](https://core.ac.uk/download/pdf/81154582.pdf) [arXiv:0912.4551](https://arxiv.org/abs/0912.4551)

* [[Peter T. Johnstone]], _The ‘closed subgroup theorem’ for localic herds and pregroupoids_, Journal of Pure and Applied Algebra 70 (1991) 97-106.  [doi](http://dx.doi.org/10.1016/0022-4049(91)90010-y).

* [wikipedia:heap](http://en.wikipedia.org/wiki/Heap_%28mathematics%29)

* [[John Baez]] on [Heaps and torsors](http://www.math.ucr.edu/home/baez/torsors.html)

There is an oidification ([[horizontal categorification]]) of a heap, sometimes called a _heapoid_. 


[[!redirects groud]]
[[!redirects grouds]]

[[!redirects heap]]
[[!redirects heaps]]
[[!redirects Heap]]
[[!redirects herd]]
[[!redirects associative Malcev algebra]]