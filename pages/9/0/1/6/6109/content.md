
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[path integral]] in [[quantization]] can be understood -- to the extent and in the cases that it can be understood at all -- as an [[integral transform]] induced from a [[span]] that is given by [[hom-space]]s.  According to the general reasoning of [[integral transforms on sheaves]] this means that it is given by a _pull-push_ operation through spans.


## Examples

### The quantum particle

The archetypical example of the [[path integral]] is that for the [[sigma model]] that describes the [[quantum mechanics]] of the [[particle]] propagating on the [[target space]] $X = \mathbb{R}$ --  the [[line]]. 

In a finite approximation, one considers for $N \in \mathbb{N}$ paths consisting on $N$ discrete steps: let $I_N := \{0, 1, \cdots, N\}$ be the set of $N+1$ elements. Regarding this as an abstract discrete [[cobordism]] of $N$ steps, we consider the [[cospan]]

$$
  \array{
    && I_N
    \\
    & {}^{\mathllap{in}}\nearrow && \nwarrow^{\mathrlap{out}}
    \\
    * &&&& * 
  }
  \,,
$$

where $in : * \to I_N$ is the inclusion of the first elements 0, and $out : * \to I_N$ the inclusion of the last element, $N$.

The mapping space $X^{I_N} \simeq X \times X \times \cdots \times X$ is the _space of paths_ -- the space of paths in $X = \mathbb{R}$ consisting of $n$ linear steps. Homming the above cospan into $X$ produces the span

$$
  \array{ 
    && X^{I_N}
    \\
    & {}^{\mathllap{X^{in}}}\swarrow && \searrow^{\mathrlap{X^{out}}}
    \\
    X \simeq X^* &&&& X^* \simeq X
  }
  \,.
$$

In the canonical coordinates on $X^{I_N}$ a path $\gamma \in X^{I_N}$ is parameterized as 

$$
  \gamma = (x_0, x_1, \cdots, x_N)
  \,.
$$ 
 
The [[action functional]] that encodes the dynamics of the free particle on $X$ is the [[differential form|differential form]] on $X^{I_N}$ given by

$$
  \exp(i S) := \exp(i \sum_{i = 1}^N \frac{m}{2}(\frac{x_i -  x_{i-1}}{1/N})^2) d x_0 \wedge d x_1 \wedge \cdots \wedge d x_{N-1}
  \in 
  \Omega^{N}(X^{I_n})
  \,.
$$

Denote by

$$
  (X^{in})^* : \Omega^\bullet(X) \to \Omega^\bullet(X^{I_N})
$$

the pullback of differential forms along $X^{in}$, and by

$$
  (X^{out})_* := \int_{X^{I_N}/X} : \Omega^\bullet(X^{I_N}) \to \Omega^{\bullet - N}(X)
$$

the "pushforward": the [[fiber integration]] of differential forms.

Then then standard path integral for the particle is given by 

1. pulling back functions along $X^{in}$;

1. taking their wedge product with $\exp(i S)$;

1. pushing the result forward along $X^{out}$. 

This gives the map

$$
   (X^{out})_* \circ exp(i S) \wedge (-) \circ (X^{in})^*
   :
   \Omega^0(X) \stackrel{(X^{in})^*}{\to} C^\infty(X^{I_n}) \stackrel{\exp(i S)\wedge}{\to} 
   \Omega^{N}(X^{I_N}) \stackrel{(X^{out})_*}{\to} 
   \Omega^0(X)
$$

that acts by

$$
  (\psi \in C^\infty(X))
  \mapsto
  \left(
   x \mapsto
  \int_{X^{I_N}/X}
     \psi(x_0) \exp(i \frac{m}{2} \sum_{i = 1}^N (\frac{x_i - x_{i-1}}{1/N})^2 )
     d x_0 \wedge \cdots \wedge d x_{N-1}
  \right)
  \,.
$$

This is the standard expression for the path integral of the particle on the line, at the approximation of $N$ discrete steps. 

### Gromov-Witten theory

* [[Gromov-Witten theory]]

### String topology

On the [[singular homology]] of [[smooth manifold]]s and other [[topological space]]s, pullback operations can be defined by [[Thom isomorphism]]s and [[fiber integration]] ("[[Umkehr map]]s"). Together with the canonically defined push-forward of singular cycles, this yields a definition of pull-push transformations on singular homology.

It was realized in ([CohenGodin](#CohenGodin)) and ([Godin](#Godin)) that such pull-push operations define a 2-dimensional [[HQFT]] whose [[space of states]] is the singular complex, and that the [[correlator]]s of the thus defined [[FQFT]] are the Chas-Sullivan [[string topology]] operations. See there for more details.

* [[string topology]]

### Geometric $\infty$-function theory

Every perfect [[derived stack]] in [[dg-geometry]] forms the [[target space]] for a pull-push transform on the [[stable (infinity,1)-category]] of [[quasicoherent sheaves]] and yields a 2-dimensional [[TQFT]]. For details on this see _[[geometric infinity-function theory]]_ .


## Related concepts

* [[motivic quantization]]

* [[integral transforms on sheaves]]


## References

The pull-push nature of the path integral was originally amplified somewhat implicitly in

* [[Dan Freed]]

  * _Quantum groups from path integrals_ ([arXiv:q-alg/9501025](http://xxx.lanl.gov/abs/q-alg/9501025))

  * _Higher algebraic structures and quantization_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115))

and fully explicitly in

* [[Dan Freed]], _Twisted K-theory and the Verlinde ring_ ([pdf slides](http://www.ma.utexas.edu/users/dafr/Andrejewski%20Lectures.html))

The description of [[string topology]] operations as an [[HQFT]] defined by pull-push transforms was originally realized in 

* [[Ralph Cohen]], [[Veronique Godin]], 
  _[[A Polarized View of String Topology]]_

* Hirotaka Tamanoi, _Loop coproducts in string topology and triviality of higher genus TQFT operations_ (2007) ([arXiv:0706.1276](http://arxiv.org/abs/0706.1276))
 {#Tamanoi07}

A detailed discussion and generalization to the open-closed [[HQFT]] in the presence of a single space-filling [[brane]] is in

* [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 {#Godin}

For more see the references at _[[motivic quantization]]_.


[[!redirects path integral as a pull-push transformation]]