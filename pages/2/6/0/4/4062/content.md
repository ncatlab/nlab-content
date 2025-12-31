
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

\begin{proposition}\label{MateBijection}
**(mate bijection)**
\linebreak
Given a [[2-category]] $K$, [[adjunction|adjoint pairs]] $(\eta,\epsilon) \colon f \dashv u \colon b \to a$ and $(\eta',\epsilon') \colon f' \dashv u' \colon b' \to a'$, and [[1-morphisms|1-cells]] $x \colon a \to a'$ and $y \colon b \to b'$, there is a [[bijection]]
$$ K(a,b')(f' x,y f) \cong K(b,a')(x u,u' y) $$
given by [[pasting]] with the [[unit of an adjunction|unit]] of one adjunction and the [[counit of an adjunction|counit]] of the other, i.e.:

\begin{tikzcd}[
   sep = 30pt
  ]
    a
    \ar[r, "{ x }"{description}]
    \ar[d, "{ f }"{description}]
    &
    a'
    \ar[
      d, 
      "{ f' }"{description}
    ]
    \ar[
      dl,
      Rightarrow,
      shorten=10pt,
      "{ \lambda }"
    ]
    \ar[
      rr,
      phantom,
      shift right=20pt,
      "{ \mapsto }"
    ]
    &&
    b
    \ar[d, equals]
    \ar[r, "{ u }"{description}]
    &
    a
    \ar[
      dl,
      Rightarrow,
      shorten=10pt,
      "{ \epsilon }"
    ]
    \ar[r, "{ x }"{description}]
    \ar[d, "{ f }"{description}]
    &
    a'
    \ar[
      d, 
      "{ f' }"{description}
    ]
    \ar[
      dl,
      Rightarrow,
      shorten=10pt,
      "{ \lambda }"
    ]
    \ar[r, equals]
    &
    a'
    \ar[
      dl,
      Rightarrow,
      shorten=10pt,
      "{ \eta' }"
    ]
    \ar[
      d,
      equals
    ]
    \\
    b
    \ar[r, "{ y }"{description}]
    &
    b'
    &&
    b
    \ar[r, equals]
    &
    b
    \ar[r, "{ y }"{description}]
    &
    b'
    \ar[r, "{ u' }"{description}
    ]
    &
    a'
\end{tikzcd}

and

\begin{tikzcd}[
   sep = 30pt
  ]
    b
    \ar[r, "{ y }"{description}]
    \ar[d, "{ u }"{description}]
    &
    b'
    \ar[
      d, 
      "{ u' }"{description}
    ]
    \ar[
      from=dl,
      Rightarrow,
      shorten=10pt,
      "{ \mu }"{swap}
    ]
    \ar[
      rr,
      phantom,
      shift right=20pt,
      "{ \mapsto }"
    ]
    &&
    a
    \ar[d, equals]
    \ar[r, "{ f }"{description}]
    &
    b
    \ar[
      from=dl,
      Rightarrow,
      shorten=10pt,
      "{ \eta }"{swap}
    ]
    \ar[r, "{ y }"{description} ]
    \ar[d, "{ u }"{description}]
    &
    b'
    \ar[
      d, 
      "{ u' }"{description}
    ]
    \ar[
      from=dl,
      Rightarrow,
      shorten=10pt,
      "{ \mu }"{swap}
    ]
    \ar[r, equals]
    &
    b'
    \ar[
      from=dl,
      Rightarrow,
      shorten=10pt,
      "{ \epsilon' }"{swap}
    ]
    \ar[
      d,
      equals
    ]
    \\
    a
    \ar[r, "{ x }"{description}]
    &
    a'
    &&
    a
    \ar[r, equals]
    &
    a
    \ar[r, "{ x }"{description}]
    &
    a'
    \ar[r, "{ f' }"{description}
    ]
    &
    b'
\end{tikzcd}

\end{proposition}


\begin{proof}\label{ProofOfMateBijection}
That this is a bijection follows easily from the [[triangle identities]], which say that the gray-shaded cells in the following [[pasting diagram]] cancel out;

