
## In dependent type theory

Assuming the [[type of natural numbers]], we display the construction of, consecutively, the [[rings]] of 

* [[integer numbers]]

* [[rational numbers]]

* [[real numbers]]

* [[complex numbers]]

in [[dependent type theory]] with [[quotient types]] (such as [[homotopy type theory]] with the [[univalence axiom]]), as [[terms]] of [[ring]] [[structure]] (see [there](structure#RingDataStructure)):

<img src="/nlab/files/RingDataStruture-230129.jpg" width="740">

Here we use the notation for [[dependent functions]], [[dependent pairs]] and their [[type telescopes]] from *[[dependent functions and dependent pairs -- table]]*.

Throughout we omit displaying the certificates of [[identification type]] involved ([[associativity]] etc.). Mostly their construction is immediate, a little thought is required only for the [[real numbers]]: We show the "regular Cauchy real number type" due to [Bishop (1967)](#Bishop67); the ideas for obtaining the required identification certificates may be found in in [Bishop (1967, pp. 15)](#Bishop67) and [Bishop & Bridges (1985, pp. 18)](#BishopBridges85), full formalization in [[Agda]] is in [Murray (2022)](#Murray22).

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


### The [[rational numbers]]
 
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
  \begin{array}{l}
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
        (x_n - y_b)^2
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
    \begin{array}{ccl}
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




## References

Construction of the number systems up to the [[real numbers]] in [[constructive analysis]]:

* {#Bishop67} [[Errett Bishop]], *[[Foundations of Constructive Analysis]]*, McGraw-Hill (1967)

* {#BishopBridges85} [[Errett Bishop]], [[Douglas Bridges]] *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

Formalization in [[Agda]]:

* {#Murray22} [[Zachary Murray]], *Constructive Analysis in the Agda Proof Assistant* &lbrack;[arXiv:2205.08354](https://arxiv.org/abs/2205.08354), [github](https://github.com/z-murray/honours-project-constructive-analysis-in-agda)&rbrack;












$$
  \begin{array}{ll}  
    xx
    \\
    \hline
    yy
  \end{array}
$$

§



\begin{tikzcd}
b_{ij}
\;\;
  :=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[yscale=1, xscale=1.3]

\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);


\begin{scope}[shift={(-1.4,0)}]
\draw[line width=1.4]
  (-.3,1) to (-.3,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw
  (+.05,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(-0,0)}]
\draw[line width=1.4]
  (-.6,1) to (-.6,-1);
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=4, white]
  (+.4,1) to (+.4,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw[line width=4, white]
  (+.2,1) to (+.2,-1);
\draw[line width=1.4]
  (+.2,1) to (+.2,-1);
\draw
  (-.1,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(+.8,0)}]
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=1.2]
  (+.3,1) to (+.3,-1);
\draw
  (-.01,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=4, white]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);
\draw[line width=1.4]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);

\begin{scope}
\clip
  (-.9,0) rectangle (+.3,1.2); 
\draw[line width=4, white]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\end{scope}

\draw
  (-.8,-1.3) node {
    \scalebox{.7}{
      \color{blue}
      $i$
    }
  };

\draw
  (+.4,-1.3) node {
    \scalebox{.7}{
      \color{blue}
      $j$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;
=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[yscale=-1, xscale=-1.3]

\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);


\begin{scope}[shift={(-1.4,0)}]
\draw[line width=1.4]
  (-.3,1) to (-.3,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw
  (+.05,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(-0,0)}]
\draw[line width=1.4]
  (-.6,1) to (-.6,-1);
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=4, white]
  (+.4,1) to (+.4,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw[line width=4, white]
  (+.2,1) to (+.2,-1);
\draw[line width=1.4]
  (+.2,1) to (+.2,-1);
\draw
  (-.1,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(+.8,0)}]
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=1.2]
  (+.3,1) to (+.3,-1);
\draw
  (-.01,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=4, white]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);
\draw[line width=1.4]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);

\begin{scope}
\clip
  (-.9,0) rectangle (+.3,1.2); 
\draw[line width=4, white]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\end{scope}

\draw
  (-.8,+1.3) node {
    \scalebox{-.7}{
      \color{blue}
      $j$
    }
  };

\draw
  (+.4,+1.3) node {
    \scalebox{-.7}{
      \color{blue}
      $i$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}



## Definition in an additive category

Let $\mathcal{C}$ be an [[additive category]]; that is, $\mathcal{C}$ is enriched over [[abelian groups]]. For $A, B$ a [[pair]] of objects in $\mathcal{C}$, a biproduct ((#MacLane) p.194) is an object $A \oplus B$ together with maps

\begin{tikzcd}
A \arrow[rr, "i_{1}"', shift right] &  & A \oplus B \arrow[ll, "p_{1}"', shift right] \arrow[rr, "p_{2}", shift left] &  & B \arrow[ll, "i_{2}", shift left]
\end{tikzcd}

which satisfy the identities

$$
i_{1};p_{1}=1_{a}, \quad i_{2};p_{2}=1_{b}, \quad p_{1};i_{1} + p_{2};i_{2}
$$