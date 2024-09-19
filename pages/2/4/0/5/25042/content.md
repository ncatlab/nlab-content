\tableofcontents

## Definition

The principle of **weak function extensionality** states that the [[dependent product type]] of a family of contractible types is itself contractible. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isContr}(B(x))}{\Gamma \vdash \mathrm{weakfunext}(\lambda x.p(x)):\mathrm{isContr}\left(\prod_{x:A} B(x)\right)}$$

This is equivalent to the condition that the dependent product type of a family of [[h-propositions]] itself is an [[h-proposition]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isProp}(B(x))}{\Gamma \vdash \mathrm{weakfunext}(\lambda x.p(x)):\mathrm{isProp}\left(\prod_{x:A} B(x)\right)}$$

Weak function extensionality is not equivalent to the [[principle of unique choice]]. The principle of unique choice states that the dependent product type of a family of contractible types is pointed

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isContr}(B(x))}{\Gamma\vdash \mathrm{uniquechoice}(\lambda x.p(x)):\prod_{x:A} B(x)}$$

## Properties

* Weak function extensionality is equivalent to [[function extensionality]]. 

* In the presence of a [[universe of all propositions]] $\Omega$, weak function extensionality is equivalent to [[impredicative polymorphism]] for $\Omega$. 

## See also

* [[function extensionality]]
* [[principle of unique choice]]

## References

Weak function extensionality appears in section 13.1 of 

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)