
#Contents#
* table of contents
{:toc}

## Definition

For $A$ a [[ring]], its _analytic spectrum_ or _Berkovich spectrum_ $Spec_an A$ is the set of all non-zero multiplicative [[seminorms]] on $A$, regarded as a [[topological space]] when equipped with the weakest topology such that all [[functions]]

$$
  Spec_an A \to \mathbb{R}_+
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
  {\vert x \vert}_A \leq C {\Vert x\Vert}
  \,.
$$

## Examples

### Affine line

For $k$ a [[field]] and $k[T]$ the [[polynomial ring]] over $k$ in one generator, 

$$
  \mathbb{A}_k := Spec_{an} k[T]
$$

is the [[analytic affine line]] over $k$.

If $k = \mathbb{C}$, then $\mathbb{A}_k = \mathbb{C}$ is the ordinary [[complex plane]].

## Related concepts

* [[analytic geometry]], [[analytic space]]

## References

### Original

The notion originates in 

* [[Vladimir Berkovich]], _Spectral theory and analytic geometry over non-Archimedean fields_, Mathematical Surveys and Monographs, vol. 33, American Mathematical Society, Providence, RI, (1990) 169 pp.
  {#Berkovich90}



### Expositions

An exposition of examples of Berkovich spectra is in

* [[Scott Carnahan]], _Berkovich spaces I_ ([web](http://sbseminar.wordpress.com/2007/09/18/berkovich-spaces-i/))


### Lecture notes

Course notes are around definition 4 of 

* [[Frédéric Paugam]], _Global analytic geometry and the functional equation_ (2010) ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-global-analytic-geometry.pdf))

and section 1 of 

* [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))


[[!redirects analytic spectra]]
[[!redirects Berkovich analytic spectrum]]
[[!redirects Berkovich spectrum]]
[[!redirects Berkovich spectra]]

[[!redirects Bercovich spectrum]]
[[!redirects Bercovich spectra]]
