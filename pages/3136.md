
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A lifting gerbe is a [[cohomology|cocycle]]/[[gerbe]] -- or equivalently the [[principal infinity-bundle]] that it classifies -- arising as the obstruction to the lift of a $G$-[[principal bundle]] or more generally of any $G$-[[principal infinity-bundle]], through a [[group extension|shifted central extension]]


$$
  \mathbf{B}^{n-1} A \to \hat G \to G
$$

of $G$, for some abelian group $A$.

## Definition

Such an extension is classified (or rather its [[delooping]] is) by a cocycle

$$
  \mathbf{B}G \to \mathbf{B}^{n+1} A
$$

in [[group cohomology]].

For $X \to \mathbf{B}G$ the cocycle in [[nonabelian cohomology]] classifying a $G$-[[principal bundle]] or [[principal infinity-bundle]], the corresponding lifting $A$-gerbe is the thing classified by the composite cocycle

$$
  X \to \mathbf{B}G \to \mathbf{B}^n A
  \,.
$$

## Examples

### Lifting 1-gerbes

In the literature the following simplest case of the general situation is usually considered exclusively:

For $G$ an ordinary topological or Lie [[group]] and 

$$
  U(1) \to \hat G \to G
$$

a $U(1)$-central [[group extension]], classified by a 2-cocycle 
$\mathbf{B}G \to \mathbf{B}^2 U(1)$ in ordinary [[group cohomology]], and for $X \to \mathbf{B}G$ the cocycle of a $G$-[[principal bundle]], the corresponding lifting gerbe is given by the cocycle

$$
  X \to \mathbf{B}G \to \mathbf{B}^2 U(1)
  \,.
$$

In the literature this is often discussed in terms of the model for gerbes given by $U(1)$-principal [[bundle gerbe]]s: let $P \to X$ be the total space of the [[bundle]] classified by $X \to \mathbf{B}G$. Regard this as the [[surjective submersion]] that is part of the data of the [[bundle gerbe]] to be constructed. By principality of $P$, there is a canonical morphism

$$
  P \times_X P \to G
$$

that sends two elements in the fiber of the bundle to the unique group element that takes the first to the second. Along this morphism, form the [[pullback]] of the extension $\hat G \to G$ to get $L$ in

$$
  \array{
    L &\to& \hat G
    \\
    \downarrow && \downarrow
    \\
    P \times_X P &\to& G
  }
  \,.
$$

This $L$ is the line bundle ingredient in the lifting bundle gerbe. There is canocically a multiplication map that completes the definition.

+-- {: .num_prop}
###### Proposition

Let $\mathcal{H}$ be a separable infinite-dimensiona [[Hilbert space]], $U(\mathcal{H})$ its [[unitary group]] and $P U(\mathcal{H})$ its [[projective unitary group]]. Then the extension

$$
  0 \to U(1) \to U(\mathcal{H}) \to P U(\mathcal{H}) \to 0
$$

is universal with the above property: every $U(1)$-[[bundle gerbe]]/[[circle n-bundle with connection|circle 2-bundle]] is the lifting gerbe of some $P U(\mathcal{H})$-[[principal bundle]] through this extension.

=--

See [[projective unitary group]] for details.

To contrast, in ([Roberts 2021](#Roberts21)), _finite dimensional_ lifting gerbes are very often those gerbes with torsion [[Dixmier-Douady class]]. This is in particular true if the [[fundamental group]] of the base is finite, or the Lie group $G$ is compact.


### Lifting 2-gerbes

The archetypical example of a lifting 2-gerbe is a [[Chern-Simons gerbe]].


## References

A review is for instance in section 2.2 of

* {#CBMMS}  [[Alan Carey]], [[Peter Bouwknegt]], [[Varghese Mathai]], [[Michael Murray]] and [[Danny Stevenson]], _K-theory of bundle gerbes and twisted K-theory_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv](http://arxiv.org/abs/hep-th/0106194))
  


* {#Roberts21} [[David Roberts]], _Many finite-dimensional lifting bundle gerbes are torsion_ (2021), arXiv:[2104.07936](https://arxiv.org/abs/2104.07936).


[[!redirects lifting gerbes]]
[[!redirects lifting bundle gerbe]]
[[!redirects lifting bundle gerbes]]
