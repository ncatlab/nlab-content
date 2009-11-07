<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

Just as [[functor|functors]] is a [[morphism]] between [[category|categories]], a natural transformations is a morphism between two functors.

## Definition ##

Given categories $C$ and $D$ and functors $F, G:C \to D,$ a __natural transformation__ $\alpha:F \Rightarrow G$, denoted

$$
  \array{
    \\
    & \nearrow \searrow^F
    \\
    C
    &\Downarrow^{\alpha}&
    D
    \\
    & \searrow \nearrow_G
  }
  \,,
$$

assigns to every [[object]] $x$ in $C$ a [[morphism]] 
$\alpha_x:F(x) \to G(x)$ in $D$ (called the __component__ of $\alpha$ at $x$) such that for any morphism $f:x \to y$ in $C$, the following diagram commutes in $D$:

\[ 
  \array{ 
    F(x) 
    & 
    \stackrel{F(f)}{\to} 
    & 
    F(y) 
    \\ 
    \alpha_x\downarrow 
    && 
    \downarrow \alpha_y 
    \\ G(x) 
    & 
    \stackrel{G(f)}{\to} & G(y) 
  }
  \,. 
\] 

Natural transformations between functors $C \to D$ compose in the obvious way
and functors $F : C \to D$ with natural transformations between them form the [[functor category]] 

$$
  [C,D] \in Cat
$$ 

The notation alludes to the fact that this makes [[Cat]] a [[closed monoidal category]].  Since $Cat$ is in fact a [[cartesian closed category]], another common notation is $D^C$.  In fact, if we want $Cat$ to be cartesian closed, the definition of natural transformation is forced (since an [[adjoint functor]] is unique).

There is also a horizontal composition of natural transformations, which makes [[Cat]] a [[2-category]]. In fact, [[Cat]] is a 2-category (a $Cat$-enriched category) _because_ it is (cartesian) closed: closed monoidal categories are automatically enriched over themselves, via their [[internal hom]]. 

## in terms of the cartesian closed monoidal structure on $Cat$ ##

The definition of the [[functor category]] $[C,D]$ with morphisms being natural transformations is precisely the one that makes $Cat$ a [[cartesian monoidal category|cartesian]] [[closed monoidal category]].

The category [[Cat]] of all categories (regarded for the moment just as an ordinary 1-[[category]]) is a [[cartesian monoidal category]]: for every two categories $C$ and $D$ there is the cartesian [[product]] category $C \times D$, whose objects and morphisms are simply pairs of objects and morphisms in $C$ and $D$: $Mor(C \times D) = Mor(C) \times Mor(D)$.

It therefore makes sense to ask if there is for each category $C \in Cat$ an [[internal hom]] functor $[C,-] : Cat \to Cat$ that would make [[Cat]] into a [[closed monoidal category]] in that for $A,B,C \in Cat$ we have natural isomorphisms of _sets_ of functors

$$
  Funct(A \times C , B) \simeq Funct(A, [C,B])
  \,.
$$

This is precisely the case for $[C,B]$ being the [[functor category]] with functors $C \to B$ as objects and natural transformations, as defined above, as morphisms.

Since $Cat$ here is cartesian closed, one often uses the exponential notation $B^C := [B,C]$ for the functor category.

To derive from this the definition of natural transformations above, it is sufficient to consider the [[interval category]] $A := I := \{a \to b\}$. For any category $E$, a functor $I \to E$ is precisely a choice of morphism in $E$. This means that we can check what a morphism in the [[internal hom]] category $[C,B]$ is by checking what functors $I \to [C,D]$ are. But by the defining property of $[C,D]$ as an [[internal hom]], such functors are in natural bijection to functors $I \times C \to B$.

$$
  Funct(I, [C,B]) \simeq Funct(I \times C, B)
  \,.
$$

But, as mentioned above, we kown what the category $I \times C$ is like: its morphisms are pairs of morphisms in $I$ and $C$, subject to the obvious composition law, which says in particular that for $f : c_1 \to c_2$ any morphism in $C$ we have

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
    \stackrel{(f,Id}{\to}
    (c_2, b)
  \end{aligned}
  \,.
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
  \,.
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


## in terms of double categories ##

There is a nice way of describing these structures due to [[Charles Ehresmann]]. For a category $D$ let $(\square D,\circ_1,\circ_2)$  be the double category of commutative squares in $D$. Then the class of natural transformations of functors $C \to D$ can be described as $Cat(C,(\square D,\circ_1))$. But then $\circ_2$ induces a category structure on this and so we get $CAT(C,D)$. 

An advantage of this approach is that it applies to the case of topological categories and groupoids (working in a convenient category of spaces). 

An analogous approach works for strict cubical $\omega$-categories with connections, using the good properties of [[cube]]s, so leading to a [[closed monoidal category|monoidal closed structure]] for these objects. This yields by an [[equivalence of categories]] a monoidal closed structure on [[strict omega-category|strict globular omega-categories]], where the [[tensor product]] is the [[Crans-Gray tensor product]]. 

* See [[natural transformation (discussion)]] for an informal discussion about natural transformations.

[[!redirects natural transformations]]