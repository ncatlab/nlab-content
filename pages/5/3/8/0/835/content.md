
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

A **$2$-groupoid** is 

* a [[(n,r)-category|(2,0)-category]]

* a [[2-category]] in which all morphisms are [[equivalence]]s

* an [[n-groupoid]] for $n = 2$

* a $2$-[[truncated]] [[∞-groupoid]].


## Definition

Fix a meaning/model of [[∞-groupoid]], however weak or strict you wish. Then a __$2$-groupoid__ is an $\infty$-groupoid such that all [[parallel pair]]s of $j$-morphisms are [[equivalence|equivalent]] for $j \geq 3$. Thus, up to [[equivalence of categories|equivalence]], there is no point in mentioning anything beyond $2$-morphisms, except whether two given parallel $2$-morphisms are equivalent. This definition may give a concept more general than your preferred definition of $2$-groupoid, but it will be equivalent; basically, you may have to rephrase equivalence of $2$-morphisms as [[equality]].


## Specific models

There are various objects that model the abstract notion of $2$-groupoid.

### Bigroupoids

A **[[bigroupoid]]** is a [[bicategory]] in which all morphisms are [[equivalences]]. 

Bigroupoids may equivalently be thought of in terms of their [[Duskin nerve]]s. These are precisely the [[Kan complex]]es that are 2-[[hypergroupoid]]s.

### 2-Hypergroupoids

A $2$-[[hypergroupoid]] is a model for a 2-groupoid. This is a [[simplicial set]], whose vertices, edges, and 2-[[simplices]] we identify with the [[object]]s, [[morphism]]s and [[2-morphism]]s of the form

$$
  \array{
     && y
     \\
     & \nearrow &\Downarrow& \searrow
      \\
     x &&\stackrel{}{\to}&& z
  }
$$
  
in the 2-groupoid, respectively. 

Moreover, the 3-[[simplices]] in the simplicial set encode the composition operation: given three composable 2-simplex faces of a tetrahedron (a 3-[[horn]])

$$
  \array{
    y &\to& &\to& z
    \\
    \uparrow &\seArrow& &\nearrow&  \downarrow
    \\
    \uparrow &\nearrow& &\Downarrow& \downarrow
    \\
    x &\to&&\to& w
  }
  \;\;\;
  \;\;\;
  \array{
    y &\to& &\to& z
    \\
    &\searrow& &\swArrow&  \downarrow
    \\
    && &\searrow& \downarrow
    \\
    &&&& w
  }
$$

the unique composite of them is is a fourth face $\kappa$ and a 3-cell $comp$ filling the resulting hollow tetrahedron:

$$
  \array{
    y &\to& &\to& z
    \\
    \uparrow &\seArrow& &\nearrow&  \downarrow
    \\
    \uparrow &\nearrow& &\Downarrow& \downarrow
    \\
    x &\to&&\to& w
  }
  \;\;\;
  \stackrel{comp}{\to}
  \;\;\;
  \array{
    y &\to& &\to& z
    \\
    \uparrow &\searrow& &\swArrow&  \downarrow
    \\
    \uparrow &{}_\kappa\Downarrow& &\searrow& \downarrow
    \\
    x &\to&&\to& w
  }
  \,.
$$


The 3-[[coskeletal]]-condition says that every boundary of a 4-[[simplex]] made up of five such tetrahedra has a unqiue filler. This is the [[associativity]] [[coherence law]] on the comoposition operation:

$$
 \array{\arrayopts{\rowalign{center}}
 \array{\begin{svg}
 [[!include monoidal category > pentagonator]]
 \end{svg}} 
 }
$$

This says that any of the possible ways to use several of the 3-simpleces to compose a bunch of compsable 2-morphisms are actually equal.

### Homotopy 2-types

More generally one may consider a [[Kan complex]] that are just [[homotopy equivalent]] to a $3$-[[coskeletal]] one as a $2$-groupoid -- precisely: as representing the same [[homotopy type]], namely a [[homotopy 2-type]].


## Strict $2$-groupoids

The general notion of $2$-groupoid above is also called __weak $2$-groupoid__ to distinguish from the special case of **[[strict 2-groupoids]]**. A strict $2$-groupoid is a [[strict 2-category]] in which all morphisms are strictly invertible. This is equivalently a certain type of [[Grpd]]-[[enriched category]].


## Examples

* For $A$ an [[abelian group]], there is its double [[delooping]] 2-groupoid $\mathbf{B}^2 A$. This is given by the [[strict]] 2-groupoid that comes from the [[crossed complex]] $A \to 0 \stackrel{\to}{\to} 0$. As a [[Kan complex]] this is the image under the [[Dold-Kan correspondence]] of the [[chain complex]] $[A \to 0 \to 0]$.

* The [[fundamental 2-groupoid]] of a [[topological space]].

* The [[fundamental infinity-groupoid|fundamental $\infty$-groupoid]] of a [[topological space]] that is itself a [[homotopy 2-type]].

* The [[path 2-groupoid]] of a [[smooth manifold]].

## Related concepts

* [[Grpd-enriched category]]

[[!include homotopy n-types - table]]


[[!redirects 2-groupoid]]
[[!redirects 2-groupoids]]

[[!redirects weak 2-groupoid]]
[[!redirects weak 2-groupoids]]
