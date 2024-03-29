
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given an [[abelian category]] $\mathcal{A}$, write $Ch_\bullet(\mathcal{A})$ for its [[category of chain complexes]]. 

+-- {: .num_prop}
###### Proposition

The [[relation]] of [[chain homotopy]] is an [[equivalence relation]] on the [[hom sets]] of this category. 

=--

+-- {: .num_defn}
###### Definition

Write $
  \mathcal{K}(\mathcal{A})$
for the [[category]] whose [[objects]] are [[chain complexes]], and whose [[morphisms]] between objects $C_\bullet, D_\bullet$ are chain homotopy-equivalence classes

$$
  \mathcal{K}(\mathcal{A})(C_\bullet, D_\bullet)
  \coloneqq
  Ch_\bullet(\mathcal{A})(C_\bullet, D_\bullet)_{\sim_{ch}}
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

Analogous to the variants discussed at _[[category of chain complexes]]_ one considers also the [[full subcategories]]

$$
  K^{+,-,b}(\mathcal{A}) \hookrightarrow \mathcal{K}(\mathcal{A})
$$

on the chain complexes which are bounded above or bounded below or bounded, respectively.

=--

+-- {: .num_remark}
###### Remark

The category $\mathcal{K}(\mathcal{A})$ is sometimes called the "homotopy category of chain complexes". But beware that there is another category that also and more properly deserves to be called by this name:

the _[[homotopy category]]_ $Ho(Ch_\bullet(\mathcal{A}))$ in the sense of the result of [[localization]] at the [[chain maps]] that are [[quasi-isomorphisms]] is traditionally called the _[[derived category]]_ $\mathcal{D}(\mathcal{A})$ of $\mathcal{A}$:

$$
  \mathcal{D}(\mathcal{A}) \coloneqq Ho(Ch_\bullet(\mathcal{A}))
  \,.
$$

=--

