

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

A [[model category]] is __pointed__ if its underlying [[category]]
is a [[pointed category]], i.e., if the unique
[[morphism]] from the [[initial object]] to the [[terminal object]] is an [[isomorphism]], in which case both of them are denoted by $0$ (the [[zero object]]).

In any pointed category, one has a canonical __[[zero morphism]]__
between any objects $A$ and $B$, given by the composition $A\to 0\to B$.

The [[homotopy equalizer]] of $f\colon A\to B$ and $0\colon A\to B$ is known as the [[homotopy fiber]] of $f$.

The [[homotopy coequalizer]] of $f\colon A\to B$ and $0\colon A\to B$ is known as the [[homotopy cofiber]] of $f$.

In particuar there is the homotopy (co)-fiber of the [[zero object]] with itself, the [[loop space object]]- and [[reduced suspension]]-operation. Asking these operations to be equivalences in a suitable sense leads to the concept of _[[linear model categories]]_ and _[[stable model categories]]_.

## Examples

Model categories which are pointed without being [[linear model category|linear]] or even [[stable model category|stable]]:

* [[classical model structure on pointed topological spaces]]

Pointed model categories which are [[stable model category|stable]]:

* [[model structure on spectra]]

## Related entries

* [[homotopy fiber]]

* [[homotopy cofiber]]

* [[pointed category]], [[pointed (∞,1)-category]]

* [[linear model category]]

* [[stable model category]]

## References

* [[Mark Hovey]], Chapter 6 in: _[[Model Categories]]_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s),   [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

* [Section 4 -- Homotopy fiber sequences](Introduction+to+Homotopy+Theory#HomotopyFiberSequences) in: _[[Introduction to Homotopy Theory]]_


[[!redirects pointed model categories]]