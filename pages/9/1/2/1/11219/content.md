
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# Contents 
* table of contents 
{: toc} 

## Idea

Throughout [[mathematics]] there are various entities referred to as "numbers"; in modern mathematics it would be more accurate to refer to any one of various [[types]] called "number systems", and simply define a *number* to be a [[term]] of such a type. 

A *[[numeral]]* on the other hand is a [[syntax|syntactic]] representation of a number, part of a system of numeration. 

It is interesting to try to describe the general conditions under which something comes to be designated as a "number". After all, such number systems tend to form [[commutative rings]] or at least commutative [[rigs]], but not all commutative rigs are considered to consist of "numbers", or at least that is not how the language is used in practice. 

The root notion, known to the great ancient civilizations and particularly ancient Hellenic civilization, is that of (the system of) [[natural numbers]], and in some way or other each of the various number systems are extensions of that one. If we may attempt a broad classification, qualitatively there are two broad types of number systems: 

* systems of [[transfinite arithmetic|transfinite numbers]] (e.g., cardinal numbers, ordinal numbers, surreal numbers) 

Roughly speaking, transfinite numbers tend to be quantities that measure sizes of elements in ZF-type structures (as in [[algebraic set theory]], or in the study of games in the sense of Conway), sometimes arising through a process of [[decategorification]]. 

* structures arising in [[algebraic number theory]] 

In algebraic number theory, there seem to be two distinct general trends in the creation of new number systems from old (starting from the natural numbers): 

* * Passing to a [[completion]] in some sense 

* * Passing to a *finite* extension of some sort 

For example, one passes from the rig of natural numbers to the ring of integers through additive [[group completion]], or from the [[integral domain]] of integers to the [[field]] of rationals through a [[field of fractions]] completion. Or, one constructs number fields as finite extensions of the field of rational numbers (similarly, algebraic integers $\alpha$ inside such a number field $K/\mathbb{Q}$ as those elements such that $\mathbb{Z}[\alpha]$ is a finite rank extension of $\mathbb{Z}$). Or, one constructs various [[local field]] completions of number fields, based on the [[valuations]] one can define on them; these include the real numbers and complex numbers and $p$-adic numbers. Or, one has various finite-dimensional algebra extensions such systems, including for example the [[quaternions]] (aka Hamiltonian numbers) and [[octonions]] (aka Cayley numbers), and various $p$-adic relatives of these. 

Sometimes one singles out subtypes of such types; for example, the field of all algebraic numbers is the union of all number fields considered within the type of complex numbers. Sometimes numbers are designated according to what they are *not*, for example one speaks of irrational (= non-rational) numbers and of transcendental (= non-algebraic complex) numbers. 









