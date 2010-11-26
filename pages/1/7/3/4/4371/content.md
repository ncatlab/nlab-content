
# Double negation
* table of contents
{: toc}

## Definition

Double negation is the operation from $P$ to $\neg{\neg{P}}$, where $\neg$ is [[negation]].  In other words, double negation is the [[composite]] of [[negation]] with itself.


## In logic

In [[classical logic]], the double negation of any [[truth value]] or [[proposition]] is itself.  More abstractly, double negation is the [[identity function]] on any [[boolean algebra]].

In [[intuitionistic logic]], double negation is weaker than the identity.  That is, we have $P \Rightarrow \neg{\neg{P}}$ but not conversely.  In [[paraconsistent logic]], it is the other way around.  More abstractly, this holds in any [[Heyting algebra]] (intuitionistic) or its dual (paraconsistent).

In [[linear logic]], double negation is the identity again, although linear logic also has notions of intuitionistic negation and paraconsistent negation which act as above.


## In locale theory

Even in [[classical mathematics]], a [[frame]] is a Heyting algebra but not a boolean algebra.  Accordingly, double negation is usually not the identity on a frame.  However, the operation of double negation is a [[nucleus]] on any frame.

Thus, every [[locale]] $L$ has a [[sublocale]] given by that nucleus, called the __double negation sublocale__ and denoted $L_{\neg\neg}$.  This sublocale is [[dense sublocale|dense]], and in fact it is the smallest dense sublocale of $L$, the [[intersection]] of all dense sublocales.

Classically, we have $L = L_{\neg\neg}$ if and only if $L$ is the [[discrete locale]] on some [[set]] $S$ of points.  In [[constructive mathematics]], $S$ must also have [[decidable equality]].


## In topos theory

The notion of double negation sublocale may be [[categorification|categorified]] from locales to [[toposes]].  (More details needed ....)


[[!redirects double negation]]
[[!redirects double negations]]
[[!redirects double-negation]]

[[!redirects double negation sublocale]]
[[!redirects double negation sublocales]]
[[!redirects double negation nucleus]]
[[!redirects double negation nuclei]]
[[!redirects double-negation sublocale]]
[[!redirects double-negation sublocales]]
[[!redirects double-negation nucleus]]
[[!redirects double-negation nuclei]]
