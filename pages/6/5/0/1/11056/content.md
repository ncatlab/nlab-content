+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a [[monoidal category]] a _self-duality_ on a [[dualizable object]] $X$ is a choice of [[equivalence]] $X \simeq X^\ast$ with its [[dual object]].

## Properties

### Relation to $\dagger$-compact structure
 {#RelationToDaggerCompactStructure}

If each object $X$ of a [[compact closed category]] is equipped with a self-duality structure $h_X : X \simeq X^\ast$, then sending morphisms to their [[dual morphisms]] but with these identifications pre- and postcomposed

$$
  (-)^\dagger \;\colon\; 
  (X \stackrel{f}{\longrightarrow} Y)
  \mapsto
  (Y \stackrel{h_Y}{\to} Y^\ast \stackrel{f^\ast}{\longrightarrow} X^\ast \stackrel{h_X^{-1}}{\to} X)
$$

constitutes a [[dagger-compact category]] structure.

See for instance ([Selinger, remark 4.5](#Selinger)).

Applied for instance to the category of finite-dimensional [[inner product spaces]] this dagger-operation sends [[matrices]] to their [[transposed matrix]]. 

## Graphical language
 {#GraphicalLanguage}

In terms of [[string diagrams]] (following Joyal and Street's conventions for [[braided monoidal categories]]), [Selinger](#Selinger) argues that the isomorphism $h_X : X \simeq X^\ast$ should be depicted as a half-twist.  In particular, for a [[tortile category]] equipped with a self-duality structure, the [[coherence]] condition

$$
(X^\ast \stackrel{h_{X^\ast}}{\to} X^{\ast\ast} \stackrel{h_X^\ast}{\to} X^\ast) \; =\; 
(X^\ast \stackrel{\theta_{X^\ast}}{\longrightarrow} X^\ast)
$$

decomposes a full [[twist]] into a pair of half-twists.

This is a special case of half-twists as described by [Egger 2011](#Egger11).

## Related concepts

* [[inner product]]

## References

* {#Selinger} [[Peter Selinger]], _Autonomous categories in which $A \simeq A^\ast$_, talk at QPL 2012 ([[SelingerSelfDual.pdf:file]])

* [[Matthew B. Young]], §3.1 in *Self-Dual Hall modules*, PhD thesis, Stony Brook (2013) &lbrack;[pdf](https://www.math.stonybrook.edu/alumni/2013-Matthew-Young.pdf), [[Young-HallModules.pdf:file]]&rbrack;

  > (in a context relating to [[orientifold]]-[[BPS state|BPS]]-algebras)


* Chenjing Bu, Def. 3.2 in: *Enumerative invariants in self-dual categories. I. Motivic invariants* &lbrack;[arXiv:2302.00038](https://arxiv.org/abs/2302.00038)&rbrack;

On half-twists as [above](#GraphicalLanguage)

* {#Egger11} [[Jeff Egger]], *On involutive monoidal categories*, Theory and Applications of Categories **25** 14 (2011) 368-393 &lbrack;[tac:25-14](http://www.tac.mta.ca/tac/volumes/25/14/25-14abs.html)&rbrack;

{#InTQFT} Under the [[cobordism hypothesis]] (which is a theorem certainly for the relevant case $n = 1$), self-dual objects in [[symmetric monoidal (infinity,1)-categories|symmetric monoidal $\infty$-categories]] correspond equivalently to *un*-oriented 1-dimensional [[TQFTs]]: 

* [[Jacob Lurie]]: Ex. 2.4.28 in: *[[On the Classification of Topological Field Theories]]*, Current Developments in Mathematics **2008** (2009) 129-280 &lbrack;[arXiv:0905.0465](http://arxiv.org/abs/0905.0465), [doi:10.4310/CDM.2008.v2008.n1.a3](https://dx.doi.org/10.4310/CDM.2008.v2008.n1.a3), [euclid:cdm/1254748657](https://projecteuclid.org/euclid.cdm/1254748657)&rbrack;

* {#Teleman16} [[Constantin Teleman]], Rem. 1.7 in: *Five lectures on topological field theory*, in *Geometry and Quantization of Moduli Spaces*, CRM Advanced Courses in Mathematics, Birkhäuser (2016) &lbrack;[doi:10.1007/978-3-319-33578-0_3](https://doi.org/10.1007/978-3-319-33578-0_3), [pdf](http://math.berkeley.edu/~teleman/math/barclect.pdf), [[Teleman-LecturesOnTFT.pdf:file]]&rbrack;

same in the non-topological case:

* {#GradyPavlov21} [[Daniel Grady]], [[Dmitri Pavlov]], Thm 6.1.5 in: *The geometric cobordism hypothesis* &lbrack;[arXiv:2111.01095](https://arxiv.org/abs/2111.01095)&rbrack;


[[!redirects self-dual objects]]

[[!redirects self-dual]]

[[!redirects self-duality]]
[[!redirects self-dualities]]