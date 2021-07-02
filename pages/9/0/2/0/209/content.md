
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

### In 1-category theory

A [[functor]] $F: C \to D$ from the category $C$ to the category $D$ is _faithful_, or an embedding, if for each pair of objects $x, y \in C$, the function

$$F : C(x,y) \to D(F(x), F(y))$$

between [[hom sets]] is [[injection|injective]]. The arrow function of $F$ assigns to each $f : x \rightarrow y$ an arrow $Ff : Fx \rightarrow Fy$, thereby defining a function 
$$ F_{x,y} : hom(x,y) \rightarrow hom(Fx, Fy). f \mapsto Ff $$

More abstractly, we may say a functor is faithful if it is $2$-[[k-surjective functor|surjective]] &#8211; or loosely speaking, 'surjective on equations between given morphisms'. 



### In higher category theory
 {#InHigherCategoryTheory}

See also _[[faithful morphism]]_ for a generalization to an arbitrary [[2-category]].

And see [[0-truncated morphism of an (∞,1)-category|0-truncated morphism]] for generalization to [[(∞,1)-categories]] (see <a href="n-truncated+object+of+an+(infinity,1)-category#TruncatedMorphismsBetweenGroupoids">there</a>).

## Properties

+-- {: .num_prop }
###### Proposition

A faithful functor [[reflected limit|reflects]] [[epimorphisms]] and [[monomorphisms]].

=--

(The simple proof is spelled out for instance at _[[epimorphism]]_.)


## Related concepts

[[!include properties of functors -- contents]]




[[!redirects faithful]]
[[!redirects faithful functors]]
