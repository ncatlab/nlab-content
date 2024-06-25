
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Heaps
* table of contents
{: toc}

## Idea
 {#Idea}

In [[algebra]], a _heap_ is an algebraic [[structure]] which is almost that of a [[group]] structure but without the specification of a [[neutral element]].  

While closely related to notions such as *[[affine space]]*, *[[principal homogeneous space]]* and *[[torsor]]*, the concept of heap is simpler in the sense that it postulates just a single set with a single [[ternary]] operation obeying two [[axioms]] (see Def. \ref{TheDefinition} below).

Concretely, any [[group]] gives a heap where this ternary operation is defined from the group's [[binary operation]] $(\text{-})\cdot(\text{-})$ and [[inverse element|inversion]] $(-)^{-1}$ by 

\[
  \label{HeapOperationInAGroup}
  t
  \,\colon\,
  (a,b,c) 
  \;\mapsto\; 
  a \cdot b^{-1} \cdot c
\]  

and every heap arises this way, up to [[isomorphism]] (cf. Prop. \ref{PrinIsEssentiallySurjective} below) from a group that may be called its *[[structure group]]*.  

However, the [[category]] of heaps (Def. \ref{CategoryOfHeaps} below) is not [[equivalence of categories|equivalent]] to the [[Grp|category of groups]]. Instead:

\begin{proposition}  
The [[category]] of heaps (Def. \ref{CategoryOfHeaps}) is [[equivalence of categories|equivalent]] to the evident category of [[pairs]] consisting of a [[group]] $G$ and a $G$-torsor $H$. 
\end{proposition}
\begin{proof}
 On the one hand, for any heap $H$, choosing any element $h' \in H$, the [[endofunctions]] $t(h,h',-) \colon H \to H$ for $h \in H$ constitute a group $G$ under [[composition]], and the [[underlying]] set $H$ of the heap manifestly carries the [[structure]] of a $G$-torsor. On the other hand, given a group $G$ and a $G$-torsor $H$ we can make $H$ into a heap as follows: given elements $a,b,c \in H$ let $t(a,b,c) = g c$ where $g$ is the unique $g \in G$ with $g b = a$. 
\end{proof}

There is also a [[duality|dual]] version of the concept of heap, see at *[[quantum heap]]*.

\begin{remark}\label{Disambiguation}
**(disambiguation)**
\linebreak
Heaps in the sense of algebra should not be confused with either

