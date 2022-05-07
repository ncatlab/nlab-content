+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The formalism of Markov categories can be thought of as a way to express certain aspects of [[probability]] and [[statistics]] [[analytic versus synthetic|synthetically]]. In other words, it consists of [[structures]] and [[axioms]] which one can think of as "fundamental" in probability and statistics, which one can use to prove theorems, without having to use [[measure theory]] directly. One then proves that the usual measure-theoretic treatment is a [[model]] (or [[semantics]]) of this theory.

Intuitively, for the purposes of probability a Markov category can be seen as a category where morphisms behave like "random functions", or "[[Markov kernels]]" (hence the name). Canonical examples are [[Kleisli categories]] of [[probability monads]]. The formalism is however far more general. 

**Caveat**: some of the content of this page reflects work in progress. Content may change.



## Definition

A **Markov category** is a [[semicartesian monoidal category|semicartesian]] [[symmetric monoidal category]] $(C,\otimes,1)$ in which every object $X$ is equipped with the structure of a [[commutative]] [[internal monoid|internal comonoid]].
We denote the [[comultiplication]] and [[counit]] maps by $copy: X \to X \otimes X$ and $delete: X\to 1$. 

We require the following compatibility property between the copy map and the tensor product: for all objects $X$ and $Y$, 
$$
copy_{X\otimes Y} \; =\; (id_X\otimes b_{Y,X} \otimes id_Y) ( copy_X \otimes copy_Y ),
$$
where $b$ denotes the [[braiding]].

Note that the map $delete: X\to 1$ is uniquely determined by the fact that 1 is [[terminal]], hence it is also [[natural transformation|natural]] in $X$ (see [[semicartesian monoidal category]] for more). On the other hand, the copy map is _not_ required to be natural.


### In terms of string diagrams

(...)


## Examples 

- The category $\mathsf{FinStoch}$ of finite sets and stochastic matrices.
- The category $\mathsf{Stoch}$ of [[measurable spaces]] and [[Markov kernels]]
- For any [[cartesian monoidal category]] $\mathsf{C}$ equipped with a [[monoidal monad]] $T$, the [[Kleisli category]] $Kl(T)$ is a Markov category.

See also the [[Markov category#detailed_list|detailed list below]].

## Deterministic morphisms

A morphism $f:X\to Y$ in a Markov category is called **deterministic** if it commutes with the copy map,
$$
copy \circ f \;=\; (f\otimes f) \circ copy .
$$

A way to motivate the definition is the following. Suppose that $f$ is a "random" function between real numbers, which adds to the input the result of the roll of a die. Given a number $x$, we can roll a die, add the resulting value (say, $n$) to $x$, and then copy the result, to get $(x+n,x+n)$. Or, we could copy the value $x$, roll two dice (or roll the die twice), and add the two resulting values (say, $m$ and $n$) to the two copies of $x$, obtaining $(x+m,x+n)$. The two results are likely to differ. 
One can take this as a _definition_ of randomness: it's a process that may give a different result if you do it twice. Or equivalently, that copying the information before or after the process has taken place gives different results.

A _deterministic_ morphism is instead one that does _not_ exhibit this behavior, i.e. that commutes with the copy map.

(...)

## Further structures and properties

(...)

### Conditionals

### Kolmogorov products

### Positivity

(to be expanded)


## Representable Markov categories

For now, see [[probability monad]].


## Detailed list

(...to be expanded...)

<table>
 <tr>
  <th markdown="1">Category</th>
  <th markdown="1">[[probability monad|Probability monad]]</th>
  <th markdown="1">[[Markov category#conditionals|Conditionals]]</th>
  <th markdown="1">[[Markov category#positivity|Positivity]]</th>
  <th markdown="1">[[Markov category#kolmogorov_products|Kolmogorov products]]</th>
  <th markdown="1">Further references</th>
 </tr>
 <tr>
  <th markdown="1">[[Stoch]]</th>
  <td markdown="1">[[Giry monad]] on [[Meas]]</td>
  <td markdown="1">No ([Fritz'19](#fritzmarkov), Example 11.3)</td>
  <td markdown="1">(...)</td>
  <td markdown="1">(...)</td>
  <td markdown="1">[Fritz'19](#fritzmarkov)</td>
 </tr>
<tr>
  <th markdown="1">[[BorelStoch]]</th>
  <td markdown="1">[[Giry monad]] on [[Pol]]</td>
  <td markdown="1">Yes ([Kallenberg '17](#Kallenberg17), [B-M'19](#BM19))</td>
  <td markdown="1">(...)</td>
  <td markdown="1">(...)</td>
  <td markdown="1">[Fritz'19](#fritzmarkov)</td>
 </tr>
<tr>
  <th markdown="1">[[FinStoch]]</th>
  <td markdown="1">Not representable</td>
  <td markdown="1">Yes ([Fritz'19](#fritzmarkov), Example 11.6)</td>
  <td markdown="1">(...)</td>
  <td markdown="1">(...)</td>
  <td markdown="1">[Fritz'19](#fritzmarkov)</td>
 </tr>
</table>


## See also

* [[probability monad]]
* [[probability theory]]
* [[statistics]]
* [[zero-one law]]
* [[doctrine]]


## References

Markov categories as defined here appear in:

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, 2019. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _The zero-one laws of Kolmogorov and Hewitt--Savage in categorical probability_, 2019. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))
* Tobias Fritz, Tomáš Gonda, Paolo Perrone, Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, [arXiv:2010.07416](https://arxiv.org/abs/2010.07416)

See also the references therein.

The first idea of defining a "category of probabilistic mappings" seems to be due to [[Lawvere]], in

*{#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

(...more to come...)


Further references:

* {#Kallenberg17} Olaf Kallenberg, _Random Measures, Theory and Applications_, Springer, 2017.

* {#BM19} Vladimir Bogachev and Il'ya Malofeev, _Kantorovich problems and conditional measures depending on a parameter_. ([arXiv:1904.03642](https://arxiv.org/abs/1904.03642))


[[!redirects Markov categories]]
[[!redirects markov category]]
[[!redirects markov categories]]