

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Among all [[special orthogonal groups]] $SO(n)$, the case of $SO(8)$ is special, since in the [[ADE classification]] of [[simple Lie groups]] it corresponds to [[D4]], which makes its [[representation theory]] enjoy _[[triality]]_.

## Properties

### Subgroup lattice
 {#SubgroupLattice}

+-- {: .num_prop }
###### Proposition

We have the following [[commuting diagram]] of [[subgroup]] inclusions, where each [[square]] exhibits a [[pullback]]/[[fiber product]], hence an [[intersection]] of subgroups:

\begin{center}
\begin{xymatrix}
    \mathrm{SU}(2)
    \ar@{^{(}->}[r]
    \ar@{^{(}->}[d]
    \ar@{}[dr]|-{
      \mbox{
        \tiny
        (pb)
      }
    }
    &
    \mathrm{SU}(3)
    \ar@{^{(}->}[r]
    \ar@{^{(}->}[d]
    \ar@{}[dr]|-{
      \mbox{
        \tiny
        (pb)
      }
    }
    &
    \mathrm{G}_2
    \ar@{^{(}->}[r]
    \ar@{^{(}->}[d]
    \ar@{}[dr]|-{
      \mbox{
        \tiny
        (pb)
      }
    }
    &
    \mathrm{Spin}(7)
    \ar@{^{(}->}[d]
    \\
    \mathrm{Spin}(5)
    \ar@{^{(}->}[r]
    &
    \mathrm{Spin}(6)
    \ar@{^{(}->}[r]
    &
    \mathrm{Spin}(7)
    \ar@{^{(}->}[r]
    &
    \mathrm{Spin}(8)
\end{xymatrix}
\end{center}

Here in the bottom row we have the [[Lie groups]]

[[Spin(5)]] $\hookrightarrow$ [[Spin(6)]] $\hookrightarrow$ [[Spin(7)]] $\hookrightarrow$ [[Spin(8)]]

and in the top row we have 

[[SU(2)]] $\hookrightarrow$ [[SU(3)]] $\hookrightarrow$ [[G2]] $\hookrightarrow$ [[Spin(7)]]

=--

This is a re-statement of 
[Onishchik 93, Table 2, p. 144](#Onishchik93):

\begin{center}
\begin{imagefromfile}
  "file_name": "SO8SubgroupIntersection.jpg",
  "width": 690
\end{imagefromfile}
\end{center}


### Cohomology of classifying spaces

+-- {: .num_prop}
###### Proposition

The [[ordinary cohomology|ordinary]] [[cohomology ring]] of the [[classifying space]] $B Spin(8)$ is:

**1)** with [[coefficients]] in the [[cyclic group of order 2]]:

$$
  H^\bullet
  \big(
    B Spin(8), \mathbb{Z}_2
  \big)
  \;\simeq\;
  \mathbb{Z}
  \big[
    w_4, w_6, w_7, w_8, 
    \;
    \rho_2
    \left(
    \tfrac{1}{4}
    \left(
      p_2
      -
      \big(\tfrac{1}{2}p_1\big)^2
      -
      2 \chi
    \right)
    \right)
  \big]
$$

where $w_i$ are the [[universal characteristic class|universal]] [[Stiefel-Whitney classes]], 

and where 

$$
  \rho_2 \;\colon\; H^\bullet(B Spin(8), \mathbb{Z}) \to H^\bullet(B Spin(8), \mathbb{Z}_2)
$$ 

is [[cyclic group|mod 2 reduction]]

**2)** with [[coefficients]] in the [[integers]]:

$$
  H^\bullet
  \big(
    B Spin(8), \mathbb{Z}
  \big)
  \;\simeq\;
  \mathbb{Z}
  \Big[
    \tfrac{1}{2}p_1,
    \;
    \tfrac{1}{4}
    \left(
      p_2
      -
      \big(\tfrac{1}{2}p_1\big)^2
      -
      2 \chi
    \right)
    ,
    \;
    \chi,
    \;
    \beta(w_6)
  \Big]
  /
  \big\langle 2 \beta(w_6)\big\rangle
  \,,
$$

where $p_1$ is the [[first fractional Pontryagin class]], $p_2$ is the [[second Pontryagin class]], $\chi$ is the [[Euler class]], and

$$
  \delta
  \;\colon\;
  H^\bullet
  \big(
    B Spin(8),
    \mathbb{Z}_2
  \big)
  \longrightarrow
  H^{\bullet + 1}
  \big(
    B Spin(8),
    \mathbb{Z}
  \big)
$$

is the [[Bockstein homomorphism]].

Moreover, we have the following relations:

$$
  \begin{aligned}
    \rho_2\left(
      \tfrac{1}{2}p_1
    \right)  
    & = 
    w_4
    \\
    \rho_2\big( \chi\big) 
    & =
    w_8
  \end{aligned}
$$

=--

This is due to [Quillen 71](#Quillen71), [Čadek-Vanžura 95](#CadekVanzura95), see [Čadek-Vanžura 97, Lemma 4.1](#CadekVanzura97).

\linebreak

## Related concepts

[[!include low dimensional rotation groups -- table]]

\linebreak

## References

### General

See also

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/SO(8)">SO(8)</a>_

### Subgroup lattice

* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993


### Cohomology

The [[integral cohomology]] of the [[classifying spaces]] $B SO(8)$ and $B Spin(8)$ and the [[action]] of [[triality]] on these is discussed in


* {#GrayGreen70} Alfred Gray, Paul S. Green, _Sphere transitive structures and the triality automorphism_, Pacific J. Math. Volume 34, Number 1 (1970), 83-96 ([euclid:1102976640](https://projecteuclid.org/euclid.pjm/1102976640))

* {#Quillen71} [[Daniel Quillen]], _The mod 2 cohomology rings of extra-special 2-groups and the spinor groups_, Math. Ann . 194 (1971), 19

* {#CadekVanzura95} [[Martin Čadek]], [[Jiří Vanžura]], _On the existence of 2-fields in 8-dimensional vector bundles over 8-complexes_, Commentationes Mathematicae Universitatis Carolinae, vol. 36 (1995), issue 2, pp. 377-394 ([dml-cz:118764](https://dml.cz/handle/10338.dmlcz/118764))

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], Section 2 of _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))


[[!redirects Spin(8)]]

[[!redirects SO8]]

[[!redirects Spin8]]