\begin{tikzcd}[
   sep = 30pt
  ]
    \color{gray}
    a
    \ar[
      d, 
      gray,
      "{ f }"{description}
    ]
    \ar[r, equals, gray]
    &
    \color{gray}a
    \ar[
      dl,
      gray,
      Rightarrow,
      shorten=10pt,
      "{ \eta }"
    ]
    \ar[d, equals, gray]
    \\
    \color{gray}
    b
    \ar[d, equals, gray]
    \ar[r, gray, "{ u }"{description}]
    &
    a
    \ar[
      dl,
      gray,
      Rightarrow,
      shorten=10pt,
      "{ \epsilon }"{gray}
    ]
    \ar[r, "{ x }"{description}]
    \ar[d, "{ f }"{description}]
    &
    a'
    \ar[
      d, 
      "{ f' }"{description}
    ]
    \ar[
      dl,
      Rightarrow,
      shorten=10pt,
      "{ \lambda }"
    ]
    \ar[r, gray, equals]
    &
    \color{gray}
    a'
    \ar[
      dl,
      gray,
      Rightarrow,
      shorten=10pt,
      "{ \eta' }"
    ]
    \ar[
      d,
      gray,
      equals
    ]
    \\
    \color{gray}
    b
    \ar[r, gray, equals]
    &
    b
    \ar[r, "{ y }"{description}]
    &
    b'
    \ar[r, gray, "{ u' }"{description}
    ]
    \ar[
      d, gray, equals
    ]
    &
    \color{gray}
    a'
    \ar[
      dl,
      gray,
      Rightarrow,
      shorten=10pt,
      "{ \epsilon' }"
    ]
    \ar[d, gray, "{ f' }"]
    \\
    & & 
    \color{gray}
    b'
    \ar[r, equals, gray]
    &
    \color{gray}
    b'
\end{tikzcd}

\end{proof}


