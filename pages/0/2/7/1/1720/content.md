<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

In a [[model category]] fibrations enjoy [[pullback stability]] and cofibrations are stable under [[pushout]], but weak equivalences need not have either property. In a proper model category weak equivalences are also preserved under certain pullbacks and/or certain pushouts.



## Definition ##

A [[model category]] is called 

* **right proper** if weak equivalences are preserved by [[pullback]] along fibrations

* **left proper** if weak equivalence are preserved by [[pushout]] along cofibrations

* **proper** if it is both left and right proper.


So a model category is right proper if for every weak equivalence $f : A \to B$ in $W\subset Mor(C)$ and every fibration $h : C \to B$ the pullback $h^* f : A \times_B C \to C$ in

$$
  \array{
    A \times_C B &\to& A
    \\
    \;\;\downarrow^{\mathrlap{\Rightarrow h^* f \in W}} && \downarrow^{\mathrlap{f \in W}}
    \\
    C &\stackrel{h \in F}{\to}& B
  }
$$

is a weak equivalence.

## Examples ##


### Left proper model categories

* the left [[Bousfield localization]] of every left proper [[combinatorial model category]] at a set of morphisms is again left proper.

* every full subcategory on cofibrant objects

### Right proper model categories ###


* every [[category of fibrant objects]] is right proper

### Proper model categories ###

* [[Top]]: [[model structure on topological spaces]]

* [[SSet]]: [[model structure on simplicial sets]]

All [[model category|model categories]] that model aspects of [[infinity-stack]]s and hence of [[cohomology]] are right proper: 

* [[model structure on simplicial presheaves]]

  for presheaves over the point this restricts to:

  * [[model structure on simplicial sets]]

  * [[model structure on topological spaces]]



* [[model structure on presheaves of spectra]] 

  for presheaves over the point this restricts to:

  * [[model structure on spectra]]

## Properties ##


### Homotopy (co)limits in proper model categories ###

+-- {: .un_lemma }
###### Lemma


In a left proper model category, ordinary [[pushout]]s along cofibrations out of cofibrant objects are [[homotopy pushout]]s.

Dually, in a right proper model category, ordinary [[pullback]]s along fibrations into fibrant objects are [[homotopy pullback]]s.


=--

+-- {: .proof}
###### Proof


Let $A \hookrightarrow B$ be a cofibration with $A$ cofibrant and let $A \to C$ be any other morphism. Factor this morphism as
$A \hookrightarrow C' \stackrel{\simeq}{\to} C$ by a cofibration
followed by an acyclic fibration. This give a weak equivalence
of pushout diagrams

$$
  \array{
    C' &\stackrel{\simeq}{\to}& C
    \\
    \uparrow && \uparrow
    \\
    A &\stackrel{=}{\to}& A
    \\
    \downarrow && \downarrow
    \\
    B &\stackrel{=}{\to}& B
  }
  \,.
$$

In the diagram on the left all objects are cofibrant and one morphism is a cofibration,
hence this is a cofibrant diagram and its ordinary colimit is the homotopy colimit.
Using that [[pushout]] diagrams compose to pushout diagrams, that cofibrations are preserved under pushout and that in a left proper model category weak equivalences
are preserved under pushout along cofibrations, we find a weak equiovalence
$hocolim \stackrel{\simeq}{\to} B \coprod_A C$

$$
  \array{
    A &\stackrel{\in cof}{\to}& C' &\stackrel{\in W \cap fib}{\to}& C
    \\
    \downarrow^{\mathrlap{\in cof}} &&
    \downarrow^{\mathrlap{\in cof}} &&
    \downarrow^{\mathrlap{\in cof}}
    \\
    B &\to& hocolim &\stackrel{\in W}{\to}&
    B \coprod_A C
  }
  \,.
$$

The proof for the second statement is the precise formal dual.

=--


## References ##


The usefulness of right properness for constructions of [[homotopy category|homotopy categories]] is discussed in

* J. Jardine, _Cocycle categories_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0605/0605198v1.pdf))

[[!redirects right proper model category]]
[[!redirects left proper model category]]