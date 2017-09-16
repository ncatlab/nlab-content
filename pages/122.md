#Idea#

Just as [[functor|functors]] go between [[category|categories]], natural transformations go between functors.

#Definition#

Given categories $C$ and $D$ and functors $F, G:C \to D,$ a _natural transformation_ $\alpha:F \Rightarrow G$ 

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
$$
assigns to every object $x$ in $C$ a morphism 
$\alpha_x:F(x) \to G(x)$ in $D$ such that for any morphism $f:x \to y$ in $C$, the following diagram commutes in $D$:

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
  [C,D]
$$ 
The notation alludes to the fact that this makes [[Cat]] a [[closed monoidal category]].  Since $Cat$ is in fact a [[cartesian closed category]], another common notation is $D^C$.  In fact, if we want $Cat$ to be cartesian closed, the definition of natural transformation is forced (since an [[adjoint functor]] is unique).

There is also a horizontal composition of natural transformations, which makes [[Cat]] a [[2-category]].

##Remark##

There is a nice way of describing these structures due to C. Ehresmann. For a category $D$ let $(\square D,\circ_1,\circ_2)$  be the double category of commutative squares in $D$. Then the class of natural transformations of functors $C \to D$ can be described as $Cat(C,(\square D,\circ_1))$. But then $\circ_2$ induces a category structure on this and so we get $CAT(C,D)$. 

An advantage of this approach is that it applies to the case of topological categories and groupoids (working in a convenient category of spaces). 

An analogous approach works for strict cubical $\omega$-categories with connections, using the good properties of cubes, so leading to a monoidal closed structure for these objects. This yields by an equivalence of categories a monoidal closed closed structure on strict globular $\omega$-categories, where the tensor product is the Gray tensor product. 
