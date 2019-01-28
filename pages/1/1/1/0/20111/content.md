

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Brauer induction theorem_ ([Brauer 46](#Brauer46)) states that, for [[ground field]] the [[complex numbers]], [[finite dimensional vector space|finite-dimensional]] [[linear representations]] $V$ of a [[finite group]] $G$ all arise as [[virtual representation|virtual combinations]] of [[induced representations]] $ind_{H}^G W$ of just 1-dimensional representations $W$, $dim_{\mathbb{C}}(W) =1$. Hence the [[representation ring]] $R_{\mathbb{C}}(G)$ is generated from [[isomorphism classes]] $[ind_{H}^G W]$ of  [[induced representations]] $ind_{H}^G W$ of 1-dimensional representations $W$ of [[subgroups]] $H \subset G$:

$$
  [V] 
  \;=\;
  \underset{
    \mathclap{
    {
      H_i \hookrightarrow G
    }
    \atop
    {
      W_i \in Rep(H_i),
      \;
      dim(W_i) = 1
    }
    }
  }{\sum}
  a_i 
  \big[ 
    ind_{H_i}^G W_i
  \big]
  \,,
  \phantom{AAA}
  a_i \in \mathbb{Z}
  \,.
$$

This may be thought of as a [[splitting principle]] for [[linear representations]] ([Symonds 91](#Symonds91)).

Brauer induction generalizes the immediate statement that [[finite dimensional vector space|finite-dimensional]] [[permutation representations]] are all [[direct sums]] of [[induced representations]] of the _[[trivial representation|trivial]]_ 1-dimensional representation.

The analogous statement holds true also for [[ground ring]] the [[quaternions]], while for [[ground field]] the [[real numbers]] one has to induce not just from 1-dimensional but also from 2-dimensional representations.

<br/>

## References

Due to 

* {#Brauer46} [[Richard Brauer]], ... (1946)

See also 

* Wikipedia, _[Brauer's theorem on induced characters](https://en.wikipedia.org/wiki/Brauer%27s_theorem_on_induced_characters)_

In the context of [[characteristic classes of linear representations]]:

* {#Symonds91} [[Peter Symonds]], _A splitting principle for group representations_, Comment. Math. Helv. (1991) 66: 169 ([dml:140229](https://eudml.org/doc/140229), [doi:10.1007/BF02566643](https://doi.org/10.1007/BF02566643))



[[!redirects Brauer's theorem]]

[[!redirects Brauer's theorem on induced characters]]