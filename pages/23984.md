> This page is about the notion in [[homotopy type theory|homotopy]] [[type theory]]. For *[[parallel transport]]* via [[connections]] in [[differential geometry]] see there. For the relation see [below](#RelationToParallelTransport).

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##
 {#Idea}

In [[Martin-Löf type theory]], given 

* a [[type]] $A$, 

* a [[judgment]] $z \colon A \vdash B(z)\ \mathrm{type}$ (hence an $A$-[[dependent type]] $B$), 

* [[terms]]$\,$ $x \colon A$ and $y \colon A$, 

* an [[term]] of their [[identity type]] $p \colon (x =_A y)$, 

then there are compatible **transport functions** 

\[
  \label{TheTransportFunctions}
  \overrightarrow{\mathrm{tr}}_{B}^{p}:B(x) \to B(y) 
  \;\;\;
  \text{and}
  \;\;\;
  \overleftarrow{\mathrm{tr}}_{B}^{p}:B(y) \to B(x)
  \,,
\] 

such that for all $v:B(y)$, the [[fiber]] of $\overrightarrow{\mathrm{tr}}_{B}^{p}$ at $v$ is [[contractible]], and for all $u:B(x)$, the [[fiber]] of $\overleftarrow{\mathrm{tr}}_{B}^{p}$ at $u$ is [[contractible]]. 

## Examples and applications

\begin{remark}\label{RelationToParallelTransport}
**(relation to parallel transport -- [[schreiber:differential cohomology in a cohesive topos|dcct §3.8.5]], [ScSh12 §3.1.2](cohesive+homotopy+type+theory#SchreiberShulman2012))**
\linebreak
  In [[cohesive homotopy type theory]] the [[shape modality]] $\esh$ has the [[shape via cohesive path ∞-groupoid|interpretation]] of turning any cohesive type $X$ into its [[path infinity-groupoid|path $\infty$-groupoid]] $\esh X$: The [[1-morphisms]] $p \colon (x =_{\esh X} y)$ of $\esh X$ have the [[shape via cohesive path ∞-groupoid|interpretation]] of being (whatever identities existed in $X$ composed with) cohesive (e.g. [[continuous function|continuous]] or [[smooth function|smooth]]) *[[paths]]* in $X$, and similarly for the higher order paths-of-paths.

Accordingly, an [[shape modality|$\esh X$]]-[[dependent type]] $B$ has the interpretation of being a "[[local system]]" of $B$-[[coefficients]] over $X$, namely a $B(x)$-[[fiber infinity-bundle|fiber $\infty$-bundle]] equipped with a [[flat infinity-connection|flat $\infty$-connection]]. 

In this case, the identity transport (eq:TheTransportFunctions) along paths in [[shape modality|$\esh X$]] has the interpretation of being the *[[parallel transport]]* (in the original sense of [[differential geometry]]) with respect to this [[flat infinity-connection|flat $\infty$-connection]] (and the [[higher parallel transport]] when applied to paths-of-paths).
\end{remark}

## See also ##

* [[identity type]]

* [[dependent identity type]]

## References ##

* [[Univalent Foundations Project|UVP]], [§2.3 "Type families and fibrations"](https://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf#page=81) in: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects transports]]
[[!redirects transporting]]

[[!redirects identity transport]]
[[!redirects identity transports]]

[[!redirects type transport]]
[[!redirects type transports]]
