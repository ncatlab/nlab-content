
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[cochain cohomology]] of the framed [[knot graph complex]] (sometimes called the "Wilson graph complex") in the bidegree corresponding to trivalent graphs, hence to [[Jacobi diagrams]], coincides with the space of framed [[weight systems]] on [[Jacobi diagrams]], [[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] on [[round chord diagrams]]:

$$
  \underset{
    \mathclap{
    {\phantom{a}}
    \atop
    {
      {\color{blue}cohomology\;of\;knot\;graph\;complex}
      \atop
      {\color{blue}spanned\;by\;trivalent\;graphs}
    }
    }
  }{
  H^{\bullet,  
   \overset{ 
     \mathclap{
       {deg=0} \atop {i.e.\; trivalent} 
     }
   }{
     \overbrace{ 0 }}
   }
  \big(
    KnotGraphs 
  \big)
  }
  \underoverset{
    \phi
  }{
   \;\;\;\simeq\;\;\;
  }{
    \longleftarrow
  }
  \underset{
    \phantom{a}
    \atop
    {
      {\color{blue}framed\;weight\;systems\;on}
      \atop
      {\color{blue}round\;chord\;diagrams}
    }
  }{
    (\mathcal{W}^c)^\bullet
  }
  \;\simeq\;
  \underset{
    \phantom{a}
    \atop
    {
      {\color{blue}\weight\;systems\;on}
      \atop
      {\color{blue}Jacobi\;diagrams}
    }
  }{
    (\mathcal{W}^t)^\bullet
  }
$$

This is stated as [CCRL 02, Prop. 7.6](#CattaneoCottaRamusinoLongoni02), attributed there to the proof of [AF 96, Theorem 1](#AF96), where in turn the argument is attributed to ([Kohno 94](#Kohno94)). (?)

Moreover: 

If $w \in \mathcal{W}^c$ is a [[weight system]] and $D \in \mathcal{D}^t$ is a [[Jacobi diagram]] such that $w(D) \neq 0$, then $\phi(w) \in KnotGraphs$ contains a non-vanishing multiple of $D$ as a summand.

This is [CCRL 02, Remark 7.7](#CattaneoCottaRamusinoLongoni02).

## References

The statement is made explicit in

* {#CattaneoCottaRamusinoLongoni02} [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Configuration spaces and Vassiliev classes in any dimension_, Algebr. Geom. Topol. 2 (2002) 949-1000 ([arXiv:math/9910139](https://arxiv.org/abs/math/9910139))

following

* {#AF96} Daniel Altschuler, Laurent Freidel, _Vassiliev knot invariants and Chern-Simons perturbation theory to all orders_, Commun. Math. Phys. 187 (1997) 261-287 ([arXiv:q-alg/9603010](https://arxiv.org/abs/q-alg/9603010))

See also

* {#Kohno94} [[Toshitake Kohno]], _Vassiliev invariants and de Rham complex on the space of knots_, 
In: Yoshiaki Maeda, Hideki Omori, [[Alan Weinstein]] (eds.), _Symplectic Geometry and Quantization_, Contemporary Mathematics 179 (1994): 123-123 ([doi:10.1090/conm/179](http://dx.doi.org/10.1090/conm/179))

