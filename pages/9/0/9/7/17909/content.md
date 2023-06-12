
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

## Idea ##

The Wedderburn--Artin theorem gives a clean characterization of rings that are matrix algebras over division rings.   
A [[ring]] is [[semisimple ring| semisimple]] if each of its left (or equivalently, right) modules is a finite direct sum of [[simple modules]].   The Wedderburn--Artin theorem says that any semisimple ring is a finite direct sum of matrix algebras over [[division rings]].

## Statement ##

**Wedderburn--Artin Theorem**.   Every semisimple ring is isomorphic to a finite direct sum of matrix algebras over division rings

There is also a version for [[associative algebras]] over [[fields]]:

**Wedderburn--Artin Theorem for Algebras over Fields**.   Every semisimple algebra over a field $k$ is isomorphic to a finite direct sum of matrix algebras over division algebras over $k$.

## Proof ##

There are many proofs of the Wedderburn--Artin theorem.  A common modern approach proceeds as follows.  Suppose $R$ is semisimple.  Then the right $R$-module ${}_R R$ is isomorphic to a finite direct sum of simple $R$-modules (which are the same as minimal right ideals of $R$).  Write this direct sum as

$$ {}_R R \cong \bigoplus_i I_i^{\oplus m_i} $$

where the $I_i$ are mutually nonisomorphic simple right $R$-modules, the $i$th one appearing with multiplicity $m_i$. Then we have

$$ End({}_R R) \cong \bigoplus_i End(I_i^{\oplus m_i}) $$

and we can identify $End(I_i^{\oplus m_i})$ with a ring of matrices

$$ End(I_i^{\oplus m_i}) \cong M_{m_i}(End(I_i)) $$

where the endomorphism ring $End(I_i)$ of the right $R$-module $I_i$ is a division ring by [[Schur's lemma]] because $I_i$ is simple.

Here is a different style of proof:

* William K. Nicholson, [A short proof of the Wedderburn--Artin theorem](https://www.thebookshelf.auckland.ac.nz/docs/NZJMaths/nzjmaths022/nzjmaths022-01-010.pdf), *New Zealand J. Math* **22** (1993), 83--86.

A key step in this approach is "Brauer's Lemma". 

**Brauer's Lemma.**   Suppose $R$ is a ring and $K \subseteq R$ is a minimal left ideal with $K^2 \ne 0$.  Then $K = R e$  for some $e \in K$ with $e^2 = e$, and $e R e$ is a division ring.

Here a **minimal left ideal** is a nonzero left ideal for which the only smaller left ideal is $\{0\}$.   For example, suppose $R$ is the ring of $n \times n$ matrices over some division ring $D$  This has a minimal ideal $K$ consisting of matrices with just one nonzero column, say the $j$th column.  You can see $K^2 \ne 0$.  To write $K = R e$, we can take $e$ to be the matrix that's zero everywhere except for a 1 in the $j$th row and $j$th column.  Clearly $e^2 = e$, and $e R e$ consists of matrices that are zero except in the $j$th row and $j$th column, so $e R e$ is isomorphic to $D$.

No deep techniques or preliminary lemmas are required to prove Brauer's Lemma.  

**Proof of Brauer's Lemma.**   Since $0 \ne K^2$, we must have $K u \ne 0$ for some $u \in K$.  Of course $u \ne 0$.  But $K u$ is a left ideal contained in $K$, so by minimality 

$$ K u = K.$$

Thus $u = e u$ for some $e \in K$.  Now, let

$$  L = \{a \in K : a u = 0 \} $$

$L$ is a left ideal since for any $r \in R$ we have

$$ a \in L \; \implies \; a u = 0 \; \implies \; r a u  = 0 \; \implies \; r a \in L.$$

Note $L \subseteq K$ by definition, so by the minimality of $K$ we must have either $L = 0$ or $L = K$.   But $e$ is in $K$ but not in $L$, since $e u = u \ne 0$, so we must have $L = 0$.  In other words

$$ a \in K \; and \; a u = 0 \quad \implies \quad a = 0. $$

To use this implication, recall that $u = e u$ so $e u = e^2 u$ so $(e - e^2)u = 0$, and take $a$ above to be $e - e^2$.   We conclude that $e - e^2 = 0$, so $e$ is [[idempotent]]:

$$ e^2 = e.$$

Now we claim that $K = R e$.  The reason is that $e$ is in the left ideal $K$, so $R e \subseteq K$.  Since $K$ is minimal this implies either $R e = 0$ or $R e = K$.  But $e \ne 0$ so $R e \ne 0$.

Why is $e R e$ a division ring?  Its unit is $e$, of course.  Suppose $b \in e R e$ is nonzero.  To show $b$ has an inverse, note that $R b$ is a nonzero ideal contained in $R e = K$ so by minimality $R b = R e$.   So, we must have $e = r b$ for some $r \in R$.   But this implies $e r e$ is the left inverse of $b$ in $e R e$:

$$  (e r e) b = e r (e b) = e r b = e^2 = e.$$

Finally, in a ring where every nonzero element has a *left* inverse, every element has a two-sided inverse, so it's a division ring!  To see this, say $b \ne 0$.  It has a left inverse, say $x$ for short.  To see that $x$ also the right inverse of $b$ note that $x$ must also have its own left inverse, say $y$. Thus we have $x b = 1$ and $y x = 1$, giving

$$   y = y (x b) = (y x) b = b .$$

Thus $b$ is the left inverse of $x$.  So $x$ is the right inverse of $b$.  &marker;


## Related concepts

* [[central simple algebra]]

## References

* Wikipedia, _[Wedderburn--Artin theorem](https://en.wikipedia.org/wiki/Wedderburn%E2%80%93Artin_theorem)_

[[!redirects Wedderburn's theorem]]
[[!redirects Artin-Wedderburn theorem]]