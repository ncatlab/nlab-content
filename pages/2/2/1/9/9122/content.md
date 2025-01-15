


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesion
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a context of [[differential cohesion]] the _infinitesimal shape modality_, _crystalline modality_ or _&#233;tale modality_ $\Im $ characterizes [[coreduced objects]]. It is itself the [[right adjoint]] in an [[adjoint modality]] with the [[reduction modality]] and the [[left adjoint]] in an [[adjoint modality]] with the [[infinitesimal flat modality]].

## Definition

A context of [[differential cohesion]] is determined by the existence of an [[adjoint triple]] of  [[modalities]]

$$
  \Re \dashv \Im \dashv \&
  \,,
$$

where $\Re$ and $\&$ are [[idempotent monad|idempotent]] [[comonads]] and $\Im $ is an [[idempotent monad]].

Here $\Im $ is the **infinitesimal shape modality**. The [[reflective subcategory]] that it defines is that of [[coreduced objects]].

## Properties

### Relation for formally &#233;tale morphisms

The [[modal types]] of $\Im $ in the context of some $X$, i.e. those $(Y\to X) \in \mathbf{H}_{/X}$ for which the naturality square of the $\Im $-[[unit of a monad|unit]] 

$$
  \array{
     Y &\longrightarrow& \Im Y
     \\
     \downarrow && \downarrow
     \\
     X &\longrightarrow& \Im X
  }
$$
 
is a ([[homotopy pullback|homotopy]]) [[pullback]] square, are the [[formally étale morphisms]] $Y \to X$.

### Relation to de Rham spaces

For $X$ a [[geometric homotopy type]], the result of applying the infinitesimal shape modality yields a type $ \Im X$ which has the interpretation of the [[de Rham space]] of $X$. See there for more.

### Relation to jet bundles

For any object $X$ in [[differential cohesion]], the [[base change]] [[comonad]] $Jet \coloneqq i^\ast i_\ast$ along the [[unit of a monad|unit]] $i \colon X \to \Im X$ has the interpretation of being the [[jet comonad]] which sends [[bundles]] over $X$ to their [[jet bundles]].

### Relation to crystalline cohomology

The [[cohomology]] of $\Im X$ has the interpretation of [[crystalline cohomology]] of $X$. See there for more.


## Related concepts

[[!include cohesion - table]]


## References
 {#References}

The infinitesimal shape modality as part of an extension of [[cohesive (infinity,1)-toposes|cohesive $\infty$-toposes]] to [[differential cohesive (infinity,1)-toposes|differential cohesive $\infty$-toposes]] was introduced in

* [[Urs Schreiber]], Def. 3.5.4 in: _[[schreiber:differential cohomology in a cohesive topos]]_ &lbrack;[arXiv:1310.7930](https://arxiv.org/abs/1310.7930)&rbrack;

mimicking an analogous construction (cf. *[[de Rham space]]*) for [[schemes]] in

* {#SimpsonTeleman} [[Carlos Simpson]], [[Constantin Teleman]], Section 3 of: _deRham theorem for $\infty$-stacks_ (1997) &lbrack;[pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf), [[SimpsonTeleman-deRham.pdf:file]]&rbrack;

and further developed (in relation to [[jet comonads]] and [[partial differential equations]]) in

* [[Igor Khavkine]], [[Urs Schreiber]], *[[schreiber:Synthetic geometry of differential equations]]* &lbrack;[arXiv:1701.06238](https://arxiv.org/abs/1701.06238)&rbrack;

reviewed in

* {#Loregian19} [[Fosco Loregian]], pp. 30 in: *Cohesion in Rome*, talk notes (Dec. 2019)  &lbrack;[pdf](https://tetrapharmakon.github.io/stuff/cohesive_rome.pdf), [[LoregianCohesion.pdf:file]]&rbrack;

Its implementation in [[HoTT]] and application to [[Cartan geometry]] is considered in

* {#Wellen18} [[Felix Wellen]], _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))

* [[Felix Cherubini]]: *Synthetic $G$-jet-structures in modal homotopy type theory*, Mathematical Structures in Computer Science (2024) 1–35 &lbrack;[doi:10.1017/S0960129524000355](https://doi.org/10.1017/S0960129524000355), [arXiv:1806.05966](https://arxiv.org/abs/1806.05966)&rbrack;


Called the *crystalline modality* in:

* [[David Jaz Myers]], *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))

[[!redirects infinitesimal shape modalities]]

[[!redirects infinitesimal shape]]

[[!redirects crystalline modality]]
[[!redirects crystalline modalities]]