* [heaps](http://en.wikipedia.org/wiki/Heap) in the sense of theoretical [[computer science]], 

nor with 

* *heaps of pieces* in the [[combinatorics|combinatorial]] sense of [Viennot 2006](https://link.springer.com/chapter/10.1007/BFb0072524).  

\end{remark}


\begin{remark}\label{Synonyms}
**(synonyms)**
\linebreak
There are also a number of synonyms for the term 'heap'; [below](#HeapsAndTorsors) we consider '[[torsor]]' in this light.  In Russian one term for a heap is 'груда' ('gruda') meaning a heap of soil; this is a pun as it is parallel to the Russian word 'группа' ('gruppa') meaning a group: forgetting the unit element is sort of creating an amorphous version.  This term also appears in English as 'groud'. In universal algebra the standard name is __associative Malcev algebra__ (in various spellings, including Mal'cev, Mal'tsev and Maltsev), other names include __herd__.
\end{remark}

There is an oidification ([[horizontal categorification]]) of heaps, sometimes called _heapoids_. 


## Definition

\begin{definition}
\label{TheDefinition}
A __heap__ $(H,t)$ is a [[inhabited set|nonempty]] [[set]] $H$ equipped with a ternary operation $t \colon H \times H \times H\to H$ satisfying the following two relations

1. $ t(b,b,c) = c = t(c,b,b)$,

1. $ t\big(a,b,t(c,d,e)\big) = t\big(t(a,b,c),d,e\big) $.

\end{definition}

More generally, a ternary operation in some [[variety of algebras]] satisfying the first pair of equations is called a [[Mal'cev operation]].  A Mal'cev operation is  called _associative_ if it also satisfies the latter equation (i.e. it makes its domain into a heap).

A heap is **abelian** if it additionally satisfies the relation
$$
  t(a,b,c) = t(c,b,a)
$$

\begin{definition}
\label{CategoryOfHeaps}
A *[[homomorphism]]* of heaps $f \colon H \to H'$ is, of course, a [[function]] of the [[underlying]] [[set]] which respects the ternary operations.  

This defines a [[category]] $Heap$ whose [[objects]] are heaps and whose [[morphisms]] are heap homomorphisms.
\end{definition}

The [[hom-sets]] of the [[full subcategory]] $AbHeap$ of abelian heaps inherit an abelian heap structure from the pointwise operation in the codomain: given $f,g,h\colon H \to G$, the function $a\mapsto t_G(f(a),g(a),h(a))$ is again a heap homomorphism. 

## Properties

### Structure groups of heaps
 {#StructureGroupsOfHeaps}

As indicated in (eq:HeapOperationInAGroup) a [[group]] $G$ becomes a heap by setting

\[
  a,b,c \,\in\, G
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  t(a,b,c) \,\coloneqq\, a \cdot b^{-1} \cdot c
  \,.
\] 

\begin{proposition}
\label{PrinIsEssentiallySurjective}
This construction (eq:HeapOperationInAGroup) defines a [[functor]] 

$$
  Prin 
    \,\colon\, 
  Grp \longrightarrow Heap
$$  

from the category [[Grp]] of [[groups]] to that of heaps,
which is [[essentially surjective functor|essentially surjective]], meaning that, up to [[isomorphism]] all heaps arise in this way.

In fact, there is also a functor
$$
  Str 
   \,\colon\,
  Heap \longrightarrow Grp
$$

such that

1. there exist [[natural isomorphisms|natural]] group isomorphisms of the form

   $Str\big(Prin(G)\big) \,\cong\, G$ 


1. there exist heap isomorphisms of the form 

   $Prin\big(Str(H)\big) \,\cong\, H$  
  
   which however are *not* [[natural transformation|natural]] (whence we do *not* have an [[equivalence of categories]]).

\end{proposition}
This group $Str(H)$ is called the *structure group* of the heap $H$.
\begin{proof}
Given a heap $H$, the claimed [[structure group]]  $Str(H)$ is described, up to [[isomorphism]], by any of the following constructions:

1. Choosing any [[element]] $\mathrm{e} \in H$, then the [[binary operation]]

   \[
     \label{BinaryOperationInFirstModel}
     a \cdot b \,\coloneqq\, t(a, \mathrm{e} ,b)
     \,.
   \]

   constitutes a [[group]] [[structure]] on $H$, with [[neutral element]] $\mathrm{e}$. 

   This serves as the required structure group: $Str(H) \,\coloneqq\, (H, \cdot)$.


2. Take the [[underlying set]] of $Str(H)$ to be that of [[equivalence classes]] of [[pairs]] $(a,b) \in H\times H$, subject to the [[equivalence relation]] 

   $$
     (a,b) \,\sim\, (a',b')
     \;\;\;\;\text{iff}\;\;\;\;
     t(a,a',b') \,=\, b
   $$  

   (the idea is to think of the pair $(a,b)$ as the representative of $a b^{-1}$)

   and take the [[binary operation]] on the group to be given on representatives by

   \[
     \label{BinaryOperationInSecondModel}
     (c,d) \cdot (a,b) 
     \,\coloneqq\, 
     \big( c, t(d,a,b) \big)
     \,.
   \] 

   This again defines a group $Str(H)$. 

   Notice that: 

   * the [[inverse element|inverse]] of (the [[equivalence class]] of) $(a,b)$ is (the equivalence class of) $(b,a)$ 

   * the [[neutral element]] is (the equivalence class of) $(a,a)$ (for any $a$).

3. Finally, $Str(H)$ is realized also as an actual [[subgroup]] of the [[symmetric group]] on the [[underlying set]] of  $H$, analogously to [[Cayley's theorem]] for groups.  We take the elements of $Str(H)$ to be set [[bijections]] of the form 

   \[
      \label{GroupActionInThirdModel}
      t(a,b,-) \,\colon\, H \rightarrow H
      \,,
   \]

    where $a,b \in H$, with [[composition]] as the group's [[binary operation]].  

   Notice here that 

   \[ 
      t(c,d,-) \cdot_{Str(H)} t(a,b,-) 
      \;=\;
      t\big(c,d,t(a,b,-)\big) \;=\; t\big(t(c,d,a),b,-\big)
      \,, 
   \]

   so that $Str(H)$ is closed under this operation.  

   The first axiom of a  heap shows that $Str(H)$ contains the [[neutral element]] $t(-,x,x)$, for any  $x$), and the [[inverse element]] of $t(\cdot,a,b)$ is $t(\cdot,b,a)$; thus  $Str(H)$ is a subgroup of the symmetric group of $H$.

It remains to see that these constructions all agree and are functorial.

First to see that the [[equivalence relations]] used in the second and third construction agree, notice that 
the following are equivalent:

* (i) the bijections $t(\cdot,a,b)$ and $t(\cdot,a',b')$ coincide

* (ii) $t(a,a',b') = b$,

* (iii) $t(b,b',a') = a$.

Namely:

(ii) follows from (i) and $t(a,a,b) = b$.

(iii) follows from (ii) by applying $t(\cdot,b',a')$ on the
right. Similarly (ii) follows from (iii).

(i) follows from (ii) by the calculation:
\[ t(x,a',b') = t(t(x,a,a),a',b')= t(x,a,t(a,a',b'))
 = t(x,a,b).\]

Since the composition laws are also easily seen to agree, we have that the second two constructions of $Str(H)$ are canonically isomorphic.  

To compare them to the first construction, observe that for a fixed $\mathrm{e} \in H$, any equivalence class contains a unique pair of the form $(\mathrm{e},a)$.  (If $(b,c)$ is in the equivalence class, then $a$ is determined by $a = t(\mathrm{e},b,c)$.)  This sets up a bijection between the first two constructions, which we can easily show is an isomorphism.

Finally, the second constructions is manifestly functorial.
\end{proof}



### Relation to torsors
 {#HeapsAndTorsors}

Given a group $G$, a $G$-[[torsor]] is a nonempty set $X$ with a free and transitive action of $G$, which we may write as

$$ \begin{array}{ccl}
G \times X &\to& X \\
(g, x) &\mapsto& g x 
\end{array}
$$

Equivalently, a $G$-torsor is a set $X$ with an [[group action|action]] of the group $G$ but also a "division" operation

$$ \begin{array}{ccl}
X \times X &\to& G \\
(x, y) &\mapsto& x/y
\end{array}
$$

obeying

$$ (x/y) y = x $$

Given a group $G$ together with a $G$-torsor $X$, we can make $X$ into a heap by giving it the ternary operation

$$ \begin{array}{ccl}
X \times X \times X &\to& G \\
(x, y, z) &\mapsto& (x/y) z
\end{array}
$$

Conversely, from any heap $H$ we can construct a group $G$ together with a $G$-torsor whose underlying set is $H$ itself.
To see this, note that the group $G = Str(H)$ (eq:PrinIsEssentiallySurjective) comes equipped with a canonical [[group action]] on $H$, as is most clear from the third definition (eq:GroupActionInThirdModel).  

This action is 

* [[transitive action|transitive]] 

  by $t(a,a,b) = b$

and

* [[free action|free]]

  since if $t(a,b,c) = a$ then by the previous statement $t(x,b,c) = x$ for each $x$, and in particular $t(b,b,c) = b$ and also $t(b,b,c) = c$.  

Therefore, $H$ is an $Str(H)$-[[torsor]] (over a point).  

Conversely, any [[torsor]] $H$ over a group $G$ becomes a heap, by defining 

$$
  t(a,b,c) \,\coloneqq\, g \cdot c
  \,,
$$

where $g\in G$ is the unique group element such that $g\cdot b = a$.

In fact, the category $Heap$ is [[equivalence of categories|equivalent]] to the following category $Tors$: its objects are pairs $(G,H)$ consisting of a group $G$ and a $G$-torsor $H$, and its morphisms are pairs $(\phi,f):(G,H)\to (G',H')$ consisting of a group homomorphism $\phi:G\to G'$ and a $\phi$-equivariant map $f:H\to H'$.


## The empty heap {#empty}

If we wish $Heap$ to be an [[algebraic category]], then we must remove the clause that the underlying set of a heap must be nonempty (see also at *[[pseudo-torsor]]*).  Then the [[empty set]] becomes a heap in a unique way. 

However, in this case, the various theorems relating heaps to groups above all break down.  For this reason, one usually requires a heap to be inhabited.

On the other hand, we could generalize the notion of [[group]] to allow for an empty group.  This even remains a purely algebraic notion: we can define a group as an [[inhabited]] [[invertible semigroup]] $(S,\cdot,(-)^{-1})$ or an inhabited [[associative quasigroup]]. Then any [[invertible semigroup]] or [[associative quasigroup]] is a possibly-empty-heap, and every possibly-empty-heap arises in this way from its automorphism invertible semigroup or automorphism associative quasigroup (defined by either method (2) or (3)); the category of possibly-empty-heaps is equivalent to the category of invertible semigroups equipped with torsors over the point, and the category of associative quasigroups equipped with torsors over the point; etc.

This is even [[constructive mathematics|constructive]]; the theorems can be proved uniformly, rather than by treating the empty and inhabited cases separately. (This rather trivial method is obvious to a classical mathematician, but it\'s not constructively valid, since a invertible semigroup/associative quasigroup/heap as defined here can\'t be constructively proved empty or inhabited; it can only be proved empty iff not inhabited.  Indeed, taking any group $G$ and any [[truth value]] $P$, the invertible subsemigroup or associative subquasigroup $\{x \in G \;|\; P\}$ is empty or inhabited iff $P$ is false or true.)

## Examples in homotopy theory

The map $[0,1]\to[0,1]$ that sends $0\mapsto 0$, $1/3\mapsto 1$, $2/3\mapsto 0$, $1\mapsto 1$,
and interpolates linearly between these points
yields an associative Malcev operation on $[\Sigma X,Y]$,
where $X$ and $Y$ are (unpointed) spaces, $\Sigma$ is the [[suspension]] functor, and $[-,-]$ denotes the set of morphisms in the [[homotopy category]].

Thus, $[\Sigma X,Y]$ is a (nonabelian) heap.
Likewise, the full mapping space $Map(\Sigma X,Y)$ can be turned into an (∞,1)-heap, defined as an (∞,1)-algebra (in spaces) over the algebraic theory of heaps.

See Vokřínek {#Vokrinek} for more information.

## Related concepts 

* [[torsor]]

* [[affine space]]

* [[Mal'cev variety]]

* [[truss]]


## References

* [[A. K. Sushkevich]], *Theory of generalised groups*, DNTVU, Kharkov-Kiev (1937) (Russian original: [[А. К. Сушкевич]], _Теория обобщенных групп_, Государственное научно-техническое издательство Украины, 1937).

* [[Peter T. Johnstone]], _The ‘closed subgroup theorem’ for localic herds and pregroupoids_, Journal of Pure and Applied Algebra **70** (1991) 97-106 \[<a href="http://dx.doi.org/10.1016/0022-4049(91)90010-y">doi:10.1016/0022-4049(91)90010-y</a>\]

* G. M. Bergman, A.O. Hausknecht, Ch.IV §22 pp 95 in:
*Cogroups and co-rings in categories of associative rings*, AMS (1996) &lbrack;[ams:surv-45](https://bookstore.ams.org/surv-45)&rbrack;

* [[Christopher D. Hollings]], [[Mark V. Lawson]], *Wagner’s theory of generalised heaps*, Springer (2017)  &lbrack;[doi:10.1007/978-3-319-63621-4](https://doi.org/10.1007/978-3-319-63621-4)&rbrack;

* [[Zoran Škoda]], _Quantum heaps, cops and heapy categories_, Mathematical Communications **12** 1  (2007) 1-9 &lbrack;[math.QA/0701749](http://arxiv.org/abs/math.QA/0701749)&rbrack;

* Thomas Booker, [[Ross Street]], _Torsors, herds and flocks_, J. Algebra **330** (2011) 346-374 &lbrack;[pdf](https://core.ac.uk/download/pdf/81154582.pdf) [arXiv:0912.4551](https://arxiv.org/abs/0912.4551)&rbrack;


Review:

* Wikipedia: *<a href="https://en.wikipedia.org/wiki/Heap_%28mathematics%29">Heap (mathematics)</a>*

* [[John Baez]], *[Torsors made easy](http://math.ucr.edu/home/baez/torsors.html)* (2009)

* [[John Baez]], *[The group with no elements](https://golem.ph.utexas.edu/category/2020/08/the_group_with_no_elements.html)* (2020)

In the context of [[stable homotopy theory]]:

* [[Lukáš Vokřínek]], *Heaps and unpointed stable homotopy theory*, Archivum Mathematicum **50** 5 (2014) 323-332 &lbrack;[arXiv:1312.1709](https://arxiv.org/abs/1312.1709), [doi:10.5817/AM2014-5-323](http://dx.doi.org/10.5817/AM2014-5-323)&rbrack;


category: algebra

[[!redirects groud]]
[[!redirects grouds]]

[[!redirects heap]]
[[!redirects heaps]]
[[!redirects Heap]]
[[!redirects herd]]
[[!redirects associative Malcev algebra]]