## In dependent type theory
 {#InDependentTypeTheory}

Assuming the [[type of natural numbers]], we display the construction of, consecutively, the [[rings]] of 

* [[integer numbers]]

* [[rational numbers]]

* [[real numbers]]

* [[complex numbers]]

in [[dependent type theory]] with [[quotient types]] (such as [[homotopy type theory]] with the [[univalence axiom]]), as [[terms]] of [[ring]] [[structure]] (see [there](structure#RingDataStructure)):

<img src="/nlab/files/RingDataStruture-230129.jpg" width="740">

Here we use the notation for [[dependent functions]], [[dependent pairs]] and their [[type telescopes]] from *[[dependent functions and dependent pairs -- table]]*.

Throughout we omit displaying the certificates of [[identification type]] involved ([[associativity]] etc.). Mostly their construction is immediate, a little thought is required only for the [[convergence of a sequence|convergence]] certificates of the operations on the [[real numbers]]: We show the "regular Cauchy real number type" due to [Bishop (1967)](#Bishop67); the ideas for obtaining the required identification certificates may be found in [Bishop (1967, pp. 15)](#Bishop67) and [Bishop & Bridges (1985, pp. 18)](#BishopBridges85), full formalization in [[Agda]] is in [Lundfall (2015)](#Lundfall15),  [Murray (2022)](#Murray22).

For $X \,\colon\, Set$ and $P \colon X \to Prop$ an [[equivalence relation]] with [corresponding](dependent+type#TypeBundlesReflectedInTypeUniverse) $R \,\coloneqq\, (x \colon X) \times P(x)$, we write

$$
  X / R \,\colon\, Set
$$

for the corresponding [[quotient type]].

We display functions on such quotient sets as operations on the quotien*ed* set $X$, leaving again implicit the certificates that these functions do respect the relations and hence do restrict to the quotient.
 

### The natural numbers

Here we assume the [[type of natural numbers]], for detailed discussion see there.

Just briefly:

$$
  \mathbb{N}
  \;\colon\;
  Type
$$

denotes the [[inductive type]] generated from

$$
  0 \,\colon\, \mathbb{N}
  ,\;\;\;\;
  succ \,\colon\, \mathbb{N} \to \mathbb{N}
  \,.
$$

By [[recursion]] this induces the usual operations of 
[[addition]] and [[multiplication]], which we denote as usual:

$$
  \begin{array}{ccl}
  + &\colon& \mathbb{N} \times \mathbb{N} \to \mathbb{N}
  \\
  \cdot &\colon& \mathbb{N} \times \mathbb{N} \to \mathbb{N}
  \,.
  \end{array}
$$

Not to clutter the notation, we will consecutively *overload* this notation in the following. For example, the addition of integer numbers in the following is defined on representatives as

$$
  (n_1 ,\, m_1)
  \;+\;
  (n_2 ,\, m_2)
  \;\;
  =
  \;\;
  \big(
    n_1 + n_2
    ,\,
    m_1 + m_2
  \big)
$$

and it is tacitly understood that the addition symbol operation on the left goes $\mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$, while that on the right is the one from above: $\mathbb{N} \times \mathbb{N} \to \mathbb{N}$.


### The integer numbers

The [[ring]] of [[integer numbers]]:

\[
  \label{TypeOfIntegers}
  \begin{array}{l}
    \mathllap{
      \vdash
      \;\;\;\;\;\;
    }
    \big(
      \mathbb{Z}
      ,\,
      0 
      ,\,
      +
      ,\,
      -
      ,\,
      1
      ,\,
      \cdot
    \big)
    \;\colon\;
    Ring
    \\
    \text{where}
    \\
    \begin{array}{ccl}
      \mathbb{Z}
      &\coloneqq&
      \mathbb{N} \times \mathbb{N}
      \;\bigg/\;
      \big(
        (n_1,\,m_1)
        ,\,
        (n_2,\,m_2)
        \;\colon\;
        \mathbb{N} \times \mathbb{N}
      \big)
      \times
      Id_{\mathbb{N}}
      \big(
        n_1 + m_2
        ,\;
        m_1 + n_2
      \big)
      \\
      0 
      &\coloneqq& 
      (0,0)
      \\
      + 
      &\colon&
      \big(
        (n_1,\,m_1)
        ,\,
        (n_2,\,m_2)
      \big)
      \;\mapsto\;
      \big(
        n_1 + n_2
        ,\,
        m_1 + m_2
      \big)
      \\
      - 
      &\colon&
      (n,\, m)
      \;\mapsto\;
      (m,\, n)
      \\
      1 
      &\coloneqq& 
      \big( 
        \mathrm{succ}(0) 
        ,\,
        0 
      \big)
      \\
      \cdot 
      &\colon&
      \big(
        (n_1,\,m_1)
        ,\,
        (n_1,\,m_2)
      \big)
      \;\mapsto\;
      \big(
        n_1 \cdot n_2
        +
        m_1 \cdot m_2
       ,\;\;
       m_1 \cdot n_2
       +
       n_1 \cdot m_2
      \big)
    \end{array}
  \end{array}
\]

The inclusion of [[natural numbers]] into [[integer numbers]]:

\[
  \begin{array}{rcl} 
    \iota \;\colon &
    \mathbb{N}
    &\longrightarrow&
    \mathbb{Z}
    \\
    &
    n &\mapsto& (n,\,0)
  \end{array}
\]

The [[ordering]] of [[integer numbers]]:

\[
  \label{OrderRelationOnIntegers}
  \begin{array}{rrcl}
    \leq \;\colon
    &
    \mathbb{Z} \times \mathbb{Z}
    &\longrightarrow&
    Prop
    \\
    &
    (n_1 ,\, n_2) 
      &\mapsto& 
    (k \colon \mathbb{N}) 
     \times 
    Id_{\mathbb{Z}}
    \big(    
      n_2 ,\;  n_1 + \iota(k) 
    \big)
  \end{array}
\]

The [[positive number|positive]] [[integer numbers]]:

\[
  \label{PositiveNaturalNumbers}
    \mathbb{Z}_+
    \;\coloneqq\;
    (n \,\colon\, \mathbb{Z})
    \times
    (1 \leq n)
\]


### The rational numbers
 
The [[ring]] of [[rational numbers]]:
\[
  \label{DataStructureOfRationalNumbers}
  \begin{array}{l}
    \mathllap{
      \vdash
      \;\;\;\;\;\;
    }
    \big(
      \mathbb{Q}
      ,\,
      0
      ,\,
      +
      ,\,
      -
      ,\,
      1
      ,\,
      \cdot
    \big)
    \;\colon\;
    Ring
    \\
    \text{where}
    \\
    \begin{array}{ccl}
      \mathbb{Q}
      &\coloneqq&
     \mathbb{Z} 
       \times
     \mathbb{Z}_+
     \;\bigg/\;
     \big(
       (p_1 ,\, q_1)
       ,\,
       (p_1 ,\, q_2)
       \,:\,
       \mathbb{Z}  
       \times
       \mathbb{Z}_+
     \big)
     \times
     \Id_{\mathbb{Z}}
     \big(
       p_1 \cdot q_2 
       ,\;
       q_1 \cdot p_2
     \big)
      \\
      0 &\coloneqq& (0,1)
      \\
      + 
      &:&
      \big(
        (p_1 ,\, q_1)
        ,\,
        (p_2 ,\,q_2)
      \big)
      \;\;\mapsto\;\;
      \big(
        p_1 \cdot q_2 
        \,+\,
        p_2 \cdot q_1
        ,\;\;
        q_1 \cdot q_2
      \big)
      \\
      - 
      &\colon&
      (p,\,q) 
        \;\mapsto\;
      (-p,\, q)
      \\
      1 
      &\coloneqq& 
      (1,\, 1)
      \\
      \cdot 
      &\colon&
      \big(
        (p_1,\, q_1)
        ,\,
        (p_,\,q_2)
      \big)
      \;\mapsto\;
      \big(
        p_1 \cdot p_2
        ,\;
        q_1 \cdot q_2
      \big)
    \end{array}
  \end{array}
\]

[[ordering]] of the rational numbers induced from the ordering (eq:OrderRelationOnIntegers) of the integer numbers:

\[
  \label{OrderRelationOnRationals}
  \begin{array}{rrcl}
    \leq \;\colon
    &
    \mathbb{Q} \times \mathbb{Q}
    &\longrightarrow&
    Prop
    \\
    &
    \big(
      (q_1 ,\, p_1)
      ,\,
      (q_2 ,\, p_2)
    \big)
      &\mapsto& 
    \big(
      q_1 \cdot p_2 
      \,\leq\,
       q_2 \cdot p_1
    \big)
  \end{array}
\]

When constructing the real numbers in (eq:DataStructureOfRealNumbers) below, we use the following common abbreviations:

The [[fraction|multiplicative inverse]] of a [[positive number|positive]] [[natural number]]:

\[
  \label{MultiplicativeInverseOfPositiveNaturalNumber}
  \begin{array}{rrcl}
    \frac{1}{(-)}
    \;\colon
    &
    \mathbb{N}_+
    &\longrightarrow&
    \mathbb{Q}
    \\
    &
    n &\mapsto& (1,\,n)
  \end{array}
\]

The [[monomial|square]] of a [[rational number]]:

\[
  \label{SquareOfARationalNumber}
  \begin{array}{rrcl}
    (-)^2
    \;\colon
    &
    \mathbb{Q}
    &\longrightarrow&
    \mathbb{Q}
    \\
    &
    r &\mapsto& r \cdot r
  \end{array}
\]

### The real numbers

The [[real numbers]]:

\[
  \label{DataStructureOfRealNumbers}
  \begin{array}{l}
    \mathllap{
      \vdash
      \;\;\;\;\;\;
    }
    \big(
      \mathbb{R}
      ,\,
      0
      ,\,
      +
      ,\,
      -
      ,\,
      1
      ,\,   
      \cdot
    \big)
    \;\colon\;
    Ring
    \\
    \text{where}
    \\
    \begin{array}{ccl}
    \mathbb{R}
    &\coloneqq&
    \Big(
      x_{(-)}
      :
      \mathbb{Z}_+
      \to
      \mathbb{Q}
    \Big)
    \times
    \bigg(
      (
        n,\,m \,\colon\, \mathbb{Z}_+
      )
      \to
      \Big(
        (x_n - x_m)^2
        \,\leq\, 
        \big(
          \frac{1}{n} + \frac{1}{m}
        \big)^2
      \Big)
    \bigg)
    \\
    &&
    \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
    \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
    \bigg/
    \Big(
      x_{(-)} ,\, y_{(-)}
    \Big)
    \times
    \bigg(
      (n \colon \mathbb{Z}_{+})
      \to
      \Big(
        (x_n - y_n)^2
        \,\leq\,
        \big(\frac{2}{n}\big)^2
      \Big)
    \bigg)
    \\
    0 &\colon& n \mapsto 0
    \\
    + 
    &\colon& 
    \big(
      x_{(-)}
      ,\,
      y_{(-)}
    \big)
    \;\mapsto\;
    \big(
      n \,\mapsto\, x_n + y_n
    \big)
    \\
    - 
    &\colon&
    x_{(-)}
    \,\mapsto\,
    \big(
      n \,\mapsto\, - x_n
    \big)
    \\
    1 
    &\colon&
    n \,\mapsto\, 1
    \\
    \cdot
    &\colon&
    \big(
      x_{(-)}
      ,\,
      y_{(-)}
    \big)
    \;\mapsto\;
    \big(
      n
      \,\mapsto\,
      x_n
      \cdot
      y_n
    \big)
    \end{array}
  \end{array}
\]

### The complex numbers

The [[complex numbers]]:

$$
  \begin{array}{l}
    \mathllap{
      \vdash
      \;\;\;\;\;\;
    }
    \big(
      \mathbb{C}
      ,\,
      0
      ,\,
      +
      ,\,
      -
      ,\, 
      1
      ,\,
      \cdot
    \big)
    \;\colon\;
    Ring
    \\
    \text{where}
    \\
    \begin{array}{rcl}
    \big(
      z \colon \mathbb{C}
    \big)
    &\coloneqq&
    \big(
      \mathrm{Re}(z)
      ,\,
      \mathrm{Im}(z)
    \big)
    \,:\,
    \mathbb{R} \times \mathbb{R}
    \\
    0  
    &\coloneqq& 
    (0,\,0) 
    \\
    + 
    &\colon&
    \Big(
    \big(
      \mathrm{Re}(z_1)
      ,\,
      \mathrm{Im}(z_1)
    \big)
    ,\,
    \big(
      \mathrm{Re}(z_2)
      ,\,
      \mathrm{Im}(z_2)
    \big)
    \Big)
    \;\;\mapsto\;\;
    \big(
      \mathrm{Re}(z_1) + \mathrm{Re}(z_2)
      ,\,
      \mathrm{Re}(z_1) + \mathrm{Re}(z_2)
    \big)
    \\
    - 
    &\colon&
    \big(
      \mathrm{Re}(z)
      ,\,
      \mathrm{Im}(z)
    \big)
    \;\mapsto\;
    \big(
      - \mathrm{Re}(z)
      ,\,
      - \mathrm{Im}(z)
    \big)
    \\
    1 
    &\coloneqq& 
    (1,\, 0)
    \\
    \cdot 
    &\colon&
    \Big(
      \big(
        \mathrm{Re}(z_1)
        ,\,
        \mathrm{Im}(z_1)
      \big)
      ,\,
      \big(
        \mathrm{Re}(z_2)
        ,\,
        \mathrm{Im}(z_2)
      \big)
    \Big)
    \\
    \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
    &&
    \;\;\mapsto\;\;
    \Big(
    \mathrm{Re}(z_1)
    \cdot
    \mathrm{Re}(z_2)
    -
    \mathrm{Im}(z_1)
    \cdot
    \mathrm{Im}(z_2)
    ,\;\;
    \mathrm{Re}(z_1) \cdot \mathrm{Im}(z_2)
    +
    \mathrm{Im}(z_1) \cdot \mathrm{Re}(z_2)
    \Big)
    \end{array}
  \end{array}
$$




\linebreak

\linebreak







## Related pages on numbers 

* [[natural number]]

  * [[even number]], [[odd number]]

* [[integer]]

  * [[positive number]], [[negative number]]

* [[real number]]

  * [[rational number]], [[irrational number]]

  * [[algebraic number]], [[transcendental number]]

* [[complex number]]

  * [[imaginary number]]

* [[hypercomplex number]]

  * [[dual number]], [[quaternion]], [[octonion]]

* [[adic number]] 

* [[infinite number]], [[infinitesimal]]

  * [[extended real number]]

  * [[cardinal number]]

  * [[ordinal number]]

  * [[nonstandard natural number]]

  * [[hyperreal number]]

  * [[surreal number]]


## Related entries

* [[number of supersymmetries]]

(...)

## References

History:

* [[Leo Corry]], *A Brief History of Numbers*, Oxford University Press (2015) &lbrack;[ISBN:9780198702597](https://global.oup.com/academic/product/a-brief-history-of-numbers-9780198702597)&rbrack;

Construction of the number systems up to the [[real numbers]] in [[constructive analysis]]:

* {#Bishop67} [[Errett Bishop]], *[[Foundations of Constructive Analysis]]*, McGraw-Hill (1967)

* {#BishopBridges85} [[Errett Bishop]], [[Douglas Bridges]] *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

Formalization in [[Agda]]:

* {#Lundfall15} [[Martin Lundfall]], *Formalizing real numbers in Agda* (2015) &lbrack;<a href="https://wcl.cs.rpi.edu/pilots/library/papers/TAGGED/4211-Lundfall%20(2015)%20-%20Formalizing%20Real%20Numbers%20in%20Agda.pdf">pdf</a>, [[Lundfall-RealNumbersInAgda.pdf:file]], [github](https://github.com/MrChico/Reals-in-agda)&rbrack;

* {#Murray22} [[Zachary Murray]], *Constructive Analysis in the Agda Proof Assistant* &lbrack;[arXiv:2205.08354](https://arxiv.org/abs/2205.08354), [github](https://github.com/z-murray/honours-project-constructive-analysis-in-agda)&rbrack;


[[!redirects number]]
[[!redirects numbers]]
