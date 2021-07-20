
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

\begin{definition}\label{OppositeModelCategories}
**(opposite model categories)** \linebreak

If a [[category]] $C$ carries a [[model category]] structure, then the [[opposite category]] $C^{op}$ carries the **opposite model structure**: 

* its [[weak equivalences]] are those morphisms whose dual was a weak equivalence in $C$, 

* its [[fibrations]] are those morphisms that were cofibrations in $C$ 

* its [[cofibrations]] are those that were fibrations in $C$.

\end{definition}

## Properties

\begin{prop}\label{OppositeQuillenAdjunction}
**([[opposite Quillen adjunction]])** \linebreak
  Given a [[Quillen adjunction]]
  $$
    \mathcal{D}  
      \underoverset
        {\underset{R}{\longrightarrow}}
        {\overset{L}{\longleftarrow}}
        {\;\;\;\;\; \bot_{\mathrlap{{}_{Qu}}} \;\;\;\;\;}
    \mathcal{C}
    \,,
  $$
  its [[opposite adjunction]] is a Quillen adjunction 
  $$
    \mathcal{D}^{op}  
      \underoverset
        {\underset{L^{op}}{\longrightarrow}}
        {\overset{R^{op}}{\longleftarrow}}
        {\;\;\;\;\; \bot_{\mathrlap{{}_{Qu}}} \;\;\;\;\;}
    \mathcal{C}^{op}
  $$
  between the opposite model categories (Def. \ref{OppositeModelCategories}).
\end{prop}


## Related concepts

* [[slice model structure]]

* [[opposite category]], [[opposite 2-category]]

* [[opposite (∞,1)-category]]

## References

Textbook accounts:

* {#Hirschhorn02} [[Philip Hirschhorn]], Proposition 7.1.10 of: _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

[[!redirects opposite model structures]]

[[!redirects opposite model category]]
[[!redirects opposite model categories]]

[[!redirects opposite Quillen adjunction]]
[[!redirects opposite Quillen adjunctions]]

