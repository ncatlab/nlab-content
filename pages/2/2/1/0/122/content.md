
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
* table of contents
{:toc}



## Idea 

Just as a [[functor|functor]] is a [[morphism]] between [[category|categories]], a natural transformation is a [[2-morphism]] between two functors.

Natural transformations are the [[2-morphism]]s in the [[2-category]] [[Cat]].


## Definition ##

### Explicit definition
 {#ExplicitDefinition}

\begin{definition}
**(natural transformations)**
\linebreak
Given [[categories]] $C$ and $D$ and [[functors]] $F,G \colon C \to D,$ a __natural transformation__ $\alpha \colon F \Rightarrow G$ between them, denoted

\begin{xymatrix}
  C
  \ar@/^2pc/[rr]^-{ F }_-{\ }="s"
  \ar@/_2pc/[rr]_-{ G }^-{\ }="t"
  &&
  D
  %
  \ar@{=>}^-{\alpha} "s"; "t"
\end{xymatrix}

is an assignment to every [[object]] $x$ in $C$ of a [[morphism]] 
$\alpha_x:F(x) \to G(x)$ in $D$ (called the __component__ of $\alpha$ at $x$) such that for any morphism $f:x \to y$ in $C$, the following [[diagram]] [[commuting diagram|commutes]] in $D$:

\begin{tikzcd}
    F(x) \arrow[r, "F(f)"] \arrow[d, "\alpha_x"'] & F(y) \arrow[d, "\alpha_y"] \\
    G(x) \arrow[r, "G(f)"']                        & G(y)                       
\end{tikzcd}

\end{definition}

\begin{remark}
**([[composition]] of natural transformations)**
Natural transformations between functors $C \to D$ and $D \to E$ compose in the obvious way to natural transformations $C \to E$ (this is their [[vertical composition]] in the [[2-category]] [[Cat]])
and functors $F : C \to D$ with natural transformations between them form the [[functor category]] 

\[
  \label{FunctorCategory}
  [C,D] \;\in\; Cat
\] 

The notation alludes to the fact that this makes [[Cat]] a [[closed monoidal category]].  (Since $Cat$ is in fact a [[cartesian closed category]], another common notation is $D^C$, cf. *[[exponential objects]]*.) 

 In fact, if we want $Cat$ to be [[cartesian closed category|cartesian closed]], the definition of natural transformation is forced (since an [[adjoint functor]] is unique). This is discussed in [a section below](#InTermsOfCartMon).

There is also a [[horizontal composition]] of natural transformations, which makes [[Cat]] a [[2-category]]: the [[Godement product]]. See there for details. 

In fact, [[Cat]] is a 2-category (a $Cat$-enriched category) _because_ it is (cartesian) closed: closed monoidal categories are automatically enriched over themselves, via their [[internal hom]].
\end{remark}

\begin{remark}\label{CategoryOfPresheaves}
**([[categories of presheaves]])**
  \linebreak
  The [[functor categories]]  (eq:FunctorCategory) are also called *[[categories of presheaves]]*, in particular if they are of the form
$$
  PSh(C) \,\coloneqq\, [C^{op}, Set]
  \,,
$$
hence if they are categories whose 

* [[objects]] are [[functors]] out of the [[opposite category]] of a given category $C$ into the category [[Set]] of [[sets]] and [[functions]]

* [[morphisms]] are natural transformations between these.

Similarly, functor categories of the form
$$
  CPSh(C) \,\coloneqq\, [C, Set]
$$
are also called *[[categories of copresheaves]]*.

\end{remark}


### In terms of morphismwise components
{#morphismwiseDefn}

An alternative but ultimately equivalent way to define a natural transformation $\alpha : F \rightarrow G$ is as an assignment to every morphism $m : x \rightarrow y$ in $C$ of a morphism $\alpha(m) : F(x) \rightarrow G(y)$, in such a way as that $G(m_1)\alpha(m_0) = \alpha(m_1)F(m_0)$ for every binary composition $m_1 m_0$ in $C$ (or equivalently $\alpha(m_2 m_1 m_0) = G(m_2) \alpha(m_1) F(m_0)$ for every ternary composition $m_2m_1m_0$ in $C$).

The relation of this to the previous definition is that the commutative squares in the previous definition for any morphism $f$ give the value $\alpha(f) = G(f) \circ \alpha_x = \alpha_y \circ F(f)$, and the identity morphisms for any object $x$ give the component $\alpha_x = \alpha(id_x)$.

Vertical composition of natural transformations can be specified directly in terms of this account as well: specifically, an $n$-ary composition $\alpha_1 ... \alpha_n$ of natural transformations is uniquely determined by the property that $(\alpha_1 ... \alpha_n)(m_1 ... m_n) = \alpha_1(m_1) ... \alpha_n(m_n)$, for every $n$-ary composition $m_1 ... m_n$ in $C$.

Horizontal composition is even easier, as the horizontal composite of $\alpha_1, ..., \alpha_n$ is just $\alpha_1 ... \alpha_n$.

### In terms of the cartesian closed monoidal structure on $Cat$ {#InTermsOfCartMon}

The definition of the [[functor category]] $[C,D]$ with morphisms being natural transformations is precisely the one that makes $Cat$ a [[cartesian monoidal category|cartesian]] [[closed monoidal category]].

The category [[Cat]] of all categories (regarded for the moment just as an ordinary 1-[[category]]) is a [[cartesian monoidal category]]: for every two categories $C$ and $D$ there is the cartesian [[product]] category $C \times D$, whose objects and morphisms are simply pairs of objects and morphisms in $C$ and $D$: $Mor(C \times D) = Mor(C) \times Mor(D)$.

It therefore makes sense to ask if there is for each category $C \in Cat$ an [[internal hom]] functor $[C,-] : Cat \to Cat$ that would make [[Cat]] into a [[closed monoidal category]] in that for $A,B,C \in Cat$ we have natural isomorphisms of _sets_ of functors

$$
  Funct(A \times C , B) \simeq Funct(A, [C,B])
  \,.
$$

This is precisely the case for $[C,B]$ being the [[functor category]] with functors $C \to B$ as objects and natural transformations, as defined above, as morphisms.

Since $Cat$ here is cartesian closed, one often uses the exponential notation $C^B := [B,C]$ for the functor category.

To derive from this the definition of natural transformations above, it is sufficient to consider the [[interval category]] $A := I := \{a \to b\}$. For any category $E$, a functor $I \to E$ is precisely a choice of morphism in $E$. This means that we can check what a morphism in the [[internal hom]] category $[C,B]$ is by checking what functors $I \to [C,B]$ are. But by the defining property of $[C,B]$ as an [[internal hom]], such functors are in natural bijection to functors $I \times C \to B$.

$$
  Funct(I, [C,B]) \simeq Funct(I \times C, B)
  \,.
$$

But, as mentioned above, we know what the category $I \times C$ is like: its morphisms are pairs of morphisms in $I$ and $C$, subject to the obvious composition law, which says in particular that for $f : c_1 \to c_2$ any morphism in $C$ we have

$$
  \begin{aligned}
    (c_1,a) \stackrel{(f,(a \to b))}{\to} (c_2,b)
    & =
    (c_1,a) \stackrel{(f, Id)}{\to} (c_2,a) 
    \stackrel{(Id, (a \to b)}{\to}
    (c_2, b)
    \\
    &=
    (c_1,a) \stackrel{(Id, (a\to b))}{\to} (c_1,b) 
    \stackrel{(f,Id)}{\to}
    (c_2, b)
  \end{aligned}
$$

Here the right side is more conveniently depicted as a commuting square

$$
  \array{
     (c_1,a) &\stackrel{(f,Id)}{\to}& (c_2,a)
     \\
     \downarrow^{\mathrlap{(Id,(a \to b))}} 
     && 
     \downarrow^{\mathrlap{(Id, (a \to b))}}
     \\
     (c_1,b) &\stackrel{(f,Id)}{\to}& (c_2,b)
  }
$$

So a natural transformation between functors $C \to D$ is given by the images of such squares in $D$. By tracing back the way the hom-isomorphism works, one finds that the image of such a square in $D$ for a natural transformation $\alpha : F \to G$ is the naturality square from above:

$$
  \array{ 
    F(c_1) 
    & 
    \stackrel{F(f)}{\to} 
    & 
    F(c_2) 
    \\ 
    \alpha_x\downarrow 
    && 
    \downarrow \alpha_y 
    \\ G(c_1) 
    & 
    \stackrel{G(f)}{\to} & G(c_2) 
  }
  \,. 
$$ 


### In terms of double categories 

There is a nice way of describing these structures due to [[Charles Ehresmann]]. For a category $D$ let $(\square D,\circ_1,\circ_2)$  be the [[double category]] of commutative squares in $D$. Then the class of natural transformations of functors $C \to D$ can be described as $Cat(C,(\square D,\circ_1))$. But then $\circ_2$ induces a category structure on this and so we get $CAT(C,D)$. 

An advantage of this approach is that it applies to the case of topological categories and groupoids (working in a convenient category of spaces). 

An analogous approach works for strict cubical $\omega$-categories with connections, using the good properties of [[cube]]s, so leading to a [[closed monoidal category|monoidal closed structure]] for these objects. This yields by an [[equivalence of categories]] a monoidal closed structure on [[strict omega-category|strict globular omega-categories]], where the [[tensor product]] is the [[Crans-Gray tensor product]].

## Examples ##
 {#Examples}

\begin{example}\label{UnitOfDoubleDualization}
**(unit of double-dualization)**
\linebreak
  For any [[ground field]] $\mathbb{K}$,
  the canonical [[linear map]] from a [[vector space]] $V$ to its [double dual](dual+vector+space#DoubleDualVectorSpaces) $\big(V^{\ast}\big)^\ast$ 
\[\label{UnitMapToDoubleDual}\]
\begin{tikzcd}[sep=0pt]
  V \ar[rr] && \big(V^\ast\big)^\ast
  \\
  v 
    &\mapsto& 
  \big(
    \omega(-) \mapsto \omega(v)
  \big)
\end{tikzcd}
is a natural transformation 
$$
  Id \longrightarrow \big((-)^{\ast}\big)^\ast
$$

from the [[identity functor]] $Id$ on [[Vect|$\mathbb{K} Vect$]] to the [[composition]] $\big((-)^{\ast}\big)^\ast$ of the [[linear dual space|linear dual]]-[[endofunctor]] with itself.

This example was the motivating example of [Eilenberg & MacLane 1945](#EilenbergMacLane45) (right on the first pages) for introducing the notion of natural transformation (and with it [[category theory]]) in the first place.

The conceptual subtlety that these authors sought to resolve here is that for any *[[finite-dimensional vector space|finite-dimensional]]* [[vector space]] there exists also an [[isomorphism]] from $V$ to its *single*-[[dual vector space]]:

$$
  V \in \mathbb{K} Vect^{fdim}
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  \exists
  \;
  V \xrightarrow{\sim} V^\ast
  \,.
$$

But these linear maps are conceptually different from (eq:UnitMapToDoubleDual) in that they are *not natural* in the technical sense that they do not form the components of a natural transformation between the evident functors. Instead they involve an arbitrary choice equivalent to that of an (possibly indefinite) [[inner product]] on $V$, which is not preserved by general [[linear isomorphisms]] (but just by the corresponding [[isometries]]).
\end{example}

\begin{example}
The [[determinant]] is a natural transformation $det\colon GL_n\rightarrow (-)^\times$ from the [[general linear group]] to the [[group of units]] of a [[ring]], which are both functors from [[Ring]] to [[Grp]].
\end{example}

\begin{example}
The [[Frobenius homomorphism]] is a natural transformation $Frob_p\colon Id_{Ring_p}\Rightarrow Id_{Ring_p}$ from the [[identity functor]] on the [[full subcategory]] of [[Ring]] containing all rings with [[characteristic]] $p$ to itself.
\end{example}

\begin{example}
The [[Hurewicz homomorphism]] is a natural transformation $h_n\colon\pi_n\Rightarrow H_n(-;\mathbb{Z})$ from the [[homotopy group]] to [[singular homology]], which are both functors from [[Top]] to [[Grp]].
\end{example}

\begin{example}
The [[inverse element|inversion]] $G \rightarrow G^{op},g\mapsto g^{-1}$ for every [[group]] $G$ yields a natural transformation $\Id_{Grp}\Rightarrow (-)^{op}$ from the [[identity functor]] on [[Grp]] to the [[opposite group]]-assigning functor.
\end{example}

\begin{example}
The [[coprojection]] $G\rightarrow G^{ab},g\mapsto[g]$ for every group $G$ yields a natural transformation $\Id_{Grp}\Rightarrow -^{ab}$ from the [[identity functor]] on $Grp$ to the [[abelianization]] functor. 
\end{example}

\begin{example}\label{HomomorphismsOfDiagrams}
**(homomorphisms of diagrams)**
\linebreak
By Remark \ref{CategoryOfPresheaves}, every category identified with a [[category of presheaves]] or [[copresheaves]] has its morphisms identified with natural transformations.

For instance, the category of [[directed graphs]] ([[digraphs]]) may be identified with the category of [[copresheaves]] on the [[diagram]] shape $\big\{ V \rightrightarrows E\big\}$, and under this identification the natural transformations between functors $\big\{ V \rightrightarrows E \big\} \longrightarrow Set$ are identified with [[digraph]] [[homomorphisms]].
\end{example}



## Variations

For functors between [[n-category|higher categories]], see *[[lax natural transformation]]* etc.

A transformation which is natural only relative to [[isomorphisms]] may be called a [[core-natural transformation|canonical transformation]].

For functors with more complicated shapes than $C \rightrightarrows D$, see [[extranatural transformation]] and [[dinatural transformation]].


## Related entries

* [[intertwiner]]

* [[homotopy]]

* [[transfor]]

  * **natural transformation**

    * [[transformation of adjoints]]

    * [[monad transformation]]

    * [[extranatural transformation]], [[dinatural transformation]]

    * [[cartesian natural transformation]]

    * [[enriched natural transformation]]
    
    * [[strong natural transformation]]

  * [[pseudonatural transformation]]

  * [[lax natural transformation]]



* See [[natural transformation (discussion)]] for an informal discussion about natural transformations.


## References

The notion of *natural transformations* between functors is due to

* {#EilenbergMacLane45} [[Samuel Eilenberg]], [[Saunders MacLane]], _[[General Theory of Natural Equivalences]]_,  Transactions of the American Mathematical Society **58** 2 (1945) 231-294 &lbrack;[doi:10.1090/S0002-9947-1945-0013131-6](https://doi.org/10.1090/S0002-9947-1945-0013131-6), [jstor:1990284](http://www.jstor.org/stable/1990284)&rbrack;

where it served as the motivation for the definition of *[[categories]]* and *[[functors]]* in the first place.


Textbook accounts:

* [[Saunders MacLane]], §I.4 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* [[Francis Borceux]], Section 1.3 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory* &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;


See also *[[category theory#references|category theory - references]]*.


[[!redirects natural transformations]]

[[!redirects naturality square]]
[[!redirects naturality squares]]

[[!redirects natural map]]
[[!redirects natural maps]]

[[!redirects internal natural transformation]]
[[!redirects internal natural transformations]]

