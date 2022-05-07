
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

# Contents #
* table of contents 
{: toc}

## Idea

The **cellular approximation theorem** states that every [[continuous map]] between [[CW complexes]] (with chosen CW presentations) is [[homotopy|homotopic]] to a [[cellular map]], hence a map that respects the [[cell complex]]-structure, mapping [[n-skeleta]] to $n$-skeleta for all $n$.

This is the analogue for [[CW-complexes]] of the [[simplicial approximation theorem]] (sometimes also called lemma): that every continuous map between the [[geometric realizations]] of [[simplicial complexes]] is [[homotopy|homotopic]] to a map induced by a map of [[simplicial complexes]] (after subdivision). 

## Statement 

+-- {: .num_theorem} 
###### Theorem 

Given a [[continuous map]] $f \colon (X, A) \to (X', A')$ between [[relative CW-complexes]] that is cellular on a subcomplex $(Y, B)$ of $(X, A)$, there is a cellular map $g \colon (X, A) \to (X', A')$ that is [[homotopy|homotopic]] to $f$ relative to $Y$. 

=-- 


It follows that if two cellular maps between CW-complexes are homotopic, then they are so by a cellular homotopy.

([Spanier 66, p. 404](#Spanier66), review in [May 99, Section 10.4](#May99), [Hatcher 02, Thm. 4.8](#Hatcher02))

## References

* {#Spanier66} [[Edwin Spanier]], ch. 7. sec. 6, cor. 18 (p. 404)  of: _Algebraic topology_, Springer 1966 ([doi:10.1007/978-1-4684-9322-1](https://link.springer.com/book/10.1007/978-1-4684-9322-1))

* {#May99} [[Peter May]],  sec. 10.4 in: _[[A Concise Course in Algebraic Topology]]_, University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* {#Hatcher02} [[Allen Hatcher]], Theorem 4.8, [p. 349](http://pi.math.cornell.edu/~hatcher/AT/AT.pdf#page=358) in: _Algebraic topology_, Cambridge Univ. Press 2002 ([web](http://pi.math.cornell.edu/~hatcher/AT/ATpage.html))




See also

* Wikipedia, _[Cellular approximation](http://en.wikipedia.org/wiki/Cellular_approximation)_


