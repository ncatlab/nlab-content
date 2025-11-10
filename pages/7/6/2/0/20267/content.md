
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The [[special unitary group]] in 3 complex [[dimensions]].

## Properties

### Subgroups and Supgroups

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

[[SU(2)]] $\hookrightarrow$ [[SU(3)]] $\hookrightarrow$ [[G₂]] $\hookrightarrow$ [[Spin(7)]]

=--

This is a re-statement of 
[Onishchik 93, Table 2, p. 144](#Onishchik93):

\begin{center}
\begin{imagefromfile}
  "file_name": "SO8SubgroupIntersection.jpg",
  "width": 620
\end{imagefromfile}
\end{center}

[[!include coset space structure on n-spheres -- table]]



### $G$-Structure and exceptional geometry


[[!include Spin(8)-subgroups and reductions -- table]]



## Related concepts

* [[principal SU(3)-bundle]]

* [[Calabi-Yau manifold]]

* [[U(1)]], [[SU(2)]], [[SU(4)]], [[SU(5)]]

## References

* {#MimuraToda63} [[Mamoru Mimura]] and [[Hiroshi Toda]], _Homotopy Groups of SU(3), SU(4) and Sp(2)_ (1963), Journal of Mathematics of Kyoto University **3** (2), p. 217–250, [doi:10.1215/kjm/1250524818](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-3/issue-2/Homotopy-Groups-of-SU3-SU4-and-Sp2/10.1215/kjm/1250524818.full)

* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993

* [[Howard Georgi]], §7 & §9  in: *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;

  > with an eye towards application to (the [[standard model of particle physics|standard model]] of) [[particle physics]]

