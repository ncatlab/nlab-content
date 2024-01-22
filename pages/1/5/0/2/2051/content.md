
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### In sets

\begin{definition}
A [[discrete  group]] $G$ is called a __Hopfian group__ if every [[surjection|surjective]] [[endomorphism]] $\phi \colon G\to G$ is an [[isomorphism]]. 

[[formal duality|Dually]], it is called __coHopfian__ if any [[injection|injective]] endomorphism of $G$ is an isomorphism.
\end{definition}

### In concrete categories

As the [[epimorphisms]] and [[monomorphisms]] in [[Grp]] are precisely the surjections and injections (see [[epimorphisms of groups are surjective]]), the definition generalises immediately to that of a [[Hopfian object]] in any [[category]]. In other words, we *could* define an object $X$ to be Hopfian if every epimorphic endomorphism is an isomorphism (cf. *[[Dedekind finite object]]*). 

Whatever that generalization is worth, much of the literature (such as [Varadarajan 1992](#Varadarajan92)) adopts the more concrete notion: 

\begin{definition}
Given a [[concrete category]] $U \colon C \to Set$ with $U$ a [[faithful functor]], say that an [[object]] $X$ of $C$ is *Hopfian* if every [[morphism]] $\phi \colon X \to X$ in $C$ with $U(\phi)$ surjective is an isomorphism. 
\end{definition}

\begin{remark}
Notice that if $U$ if [[faithful functor|faithful]], then $\phi$ is epimorpic if $U(\phi)$ is surjective.
\end{remark}

\begin{remark}
For [[monadic functors]] $U \colon C \to Set$, this surjectivity assumption is the same as the assumption that $\phi$ is a [[regular epimorphism]]. 
\end{remark}

Of course there is a dual notion of being co-Hopfian; here the hypothesis that $U(\phi)$ is injective frequently coincides simply with $\phi$ being monomorphic -- certainly that is true if $U$ [[preserved limit|preserves]] [[finite limits]] (which is frequently the case in application). 

## Examples

\begin{example}
Clearly all [[finite groups]] are both Hopfian and coHopfian.
\end{example}

\begin{example}
Using Nielsen's method, one can show that every finitely generated [[free group]] and the union of any ascending chain of such free groups (for example, $\mathbb{Q}$) are Hopfian. 
\end{example}

\begin{example}
Every [[torsion-free group|torsion-free]] [[hyperbolic group]] is Hopfian.
\end{example}

## References 

* {#Varadarajan92} K. Varadarajan, _Hopfian and Co-Hopfian Objects_, Publicacions Matem&#225;tiques, Vol. 36 (1992), 293-317. ([web](http://www.raco.cat/index.php/PublicacionsMatematiques/article/viewFile/37700/37574)) 
  


[[!redirects Hopf group]]
[[!redirects coHopfian group]]
[[!redirects co-Hopfian group]]