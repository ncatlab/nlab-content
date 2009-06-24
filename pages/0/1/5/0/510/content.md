# Idea #

In [[homotopy theory]], a _spectrum_ is an object containing only "stable information."  One way for a higher category theorist to understand the notion of spectrum is to start with the idea of a [[groupal n-groupoid|grouplike]] [[k-tuply monoidal n-category|stably monoidal]] $\infty$-[[infinity-groupoid|groupoid]].  To a homotopy theorist, this means a space with a multiplication which is associative, unital, commutative, and has inverses up to all coherent higher homotopies (as encoded, for instance, by an [[operad]]).

The collection of grouplike stably monoidal $\infty$-groupoids is a sub-$(\infty,1)$-category of the $(\infty,1)$-category of spectra, called the _connective_ ones.  The passage from connective spectra to arbitrary spectra can perhaps best be explained as analogous to the passage from bounded-below [[chain complex|chain complexes]] to arbitrary chain complexes.  So while a connective spectrum, like a topological space, contains data only in dimensions $\ge 0$, an arbitrary spectrum contains data in all dimensions.  In particular, a spectrum $E$ has homotopy groups $\pi_k(E)$ for all _integers_ $k$, all of which are abelian groups.

# Definition #

There are many "models" for spectra, all of which present the same homotopy theory (and in fact, nearly all of them are [[Quillen equivalence|Quillen equivalent]] [[model category|model categories]]).  One fairly simple, and quite useful, approach is to define a spectrum $E$ to be a [[sequence]] of [[pointed object|based]] spaces $E_n$, for all natural numbers $n$, together with isomorphisms $E_n \cong \Omega E_{n+1}$, where $\Omega$ denotes the based [[loop space]].  The idea is that $E_0$ contains the information of $E$ in dimensions $k\ge 0$, $E_1$ contains the information of $E$ in $k\ge -1$ (but shifted up by one, so that it is modeled by the $\ge 0$ information in the space $E_1$), and so on.

#Remarks#

* In direct analogy to how topological spaces form the archetypical example, [[Top]], of an [[(infinity,1)-category]], spectra form the archetypical example $Sp(Top)$ of a [[stable (infinity,1)-category]]. In fact, there is a general procedure for turning any [[pointed category|pointed]] [[(infinity,1)-category]] $C$ into a stable $(\infty,1)$-category $Sp(C)$, and doing this to the category $Top_*$ of [[pointed object|pointed]] spaces yields $Sp(Top)$.

#Examples of spectra#

* [[Eilenberg-MacLane spectrum]]

* [[K-theory spectrum]]

* [[tmf]]


# Conjectures #

There might be a type of categorical structure related to a spectrum in the same way that $\infty$-categories are related to $\infty$-groupoids.  In other words, it would contain $k$-cells for all integers $k$, not necessarily invertible.  Some people have called this conjectural object a **$Z$-category**.   "Connective" $Z$-categories could perhaps then be identified with stably monoidal $\infty$-categories.
