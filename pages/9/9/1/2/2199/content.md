
#Contents#
* table of contents
{:toc}

## Idea

The __boolean domain__ or __boolean field__ (often just: $Bool$) is a $2$-element [[set]], say $\mathbb{B} = \{ 0, 1 \}$ ("[[bits]]") or $\mathbb{B} = \{ \bot, \top \}$ ("[[bottom]]", "[[top]]"), whose elements may be interpreted as [[truth values]]. 

Note that $\mathbb{B}$ is the set of *all* [[truth values]] in [[classical logic]], but this cannot be assumed in non-classical logic such as [[intuitionistic logic]].  

If we think of $\mathbb{B}$ as a [[pointed set]] equipped with the true element, then there is an [[generalized the|effectively unique]] boolean domain.

A __boolean variable__ $x$ is a variable that takes its value in a boolean domain, as $x \in \mathbb{B}$.  If this variable depends on parameters, then it is (or defines) a [[Boolean-valued function]], that is a [[function]] whose target is $\mathbb{B}$.

An [[element]] of $\mathbb{B}$ is a __[[binary digit]]__, or __bit__.


\begin{remark}
**(relation to boolean algebra)**
\linebreak
The term 'boolean field' (or just 'field', depending on the context) is sometimes used more generally for any *[[boolean algebra]]*. In fact, the boolean domain is the [[initial object|initial]] boolean algebra.  If we interpret a boolean algebra as a [[boolean ring]], then the boolean domain is the [[finite field]] with $2$ elements.
\end{remark}

## Definition

### In type theory
 {#InTypeTheory}

As an [[inductive type]] "$Bit$", the boolean domain is defined by the following [[inference rules]]:

**[[type formation rule]]:**

$$
  \frac{
  }{
    Bit \,\colon\, Type
  }
$$

\linebreak

**[[term introduction rule]]:**

$$
  \frac{ 
  }{
    0 \,\colon\, Bit
  }
  \;\;\;\;\;
  \frac{ 
  }{
    1 \,\colon\, Bit
  }
$$

\linebreak

**[[term elimination rule]]:**

$$
  \frac{
    b \,\colon\, Bit \;\vdash\; P(b)
    ;\;
    \;\;
    0_P \,\colon\, P(0)
    ;\;
    \;\;
    1_P \,\colon\, P(1)
  }{
    ind_{(P,\,0_P,\,1_P)} 
      \,\colon\, 
    \underset{b \colon Bit}{\prod} P(b)
  }
$$

\linebreak

**[[computation rules]]:**

$$
  \frac{
    b \,\colon\, Bit \;\vdash\; P(b)
    ;\;
    \;\;
    0_P \,\colon\, P(0)
    ;\;
    \;\;
    1_P \,\colon\, P(1)
  }{
    \begin{array}{l}
    ind_{(P,\,0_P,\,1_P)}(0) \;=\; 0_P
    ;\;
    \\
    ind_{(P,\,0_P,\,1_P)}(1) \;=\; 1_P
    \end{array}
  }
$$


## References

See also:

* Wikipedia, *[Boolean domain](https://en.wikipedia.org/wiki/Boolean_domain)*

Discussion in [[type theory]] as a simple example of an [[inductive type]]:

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]), [p. 37](https://ncatlab.org/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=43) of _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

Discussion in [[homotopy type theory]]:

* {#AwodeyGambinoSojakova} [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], §3.1 in: *Inductive types in homotopy type theory*, LICS'12 (2012) 95–104 &lbrack;[arXiv:1201.3898](http://arxiv.org/abs/1201.3898), [doi:10.1109/LICS.2012.21](https://doi.org/10.1109/LICS.2012.21)&rbrack;
 

* [[Egbert Rijke]], Exc. 4.2 (pp. 35) in: *[[Introduction to Homotopy Type Theory]]* (2023) &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;


[[!redirects Boolean domain]]
[[!redirects boolean variable]]
[[!redirects Boolean variable]]
[[!redirects Boolean field]]
[[!redirects boolean field]]
[[!redirects Boolean fields]]
[[!redirects boolean fields]]

[[!redirects boolean]]
[[!redirects booleans]]

[[!redirects Boolean]]
[[!redirects Booleans]]

[[!redirects Bit]]


