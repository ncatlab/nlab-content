
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



\tableofcontents

## Idea

A *quadratic Gauss sum* is a sum of square-powers of primitive [[roots of unity]]:

\[
  \label{BasicQuadraticGaussSum}
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{2 \pi \mathrm{i}}{k}
    s^2
  }
  \;\;
  \in
  \;
  \mathbb{C}
  \,,
  \;\;\;\;\;\;
  \text{for} \; k \in \mathbb{N}_{> 0}
  \,.
\]

A *generalized Gauss sum* is a variant of this expression, admitting other prefectors or powers of $s$ in the exponent.

## Properties

### Ordinary quadratic Gauss sum

\begin{proposition}\label{EvaluationOfQuadraticGaussSum}
**(evaluation of the quadratic Gauss sum)**
\linebreak
The basic quadratic Gauss sum (eq:BasicQuadraticGaussSum) evaluates to:
\[
  \label{EvaluationFormulaOfQuadraticGaussSum}
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{2 \pi \mathrm{i}}{k}
    s^2
  }
  \;\;
  =
  \;\;
  \left\{
  \begin{array}{ccl}
    (1 + \mathrm{i}) \sqrt{k} &\vert& k = 0 \;mod\; 4
    \\
    \sqrt{k} &\vert& k = 1 \;mod\; 4
    \\
    0 &\vert& k = 2 \;mod\; 4
    \\
    \mathrm{i} \sqrt{k} &\vert& k = 3 \;mod\; 4
    \mathrlap{\,.}
  \end{array}
  \right.
\]
\end{proposition}
The original proof is due to [Gauss 1811](#Gauss1811), an early alternative proof is due to [Dirichlet 1835](#Dirichlet35), reviewed in [Dirichlet 1871](#Dirichlet1871). Several other proofs have been given. Modern review includes [Lang 1970 p 87](#Lang70), [Berndt & Evans 1981](#BerndtEvans81), [Doyle 2016  (1.1)](#Doyle16), [Ram Murty & Pathak 2017 Thm. 1.1](#MurtyPathak17), [Taylor 2022 Thm. 1.16](#Taylor22).

For odd $k$ we have more generally:

\begin{proposition}\label{EvaluationOfQuadraticGaussSumWithFactor}
**(evaluation of the quadratic Gauss sum with multiple exponents)**
\linebreak
For $k \in 2\mathbb{N} + 1$ and $q \in \mathbb{Z}$ we have
\[
  \label{EvaluationFormulaOfQuadraticGaussSum}
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{2 \pi \mathrm{i}}{k}
    q
    s^2
  }
  \;\;=\;\;
  (q \vert k)
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{2 \pi \mathrm{i}}{k}
    s^2
  }
  \;\;
  =
  \;\;
  \left\{
  \begin{array}{lcl}
    
    \,
    (1 + \mathrm{i}) \sqrt{k} &\vert& k = 0 \;mod\; 4
    \\
    (q \vert k)
    \,
    \sqrt{k} &\vert& k = 1 \;mod\; 4
    \\
    \phantom{(q \vert k)}
    \;
    0 &\vert& k = 2 \;mod\; 4
    \\
    (q \vert k)
    \,
    \mathrm{i} \sqrt{k} &\vert& k = 3 \;mod\; 4
    \mathrlap{\,,}
  \end{array}
  \right.
\]
where "$(a \vert b)$" is the [[Jacobi symbol]].
\end{proposition}
([Lang 1970 "QS 4" (p 86)](#Lang70), cf. also [Doyle 2016  (1.1)](#Doyle16) but beware of typos there)


### Qudratic Gauss sum with halved exponents
 {#PropertiesOfQuadraticGaussSumWithHalvedExponents}


\begin{proposition}
\label{EvaluationOfQuadraticGaussSumWithHalvedExponents}
**(evaluation of quadratic Gauss sum with halved exponents)**
\linebreak
For $k \in 2 \mathbb{N}_{\gt 0}$ the quadratic Gauss sum with halved exponents evaluates to:
$$
  \tfrac{1}{\sqrt{k}}
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    s^2
  }
  \;\;
  =
  \;\;
   e^{\pi \mathrm{i}/4}
$$
\end{proposition}
The following proofs are given in [MO:a/4232289](https://math.stackexchange.com/a/4232289/58526) (using Prop. \ref{EvaluationOfQuadraticGaussSum}), in [MO:a/489863](https://mathoverflow.net/a/489863/381) (using Prop. \ref{ReciprocityForQuadraticGaussSumWithHalvedExponents}), and in [MO:a/489956](https://mathoverflow.net/a/489956/381) (using Prop. \ref{TheLandsbergSchaarIdentity}).
\begin{proof}
Using the ordinary quadratic Gauss evaluation (Prop. \ref{EvaluationOfQuadraticGaussSum}) we set 
$
  r \coloneqq k/2 \,\in\, \mathbb{N}
$
and compute as follows:
$$
  \begin{array}{ccl}
    \sum_{s=0}^{k-1}
    \,
    e^{
      \tfrac
        { \pi \mathrm{i}}
        { k }
      s^2
    }
    &\equiv&
    \sum_{s=0}^{2r-1}
    \,
    e^{
      \tfrac
        {2 \pi \mathrm{i}}
        { 4r }
      s^2
    }
    \\
    &=&
    \tfrac{1}{2}
    \Big(
      \sum_{s=0}^{2r-1}
      \,+\,
      \sum_{s=2r}^{4r-1}
    \Big)
    \,
    e^{
      \tfrac
        {2 \pi \mathrm{i}}
        { 4r }
      s^2
    }
    \\
    &=&
    \tfrac{1}{2}
    \sum_{s=0}^{4r-1}
    \,
    e^{
      \tfrac
        {2 \pi \mathrm{i}}
        { 4r }
      s^2
    }
    \\
    &=&
    \tfrac{1}{2}
    (1 + \mathrm{i}) \, \sqrt{4r}
    \\
    &=&
    e^{\pi \mathrm{i}/4} \, \sqrt{2r}
    \\
    &=& 
    e^{\pi \mathrm{i}/4} \, \sqrt{k}
    \,,
  \end{array}
$$
where the steps are, in order of appearance:

1. definition of $r$,

1. observing that the summands are $2r$-periodic, because 

   $$
     e^{
       \tfrac{\pi \mathrm{i}}{2r}
       (n + 2r)^2
     }
     \;=\;
     e^{
       \tfrac{\pi \mathrm{i}}{2r}
       n^2
     }
     e^{
       2\pi \mathrm{i}
       ( n + r )
     }    
     \;=\;
     e^{
       \tfrac{\pi \mathrm{i}}{2r}
       n^2
     }
     \,,
   $$

1. collecting summands,

1. the classical evaluation formula (eq:EvaluationFormulaOfQuadraticGaussSum),

1. rearranging factors,

1. definition of $r$.

Alternatively, using reciprocity laws like the Landsberg-Schaar identity [below](#LandsbergSchaarIdentity):

The statement is the immediate special case of Prop. \ref{TheLandsbergSchaarIdentity} for $q \equiv r \coloneqq k/2$ and $p \equiv 1$.

Similarly, from Prop. \ref{ReciprocityForQuadraticGaussSumWithHalvedExponents} we immediately get:
$$
  \begin{array}{ccl}
  \tfrac{1}{\sqrt{k}}
  \sum_{s = 0}^{k-1}
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    s^2
  }
  &\equiv&
  G(k,0,1)
  \\
  &=&
  e^{ \pi \mathrm{i}/4 } 
  \,
  \overline{G(1,0,k)}
  \\
  &\equiv&
  e^{ \pi \mathrm{i}/4 } 
  \mathrlap{\,.}
  \end{array}
$$
\end{proof}



### Landsberg-Schaar identity
 {#LandsbergSchaarIdentity}

The ordinary Gauss sums and those with halved exponents are related by:

\begin{proposition}\label{TheLandsbergSchaarIdentity}
**(Landsberg-Schaar identity)**
For $p, q \in \mathbb{N}_{\gt 0}$ we have
$$
  \tfrac{1}{\sqrt{p}}
  \sum_{n = 0}^{p-1}
  \,
  e^{
    2 \pi \mathrm{i}
    \tfrac{q}{p}n^2
  }
  \;\;=\;\;
  \tfrac
    { e^{\pi \mathrm{i}/4} }
    { \sqrt{2q} }
  \sum_{n = 0}^{2q - 1}
  \,
  e^{
    -\pi \mathrm{i} 
    \tfrac{p}{2q} n^2
  }
  \,.
$$
\end{proposition}
([Schaar 1850](#Schaar1850), [Dym & McKean 1972 §4.6](#DymMcKean72), [Armitage & Rogers 2000](#ArmitageRogers2000), [Ustinov 2022](#Ustinov22))

Yet more generally:

\begin{proposition}
\label{ReciprocityForQuadraticGaussSumWithHalvedExponents}
**(reciprocity for generalized quadratic Gauss sum with halved exponents)**
\linebreak
The expressions
\[
  \label{QuadraticGaussSumWithHalvedExponents}
  G(a,b,c)
  \;\coloneqq\;
  \tfrac{1}{\sqrt{c}}
  \sum_{n=0}^{c-1}
  \, 
  e^{  
    \tfrac{\pi \mathrm{i}}{c}
    \big(
      a n^2
      +
      2 b n 
    \big)
  }
  \,,
  \;\;\;\text{for}\;\;
  a, c \in \mathbb{N}_{\gt 0}
  ,\,
  b \in \mathbb{Z}
  ,\,
  a c \in 2 \mathbb{N}
  \,.
\]
satisfy
$$
  G(a,b,c)
  \;=\;
  e^{
    \big(
    \tfrac{\pi \mathrm{i}}{4}
    -
    \tfrac{b^2}{a c}
    \big)
  }
  \;
  \overline{G(c,b,a)}
$$
(where $\overline{(-)}$ denotes [[complex conjugation]]).
\end{proposition}
This is proven by [Harcos](#Harcos).


## Related concepts

* [[quadratic reciprocity]]


## References

The original proof of Prop. \ref{EvaluationOfQuadraticGaussSum} is due to 

* {#Gauss1811} [[Carl F. Gauss]]: *Summatio Quarumdam Serierum Singularium* Societas Regia Scientiarum Gottingensis (1811)

and an early alternative proof, using a variant of [[Poisson summation]], is due to 

* {#Dirichlet35} [[P. G. L. Dirichlet]]: &Uuml;ber eine neue Anwendung bestimmter Integrale auf die Summation endlicher oder unendlicher Reihen. Abhandlungen der K&ouml;niglich Preussischen Akademie der Wissenschaften (1835)

reviewed in:

* {#Dirichlet1871} [[P. G. L. Dirichlet]]: *Vorlesungen über Zahlentheorie*, Vieweg und Sohn (1871) &lbrack;[eudml:204463](https://eudml.org/doc/204463)&rbrack;

* {#Casselman11} [[Bill Casselman]]: *Dirichlet's calculation of Gauss sums*, L’ Enseignement Math&eacute;matique **2** 57 (2011) 281–301 &lbrack;[pdf](https://content.ems.press/assets/public/full-texts/serials/lem/57/3/12115/online/10.4171-lem-57-3-2.pdf), [[Casselman-DirichletGaussSum.pdf:file]]&rbrack;

Survey and review:

* {#BerndtEvans81} [[Bruce C. Berndt]], [[Ronald J. Evans]]: *The determination of Gauss sums*, Bull. Amer. Math. Soc. **5** (1981) 107-129 &lbrack;[ams:bull/1981-05-02/S0273-0979-1981-14930-2](https://www.ams.org/journals/bull/1981-05-02/S0273-0979-1981-14930-2), [euclid:1183548292](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-5/issue-2/The-determination-of-Gauss-sums/bams/1183548292.full)&rbrack;

* [[Bruce C. Berndt]], [[Ronald J. Evans]], Kenneth S. Williams: *Gauss and Jacobi Sums*, John Wiley & Sons (1998) &lbrack;[ISBN:978-0-471-12807-6](https://www.wiley-vch.de/de/fachgebiete/mathematik-und-statistik/gauss-and-jacobi-sums-978-0-471-12807-6)&rbrack;

* {#Taylor22} Laurence R. Taylor: *Gauss Sums in Algebra and Topology* &lbrack;[arXiv:2208.06319](https://arxiv.org/abs/2208.06319)&rbrack;


Further discussion:

* {#Lang70} [[Serge Lang]], §IV.3 in: _Algebraic number theory_, Graduate Texts in Mathematics **110**, Springer (1970, 1986, 1994, 2000) &lbrack;[doi:10.1007/978-1-4612-0853-2](https://doi.org/10.1007/978-1-4612-0853-2)&rbrack;

* Kenneth Ireland, Michael Rosen: *Quadratic Gauss Sums*, chapter 6 in: *A Classical Introduction to Modern Number Theory*, Graduate Texts in Mathematics **84**, Springer (1990) &lbrack;[doi:10.1007/978-1-4757-1779-2_6](https://doi.org/10.1007/978-1-4757-1779-2_6)&rbrack;

* [[Lisa Jeffrey]], Props. 2.3 and 4.3 in: *Chern-Simons-Witten invariants of lens spaces and torus bundles, and the semiclassical approximation*, Commun.Math. Phys. **147** (1992) 563–604 &lbrack;[doi:10.1007/BF02097243](https://doi.org/10.1007/BF02097243), [spire:342446](https://inspirehep.net/literature/342446)&rbrack; 
  > (reciprocity formulas in the context of [[Chern-Simons theory]])


* George Danas: *Note on the quadratic Gauss sums*, Int. J. Math and Math. Sciences (2001) &lbrack;[doi:10.1155/S016117120100480X](https://doi.org/10.1155/S016117120100480X)&rbrack;

* Kh. M. Saliba & V. N. Chubarikov: *A generalization of the Gauss sum*, Moscow Univ. Math. Bull. **64** (2009) 92–94 &lbrack;[doi:10.3103/S0027132209020132](https://doi.org/10.3103/S0027132209020132)&rbrack;

* {#Doyle16} Greg Doyle: *Quadratic Form Gauss Sums*, PhD thesis, Ottawa (2016) &lbrack;[doi:10.22215/etd/2016-11457](https://doi.org/10.22215/etd/2016-11457), [[Doyle-QuadraticGaussSum.pdf:file]]&rbrack;

* {#MurtyPathak17} M. Ram Murty, Siddhi Pathak: *Evaluation of the quadratic Gauss sum*, The Mathematics Student **86** 1-2 (2017) 139-150 &lbrack;[pdf](https://mast.queensu.ca/~murty/quadratic2.pdf), [pdf](https://www.cmi.ac.in/~siddhi/Quadratic_Gauss_Sum.pdf), [[RamMurtyPathak-GaussSum.pdf:file]]&rbrack;

* Ramin Takloo-Bighash: *Gauss Sums, Quadratic Reciprocity, and the Jacobi Symbol*, in: *A Pythagorean Introduction to Number Theory*, Undergraduate Texts in Mathematics, Springer (2018) &lbrack;[doi:10.1007/978-3-030-02604-2_7](https://doi.org/10.1007/978-3-030-02604-2_7)&rbrack;

* Frederik Broucke, Jasson Vindas, section 2 of: *The pointwise behavior of Riemann's function*, J. Fractal Geom. **10** 3/4 (2023) 333-349 &lbrack;[arXiv:2109.08499](https://arxiv.org/abs/2109.08499), [doi:10.4171/jfg/137](https://doi.org/10.4171/jfg/137)&rbrack;

* Nilanjan Bag, Antonio Rojas-León, Zhang Wenpeng: *On some conjectures on generalized quadratic Gauss sums and related problems*, Finite Fields and Their Applications
**86** (2023) 102131 &lbrack;[doi:10.1016/j.ffa.2022.102131](https://doi.org/10.1016/j.ffa.2022.102131)&rbrack;

* Alexander P. Mangerel: *On a rigidity property for quadratic Gauss sums* &lbrack;[arXiv:2502.16014](https://www.arxiv.org/abs/2502.16014)&rbrack;

See also:

* Wikipedia: *[Quadratic Gauss sum](https://en.wikipedia.org/wiki/Quadratic_Gauss_sum)*

* Wikipedia: *[Gauss sum](https://en.wikipedia.org/wiki/Gauss_sum)*

On the Landsberg-Schaar identity:

* {#Schaar1850} M. Schaar: *Mémoire sur la théorie des résidus biquadratiques*, Mémoires de l’Académie Royale des Sciences,
des Lettres et des Beaux-Arts de Belgique **24** (1850) &lbrack;[biodiversitylibrary:20728](https://www.biodiversitylibrary.org/item/20728)&rbrack;

* {#DymMcKean72} Harry Dym, Henry P. McKean, section 4.6 in: *Fourier series and integrals*, Probability and Mathematical Statistics **14**, Academic Press (1972) 

* {#ArmitageRogers2000} Vernon Armitage, [[Alice Rogers]]: *Gauss Sums and Quantum Mechanics*, J. Phys. A: Math. Gen. **33** (2000) 5993 \[<a href="https://iopscience.iop.org/article/10.1088/0305-4470/33/34/305">doi:10.1088/0305-4470/33/34/305</a>, [arXiv:quant-ph/0003107](https://arxiv.org/abs/quant-ph/0003107)\]
  > (via tools from [[quantum mechanics]])

* {#Ustinov22} [[Alexey Ustinov]]: *A Short Proof of the Landsberg–Schaar Identity*, Mathematical Notes **112** (2022) 488–490 &lbrack;[doi:10.1134/S0001434622090188](https://doi.org/10.1134/S0001434622090188)&rbrack;.  Russian original: А. В. Устинов, _Короткое доказательство тождества Ландсберга–Шаара_, Математические заметки, 2022, том 112, выпуск 3, страницы 478–480, [doi](https://doi.org/10.4213/mzm13535).

* Wikipedia: *[Landsberg-Schaar relation](https://en.wikipedia.org/wiki/Landsberg%E2%80%93Schaar_relation)*

Further generalization:

* {#Harcos} Gergely Harcos: *The reciprocity of Gauss sums via the residue theorem* &lbrack;[pdf](https://users.renyi.hu/%7Egharcos/gauss_sums.pdf), [[Harcos-ReciprocityOfGaussSums.pdf:file]]&rbrack;


\linebreak


[[!redirects Gauss sums]]

[[!redirects quadratic Gauss sum]]
[[!redirects quadratic Gauss sums]]

[[!redirects generalized quadratic Gauss sum]]
[[!redirects generalized quadratic Gauss sums]]

[[!redirects generalized Gauss sum]]
[[!redirects generalized Gauss sums]]


[[!redirects Gauß sum]]
[[!redirects Gauß sums]]

[[!redirects quadratic Gauß sum]]
[[!redirects quadratic Gauß sums]]

[[!redirects generalized quadratic Gauß sum]]
[[!redirects generalized quadratic Gauß sums]]

[[!redirects generalized Gauß sum]]
[[!redirects generalized Gauß sums]]


[[!redirects Landsberg-Schaar identity]]
[[!redirects Landsberg-Schaar identities]]

[[!redirects Landsberg-Schaar relation]]
[[!redirects Landsberg-Schaar relations]]




