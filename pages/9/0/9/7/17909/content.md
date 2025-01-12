
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

In [[algebra]], the *Wedderburn-Artin theorem* &lbrack;[Wedderburn 1908](#Wedderburn1908), [Artin 1927](#Artin27)&rbrack; gives a clean characterization of those [[rings]] that are [[matrix algebras]] over [[division rings]].
   
Concretely, the theorem says that any [[semisimple ring]] is a [[finite limit|finite]] [[direct sum]] of [[matrix algebras]] over [[division rings]]. (Here a [[ring]] is called *[[semisimple ring|semisimple]]* if each of its left or equivalently right [[modules]] is a finite [[direct sum]] of [[simple modules]].) 

## Statement ##

\begin{proposition}\label{TheTheorem}
**(Wedderburn--Artin Theorem)** \linebreak
Every [[semisimple ring]] is [[isomorphism|isomorphic]] to a finite [[direct sum]] of [[matrix algebras]] over [[division rings]].  A semisimple ring is [[simple ring|simple]] if and only if it is a matrix algebra over a division ring.
\end{proposition}

\begin{remark}
Beware: A [[simple ring]] may not be semisimple!  A ring is simple iff it has no two-sided ideals except $\{0\}$ and the whole ring, and in the absence of further hypotheses this does not imply that all of its left (or equivalently right) modules are direct sums of simple modules.  For example, the [[Weyl algebra]] is simple but not semisimple, and not isomorphic to a matrix algebra over a division ring.  
\end{remark}

However, a simple ring that is left or right [[Artinian ring|artinian]] is semisimple, so we have:

\begin{corollary}\label{Corollary}
\linebreak
Every [[simple ring]] that is left or right artinian is [[isomorphism|isomorphic]] to a matrix algebra over a division algebra.
\end{corollary}

There is also a version of the Wedderburn--Artin theorem for [[associative algebras]] over [[fields]]:

\begin{proposition}
**(Wedderburn--Artin Theorem for Algebras over Fields)**\linebreak 
Every [[semisimple algebra]] over a [[field]] $k$ is [[isomorphism|isomorphic]] to a finite [[direct sum]] of [[matrix algebras]] over [[division algebras]] over $k$.  A semisimple algebra over $k$ is simple if and only if it is a matrix algebra over a division algebra over $k$.
\end{proposition}

There is also a version for [[endomorphism rigs]] in a [[semiadditive category]]:

\begin{proposition}
**(Wedderburn--Artin Theorem for Endomorphism rigs)**\linebreak 
If $R$ is a [[semisimple object]] in a [[semiadditive category]] $\mathsf{A}$, then the [[endomorphism rig]] $End(R)$ is a [[finite product]] of matrix rigs over [[division rigs]]. 
\end{proposition}

## Proofs ##

There are many [[proofs]] of the Wedderburn--Artin theorem (Prop. \ref{TheTheorem}).  

### Common proof

A common modern approach proceeds as follows.  

Suppose $R$ is semisimple. Then by definition any right $R$-module is a direct sum of [[simple module|simple $R$-modules]], and any finitely generated $R$-module must be a finite direct sum of such.   Thus, the right $R$-module $R_R$ is isomorphic to a finite direct sum of simple $R$-modules, which will be [[minimal ideal|minimal]] right [[ideals]] of $R$.  Write this direct sum as

$$ 
   R_R 
    \;\cong\; 
  \bigoplus_i I_i^{\oplus m_i}
  \,,
$$

where the $I_i$ are mutually nonisomorphic [[simple module|simple]] right $R$-modules, the $i$th one appearing with multiplicity $m_i$. Then we have for the [[endomorphisms]]

$$ 
   End(R_R) 
  \;\cong\; 
  \bigoplus_i End\big(I_i^{\oplus m_i}\big) 
$$

and we can identify $End\big(I_i^{\oplus m_i}\big)$ with a ring of [[matrices]]

$$ 
  End\big(I_i^{\oplus m_i}\big) 
  \;\cong\; 
  M_{m_i}\big(End(I_i)\big) 
  \,,
$$

where the [[endomorphism ring]] $End(I_i)$ of the right $R$-module $I_i$ is a division ring by [[Schur's lemma]] because $I_i$ is simple.   Since $R \cong End(R_R)$ we conclude

$$ 
  R \;\cong\; 
  \bigoplus_i M_{m_i}\big(End(I_i)\big) 
  \,.
$$

(We use right modules because $R \cong End(R_R)$; if we used left modules we would have $R \cong End({}_R R)^{op}$, but the proof would still go through.)

### Nicholson's proof

A different style of proof can be found in [Nicholson (1993)](#Nicholson93).  A key step in this approach is "Brauer's Lemma". 

\begin{lemma}\label{BrauerLemma}
**(Brauer's Lemma)** \linebreak 
Suppose $R$ is a ring and $K \subseteq R$ is a [[minimal ideal|minimal left ideal]] with $K^2 \ne 0$.  Then $K = R e$  for some $e \in K$ with $e^2 = e$, and $e R e$ is a [[division ring]].
\end{lemma}

Here a **[[minimal ideal|minimal left ideal]]** is a nonzero left ideal for which the only smaller left ideal is $\{0\}$.   

For example, suppose $R$ is the ring of $n \times n$ matrices over some division ring $D$  This has a minimal ideal $K$ consisting of matrices with just one nonzero column, say the $j$th column.  You can see $K^2 \ne 0$.  To write $K = R e$, we can take $e$ to be the matrix that's zero everywhere except for a 1 in the $j$th row and $j$th column.  Clearly $e^2 = e$, and $e R e$ consists of matrices that are zero except in the $j$th row and $j$th column, so $e R e$ is isomorphic to $D$.

No deep techniques or preliminary lemmas are required to prove Brauer's Lemma.  

**Proof of Brauer's Lemma (\ref{BrauerLemma})**   
Since $0 \ne K^2$, we must have $K u \ne 0$ for some $u \in K$.  Of course $u \ne 0$.  But $K u$ is a left ideal contained in $K$, so by minimality 

$$ K u = K.$$

Thus $u = e u$ for some $e \in K$.  Now, let

$$  L = \{a \in K \colon a u = 0 \} $$

$L$ is a left ideal since for any $r \in R$ we have

$$ 
  a \in L 
   \; \implies \; 
  a u = 0 
    \; \implies \; 
  r a u  = 0 
    \; \implies \; 
  r a \in L
  \,.
$$

Note $L \subseteq K$ by definition, so by the minimality of $K$ we must have either $L = 0$ or $L = K$.   But $e$ is in $K$ but not in $L$, since $e u = u \ne 0$, so we must have $L = 0$.  In other words

$$ 
  a \in K 
    \; \text{and} \; 
  a u = 0 
    \quad \implies \quad 
  a = 0
  \,.
$$

To use this implication, recall that $u = e u$ so $e u = e^2 u$ so $(e - e^2)u = 0$, and take $a$ above to be $e - e^2$.   We conclude that $e - e^2 = 0$, so $e$ is [[idempotent]]:

$$ e^2 = e \,.$$

Now we claim that $K = R e$.  The reason is that $e$ is in the left ideal $K$, so $R e \subseteq K$.  Since $K$ is minimal this implies either $R e = 0$ or $R e = K$.  But $e \ne 0$ so $R e \ne 0$.

Why is $e R e$ a division ring?  Its unit is $e$, of course.  Suppose $b \in e R e$ is nonzero.  To show $b$ has an inverse, note that $R b$ is a nonzero ideal contained in $R e = K$ so by minimality $R b = R e$.   So, we must have $e = r b$ for some $r \in R$.   But this implies $e r e$ is the left inverse of $b$ in $e R e$:

$$  (e r e) b = e r (e b) = e r b = e^2 = e.$$

Finally, in a ring where every nonzero element has a *left* inverse, every element has a two-sided inverse, so it's a division ring!  To see this, say $b \ne 0$.  It has a left inverse, say $x$ for short.  To see that $x$ also the right inverse of $b$ note that $x$ must also have its own left inverse, say $y$. Thus we have $x b = 1$ and $y x = 1$, giving

$$   y = y (x b) = (y x) b = b .$$

Thus $b$ is the left inverse of $x$.  So $x$ is the right inverse of $b$.  &marker;

## Related concepts

* [[central simple algebra]]

## References

The original articles:

* {#Wedderburn1908} [[Joseph H. M. Wedderburn]]: *On hypercomplex numbers*, Proc. London Math. Soc. **s2-6** 1 (1908) 77-118 &lbrack;[doi:10.1112/plms/s2-6.1.77](https://doi.org/10.1112/plms/s2-6.1.77)&rbrack;

* {#Artin27} [[Emil Artin]]: *Zur Theorie der hyperkomplexen Zahlen*, Abh. Math. Semin. Univ. Hambg. **5** (1927) 251–260 &lbrack;[doi:10.1007/BF02952526](https://doi.org/10.1007/BF02952526)&rbrack;

Review:

* {#Nicholson93} William K. Nicholson, *A short proof of the Wedderburn--Artin theorem*, *New Zealand J. Math* **22** (1993) 83-86 &lbrack;[pdf](https://www.thebookshelf.auckland.ac.nz/docs/NZJMaths/nzjmaths022/nzjmaths022-01-010.pdf)&rbrack;

* Tsiu-Kwen Lee, *A short proof of the Wedderburn-Artin theorem*,  Communications in Algebra **45** 7 (2017) &lbrack;[doi:10.1080/00927872.2016.1233242](https://doi.org/10.1080/00927872.2016.1233242)&rbrack;

* [[John Baez]], *The Wedderburn–Artin Theorem*, n-Category Café, June 14, 2013 ([web](https://golem.ph.utexas.edu/category/2023/06/the_wedderburnartin_theorem.html))

See also:

* Wikipedia, _[Wedderburn-Artin theorem](https://en.wikipedia.org/wiki/Wedderburn%E2%80%93Artin_theorem)_

[[!redirects Wedderburn's theorem]]
[[!redirects Artin-Wedderburn theorem]]
[[!redirects Wedderburn–Artin theorem]]
[[!redirects Wedderburn–Artin Theorem]]