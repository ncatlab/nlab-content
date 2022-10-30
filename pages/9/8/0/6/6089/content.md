
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Beilinson-Drinfeld cup product_ is an explicit presentation of the [[cup product]] in [[ordinary differential cohomology]] for the case that the latter is modeled by the [[Cech cohomology|Cech]]-[[Deligne cohomology]]. It sends (see [[cup product in abelian Cech cohomology]])

$$
\cup: A[p]^\infty_D\otimes B[q]^\infty_D\to (A\otimes_{\mathbb{Z}} B)[p+q]^\infty_D,
$$
where $A$ and $B$ are lattices in $\mathbb{R}^n$, and $\mathbb{R}^m$ for some $n$ and $m$, respectively. 
It is a morphism of complexes, so it induces a cup product in [[Deligne cohomology]]. 

For $A=B=\mathbb{Z}$, the Beilinson-Deligne cup product is associative and commutative up to homotopy, so it induces an associative and commutatvive cup product on [[ordinary differential cohomology|differential cohomology]]

## Definition

Let the [[Deligne complex]] $\mathbf{B}^n(\mathbb{R}//\mathbb{Z})_{conn}$ be given by

$$
  \array{
     & 
     \mathbb{Z} 
       &\hookrightarrow& 
     C^\infty(-,\mathbb{R})
       &\stackrel{d_{dR}}{\to}&     
     \cdots
       &\stackrel{d_{dR}}{\to}&  
     \Omega^{n}(-)
     \\
     \\
     degree: & 0 && 1 && \cdots && (n+1)    
  }
$$

where we refer to degrees as indicated in the bottom row.

+-- {: .num_defn}
###### Definition

The _Beilinson-Deligne product_ is the morphism of [[chain complexes]]
of [[sheaves]]

$$
  \cup 
    : 
   \mathbf{B}^p (\mathbb{R}//\mathbb{Z})_{conn}
   \otimes
   \mathbf{B}^q (\mathbb{R}//\mathbb{Z})_{conn}
   \to 
   \mathbf{B}^{p+q+1} (\mathbb{R}//\mathbb{Z})_{conn}
$$

given on homogeneous elements $\alpha$, $\beta$ as follows:

$$
  \alpha \cup \beta :=
  \left\{
    \array{
    \alpha \wedge \beta = \alpha \beta & if\,deg(\alpha) = 0
    \\
    \alpha \wedge d_{dR}\beta & if\,deg(\alpha) \gt 0\,and\,deg(\beta) = q+1
    \\
    0 & otherwise
    }
  \right.
  \,.
$$

=--

## Applications

### In higher Chern-Simons theory

The [[action functional]] of abelian [[higher dimensional Chern-Simons theory]] is given by the [[fiber integration in ordinary differential cohomology]] over the BD cup product of differential cocycles

$$
  S_{CS} : H^{2k+2}(\Sigma)_diff  \to U(1)
$$

$$
  \hat C \mapsto \int_\Sigma \hat C \cup \hat C
  \,.
$$

For more on this see [[higher dimensional Chern-Simons theory]].

## References 

The original references are 

* [[Pierre Deligne]], _Th&#233;orie de Hodge II_ , IHES Pub. Math. (1971), no. 40, 5&#8211;57.

* [[Alexander Beilinson]], _Higher regulators and values of L-functions_ , J. Soviet Math. 30 (1985), 2036&#8212;2070

* [[Alexander Beilinson]], _Notes on absolute Hodge cohomology_ , Applications of algebraic $K$-theory to algebraic geometry and number theory, Part I, II, Contemp. Math., 55, Amer. Math. Soc., Providence, RI, 1986.   

A survey is for instance around prop. 1.5.8 of 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_ Birkh&#228;user (1993)

and in section 3 of 

* [[Helene Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

For the cup product of [[Cheeger-Simons differential character]]s see also

* [[Mike Hopkins]] and [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_ ([arXiv](http://arxiv.org/abs/math/0211216))


[[!redirects cup product in ordinary differential cohomology]]

[[!redirects Beilinson-Deligne cup product]]

[[!redirects differential cup-product]]
[[!redirects differential cup product]]