\begin{definition}\label{TerminologyOfMates}
The 2-cells $\lambda$ and $\mu$ in prop. \ref{MateBijection} are called **mates** &lbrack;[Kelly & Street (2006) p. 87](#KellyStreet06); [Leinster (2004), pp. 150](#Leinster04)&rbrack;
 (earlier: *[[conjugate transformation of adjoints|conjugates]]*, [MacLane (1971), p. 98](#MacLane71), see Exp. \ref{ConjugateTransformationOfAdjoints} below) with respect to the adjunctions $f \dashv u$ and $f' \dashv u'$ (and to the 1-cells $x$ and $y$).
\end{definition}


## Properties

### General

+-- {: .num_prop}
###### Proposition

Strict [[2-functors]] preserve adjunctions and [[pasting diagrams]], so that if $F \colon K \to J$ is a 2-functor and if $\lambda$ and $\mu$ are mates wrt $f \dashv u$ and $f' \dashv u'$ in $K$, then $F \lambda$ and $F \mu$ are mates wrt $F f \dashv F u$ and $F f' \dashv F u'$ in $J$.

=--

+-- {: .num_prop}
###### Proposition

If $\alpha \colon F \Rightarrow G$ is a [[2-natural transformation]], then the naturality identities $\alpha_b \circ F f = G f \circ \alpha_a$ and $\alpha_a \circ F u = G u \circ \alpha_b$ are mates wrt $F f \dashv F u$ and $G f \dashv G u$.

=--

### Naturality

There are two [[double categories]] with objects those of $K$, vertical arrows [[adjoint pairs]] in $K$ and horizontal arrows 1-cells of $K$.  In one the 2-cells are those of the form $\lambda$ above, while in the other they are those of the form $\mu$.  It is easily shown, as in Kelly--Street, that the triangle identities and the definition of composition of adjoints make these two double categories isomorphic.  So for any $K$ there is a double category $Adj(K)$, defined up to isomorphism as above but with mate-pairs in $K$ as 2-cells.

What this means is that, for example, the mate of a square coming from a [[pasting diagram]] is given by pasting the mates of the individual 2-cells (whenever this makes sense).

In the double category $Adj(K)$, every vertical arrow has both a [[companion]] (the left adjoint) and a [[conjoint]] (the right adjoint).  (In fact, in some sense it is the universal double category constructed from $K$ with this property.)  Therefore, it is equivalent to a [[2-category equipped with proarrows]].  More explicitly, there is a forgetful functor $L \colon Adj_V(K) \to K$ from the 2-category of objects, adjunctions and mate-pairs in $K$ to $K$ that sends an adjunction $f \dashv u$ to $f$.  It is [[locally fully faithful 2-functor|locally fully faithful]], and moreover every $L f$ has a right adjoint in $K$ by definition; this gives the more traditional definition of a proarrow equipment.

## Examples
 {#Examples}

\begin{example}\label{ConjugateTransformationOfAdjoints}
**([[conjugate transformation of adjoints]])**
\linebreak
Let $F \dashv U \colon D \to C$ be an [[adjunction]] in the [[2-category]] [[Cat]], i.e. a pair of [[adjoint functors]], and $A \colon * \to C$ and $X \colon * \to D$ be [[objects]] of $C$ and $D$ considered as [[functors]] out of the [[terminal category]] $*$.  Then taking mates with respect to $1 \dashv 1 \colon * \to *$ and $F \dashv U$ yields the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism)
$$ 
  D(F A,\, X) \;\cong\; C(A,\, U X) 
$$
and the pasting operations as above yield the notion of [[conjugate transformation of adjoints]]. (This is the original notion, due to [MacLane (1971), p. 98](#MacLane71))

Moreover, the naturality of the mate correspondence yields [[natural isomorphism|naturality]] of the bijection.
\end{example}


+-- {: .num_example}
###### Example

If the ambient [[2-category]] $K$ is the [[delooping]] of a [[monoidal category]] $(\mathcal{C}, \otimes)$ in that

$$
  K \simeq \mathbf{B}_\otimes \mathcal{C}
$$

then an [[adjunction]] in $K$ is a pair of [[dual objects]] and the mate-construction is the construction of [[dual morphisms]] between [[dualizable objects]].

=--

+-- {: .num_example}
###### Example


Suppose given a [[commutative square]] (up to [[isomorphism]]) of [[functor]]s:
$$\array{ & \overset{f^*}{\to} & \\
  ^{g^*}\downarrow && \downarrow^{k^*}\\
  & \underset{h^*}{\to} & }$$
in which $f^*$ and $h^*$ have [[left adjoint]]s $f_!$ and $h_!$, respectively. (The classical example is a [[Wirthmüller context]].)  Then the [[natural isomorphism]] that makes the square commute 

$$
  k^* f^* \to h^* g^*
$$

has a mate

$$ 
  h_! k^* \to g^* f_! 
$$

defined as the composite

$$ 
  h_! k^* \overset{\eta}{\to} h_! k^* f^* f_! \overset{\cong}{\to} h_! h^* g^* f_! \overset{\epsilon}{\to} g^* f_!   
  \,.
$$

One says that the original square satisfies the **[[Beck-Chevalley condition]]** if this mate is an [[equivalence]].

=--

## Multi-variable mates

There is a version of the mate correspondence that applies to [[two-variable adjunctions]] and $n$-variable adjunctions; see [Cheng-Gurski-Riehl](#CGR).

The relationship between two of the adjoints in a multivariable adjunction can be described as a **parametrized adjunction**: fixing the variables in each of the categories that appear in the domains of both adjoints, the pair of functors define an adjunction between the remaining two categories. Relative to the parametrized adjunctions that define a multivariable adjunction, the multivariable mates can be understood as [parametrized mates](https://golem.ph.utexas.edu/category/2012/11/parametrized_mates_and_multiva.html). 

## References

The example of [[conjugate transformation of adjoints]] (but without the terminology of "mates")

* {#MacLane71} [[Saunders MacLane]], p. 98 of: _[[Categories Work|Categories for the working mathematician]]_, Graduate texts in mathematics, Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

The explicit notion of mates may be officially due to

* {#KellyStreet06} [[Max Kelly]], [[Ross Street]], §2.2 (esp. p. 87) of: *Review of the elements of 2-categories*, in: G.M. Kelly (ed.), Category Seminar, Lecture Notes in Mathematics **420** (1974) &lbrack;[doi:10.1007/BFb0063101](https://doi.org/10.1007/BFb0063101)&rbrack;

and is reviewed in:

* {#Leinster04} [[Tom Leinster]], Section 6.1, pp. 150 in: *Higher operads, higher categories*, London Math. Soc. Lec. Note Series **298**, Cambridge University Press (2004) &lbrack;[math.CT/0305049](http://arxiv.org/abs/math.CT/0305049), [doi:10.1017/CBO9780511525896](https://doi.org/10.1017/CBO9780511525896)&rbrack;

Further review and discussion:

* {#CGR} [[Eugenia Cheng]], [[Nick Gurski]], [[Emily Riehl]], _Multivariable adjunctions and mates_, J. K-Theory **13** (2014), 337–396, [doi:10.1017/is013012007jkt250](https://doi.org/10.1017/is013012007jkt250), [arXiv:1208.4520](http://arxiv.org/abs/1208.4520). 

* [[Emily Riehl]], _Parametrized mates and multivariable adjunctions_ [blog post](https://golem.ph.utexas.edu/category/2012/11/parametrized_mates_and_multiva.html).

{#ReferencesGeneralizationtoBicategories} Discussion in the generalization of [[bicategories]]:

* [[Aaron Lauda]], &#167;3 of _Frobenius algebras and ambidextrous adjunctions_, Theory and Applications of Categories, **16** 04 (2006) 84-122 &lbrack[tac:16-04](http://www.tac.mta.ca/tac/volumes/16/4/16-04abs.html)&rbrack;

* [[Richard Garner]], [[Michael Shulman]], around 13.7 of _Enriched categories as a free cocompletion_, Advances in Mathematics **289** (2016) Pages 1-94, [doi:10.1016/j.aim.2015.11.012](https://doi.org/10.1016/j.aim.2015.11.012), [arXiv:1301.3191](https://arxiv.org/abs/1301.3191).

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Def. 6.1.12 in: *2-Dimensional Categories*, Oxford University Press (2021) &lbrack;[arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378)&rbrack;



[[!redirects mates]]
[[!redirects mate correspondence]]
[[!redirects mates correspondence]]
