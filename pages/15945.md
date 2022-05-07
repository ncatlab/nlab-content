

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Speaking in the [[internal language]] of a given [[category]] $\mathbf{H}$, one may try to formulate [[universal constructions]] such as of [[limits]]/[[colimits]] internally.

Given the system of [[slice categories]] $\mathbf{H}_{/X}$ of $\mathbf{H}$ (or more generally any [[indexed category]] $X \mapsto \mathbf{H}_X$), then one may regard $X$ as the shape of a discrete [[internal diagram]] in $\mathbf{H}$, and regard the objects in the slice $\mathbf{H}_{/X}$ as discrete actual [[internal diagrams]] of this shape. 

If $\mathbf{H}$ happens to have a (small) [[object classifier]] $\mathbf{h}$, then this is particularly evocative, as then (small) such slice objects $\hat F$ over $X$ [[equivalence|equivalent]] to morphisms $F \colon X \to \mathbf{h}$, hence are  directly analogous to external diagrams in the form of [[functors]] $\mathcal{X}\to \mathbf{H}$.

Now if $\mathbf{H}$ has good enough properties as a (self-)[[indexed category]] in that it is a [[hyperdoctrine]] with [[dependent sum]] $\underset{X \stackrel{f}{\to} Y}{\sum} \colon \mathbf{H}_{/X} \to \mathbf{H}_{/Y}$ and [[dependent product]] $\underset{X \stackrel{f}{\to} Y}{\prod} \colon \mathbf{H}_{/X} \to \mathbf{H}_{/Y}$ operations, then it makes sense to define the _internal colimit_ of a discrete diagram as above as 

$$
  \underset{\longrightarrow}{\lim} F \coloneqq \underset{X}{\sum} \hat F
$$ 

and the _internal limit_ as

$$
  \underset{\longleftarrow}{\lim} F \coloneqq \underset{X}{\prod} \hat F
  \,.
$$ 

Of course with $X$ being, internally, a discrete diagram shape these are, so far, just internal [[coproducts]] and internal [[products]], respectively (which is of course the source of the terminology "dependent sum" and "dependent product").

