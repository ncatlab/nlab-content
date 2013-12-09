
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Dependent linear type theory should be a combination of _[[dependent type theory]]_ and _[[linear type theory]]_.

Following the notion of [[hyperdoctrine]] this should mean, in terms of [[categorical semantics]], that dependent linear type theory is for each [[context]] $\Gamma$ a [[linear type theory]]/[[star-autonomous category]] $(\mathcal{C}_{\Gamma}, \otimes, 1)$ and for each [[homomorphism]] of contexts $f \;\colon\; \Gamma_1 \longrightarrow \Gamma_2$ an [[adjoint triple]] of [[functors]]

$$
  (f_1 \dashv f^\ast \dashv f_\ast) 
    \;\colon\; 
   \mathcal{C}_{\Gamma_1}
    \stackrel{\stackrel{f_1}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longrightarrow}}{\underset{f_\ast}{\leftarrow}}}
    \mathcal{C}_{\Gamma_2}
  \,.
$$

where $f^\ast$ is [[context extension]] and where $f_!$ and $f^\ast$ are linear analogs of [[dependent sum]] and [[dependent product]], respectively. Moreover this should satisfy [[Frobenius reciprocity]], hence $f^\ast$ should be a strong [[closed monoidal functor]]. 

Equivalently this is an [[indexed closed monoidal category]] with fiberwise [[dual object|duals]].

Typically one would in addition demand the [[Beck-Chevalley condition]] for consecutive such adjoint triples.


In [[geometry]]/[[topos theory]] such a "linear hyperdoctrine" is known as _[[six operations]] yoga in [[Wirthmüller context|Wirtmüller flavor]]_. In fact there this appears in [[geometric homotopy theory]] ("[[derived functors]] on [[quasicoherent sheaves]]") hence as _dependent linear [[homotopy type theory]]_.

## Related concepts

* [[type theory]], [[homotopy type theory]]

* [[modal type theory]]

* [[stable homotopy type]]

* [[geometric homotopy type theory]]

* [[cohesive homotopy type theory]]

[[!redirects dependent linear type theories]]

[[!redirects linear dependent type theory]]
[[!redirects linear dependent type theories]]

[[!redirects linear dependent homotopy type theory]]
[[!redirects linear dependent homotopy type theories]]

[[!redirects dependent linear homotopy type theory]]
[[!redirects dependent linear homotopy type theories]]


