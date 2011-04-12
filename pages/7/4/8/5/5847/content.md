[[!redirects formally étale morphism]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
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

be a triple of [[adjoint functor]]s with $u^*$ a [[full and faithful functor]] that preserves the [[terminal object]]. 

We may think of this as exhibiting <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">infinitesimal cohesion</a> (see there for details, but notice that in the notation used there we have $u^* = i_!$, $u_* = i^*$ and $u^! = i_*$). 

We think of the objects of $\mathbf{H}$ as [[cohesive topos|cohesive space]]s and of the objects of $\mathbf{H}_{th}$ as such cohesive spaces possibly equipped with [[infinitesimal object|infinitesimal extension]]. 

As a class of examples that is useful to keep in mind consider a [[Q-category]] $(cod \dashv \epsilon \dashv dom) : \bar A \to A$  of <a href="http://nlab.mathforge.org/nlab/show/Q-category#InfinitesimalThickening">infinitesimal thickening of rings</a> and let

$$
  ((u^* \dashv u_* \dashv u^!) : \mathbf{H}_{th} \to \mathbf{H}) := 
  ([dom,Set] \dashv [\epsilon, Set] \dashv [codom,Set] : [\bar A, Set] \to [A,Set])
$$ 

be the corresponding <a href="http://nlab.mathforge.org/nlab/show/Q-category#PresheafQCategory">Q-category of copresheaves</a>.

For any such setup there is a canonical [[natural transformation]]

$$
  u^* \to u^!
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

The partial notions are: where the above morphism is a [[monomorphism]] then $f$ is a [[formally unramified morphism]], if it is an [[epimorphism]] then $f$ is a [[formally smooth morphism]].

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

## Concrete notion
 {#ConcreteNotion}

See the concrete notions of [[formally smooth morphism]] and [[formally unramified morphism]].

## Related concepts

[[formally smooth morphism]] and [[formally unramified morphism]] $\Rightarrow$ **formally &#233;tale morphism**

[[!redirects formally etale]]
