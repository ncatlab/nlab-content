
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents 
{: toc}

##Idea
Every functor $F:C\to D$ factors as a [[final functor]] followed by a [[discrete fibration]].

##Statement
 {#Statement}

+-- {: .num_theorem Comprehensive Factorization System }
###### Theorem

Let $E$ be the class of [[final functors]] and $M$ be the class of [[discrete fibrations]]. Then $(E,M)$ is an [[orthogonal factorization system]] of [[Cat]], called the **comprehensive factorization system**.

=--

+-- {: .proof}
###### Proof

Let $F:C\to D$ be a functor.  Define $K:D^{op}\to Set$ as the left Kan extension of the constant presheaf $C^{op}\to Set$ at the singleton along $F^{op}$.  Concretely, $K d$ is the set of connected components of $d/F$. Let $E=\int K$ be the category of elements of the presheaf $K$.  Explicitly, $E$ has objects pairs $(d,[\alpha:d\to F c])$ where $[\alpha]$ denotes the connected component of $(c,\alpha)$ in $d/F$, and morphisms between objects $(d,[\alpha:d\to F c])$ and $(d',[\alpha':d'\to F c'])$ are morphisms $g:d\to d'$ such that $K(g)([\alpha'])=[\alpha'\circ g]=[\alpha]$.

Observe that $E$ is the pullback in the $1$-category $Cat$ of the forgetful functor $U:Set_{\ast}^{op}\to Set^{op}$ and $K^{op}:D\to Set^{op}$.  Let $m:E\to D$ and $p:E\to Set^{op}$ be the natural projections onto $D$ and $Set_{\ast}^{op}$, respectively, arising from this pullback.

\begin{tikzcd}
	C \\
	& E & {\text{Set}_{\ast}^{\text{op}}} \\
	& D & {\text{Set}^{\text{op}}}
	\arrow["e"{description}, dashed, from=1-1, to=2-2]
	\arrow["J", from=1-1, to=2-3]
	\arrow["F"', from=1-1, to=3-2]
	\arrow["p"', dashed, from=2-2, to=2-3]
	\arrow["m", dashed, from=2-2, to=3-2]
	\arrow["U", from=2-3, to=3-3]
	\arrow["{K^{\text{op}}}"', from=3-2, to=3-3]
\end{tikzcd}

Each object $c\in C$ has a canonical representative for a connected component of $F c/F$ given by $[id_{F c}] \in K F c$ (coming from the natural transformation $1\Rightarrow K F^{op}$ of the left Kan extension).  This determines a functor $J:C\to Set_{\ast}^{op}$ defined on objects by $J c=([id_{F c}],K F c)$ and on morphisms by $J(f)=K^{op}F(f)$. Since $U J=K^{op} F$, then by the universal property of $E$, there is a unique functor $e:C\to E$ such that $m e=F$ and $p e=J$. It is readily shown that $e(c)=(F c,[id_{F c}])$ and $e(f)=F(f)$.

A sketch that $e$ is final is given, that is, $(d,[\alpha:d\to F c])/e$ is non-empty and connected. Note that $\alpha:(d,[\alpha])\to (F c,[id_{F c}])$ is an arrow in $E$ as $K(\alpha)([id_{F c}])=[\alpha]$, thus $(d,[\alpha])/e$ is non-empty. Given arrows $f:(d,[\alpha])\to (F a,[id_{F a}])$ and $g:(d,[\alpha])\to (F b,[id_{F b}])$, one has $[f]=[\alpha]=[g]$, thus $f$ and $g$ are in the same component of $d/F$. A standard zig-zag argument shows that $f$ and $g$ are in the same connected component of $(d,[\alpha])/e$.

To show that $m$ is a discrete fibration, fix $(d,[\alpha:d\to F c]) \in E$ and let $g:d'\to d$ be a morphism in $D$. Notice that $g$ is the unique morphism $(d',[\alpha\circ g])\to (d,[\alpha])$ such that $m(g)=g$.

Now we show that $E$ and $M$ are replete subcategories of $Cat$.  Clearly they include all isomorphisms.

If functors $F:C\to D$ and $G: D\to E$ are final, then we show that $G\circ F$ is final.  For $e\in E$, there is an element $(d,\alpha:e\to G d)$ of $e/G$, and thence an element $(c,\beta:d\to F c)$ of $d/F$, so we obtain an element $(c, e \stackrel{\alpha}{\to} Gd \stackrel{G\beta}{\to} G F c)$ of $e/GF$.  Now we must show that any two elements $(c,\gamma:e\to G F c),(c',\gamma':e\to G F c')$ are connected.  Since $G$ is final, elements $(F c,\gamma)$ and $(F c',\gamma')$ of $e/G$ are connected.  It suffices to consider the case of a zig-zag of length one: a morphism $f:F c\to F c'$ such that 

\begin{xymatrix}
  e 
    \ar[r]^\gamma 
    \ar[dr]_{\gamma'} 
  & 
  G F c 
    \ar[d]^{G f} 
  \\ 
  & 
  G F c'
\end{xymatrix}

By finality of $F$, the elements $(c,id:F c\to F c)$ and $(c', f:F c\to F c')$ of $F c/F$ are connected.  A zig-zag path between them, by precomposition with $\gamma$, becomes a zig-zag path between $(c,\gamma)$ and $(c',\gamma')$.  So $G\circ F$ is final.

The proof that discrete fibrations form a subcategory is omitted.

Now we must show that the lifting problem

\begin{xymatrix}
A \ar[r]^f \ar[d]_e & X \ar[d]^m \\
B \ar[r]_g \ar@{-->}[ru]^h & Y \\
\end{xymatrix}

has a unique solution $h$ when $e\in E$ and $m\in M$.

We prove uniqueness first.  For $b\in B$, let $(a,\alpha:b\to e(a))\in b/e$.  Then $h(\alpha)$ must be the unique lifting of $g(\alpha)$, and $h(b)$ the domain of this lifting, proving uniqueness of $h$ on objects.  For $\beta:b\to b'$ in $B$, $h(\beta)$ must be the unique lifting of $g(\beta)$, so $h$ is unique (if it exists).

Now we must show that this $h$ is well-defined, functorial, and a solution to the lifting problem.  If $(a',\alpha':b\to e(a'))$ is another element of $b/e$, then WLOG let $u:a\to a'$ such that

\begin{xymatrix}
  b 
    \ar[r]^\alpha 
    \ar[dr]_{\alpha'} 
  & 
  e(a) 
    \ar[d]^{e(u)} 
  \\
  & 
  e(a')
\end{xymatrix}

Lifting this diagram, we see that $g(\alpha)$ and $g(\alpha')$ must lift to morphisms with identical domain, so $h$ is well-defined on objects.

For $\beta:b\to b'$ in $B$, let $\alpha:b'\in e(a)$, and by the diagram

\begin{xymatrix}
  b 
    \ar[r]^\beta 
    \ar[dr]_{\alpha\circ\beta} 
  & 
  b' 
    \ar[d]^\alpha 
  \\
  & 
  e(a)
\end{xymatrix}

we see that $g(\beta)$ and $g(\alpha\circ\beta)$ must lift to morphisms with identical domains, so $h(\beta)$ has domain $h(b)$.

Functoriality now follows easily from uniqueness of lifting for a discrete fibration, and it is not hard to show that $h$ is a solution to the lifting problem.

=--

Dually, there is an orthogonal factorisation system $(E,M)$ on $Cat$ for which $E$ is the class of [[initial functors]] and $M$ is the class of [[discrete opfibrations]]. To obtain this factorization, let $K$ be the left Kan extension of the constant functor $C\to Set$ at the singleton along $F$. The category of elements of $K$ is the usual category of elements construction for a covariant functor. The resulting $e$ will be initial and the resulting $m$ will be a discrete opfibration.

## Remark on the terminology

Under the functorial reformulation of the [[axiom of separation|axiom of comprehension]] by [[William Lawvere|Lawvere]] ([1970](#Lawvere70)) the comprehensive factorization can be viewed as a generalization of the epi-mono factorization of a function $f:X\to Y$ occurring in the context of set-theoretic comprehension: the best approximation of $f$ by a property in $2^Y$ (i.e. $\chi_{im f}$) has extension $im f\hookrightarrow Y$. Hence (in the notation of the above proof) the discrete fibration $m:\int K\to D$ given by the factorization $F=m{}e$ can be viewed as the "extension" of the approximation of $F$ by the "property" $K$ in $Set^{D}$.

More generally, instances of the comprehension scheme correspond to factorization systems (cf. [Berger-Kaufmann](#Bergkauf)).

## Related entries

* [[axiom of separation|comprehension scheme]]

## References

* [[Ross Street]], [[R. F. C. Walters]], *The Comprehensive Factorization of a Functor*, Bulletin of the American Mathematical Society 79(5): 936-941 ([bams:1183534973](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-79/issue-5/The-comprehensive-factorization-of-a-functor/bams/1183534973.full), [doi:10.1090/S0002-9904-1973-13268-9](https://doi.org/10.1090/S0002-9904-1973-13268-9))

Note there is a mistake in the proof of the main theorem of the paper above, as noted on page 74 of:

* {#Kelly82} [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

* {#Lawvere70} [[Lawvere]], F. W. _Equality in hyperdoctrines and comprehension schema as an adjoint functor_.  In A. Heller, ed., _Proc. New York Symp. on Applications of Categorical Algebra_, pp. 1--14.  AMS, 1970. ([[LawvereComprehension.pdf:file]])

* [[Fosco Loregian]], [[Emily Riehl]], *Categorical Notions of Fibration*, Expositiones Mathematicae **38**, 2020. ([arXiv:1806.06129](https://arxiv.org/abs/1806.06129), [doi:10.1016/j.exmath.2019.02.004](https://doi.org/10.1016/j.exmath.2019.02.004))

* {#BergKauf]}[[Clemens Berger]], [[Ralph M. Kaufmann]], *Comprehensive Factorization Systems*, Tbilisi Math. J. 10 (2017), 255-277 ([doi:10.1515/tmj-2017-0112](https://projecteuclid.org/journals/tbilisi-mathematical-journal/volume-10/issue-3/Comprehensive-factorisation-systems/10.1515/tmj-2017-0112.short))

* [[Paolo Perrone]], [[Walter Tholen]], *Kan extensions are partial colimits*, Kan Extensions are Partial Colimits. Applied Categorical Structures **30**, 685–753 (2022). ([arXiv:2101.04531](https://arxiv.org/abs/2101.04531). [doi:10.1007/s10485-021-09671-9](https://doi.org/10.1007/s10485-021-09671-9))

Internal comprehensive factorisations (and [[torsors]]) are considered in:

* [[Ross Street]], [[Dominic Verity]], *The comprehensive factorization and torsors*, [[TAC]] **23** (2010)  42-75 &lbrack;[tac:23-03](http://www.tac.mta.ca/tac/volumes/23/3/23-03abs.html)&rbrack;

A generalisation to a bicategorical factorization system on $CAT$ is considered in:

* [[Ross Street]], *Variation on a Comprehensive Theme*, [[TAC]] **37** (2021)  964-978 &lbrack;[tac:37-29](http://www.tac.mta.ca/tac/volumes/37/29/37-29.pdf)&rbrack;

[[!redirects comprehensive factorization systems]]
[[!redirects comprehensive factorization]]
[[!redirects comprehensive factorisation]]
[[!redirects comprehensive factorisation system]]
[[!redirects comprehensive factorisation systems]]

