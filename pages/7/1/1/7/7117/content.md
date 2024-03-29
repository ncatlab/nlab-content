
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The concept of _analytic spectrum_ is a realization of the concept of [[spectrum (geometry)]] in the context of [[non-archimedean analytic geometry]]. Given an [[affinoid algebra]] $A$ over a [[non-archimedean field]], then the concept of [[spectrum of a commutative ring]] whose points are [[prime ideals]]/[[maximal ideals]] does not produce a sensible space that admits [[analytic geometry]]. Rather, instead of regarding points of the spectrum as ring homomorphisms to $A \to \mathbb{R}$, the analytic spectrum instead takes points to be multiplicative [[seminorms]] ${\vert -\vert} \colon A \to \mathbb{R}_{\geq 0}$ bounded by the norm on the given field.

If $Spec_{an}(A)$ is the set of all such multiplicative seminorms, then for $x \in Spec_{an}(A)$ a point one writes the corresponding seminorm as ${\vert - \vert}_x$ and thinks of it as being the norm on the function algebra on $Spec(A)$ which is given by "evaluating functions at $x$ and then applying the field norm to that".

One turns this $Spec_{an}(A)$ into a [[topological space]] in the usual way by choosing the weakest topology such that under this assignment the original elements of $A$ become [[continuous function]] on $Spec_{an}(A)$.

Globalizing this analytic spectrum construction leads to the concept of [[Berkovich analytic space]].
 
## Definition

For $A$ a [[normed ring]], its _analytic spectrum_ or _Berkovich spectrum_ $Spec_an A$ is the set of all non-zero multiplicative [[seminorms]] on $A$, regarded as a [[topological space]] when equipped with the weakest topology such that all [[functions]]

$$
  Spec_{an} A \to \mathbb{R}_+
$$

of the form 

$$
  x \mapsto {\vert x(a)\vert}
$$

for $a \in A$ are [[continuous function|continuous]].

If $A$ is equipped with the structure of a [[Banach ring]], one takes the _[[bounded map|bounded]]_ multiplicative seminorms.


So a point in the analytic spectrum of $A$ corresponds to a non-zero [[function]]

$$
  {\Vert -\Vert} : A \to \mathbb{R}
$$

to the [[real numbers]], such that for all $x, y \in A$

1. ${\Vert x \Vert} \geq 0$;

1. ${\Vert x y \Vert} = {\Vert x \Vert} {\Vert y \Vert}$;

1. ${\Vert x + y \Vert} \leq {\Vert x \Vert} + {\Vert y \Vert}$

and boundedness means that there exists $C \gt 0$ such that for all $x \in A$

$$
  {\Vert x\Vert} \leq C {\vert x \vert}_A
  \,.
$$

(e.g. [Berkovich 09, def. 1.2.3](#Berkovich09))

## Examples

### Affine line

For $k$ a [[field]] and $k[T]$ the [[polynomial ring]] over $k$ in one generator, 

$$
  \mathbb{A}_k := Spec_{an} k[T]
$$

is the [[analytic affine line]] over $k$.

If $k = \mathbb{C}$, then $\mathbb{A}_k = \mathbb{C}$ is the ordinary [[complex plane]].

## Related concepts

* [[spectrum (geometry)]]

* [[analytic geometry]], [[analytic space]]

* [[p-adic geometry]]

## References

### Original

The notion originates in 

* {#Berkovich90} [[Vladimir Berkovich]], _Spectral theory and analytic geometry over non-Archimedean fields_, Mathematical Surveys and Monographs, vol. 33, American Mathematical Society, Providence, RI, (1990) 169 pp.
 


### Expositions and Lecture notes

Introductory exposition of the Berkovich analytic spectrum includes

* [[Sarah  Brodsky]], _Non-archimedean geometry_, brief lecture notes, 2012 ([pdf](http://math.berkeley.edu/~sstich/MAT_274/Math_274_3_Feb_2012.pdf))

* [[Scott Carnahan]], _Berkovich spaces I_ ([web](http://sbseminar.wordpress.com/2007/09/18/berkovich-spaces-i/))


* {#Poineau07} [[Jérôme Poineau]], _Global analytic geometry_, pages 20-23 in EMS newsletter September 2007 ([pdf](http://www.ems-ph.org/journals/newsletter/pdf/2007-09-65.pdf))

* [[Frédéric Paugam]], section 2.1.4 of _Global analytic geometry and the functional equation_ (2010) ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-global-analytic-geometry.pdf))

* {#Berkovich09} [[Vladimir Berkovich]], section 1 of _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))


[[!redirects analytic spectra]]
[[!redirects Berkovich analytic spectrum]]
[[!redirects Berkovich analytic spectra]]


[[!redirects Berkovich spectrum]]
[[!redirects Berkovich spectra]]

[[!redirects Bercovich spectrum]]
[[!redirects Bercovich spectra]]