
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An [[operad]] whose [[algebras over an operad]] are pairs consisting of an [[associative algebra]] and a [[module]] over that algebra

## Definition

+-- {: .num_defn}
###### Definition

The **operad for modules over an algebra** $LM$ is the [[colored operad|colored]] [[symmetric operad]] whose

* [[objects]] are two elements, to be denoted $\mathfrak{a}$ and $\mathfrak{n}$;

* [[multimorphisms]] $(X_i)_{i = 1}^n \to Y$ form

  * if $Y = \mathfrak{a}$ and $X_i = \mathfrak{a}$ for all $i$ then: the set of [[linear orders]] on $n$ elements, equivalently the elements of the [[symmetric group]] $\Sigma_n$;

  * if $Y = \mathfrak{n}$ and exactly one of the $X_i = \mathfrak{n}$ then: the set of linear order $\{i_1 \lt \cdots \lt i_n\}$ such that $X_{i_n} = \mathfrak{n}$;

  * otherwise: the empty set;

* [[composition]] is given by composition of linear orders as for the [[associative operad]].

=--

In ([Lurie](#Lurie)) this appears as def. 4.2.1.1.

## Properties

### Relation to the associative operad

Write $Assoc$ for the [[associative operad]], regarded as a [[symmetric operad]]. 

There is a canonical inclusion morphism

$$
  Assoc \to LM
$$

given by labeling the unique object/color of $Assoc$ with $\mathfrak{a}$. For $(A,N) \colon LM^\otimes \to \mathcal{C}^\otimes$ a map to a [[symmetric monoidal category]] the composite

$$
  A \colon Assoc^\otimes \to LM^\otimes \stackrel{(A,N)}{\to} \mathcal{C}^\otimes
$$

is the corresponding [[associative algebra]].

There is also a morphism

$$
  LM \to Assoc
$$

given by forgetting the color and just remembering the linear orders. This is such that for

$$
  A \colon Assoc^\otimes \to \mathcal{C}^\otimes
$$

and algebra, the composite

$$
  (A,A) \colon LM^{\otimes} \to Assoc^{\otimes} \to \mathcal{C}^\otimes
$$

is the algebra canonically regarded as a module over itself.

### Relation to the operad for bimodules

Analogous relations exist to the [[operad for bimodules over algebras]].

(...)

## Related concepts

* [[associative operad]], [[commutative operad]]

* [[operad for bimodules over algebras]]

* [[model structure on modules over an algebra over an operad]]

## References

Section 4.2.1 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

[[!redirects (∞,1)-operad for (∞,1)-modules over an A-∞ algebra]]

[[!redirects operad for modules]]
