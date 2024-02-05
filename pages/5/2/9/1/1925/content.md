
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

While notions such as *[[affine spaces]]*, *[[principal homogeneous spaces]]* are very similar,
the concrete definition of heaps is more direct and simpler in the sense that it postulates just a single ternary operation satisfying just two [[axioms]]. 

Concretely, for heaps [[underlying]] a [[group]] [[structure]], this ternary operation is defined from the binary group operation $(\text{-})\cdot(\text{-})$ by 

\[
  \label{HeapOperationInAGroup}
  t
  \,\colon\,
  (a,b,c) 
  \;\mapsto\; 
  a \cdot b^{-1} \cdot c
\]  

and every heap arises this way, up to [[isomorphism]], from a group called its *automorphism group* (Prop. \ref{PrinIsEssentiallySurjective} below). 

{#HowToThinkAboutT} The discussion there (eq:BinaryOperationInSecondModel) shows that one may usefully think of this heap operation (eq:HeapOperationInAGroup) as bracketed to the right

$$
  t(a,b,c) \,=\, a \cdot \big( b^{-1} \cdot c \big)
$$

and thought of as the action of group elements $a$ on elements of its [[underlying]] [[torsor]], which reduces to the group action on itself (eq:BinaryOperationInFirstModel) once the otherwise arbitrary origin "$b$" of this torsor is (re-)identified with the [[neutral element]].


There is also a dual version of this concept, see at *[[quantum heap]]*.

\begin{remark}\label{Disambiguation}
**(disambiguation)**
\linebreak
Heaps in the sense of algebra should not be confused with wither

* [heaps](http://en.wikipedia.org/wiki/Heap) in the sense of theoretical [[computer science]], 

nor with 

* *heaps of pieces* in the [[combinatorics|combinatorial]] sense of [Viennot 2006](https://link.springer.com/chapter/10.1007/BFb0072524).  

\end{remark}

\begin{remark}\label{Synonyms}
**(synonyms)**
\linebreak
There are also a number of synonyms for the term 'heap'; [below](#HeapsAndTorsors) we consider '[[torsor]]' in this light.  In Russian one term for a heap is 'груда' ('gruda') meaning a heap of soil; this is a pun as it is parallel to the russian word 'группа' ('gruppa') meaning a group: forgetting the unit element is sort of creating an amorphous version.  This term also appears in English as 'groud'. In universal algebra the standard name is __associative Malcev algebra__ (in various spellings, including Mal'cev, Mal'tsev and Maltsev), other names include __herd__.
\end{remark}


## Definition

\begin{definition}
A __heap__ $(H,t)$ is a [[inhabited set|nonempty]] [[set]] $H$ equipped with a ternary operation $t \colon H \times H \times H\to H$ satisfying the following two relations

1. $ t(b,b,c) = c = t(c,b,b)$,

1. $ t\big(a,b,t(c,d,e)\big) = t\big(t(a,b,c),d,e\big) $.

\end{definition}

More generally, a ternary operation in some [[variety of algebras]] satisfying the first pair of equations is called a [[Mal'cev operation]].  A Mal'cev operation is  called _associative_ if it also satisfies the latter equation (i.e. it makes its domain into a heap).

A heap is **abelian** if it additionally satisfies the relation
$$
  t(a,b,c) = t(c,b,a)
$$

A **heap [[homomorphism]]**, of course, is a function that preserves the ternary operations.  This defines a [[category]] $Heap$ of heaps. 

The [[hom-sets]] of the [[full subcategory]] $AbHeap$ of abelian heaps inherit an abelian heap structure from the pointwise operation in the codomain: given $f,g,h\colon H \to G$, the function $a\mapsto t_G(f(a),g(a),h(a))$ is again a heap homomorphism. 

## Properties

### Automorphism groups of heaps
 {#AutomorphismsGroupsOfHeaps}

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

In fact, there is a converse functor
$$
  Aut 
   \,\colon\,
  Heap \longrightarrow Grp
$$

such that

1. there exist [[natural isomorphisms|natural]] group isomorphisms of the form

   $Aut\big(Prin(G)\big) \,\cong\, G$ 


1. there exist heap isomorphisms of the form 

   $Prin\big(Aut(H)\big) \,\cong\, H$  
  
   which however are *not* [[natural transformation|natural]] (whence we do *not* have an [[equivalence of categories]]).

\end{proposition}
This group $Aut(H)$ is called the *automorphism group* of the heap $H$.
\begin{proof}
Given a heap $H$, the claimed automorphism group  $Aut(H)$ is described, up to [[isomorphism]], by any of the following constructions:

1. Choosing any [[element]] $\mathrm{e} \in H$, then the [[binary operation]]

   \[
     \label{BinaryOperationInFirstModel}
     a \cdot b \,\coloneqq\, t(a, \mathrm{e} ,b)
     \,.
   \]

   constitutes a [[group]] [[structure]] on $H$, with [[neutral element]] $\mathrm{e}$. 

   This serves as the required automorphism group: $Aut(H) \,\coloneqq\, (H, \cdot)$.


2. Take the [[underlying set]] of $Aut(H)$ to be that of [[equivalence classes]] of [[pairs]] $(a,b) \in H\times H$, subject to the [[equivalence relation]] 

   $$
     (a,b) \,\sim\, (a',b')
     \;\;\;\;\text{iff}\;\;\;\;
     t(a,a',b') \,=\, b
   $$  

   (the idea is to think of the pair $(a,b)$ as the representative of $a^{-1} \cdot b$)

   and take the [[binary operation]] on the group to be given on representatives by

   \[
     \label{BinaryOperationInSecondModel}
     (c,d) \cdot (a,b) 
     \,\coloneqq\, 
     \big( c, t(d,a,b) \big)
     \,.
   \] 

   This again defines a group $Aut(H)$. 

   Notice that: 

   * the [[inverse element|inverse]] of (the [[equivalence class]] of) $(a,b)$ is (the equivalence class of) $(b,a)$ 

   * the [[neutral element]] is (the equivalence class of) $(a,a)$ (for any $a$).

3. Finally, $Aut(H)$ is realized also as an actual [[subgroup]] of the [[symmetric group]] on the [[underlying set]] of  $H$, analogously to [[Cayley's theorem]] for groups.  We take the elements of $Aut(H)$ to be set [[bijections]] of the form 

   \[
      \label{GroupActionInThirdModel}
      t(-,a,b) \,\colon\, H \rightarrow H
      \,,
   \]

    where $a,b \in H$, with [[composition]] as the group's [[binary operation]].  

   Notice here that 

   \[ 
      t(-,c,d) \cdot_{Aut(H)} t(-, a,b) 
      \;=\;
      t\big(t(-,c,d),a,b\big) \;=\; t\big(-,c,t(d,a,b)\big)
      \,, 
   \]

   so that $Aut(H)$ is closed under this operation.  

   The first axiom of a  heap shows that $Aut(H)$ contains the [[neutral element]] $t(-,x,x)$, for any  $x$), and the [[inverse element]] of $t(\cdot,a,b)$ is $t(\cdot,b,a)$; thus  $Aut(H)$ is a subgroup of the symmetric group of $H$.

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

Since the composition laws are also easily seen to agree, we have that the second two constructions of $Aut(H)$ are canonically isomorphic.  

To compare them to the first construction, observe that for a fixed $\mathrm{e} \in H$, any equivalence class contains a unique pair of the form $(\mathrm{e},a)$.  (If $(b,c)$ is in the equivalence class, then $a$ is determined by $a = t(\mathrm{e},b,c)$.)  This sets up a bijection between the first two constructions, which we can easily show is an isomorphism.

Finally, the second constructions is manifestly functorial.
\end{proof}



### Relation to torsors
 {#HeapsAndTorsors}

The automorphism group $Aut(H)$ in (eq:PrinIsEssentiallySurjective) comes equipped with a canonical [[group action]] on $H$, as is most clear from the third definition (eq:GroupActionInThirdModel).  

This action is 

* [[transitive action|transitive]] 

  by $t(a,a,b) = b$

and

* [[free action|free]]

  since if $t(a,b,c) = a$ then by the previous statement $t(x,b,c) = x$ for each $x$, and in particular $t(b,b,c) = b$ and also $t(b,b,c) = c$.  

Therefore, $H$ is an $Aut(H)$-[[torsor]] (over a point).  

Conversely, any [[torsor]] $H$ over a group $G$ becomes a heap, by defining 

$$
  t(a,b,c) \,\coloneqq\, g \cdot c
  \,,
$$

where $g\in G$ is the unique group element such that $g\cdot b = a$.

In fact, the category $Heap$ is [[equaivalence of categories|equivalent]] to the following category $Tors$: its objects are pairs $(G,H)$ consisting of a group $G$ and a $G$-torsor $H$, and its morphisms are pairs $(\phi,f):(G,H)\to (G',H')$ consisting of a group homomorphism $\phi:G\to G'$ and a $\phi$-equivariant map $f:H\to H'$.


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

## References and remarks

Related notions: [[torsor]], [[affine space]], [[Mal'cev variety]], [[truss]]

* [[Christopher D. Hollings]], [[Mark V. Lawson]], _Wagner’s theory of generalised heaps_, 2017, Springer.  [doi](https://doi.org/10.1007/978-3-319-63621-4)

* [[A. K. Sushkevich]], _Theory of generalised groups_, DNTVU, Kharkov-Kiev (1937) (Russian original: [[А. К. Сушкевич]], _Теория обобщенных групп_, Государственное научно-техническое издательство Украины, 1937).

* G.M. Bergman, A.O. Hausknecht,
_Cogroups and co-rings in categories of associative rings_, Ch.IV, paragraph 22, p.95ff, AMS 1996.

* Z. &#352;koda, _Quantum heaps, cops and heapy categories_, Mathematical Communications 12, No. 1, pp. 1--9 (2007); arXiv:[math.QA/0701749](http://arxiv.org/abs/math.QA/0701749)

* Thomas Booker, [[Ross Street]], _Torsors, herds and flocks_, J. Algebra 330 (2011) 346--374 [pdf](https://core.ac.uk/download/pdf/81154582.pdf) [arXiv:0912.4551](https://arxiv.org/abs/0912.4551)

* [[Peter T. Johnstone]], _The ‘closed subgroup theorem’ for localic herds and pregroupoids_, Journal of Pure and Applied Algebra 70 (1991) 97-106.  [doi](http://dx.doi.org/10.1016/0022-4049(91)90010-y).

* wikipedia:[heap](https://en.wikipedia.org/wiki/Heap_%28mathematics%29) (mathematics)

* [[John Baez]] on [Heaps and torsors](http://www.math.ucr.edu/home/baez/torsors.html)

* [[Lukáš Vokřínek]], _Heaps and unpointed stable homotopy theory_, [arXiv](https://arxiv.org/abs/1312.1709v1).


There is an oidification ([[horizontal categorification]]) of a heap, sometimes called a _heapoid_. 

category: algebra

[[!redirects groud]]
[[!redirects grouds]]

[[!redirects heap]]
[[!redirects heaps]]
[[!redirects Heap]]
[[!redirects herd]]
[[!redirects associative Malcev algebra]]