
> This article concerns the notion of "local field" in [[commutative algebra]]. For the notion of "local field" in [[algebraic number theory]], see [[local field]]. 

---

\tableofcontents

## Idea

In [[commutative algebra]], there are two notions of "local field", to wit: 

* As meaning "[[field of fractions]] of an [[integral domain]] that is a [[local ring]]". 

* As meaning "field of fractions of an integral domain that arises as the completion of a local ring with respect to its canonical valuation". 

The first meaning is not too serious (and is seldom if ever considered seriously), since usually a field $F$ will not uniquely determine a local subring giving rise to it, nor does this meaning imply any tight connection to local topological conditions such as local compactness. Under this interpretation, $\mathbb{Q}$ would be a "local field", which is virtually unheard of. 

The second meaning of a local field has more content, because the Cauchy completeness (with respect to an $\mathfrak{m}$-topology, where $\mathfrak{m}$ is the maximal ideal of some local ring) determines the local ring via the topology: the complement of $x$ such that $x^{-n}$ converges to $0$. The second meaning occurs in the literature, as in the famous text _Corps Loceaux_ by Serre. 

## Relation to local fields in algebraic number theory

There is nontrivial intersection with the notion of [[local field]] as defined in algebraic number theory, since the _nonarchimedean_ local fields as defined in algebraic number theory are conspicuous examples of this second meaning. Observe however that 

* The archimedean local fields in algebraic number theory $\mathbb{R}$, $\mathbb{C}$ do _not_ arise this way; 

* Under the $m$-[[adic topology]], the completion of a local ring $R$ with maximal ideal $m$, i.e., the [[inverse limit]] of the [[diagram]] 
$$\ldots R/m^{n+1} \stackrel{proj}{\to} R/m^n \to \ldots \to R/m$$
is typically not compact (and its field of fractions is not locally compact). It is of course compact if each $R/m^n$ is finite with the discrete topology. 

## See also

* [[local ring]]

* [[valuation]]

* [[integral domain]]

* [[field of fractions]]

## References

* [[Jean-Pierre Serre]], *Corps Locaux*, Berlin, New York: Springer-Verlag, ISBN 978-0-387-90424-5, MR 0554237

