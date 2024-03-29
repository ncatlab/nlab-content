
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

## Idea


In [[dependent type theory]], 
_context extension_ introduces new [[free variables]] into the [[context]].

## Definition

If $T$ is a [[type]] in a [[context]] $\Gamma$, then the __extension__ of $\Gamma$ by (a [[free variable]] of) the [[type]] $T$ is the context denoted

$$ \Gamma, x\colon T $$ 

(where $x$ is a new [[variable]]).  

(We have said 'the' extension of $\Gamma$ by $T$ using the [[generalised the]]; but it may literally be unique using certain conventions for handling [[alpha equivalence]].)

## Categorical semantics

The [[categorical semantics]] of context extension is the [[inverse image]] of the [[base change geometric morphism]] (or its analog for [[hyperdoctrines]]) along the [[projection]] morphism $T \to \Gamma$ in the [[slice topos|slice]] $\mathbf{H}_{/\Gamma}$

$$
  (\mathbf{H}_{/\Gamma})_{/T}
    \stackrel{\overset{\prod_{x : T}}{\longrightarrow}}{\stackrel{\overset{(-)\times T}{\longleftarrow}}{\underset{\sum_{x : T}}{\longrightarrow}}} 
  \mathbf{H}_{/\Gamma}
$$

Generally speaking, a [[morphism]] $\Delta \to \Gamma$ in the [[category of contexts]] (an [[interpretation]] of $\Gamma$ in $\Delta$) is a [[display morphism]] iff there is an [[isomorphism]] $\Delta \leftrightarrow \Theta$ where $\Theta$ is an extension of $\Gamma$.  (This might not actually be true in all type theories, or maybe it should be taken as the *definition* of 'display morphism'; I\'m not sure.)

## Related concepts

* [[substitution]]

[[!include notions of pullback -- contents]]

## References

The observation that context extension forms an [[adjoint pair]]/[[adjoint triple]] with [[quantifiers]] is due to

* [[Bill Lawvere]], _Adjointness in Foundations_, ([TAC](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

and further developed in 

* [[Bill Lawvere]], _Equality in hyperdoctrines and
comprehension schema as an adjoint functor_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.




[[!redirects context extension]]
[[!redirects context extensions]]