+-- {: .num_defn #ProjectionFunctor}
###### Definition

By construction there is a canonical [[functor]]

$$
  Ch_\bullet(\mathcal{A}) \to \mathcal{K}(\mathcal{A})
$$

which is the [[identity]] on objects and the [[quotient]] [[projection]] on [[hom-sets]].

=--

## Properties

### Additive category structure

+-- {: .num_prop}
###### Proposition

Under componentwise addition of [[chain maps]], $\mathcal{K}(\mathcal{A})$ is an [[additive category]].

=--

In fact using the [[abelian group]]-structure on chain maps, we can equivalently reformulate the quotient by chain homotopy as follows:

+-- {: .num_defn}
###### Definition

For $C_\bullet, D_\bullet \in Ch_\bullet(\mathcal{A})$, let 

$$
  NHt(C_\bullet, D_\bullet) \hookrightarrow Ch_\bullet(C_\bullet, D_\bullet)
$$

be the [[abelian group|abelian]] [[subgroup]] on those [[chain maps]] which are [[null homotopy|null homotopic]], hence for which there is a [[chain homotopy]] to the [[zero morphism]].


=--

+-- {: .num_prop}
###### Proposition

For $C_\bullet, D_\bullet \in Ch_\bullet(\mathcal{A})$, there is an [[natural isomorphism]] of [[abelian groups]]

$$
  \mathcal{K}(\mathcal{A})(C_\bullet, D_\bullet)
  \simeq
  Ch_\bullet(\mathcal{A})/NHt(C_\bullet, D_\bullet)
$$

of the [[hom-objects]] in $\mathcal{K}(\mathcal{A})$ with the [[quotient group]] of all chain maps by those whose are null homotopic. 
=--

### Triangulated category structure

+-- {: .num_defn #DistinguishedTriangles}
###### Definition

A **[[distinguished triangle]]** in $\mathcal{K}(\mathcal{A})$ is a sequence of [[morphisms]] of the form

$$
  Y_\bullet \to (X\sslash Y)_\bullet \to X[1]_\bullet \stackrel{}{\to} Y[1]_\bullet
  \,,
$$

where $C[1]_\bullet$ denotes the [[suspension of a chain complex]], which is [[isomorphism|isomorphic]] to the [[image]] under the projection fuctor def. \ref{ProjectionFunctor} of a [[mapping cone]] sequence in $Ch_\bullet(\mathcal{A})$ 

$$
  Y_\bullet \stackrel{}{\hookrightarrow} cone(f)_\bullet
   \stackrel{}{\to}
  X[1]_\bullet
   \stackrel{f[1]_\bullet}{\to}
  Y[1]_\bullet
$$

of a [[chain map]] $f_\bullet : X_\bullet \to Y_\bullet$ in $Ch_\bullet(\mathcal{A})$.

=--

+-- {: .num_theorem}
###### Theorem

With 

* [[shift functor]] given by [[suspension of a chain complex|suspension of chain complexes]];

* [[distinguished triangles]] as in def. \ref{DistinguishedTriangles}

the category $\mathcal{K}(\mathcal{A})$ is a [[triangulated category]].

=--

### Relation to the derived category
 {#RelationToDerivedCategory}

See at _[[derived category]]_ in the section [derived category - Properties](derived+category#Properties).

## Examples

### Chain homotopies that ought to exist but do not
 {#ChainHomotopiesThatOughtToExistButDoNot}

We discuss some basic examples of [[chain maps]]
that ought to be identified in [[homotopy theory]], but which are not yet identified in $\mathcal{K}(\mathcal{A})$, but only in the [[derived category]] $\mathcal{D}(\mathcal{A})$.

+-- {: .num_example}
###### Example

In $Ch_\bullet(\mathcal{A})$ for $\mathcal{A} = $ [[Ab]] consider the [[chain map]]

$$
  \array{
    \cdots &\to& 0 &\to& 0 &\to& 0 &\to& \mathbb{Z}_2
    \\
    && \downarrow && \downarrow && \downarrow && \downarrow^{\mathrlap{id}}
    \\
    \cdots &\to& 0 &\to& \mathbb{Z} &\stackrel{\cdot 2}{\to}& \mathbb{Z} &\stackrel{mod\,2}{\to}& \mathbb{Z}_2
  }
  \,.
$$

The [[codomain]] of this map is an [[exact sequence]], hence is [[quasi-isomorphism|quasi-isomorphic]] to the 0-chain complex. Therefore in [[homotopy theory]] it should behave entirely as the 0-complex itself. In particular, every [[chain map]] to it should be [[chain homotopy|chain homotopic]] to the [[zero morphism]] (have a _[[nLab:null homotopy]]_).

But the above chain map is chain homotopic precisely only to itself. This is because the degree-0 component of any chain homotopy out of this has to be a homomorphism of abelian groups $\mathbb{Z}_2 \to \mathbb{Z}$, and this must be the 0-morphism, because $\mathbb{Z}$ is a [[free group]], but $\mathbb{Z}_2$ is not.

This points to the problem: the components of the domain chain complex are not _free enough_ to admit sufficiently many maps out of it. 

Consider therefore a [[free resolution]] of the above domain complex by the [[quasi-isomorphism]]

$$
  \array{
     \cdots 
    &\to& 0 &\to& 0 &\to& \mathbb{Z} &\stackrel{\cdot 2}{\to}& \mathbb{Z}
    \\
    && \downarrow && \downarrow && \downarrow && \downarrow^{\mathrlap{mod\,2}}
    \\
    \cdots &\to& 0 &\to& 0 &\to& 0 &\to& \mathbb{Z}_2
  }
  \,,
$$

where now the domain complex consists entirely of [[free groups]]. 
The composite of this with the original chain map is now

$$
  \array{
     \cdots 
    &\to& 0 &\to& 0 &\to& \mathbb{Z} &\stackrel{\cdot 2}{\to}& \mathbb{Z}
    \\
    && \downarrow && \downarrow && \downarrow^{0} && \downarrow^{\mathrlap{mod\,2}}
    \\
    \cdots &\to& 0 &\to& \mathbb{Z} &\stackrel{\cdot 2}{\to}& \mathbb{Z} &\stackrel{mod\,2}{\to}& \mathbb{Z}_2
  }
  \,.
$$

This is the corresponding [[resolution]] of the original chain map. And _this_ indeed has a [[null homotopy]]: 

$$
  \array{
     \cdots 
    &\to& 0 &\to& 0 &\to& \mathbb{Z} &\stackrel{\cdot 2}{\to}& \mathbb{Z}
    \\
      && 
    \downarrow 
     &\swarrow& 
    \downarrow 
      &\swarrow_{-id}& 
    \downarrow^{0} 
      &\swarrow_{\mathrlap{id}}& 
    \downarrow^{\mathrlap{mod\,2}}
    \\
    \cdots &\to& 0 &\to& \mathbb{Z} &\stackrel{\cdot 2}{\to}& \mathbb{Z} &\stackrel{mod\,2}{\to}& \mathbb{Z}_2
  }
  \,.
$$

Indeed, for this to happen it is sufficient that the [[resolution]] is by a degreewise [[projective object|projective]] complex. This is the statement of _[this lemma](projective+resolution#MapsProjectiveIntoExactAreNullHomotopic)_ at _[[projective resolution]]_.


=--

## Related pages

* [[Hurewicz model structure on chain complexes]]

## References

Lecture notes include

section 3.1 and 7.1 of

* [[Pierre Schapira]], _Categories and homological algebra_ (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))
 {#Schapira}


[[!redirects homotopy categories of chain complexes]]
