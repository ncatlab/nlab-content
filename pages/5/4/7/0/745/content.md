+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The _comma category_ of two [[functors]] $f : C \to E$ and $g : D \to E$ is a [[category]] like an [[arrow category]] of $E$ where all arrows have their [[source]] in the image of $f$ and their [[target]] in the image of $g$ (and the morphisms between arrows keep track of how these sources and targets are in these images). It can also be seen a kind of [[2-limit]]: a [[directed homotopy theory|directed]] refinement of the [[homotopy pullback]] of two functors between [[groupoids]].

## Definition

We discuss three equivalent definitions of comma categories

* [Explicitly in components](#InComponents)

* [As a pullback](#AsAPullback)

* [As a 2-limit](#AsA2Limit)

\begin{rmk} The terminology "comma category" is a holdover from the original notation $(f,g)$ for such a category, which generalises $(x,y)$ or $C(x,y)$ for a [[hom-set]]. This is rarely used any more. More common modern notations for the comma category are $(f/g)$, which we will use on this page, and $(f\downarrow g)$. \end{rmk}


### Via components: the objectwise definition
 {#InComponents}

\begin{defn}\label{CommaCategory}
If $f\colon C\to E$ and $g \colon D\to E$ are [[functors]], their **comma category** is the [[category]] $(f/g)$ whose

* [[objects]] are [[triples]] $(c,d,\alpha)$ where $c\in C$, $d\in D$, and 

  \[
    \label{MorphismMakingAnObjectInTheComma}
    \alpha \colon f(c) \to g(d)
  \] 
  
  is a [[morphism]] in $E$, 

and whose

* [[morphisms]] from $(c_1,d_1,\alpha_1)$ to $(c_2,d_2,\alpha_2)$ are pairs $(\beta,\gamma)$, where $\beta:c_1\to c_2$ and $\gamma:d_1\to d_2$ are morphisms in $C$ and $D$, respectively, such that $\alpha_2 . f(\beta) = g(\gamma) . \alpha_1$.

$$
  \array{
    f(c_1)
    &\stackrel{f(\beta)}{\rightarrow}&
    f(c_2)
    \\
    \downarrow^{\alpha_1}
    &&
    \downarrow^{\alpha_2}
    \\
    g(d_1)
    &\stackrel{g(\gamma)}{\to}&
    g(d_2)    
    \\
    \\
    (c_1,d_1, \alpha_1)
    &\stackrel{(\beta,\gamma)}{\to}&
    (c_2,d_2, \alpha_2)
  }
$$

* [[composition]] of morphisms is given on components by composition in $C$ and $D$.

\end{defn}

\begin{remark}
  This is the [[category of elements]] of the [[profunctor]] $E(f(-), g(+)) \colon C^{op} \times D \to \mathbf{Set}$.
\end{remark}

\begin{remark}

In addition, there are two canonical [[forgetful functors]] defined on the comma category:

* there is a functor $H_C\colon (f/g)\rightarrow C$ which sends each object $(c,d,\alpha)$ to $c$, and each pair $(\beta,\gamma)$ to $\beta$.

* there is a functor $H_D\colon (f/g)\rightarrow D$ which sends each object $(c,d,\alpha)$ to $d$, and each pair $(\beta,\gamma)$ to $\gamma$.

Furthermore:

* there is a [[natural transformation]] $\theta : f \circ H_C \to g\circ H_D$ defined by $\theta_{(c,d,\alpha)} = \alpha$.

These functors and natural transformation together give the comma category a [[2-category theory|2-category theoretic]] [[universal property]]; see [this section](#AsA2Limit) for more.
\end{remark}

\begin{remark}\label{IsoCommaCategory}
  Alternatively, requiring the morphisms (eq:MorphismMakingAnObjectInTheComma) to be [[isomorphisms]] yields the notion of an **iso-comma category** (an [[iso-comma object]] in [[Cat]]). This has the [[universal property]] of a non-lax "[[2-pullback]]".
\end{remark}


### As a pullback in the 1-category of categories
 {#AsAPullback}

Let $I = \{a \to b\}$ be the (directed) [[interval category]] and $E^I = Funct(I,E)$ the [[functor category]]. 

The comma category is the [[pullback]]

$$
  \array{
    (f/g) 
    &\to&
    E^I
    \\
    \big\downarrow 
    & \scriptsize{(pb)} & 
    \big\downarrow
    \mathrlap{^{\mathrlap{(F\mapsto F(a))\times(F\mapsto F(b))}}}
    \\
    C \times D
    &
      \underset{f \times g}{\longrightarrow}
    &
    E \times E
  }
$$

in the standard sense of pullback of morphisms in the 1-category [[Cat]] of categories.

Compare this with the construction of [[homotopy pullback]] ([here](homotopy+pullback#HomotopyPullbackByFactorizationLemma)), hence with the definition of [[loop space object]] and also with [[generalized universal bundle]].

### As a 2-limit in the 2-category of categories
 {#AsA2Limit}

The comma category is the [[comma object]] of the [[cospan]] $C\overset{f}{\rightarrow}E\overset{g}{\leftarrow}D$ in the [[2-category]] $Cat$.  This means it is an appropriate [[weighted limit|weighted]] 2-categorical [[2-limit|limit]] (in fact, a [[strict 2-limit]]) of the diagram

$$
  \array{
    && C
    \\
    && \downarrow^f
    \\
    D &\stackrel{g}{\to}& E
  }
$$

Specifically, it is the universal [[span]] making the following square commute up to a specified [[natural transformation]] (such a universal square is in general called a [[comma square]]):

$$
  \array{
    (f/g) &\overset{H_C}{\to}& C
    \\
    \mathllap{{}^{H_D}} \downarrow &\swArrow& \downarrow^{\mathrlap{f}}
    \\
    D &\stackrel{g}{\to}& E
  }
$$

(Sometimes this is called a "lax pullback", but that terminology properly refers to something else; see [[comma object]] and [[2-limit]].)

Notably, the forgetful functors $H_C$ and $H_D$ from the "objectwise" definition are thus recovered via a categorical construction: they are the projections from the summit of the "appropriate" 2-categorical limit.

In terms of the imagery of [[loop space objects]], the comma category is the category of [[interval object|directed paths]] in $E$ which start in the image of $f$ and end in the image of $g$.


## Examples 

* If $f$ and $g$ are both the identity functor of a category $C$, then $(f/g)$ is the category $C ^{\mathbf{2}} $ of arrows  in $C$.

* If $f$ is the identity functor of $C$ and $g$ is the inclusion $1\to C$ of an object $c\in C$, then $(f/g)$ is the [[over category|slice category]] $C/c$.

* Likewise if $g$ is the identity and $f$ is the inclusion of $c$, then $(f/g)$ is the [[under category|coslice category]] $c/C$.

* A [[natural transformation]] $\tau \colon F \to G$ with $F,G :\colon C\to D$ may be regarded as a [[functor]] $T \colon C\to (F/G)$ with $T(c)=(c,c,\tau_c)$ and $T(f)=(f,f)$. Conversely, any such functor $T$ such that the two projections from $(F/G)$ back to $C$ are both [[left inverses]] for $T$ yields a corresponding natural transformation.  This is an expression of the universal property of $(F/G)$ as a [[comma object]].

## Properties

### Completeness and cocompleteness

If $C$ and $D$ are [[cocomplete category|cocomplete]] and $f: C \to E$ is [[cocontinuous functor|cocontinuous]] and $g: D \to E$ is an arbitrary functor (not necessarily cocontinuous) then the comma category $(f/g)$ is cocomplete and the projection functors are cocontinuous.
Similarly, as $(f/g)^{op}\cong (g^{op}/f^{op})$, if $C$ and $D$ are [[complete category|complete]] and $g: D \to E$ is [[continuous functor|continuous]] and $f: C \to E$ is an arbitrary functor (not necessarily continuous) then the comma category $(f/g)$ is complete and the projection functors are continuous.

For a proof, see 

* Rydeheard, David E., and Rod M. Burstall. Computational category theory. Vol. 152. Englewood Cliffs: Prentice Hall, 1988.  Section 5.2: colimits in comma categories.

### Functors and comma categories 

* [[functors and comma categories]]

## Related concepts

* [[Quillen's theorem A]]
* [[comma object]]

## References
 {#References}

The notion of comma categories was introduced (in order to [characterize](adjoint+functor#InTermsOfCommaCategories)  [[adjoint functors]], but without giving them a name) in: 

* [[F. W. Lawvere]], *[[Functorial Semantics of Algebraic Theories]]*, Ph.D. thesis, Columbia University (1963)

* Consolato Pellegrino, _Creazione di limiti nelle categorie comma_, Rivista di Matematica della Università di Parma 3 (1974): 201-204.

* Consolato Pellegrino, _Un teorema di completezza per le categorie comma, sue applicazioni agli n-grafi_, Atti del Seminario Matematico e Fisico dell'Università di Modena 23 (1974): 223-230.


Textbook accounts:

* [[Saunders MacLane]], §II.6 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


* [[Francis Borceux]], Section 1.6 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory* &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;


See also:

* [[Toby Bartels]], _[Comma categories](http://tobybartels.name/notes/#comma)_

[[!redirects comma categories]]


[[!redirects isocomma category]]
[[!redirects isocomma categories]]

[[!redirects iso-comma category]]
[[!redirects iso-comma categories]]

[[!redirects iso-comma-category]]
[[!redirects iso-comma-categories]]

