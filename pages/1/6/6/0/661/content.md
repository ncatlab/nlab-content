
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _double groupoid_ is, equivalently, 

* a [[double category]] in which all [[1-morphisms]] and [[2-morphisms]] are [[isomorphisms]];

* a [[groupoid]] object [[internalization|internal]] to the [[1-category]] [[Grpd]];

* an [[n-fold groupoid]] for $n = 2$.

Equipped with the relevant extra [[stuff, structure, property]] one obtains notions of double [[topological groupoids]], [[double Lie groupoids]], etc.

## Definition


+-- {: .num_defn #DoubleGroupoidInStacks}
###### Definition

Let $\mathbf{H}$ be a [[(2,1)-topos]], hence a [[(2,1)-category]] whose [[objects]] may be thought of as [[groupoids]] equipped with some geometric structure ([[stacks]]). Then a **double groupoid** with that geometric structure is a [[groupoid object in an (∞,1)-category|groupoid object in an (2,1)-category]] in $\mathbf{H}$, hence a [[simplicial object]]

$$
  \mathcal{G}_\bullet \in \mathbf{H}^{\Delta^{op}}
$$

which satisfies the groupoidal [[Segal conditions]].

=--

In the literature, the following special cases of def. \ref{DoubleGroupoidInStacks} are often taken to be the default notion of "double groupoid".

+-- {: .num_example #BareDoubleGroupoids}
###### Example

The archetypical special case of def. \ref{DoubleGroupoidInStacks} is that where $\mathbf{H} = $ [[Grpd]] is the [[(2,1)-category]] of bare (geometrically discrete) [[groupoids]]. 

=--

+-- {: .num_example}
###### Example

A special case of example \ref{BareDoubleGroupoids}, in turn, are bare double groupoids in the image of the embedding $Grpd_1^{\Delta^{op}} \to Grpd^{\Delta^{op}}$, where $Grpd_1$ is the [[1-category]] of groupoids (suppressing the [[2-morphisms]] given by [[natural isomorphisms]]). A [[groupoid object]] in $Grpd_{1}$ is equivalently a pair of groupoids $\mathcal{G}_1$ and $\mathcal{G}_0$ equipped with [[functors]] $s,t \colon \mathcal{G}_1 \to \mathcal{G}_0$, $i \colon \mathcal{G}_0 \to \mathcal{G}_1$ and $\circ \colon \mathcal{G}_1 \times_{\mathcal{G}_0} \mathcal{G}_1 \to \mathcal{G}_1$ that satisfy the usual axioms of a [[small category]] [[groupoid]] without any non-trivial [[natural isomorphisms]] weakening them. This is called a **strict double groupoid**.

=--

+-- {: .num_remark}
###### Remark

If one writes out the structure functors 

$$
  \array{
    \mathcal{G}_1
    \\
    {}^{\mathllap{s}}\downarrow \downarrow^{\mathrlap{t}}
    \\
    \mathcal{G}_0
  }
$$

of a double groupoid $\mathcal{G}_\bullet$ themselves in components, one obtains a square diagram of the form

$$
  \array{
    \mathcal{G}_{1,1}
    &
    \stackrel{\to}{\to}
    &
    \mathcal{G}_{1,0}
    \\
    \downarrow \downarrow && \downarrow \downarrow
    \\
    \mathcal{G}_{0,1}
    &
    \stackrel{\to}{\to}
    &
    \mathcal{G}_{0,0}
  }
$$

(where now we are notationally suppressing the degeneracy maps/identity assigning maps, for readability). In this form double groupoid are presented in traditional literature.


=--

+-- {: .num_example}
###### Example

For $\mathbf{H} = $ [[SmoothGrpd]], double groupoids in $\mathbf{H}$ which are in the inclusion of [[LieGrpd]]${\Delta}^{op} \to$ [[SmoothGrpd]]${}^{\Delta^{op}}$ are called **[[double Lie groupoids]]**.


=--

+-- {: .num_remark}
###### Remark

More generally, one can consider double groupoids in an arbitrary [[(∞,1)-topos]] $\mathbf{H}$, to be a 3-coskeletal [[groupoid object in an (∞,1)-category]] consisting degreewise of [[1-truncated]] objects. The [[realization]] map 

$$
 \underset{\to}{\lim} \colon \mathbf{H}^{\Delta^{op}} \to \mathbf{H}
$$

restricted to such double groupoids is a presentation of [[2-truncated]] objects in $\mathbf{H}$.

=--

## Related concepts

* [[2-group]]

* [[double Lie algebroid]]

* [[2-category equipped with proarrows]]

* [[groupoid object in an (infinity,1)-category]]


## References

Double [[Lie groupoids]] are discussed (usually for the strict case) in

* [[Ronnie Brown]], [[Kirill Mackenzie]], _Determination of a double Lie groupoid by its core diagram_. J.
Pure Appl. Algebra 80 (1992), no. 3, 237&#8211;272

* [[Kirill Mackenzie]], _General theory of Lie groupoids and Lie algebroids_ Cambridge Univ. Press, Cambridge (2005)


Some homotopical aspects of double groupoids and their relationship to  [[homotopy 2-types]] are explored in 

* [[Antonio Martínez Cegarra]]; Benjam&#305;n A. Heredia ; Josu&#233; Remedios, 
_Double groupoids and homotopy 2-types_
Appl. Categ. Struct. 20, No. 4, 323-378 (2012), see also [arXiv:1003.3820](http://arxiv.org/abs/1003.3820).

[[!redirects double groupoids]]


