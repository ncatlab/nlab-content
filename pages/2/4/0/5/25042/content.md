\tableofcontents

## Definition

The principle of **weak function extensionality** states that the [[dependent product type]] of a family of [[contractible types]] is itself contractible. Under the [[propositions as some types]] interpretation of [[predicate logic]] in [[type theory]], this states that if in the context of the variable $x:A$ the predicate $B(x)$ is true, then the proposition that "for all $x:A$, $B(x)$" is true. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isContr}(B(x))}{\Gamma \vdash \mathrm{weakfunext}(\lambda x.p(x)):\mathrm{isContr}\left(\prod_{x:A} B(x)\right)}$$

This is different from the [[principle of unique choice]] by the condition that the [[dependent product type]] itself be contractible. 

## Properties

* Weak function extensionality is equivalent to function extensionality itself. 

* The [[axiom of choice]] implies weak function extensionality, because every [[contractible type]] is an [[inhabited]] [[h-set]], and the axiom of choice states that the [[dependent product type]] of a [[family]] of inhabited [[h-sets]] is itself inhabited. Thus, this could theoretically be called the **propositional axiom of choice**, since it is the axiom of choice restricted to h-propositions. 

## See also

* [[function extensionality]]
* [[principle of unique choice]]
* [[axiom of choice]]

## References

Weak function extensionality appears in section 13.1 of 

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)