
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Depending a bit on context, a _hypercover_ is a local weak equivalence or local acyclic fibration in the [[model structure on simplicial presheaves]] for a given [[site]] $C$.

In particular, for $C = {*}$ the [[point]] hypercovers are hypercovers of [[simplicial sets]] and hence of [[topological spaces]].

So a hypercover is a morphism $Y \to X$ of [[simplicial presheaf|simplicial presheaves]] (thought of a [[model category|models]] for [[∞-stacks]] and hence for [[motivation for sheaves, cohomology and higher stacks|generalized spaces]]) that exhibits $Y$ as a possibly big "puffed-up" version of $X$.

The term hypercover is to be read in contrast with the term [[?ech cover]] of which it is, in general, a generalization.  If all hypercovers are [[?ech covers]] one deals with the [[?ech model structure on simplicial presheaves]]. The [[hom-sets]] in the corresponding [[homotopy category]] are then [[?ech cohomology]].

More generally in the standard [[local model structure on simplicial presheaves]] hypercovers are the local ([[stalk]]wise if the [[sheaf]] [[topos]] $Sh(C)$ has [[point of a topos|enough points]]) weak equivalences (local acyclic fibrations), of which there are more than [[?ech covers]]. One also speaks of the _hypercompletion_ of the &#268;ech model. 

Generally, [[cohomology]] defined in terms of the [[(∞,1)-topos]] [[presentable (infinity,1)-category|presented]] by the hypercompleted [[local model structure on simplicial presheaves]] has been regarded as the "right" notion of cohomology. In particular that coincides with standard [[abelian sheaf cohomology]] when restricted to the abelian case.


## Origin of the term

The term _hypercover_ originates in the fact that for
$\pi : Y \to X$ any [[regular epimorphism]], hence an 
ordinary [[cover]], the [[simplicial set|simplicial object]]

$$
  Y^\bullet
  :=
  (\cdots \to Y \times_X Y \times_X Y \stackrel{\stackrel{\to}{\to}}{\to} Y \times_X Y \stackrel{\to}{\to} Y)
$$

is an acyclic fibration

$$
  Y^\bullet \to X
$$

over $X$ of simplicial objects, but not all acyclic fibrations
arise this way: a generic hypercover of simplicial objects
is obtained by starting with a cover $Y \to X$, then choosing
a cover of the fiber product $Y \times_X Y$, and so on.


## Characterization by lifting property

Hypercovers are usually (for instance in the [[model structure on simplicial sets]] characterized as being those
morphisms $\pi : Y \to X$ for which all images 
$\pi(\partial C^n)$
of boundaries $\partial C^n$ of standard $n$-cells 
[[globe|globes]] $C^n = G^n$ or [[simplex|simplices]],
$C^n = \Delta^n$) every $n$-cell filling this boundary in 
$X$ lifts to $Y$.

Diagrammatically this means: $f : Y \to X$ is a hypercover
if for all commuting diagrams

$$
  \array{
    \partial C^n &\to & Y
    \\
    \downarrow && \downarrow^\pi
    \\
    C^n &\to& X
  }
$$

there exists a diagonal lift

$$
  \array{
    \partial C^n &\to & Y
    \\
    \downarrow &{}^{\exists}\nearrow& \downarrow^\pi
    \\
    C^n &\to& X
  }
  \,.
$$

## Hypercovers in different model categories

In the context of the [[model structure on simplicial sets]], these are the hypercovers proper. In the context of 
the [[folk model structure]] on 
[[strict ∞-categories]]
this are the 
$\omega$-functors which are $k$-[[k-surjective functor|surjective]]
for all $k$.

## Relation to fibrations

The condition on hypercovers, being _acyclic fibrations_ is closely related to the condition on _fibrations_. Usually the lifting property for fibrations is obtained from that for hypercovers by removing in the boundary $\partial C^n$ of the standard $n$-cell one face.

For instance the definition of a hypercover of simplicial sets becomes that of a [[Kan fibration]] if the full boundary $\partial \Delta$ is replaced by a [[horn]] $\Lambda^k[n]$.

In the globular set by replacing the inclusion $\partial G^n \hookrightarrow G^n$ of the boundary of the standard $n$-[[globe]] into the $n$-globe with the inclusion $G^{n-1} \hookrightarrow G^n$ of the standard $(n-1)$-globe (which is one-half of the full boundary), the above lifting condition is that of fibrations in the [[folk model structure]] on [[∞-groupoids]].


## Furhter conditions

A hypercover in the projective [[local model structure on simplicial presheaves]] that also satisfies a cofibrancy condition is called a [[split hypercover]].


## Reference

See the remark at the end of section 2, on p. 6 of

* Jardine, _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

For a thorough discussion see

* Daniel Dugger, Sharon Hollander, Daniel C. Isaksen, _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/))

[[!redirects hypercovers]]