It is more or less straightforward to extend the above from $\mathbf{H}$ to $Cat(\mathbf{H})$, the collection of [[internal categories]] in $\mathbf{H}$, then consider for a given internal category (hence [[internal diagram]] shape) $C \in Cat(\mathbf{H})$ the objects in $Cat(\mathbf{H})_{/C}$ as not-necessarily discrete diagrams, and proceed as before. For various specific choices of context $\mathbf{H}$, this is considered in ([Johnstone, below prop. B2.3.20](#Johnstone), [Pisani 09, p.18, p. 23](#Pisani09), [HoTTBook, section 6.12](#HoTTBook)).

To see internally the expected [[universal property]] of the above definition, consider the [[internal diagram|internal]] $X$-diagram constant on any $A \in \mathbf{H}$, namely $X^\ast A \in \mathbf{H}_{/X}$. If there is an [[object classifier]] $\mathbf{h}$ then this corresponds indeed to the [[constant map]]  $X \to \ast \stackrel{\vdash A}{\to} \mathbf{h}$. Accordingly an internal [[cone]] with tip $A$ over the diagram $F$ as above  is a morphism of $X$-diagrams (hence in $\mathbf{H}_{/X}$) of the fomr

$$
  X^\ast A \longrightarrow \hat F
  \,.
$$

Now by the defining [[adjunction]] $(X^\ast \dashv \underset{X}{\prod})$ of the [[dependent product]], such morphisms are equivalent to morphisms

$$
  A \longrightarrow \underset{X}{\prod} \hat F
$$

in $\mathbf{H}$, hence by the above definition to morphisms

$$
  A \longrightarrow \underset{\longleftarrow}{\lim} F
$$

from $A$ into the internal colimit.

This is clearly the internal version of the statement that is extrernally true [[Set]], that the [[limit]] of sets over a diagram is the set of all its [[cones]].

Dually, an internal [[cocone]] is a morphism

$$
  \hat F \longrightarrow X^\ast A
$$

in $\mathbf{H}_{/X}$, and by the defining [[adjunction]] $(\underset{X}{\sum} \dashv X^\ast)$ of the [[dependent sum]] this is equivalently a morphism

$$
  \underset{\longrightarrow}{\lim} F \longrightarrow A
$$

exhibiting internally the statement familiar externally from [[Set]] that maps out of colimits of a diagram are equivalently cocones under that diagram.

## Examples

### $\infty$-Groupoidal homotopy limits and colimits of $\infty$-groupoids
 {#ExamplesInfinityGroupoidal}

The small [[object classifier]] of the [[(∞,1)-topos]] [[∞Grpd]] is $Core(\infty Grpd_{small})$ itself. Hence an $\infty$-groupoidal-shaped diagram of [[∞-groupoids]] is _internally_ in [[∞Grpd]] a discrete diagram $ F \colon X\to Core(\infty Grpd_{small})$. The slice object classified by this is the pullback of the [[universal right fibration]], which is equivalently its [[(∞,1)-Grothendieck construction]] $\hat F = \int_X F$.

Accordingly the above gives the internal limits and colimits

$$
  \underset{\longleftarrow}{\lim} F = \underset{X}{\sum} \hat F
$$

and

$$
  \underset{\longrightarrow}{\lim} F = \underset{X}{\prod} \hat F
  \,.
$$

There are indeed also the correct external [[(∞,1)-colimits]] and [[(∞,1)-limits]], by the discussion [here](limit+in+a+quasi-category#WithValInooGrpd).

### Borel construction and homotopy-quotients, -invariants, -coinvariants
 {#BorelConstructionHomotopyQuotients}

For $\mathbf{H}$ an [[(∞,1)-topos]] and $G$ an [[∞-group]] object, consider $X = \mathbf{B}G$ its [[delooping]]. Externally this is in general highly non-discrete, but internally this, being $\infty$-groupoidal, is a disrete diagram shape.

An [[internal diagram]] of this shape

$$
  \rho \;\colon\;  \mathbf{B}G \longrightarrow \mathbf{h}
$$

is equivalently an [[∞-action]] of $G$ on the object $V$ named by

$$
  \ast \to\mathbf{B}G \longrightarrow \mathbf{h}
  \,.
$$

Now the internal colimit

$$
  \underset{\longrightarrow}{\lim} \rho = \underset{\mathbf{B}G}{\sum} \hat \rho
  \simeq
   V/\!/G
$$

is the [[homotopy quotient]] of $V$ by $G$, equivalently the object of [[homotopy coinvariants]]. In $\mathbf{H} = $ [[∞Grpd]] this is given by the [[Borel construction]].

Similarly, the internal limit

$$
  \underset{\longleftarrow}{\lim} \rho = \underset{\mathbf{B}G}{\prod} \hat\rho
  \simeq
   Ext_G(\ast, V)
$$

is the [[homotopy invariants]] of the action.

More generally, the internal left and right [[Kan extension]] give the [[induced representation]] and [[coinduced representation]] constructions. See at _[[∞-action]]_ for more on this.


## References

* [[Francis Borceux]], Chapter 8 in Vol 1 _Basic Category Theory_ of: _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)  ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))

* {#Johnstone} [[Peter Johnstone]], section B2 in _[[Sketches of an Elephant]]_

* {#Pisani09} [[Claudio Pisani]], _Balanced Category Theory II_ ([arXiv:0904.1790](http://arxiv.org/abs/0904.1790))

* {#HoTTBook} [[Univalent Foundations Project]], section 6.12 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

[[!redirects internal (co-)limits]]

[[!redirects internal limit]]
[[!redirects internal limits]]

[[!redirects internal colimit]]
[[!redirects internal colimits]]
