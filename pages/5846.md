
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


#Contents#
* table of contents
{:toc}

## Idea

A [[space]] $X$ is called **formally unramified** if every [[morphism]] $Y \to X$ into it has for every [[infinitesimal object|infinitesimal thickening]] of $Y$ at most one [[infinitesimal object|infinitesimal]] extension.

(If all thickenings exist it is called a [[formally smooth morphism]]. If the thickening exist uniquely, it is called a [[formally etale morphism]].)

Traditionally this has been considered in the context of [[geometry]] over formal duals of [[ring]]s and [[associative algebra]]s. This we discuss in the section ([Concrete notion](#ConcreteNotion)). But generally the notion makes sense in any context of <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">infinitesimal cohesion</a>. This we discuss in the section 
[General abstract notion](#GeneralAbstractNotion).

The concept of formally unramified morphisms is the infinitesimal version of that of [[unramified morphisms]].

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

We may think of this as exhibiting [[cohesive (∞,1)-topos#InfinitesimalCohesion|infinitesimal cohesion]] (see there for details, but notice that in the notation used there we have $u^* = i_!$, $u_* = i^*$ and $u^! = i_*$). 

We think of the objects of $\mathbf{H}$ as [[cohesive topos|cohesive space]]s and of the objects of $\mathbf{H}_{th}$ as such cohesive spaces possibly equipped with [[infinitesimal object|infinitesimal extension]]. 

As a class of examples that is useful to keep in mind consider a [[Q-category]] $(cod \dashv \epsilon \dashv dom) : \bar A \to A$  of <a href="http://nlab.mathforge.org/nlab/show/Q-category#InfinitesimalThickening">infinitesimal thickening of rings</a> and let

$$
  ((u^* \dashv u_* \dashv u^!) 
   : 
   \mathbf{H}_{th} \to \mathbf{H}) 
   := 
  ([dom,Set] \dashv [\epsilon, Set] \dashv [codom,Set] : 
   [\bar A, Set] \to [A,Set])
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

+-- {: .num_defn #AbstractFormallyUnramifiedMorphism}
###### Definition

A morphism $f : X \to Y$ in $\mathbf{H}$ is called **formally unramified** if (eq:MorphismIntoPullback) is a [[monomorphism]].

=--

This appears as ([KontsevichRosenberg, def. 5.1, prop. 5.3.1.1](#KontsevichRosenbergSpaces)).

The dual notion, where the morphism is required to be an [[epimorphism]] is that of [[formally smooth morphism]]s. If both conditions hold, hence if the morphism is in fact an [[isomorphism]], one speaks of [[formally etale morphism]]s.

+-- {: .num_defn #AbstractFormallyUnramifiedObject}
###### Definition

An object $X \in \mathbf{H}$ is called **formally unramified** if the morphism $X \to *$ to the [[terminal object]] is formally unramified.

=--

+-- {: .num_prop #AbstractFormallyUnramifiedObjectDirect}
###### Proposition

The object $X$ is formally unramified precisely if 

$$
  u^* X \to u^! X
$$
 
is a [[monomorphism]].

=--

This appears as ([KontsevichRosenberg, def. 5.3.2](#KontsevichRosenbergSpaces)).

### Properties

+-- {: .num_prop}
###### Proposition

Formally unramified morphisms are closed under composition.

=--

This appears as ([KontsevichRosenberg, prop. 5.4](#KontsevichRosenbergSpaces)).

## Concrete notion
 {#ConcreteNotion}

For the moment see the discussion at [[unramified morphism]].

## Related concepts

* [[unramified morphism]]

* [[ramification of ideals]]

* [[formally smooth morphism]] and **formally unramified morphism** $\Rightarrow$ [[formally etale morphism]].



[[!redirects formally unramified morphisms]]
[[!redirects formally unramified]]
