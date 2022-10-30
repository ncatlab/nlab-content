
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--
=--

#Contents#
* table of contents
{:toc}

A [[space]] $X$ is called **formally &#233;tale** if every [[morphism]]s $Y \to X$ has _unique_ [[infinitesimal object|infinitesimal]] extensions for every infinitesimal thickening of $X$.

(If there exists at least one such infinitesimal extension it is called a [[formally smooth morphism]]. If there exists at most one such extension, if is called a [[formally unramified morphism]]. The formally &#233;tale morphisms are precisely those that are both formally smoth and formally unramified.)


Traditionally this has considered in the context of [[geometry]] over formal duals of [[ring]]s and [[associative algebra]]s. This we discuss in the section ([Concrete notion](#ConcreteNotion)). But generally the notion makes sense in any context of <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">infinitesimal cohesion</a>. This we discuss in the section 
[General abstract notion](#GeneralAbstractNotion).

## General abstract notion
 {#GeneralAbstractNotion}

### Definition

Let 

$$
  \mathbf{H}
   \stackrel{\overset{u^*}{\hookrightarrow}}{\stackrel{\overset{u_*}{\leftarrow}}{\underset{u^!}{\to}}}
  \mathbf{H}_{th}   
$$

be an [[adjoint triple]] of [[functor]] with $u^*$ a [[full and faithful functor]] that preserves the [[terminal object]]. 

We may think of this as exhibiting <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">infinitesimal cohesion</a> (see there for details, but notice that in the notation used there we have $u^* = i_!$, $u_* = i^*$ and $u^! = i_*$). 

We think of the objects of $\mathbf{H}$ as [[cohesive topos|cohesive space]]s and of the objects of $\mathbf{H}_{th}$ as such cohesive spaces possibly equipped with [[infinitesimal object|infinitesimal extension]]. 

As a class of examples that is useful to keep in mind consider a [[Q-category]] 

$$
  (cod \dashv \epsilon \dashv dom) : \bar A \to A
$$  

of <a href="http://nlab.mathforge.org/nlab/show/Q-category#InfinitesimalThickening">infinitesimal thickening of rings</a> and let

$$
  ((u^* \dashv u_* \dashv u^!) : \mathbf{H}_{th} \to \mathbf{H}) := 
  ([dom,Set] \dashv [\epsilon, Set] \dashv [cod,Set] : [\bar A, Set] \to [A,Set])
$$ 

be the corresponding <a href="http://nlab.mathforge.org/nlab/show/Q-category#PresheafQCategory">Q-category of copresheaves</a>.

For any such setup there is a canonical [[natural transformation]]

$$
  \phi : u^* \to u^!
  \,.
$$

Details of this are in the section <a href="http://ncatlab.org/nlab/show/cohesive%20topos#AdjointQuadruples">Adjoint quadruples</a> at [[cohesive topos]].

From this we get for every morphism $f : X \to Y$ in $\mathbf{H}$ a canonical morphism

\[
  \label{MorphismIntoPullback}
  u^* X \to u^* Y \prod_{u^! Y} u^! X
  \,.
\]

+-- {: .num_defn #AbstractFormallyEtaleMorphism}
###### Definition

A morphism $f : X \to Y$ in $\mathbf{H}$ is called **formally &#233;tale** if (eq:MorphismIntoPullback) is an [[isomorphism]].

=--

This appears as ([KontsevichRosenberg, def. 5.1, prop. 5.3.1.1](#KontsevichRosenbergSpaces)).

In other words, $f$ is formally &#233;tale if the $f$-component naturality square

$$
  \array{
    u^* X &\stackrel{u^* f}{\to}& u^* Y
    \\
    {}^{\mathllap{\phi_X}}\downarrow && \downarrow^{\mathrlap{\phi_Y}}
    \\
    u^! X &\stackrel{u^! f}{\to}& u^! Y
  }
$$

of the [[natural transformation]] $\phi$ is a [[pullback]] [[diagram]].

+-- {: .num_remark #FormallySmooth}
###### Remark


The partial notions of this condition are: if the above morphism is a [[monomorphism]] then $f$ is a [[formally unramified morphism]], if it is an [[epimorphism]] then $f$ is a [[formally smooth morphism]].

=--

+-- {: .num_defn #AbstractFormallyEtaleObject}
###### Definition

An object $X \in \mathbf{H}$ is called **formally &#233;tale** if the morphism $X \to *$ to the [[terminal object]] is formally &#233;tale.

=--

+-- {: .num_prop #AbstractFormallyEtaleObjectDirect}
###### Proposition

The object $X$ is formally &#233;tale precisely if 

$$
  u^* X \to u^! X
$$

is an [[isomorphism]].

=--

This appears as ([KontsevichRosenberg, def. 5.3.2](#KontsevichRosenbergSpaces)).

### Properties

+-- {: .num_prop}
###### Proposition

Formally &#233;tale morphisms are closed under composition.

=--

This appears as ([KontsevichRosenberg, prop. 5.4](#KontsevichRosenbergSpaces)).

+-- {: .proof}
###### Proof

This follows by the [[pasting law]] for pullbacks: let $f : X \to Y$ and $g : Y \to Z$ be two formally &#233;tale morphisms.  Then by definition both of the small squares in

$$
  \array{
    u^* X &\stackrel{u^* f }{\to}& u^* Y &\stackrel{u^* g}{\to}& u^* Z
    \\
    \downarrow && \downarrow && \downarrow
    \\
    u^! X &\stackrel{u^! f }{\to}& u^! Y &\stackrel{u^! g}{\to}& u^! Z    
  }
$$

are pullback squares. Hence so is the total outer square.

=--

Using also the other case of the [[pasting law]],  the above proof shows more:

+-- {: .num_prop}
###### Proposition

If

$$
  \array{
    && Y
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
    \\
    X &&\stackrel{h}{\to}&& Z
  }
$$

is a [[commuting diagram]] such that $g$ and $h$ are formally &#233;tale, then also $f$ is formally &#233;tale.

=--


+-- {: .num_prop}
###### Proposition

Formally &#233;tale morphisms are closed under [[retract]]s.

=--

This means that if $f : X \to Y$ is formally &#233;tale and 

$$
  \array{
    A &\to & X &\to& A
    \\
    \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{p}}
    \\
    B &\to& Y &\to& B
  }
$$

is a [[commuting diagram]] such that the two horizontal composites are [[identities]], then also $p$ is formally &#233;tale.

+-- {: .proof}
###### Proof

By applying the [[natural transformation]] $ \phi : u^* \to u^!$ to this diagram we obtain a retract diagram in the category of squares, given by the naturality squares of $\phi$ on $f$ and $p$, where the middle square is a pullback square. By <a href="http://nlab.mathforge.org/nlab/show/retract#RetractsOfLimits">this proposition</a> at _[[retract]]_ this implies that also the retracting square is a pullback, which means that $p$ is formally &#233;tale.

=--

+-- {: .num_prop}
###### Proposition

If $u^*$ preserves [[pullbacks]], then formally &#233;tale morphisms are stable under pullback.

=--

+-- {: .proof}
###### Proof

Consider a [[pullback]] diagram

$$
  \array{
    A \times_Y X &\to& X
    \\
    {}^{\mathllap{p}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    A &\to& Y
  }
$$

where $f$ is formally &#233;tale.

Applying the [[natural transformation]] $\phi : u^* \to u^!$ to this yields a square of squares. Two sides of this are the [[pasting]] composite


$$
  \array{
    u^* A \times_Y X &\to& u^* X &\stackrel{\phi_X}{\to}&  u^! X
    \\
    \downarrow && \downarrow^{\mathrlap{u^* f}} 
                      && \downarrow^{\mathrlap{u^! f}}
    \\
    u^* A &\to& u^* Y &\stackrel{\phi_Y}{\to}& u^! Y
  }
$$

and the other two sides are the pasting composite

$$
  \array{
     u^* A \times_Y X &\stackrel{\phi_{A \times_Y X}}{\to}& u^! A \times_Y A
     &\stackrel{}{\to}& u^! X
     \\
     \downarrow^{} && \downarrow && \downarrow^{\mathrlap{u^! f}}
     \\
     u^* A &\stackrel{\phi_A}{\to}& u^! A &\to& u^! Y
  }
  \,.
$$

Counting left to right and top to bottom, we have that

* the first square is a pullback by assumption on $u^*$;

* the second square is a pullback, since $f$ is formally &#233;tale.

* the fourth square is a pullback since $u^!$ is [[right adjoint]] and so also preserves pullbacks;

* also the total bottom rectangle is a pullback, since it is equal to the bottom  total rectangle;

* therefore finally the third square is a pullback, by the [[pasting law]], hence also $p$ is formally &#233;tale.

=--

## Concrete notions
 {#ConcreteNotion}

We discuss realizations of the above general abstrac definition in concrete models of the axioms.

See also the concrete notions of [[formally smooth morphism]] and [[formally unramified morphism]].

### In differential geometry

The [[category]] [[SmoothMfd]] of [[smooth manifold]]s may naturally be thought of as sitting inside the more general context of the [[cohesive (∞,1)-topos]] [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s. This is canonically equipped with a notion of [[cohesive (∞,1)-topos -- infinitesimal cohesion|infinitesimal cohesion]] exhibited by its inclusion into [[SynthDiff∞Grpd]]. This implies that there is an intrinsic notion of [[formally étale morphism]]s of smooth $\infty$-groupoids in general and of smooth manifolds in particular

+-- {: .num_prop}
###### Proposition

A [[smooth function]] is a formally &#233;tale morphism in this sense precisely if it is a [[local diffeomorphism]] in the traditional sense.

=--

See <a href="http://nlab.mathforge.org/nlab/show/synthetic+differential+infinity-groupoid#StructureSheaves">this section</a> for more details.

### In noncommutative geometry

See ([RosenbergKontsevich, section 5.8](#RosenbergKontsevich))

## Related concepts

[[formally smooth morphism]] and [[formally unramified morphism]] $\Rightarrow$ **formally &#233;tale morphism**

## References

The idea of defining etale morphisms $f$ as those that get send to a pullback square by a natural transformartion goes back to lectures by [[André Joyal]] in the 1970s.

See the introduction and see section 4 of 

* [[Eduardo Dubuc]], _Axiomatic &#233;tale maps and a theorem of spectrum_, Journal of pure and applied algebra,  149 (2000)
 {#Dubuc}

The identification of the natural transformation in question with that induced by an [[adjoint triple]] ("[[Q-categories]]") and the relation to _formal_ &eacute;taleness is observed (apparently independently?) in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([[KontsevichRosenbergNCSpaces.pdf:file]], [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}

Formalization and discussion in the context of [[cohesive (∞,1)-toposes]] is in section 2.5.3 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

[[!redirects formally etale]]

[[!redirects formally étale morphism]]
[[!redirects formally étale morphisms]]

[[!redirects formally etale morphisms]]
