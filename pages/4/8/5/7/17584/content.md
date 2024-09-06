


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[formal logic]], *affine logic* refers to [[substructural logics]] which omit the [[contraction rule]] but retain the [[weakening rule]]. Conversely, affine logic is [[linear logic]] adjoined with the [[weakening rule]].

In terms of [[categorical semantics]], affine logic is modeled by ([[symmetric monoidal category|symmetric]]) [[monoidal categories]] whose [[tensor unit]] $I$ is [[terminal object|terminal]], also known as *[[semicartesian monoidal categories]]*, an example of which is the category of [[affine spaces]], whence the name.

(In contrast, the category of [[linear spaces]], ie. [[vector spaces]], serves as [[categorical semantics]] for the multiplicative fragment of [[linear logic]] &lbrack;eg. [Murfet 2014](linear+logic#Murfet14)&rbrack;, where also the [[weakening rule]] is dropped.)

## Categorical semantics

One might imagine that a more general notion of [[categorical semantics]] would be given by monoidal categories equipped with a [[natural transformation|natural]] (in $A$) family $A\to I$ of [[morphisms]] implementing [[weakening rule|weakening]] for each [[object]]. However, such an interpretation is in general badly behaved, unless one additionally requires these [[natural transformations]] to be *[[monoidal transformation|monoidal]]*, but it can be shown that this additional requirement already forces the [[tensor unit]] to be [[terminal object|terminal]] (specifically, this follows from the component at $I$ being the identity).

An example of the badly behaved case -- where the transformation is not monoidal, and the tensorial unit is not terminal -- is given by the category [[Rel]] of [[relations]], with cartesian product as tensor product (i.e., with $Rel$ as [[cartesian bicategory]]). Here a natural family of relations $A\to I$ is given by picking empty relations everywhere.  In the corresponding interpretation of affine logic, any weakening yields an empty relation, which contradicts intuitive principles like for example that "adding a dummy variable to a proof and then substituting a closed term" should not change the semantics.

## Examples

\begin{example}
  The substructural part of many forms of [[bunched logic]] are affine instead of [[linear type theory|linear]], sometimes inadvertently, ultimately due to former technical problems with formulating [[dependent linear types]] (see review in [Riley 2022 §1.7.2](dependent+linear+type+theory#Riley22Thesis)).
\end{example}



## Related concepts

* Affine **BCK** [[combinatory logic]] 

* [[antithesis interpretation]]

## References

* [[Vaughan Pratt]],  *Re: Affine*, mailing list discussion  (1997) &lbrack;[web](https://www.seas.upenn.edu/~sweirich/types/archive/1997-98/msg00135.html)&rbrack;

* [[Alexei P. Kopylov]], *Decidability of Linear Affine Logic*, Information and Computation **164** 1 (2001) 173-198 &lbrack;[doi:10.1006/inco.1999.2834](https://doi.org/10.1006/inco.1999.2834)&rbrack;

* Gianluigi Bellin , *Two Paradigms of Logical Computation in Affine Logic?*,  in: *Logic for Concurrency and Synchronisation*, Trends in Logic **15** (2003) &lbrack;[doi:10.1007/0-306-48088-3_3](https://doi.org/10.1007/0-306-48088-3_3)&rbrack; 

* {#Shulman22} [[Michael Shulman]], *Affine logic for constructive mathematics*, Bulletin of Symbolic Logic **28** 3 (2022) 327-386 &lbrack;[arXiv:1805.07518](https://arxiv.org/abs/1805.07518), [doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28)&rbrack;

See also:

* Wikipedia, *[Affine logic](https://en.wikipedia.org/wiki/Affine_logic)*



[[!redirects affine logics]]


