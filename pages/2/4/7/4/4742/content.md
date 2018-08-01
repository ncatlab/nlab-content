
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

In a [[category]] **associativity** is the condition that the two ways to use binary [[composition]] of [[morphisms]] to compose a sequence of three morphisms are _equal_ 

$$
  h \circ (g \circ f) = (h \circ g) \circ f
  \phantom{AAAA}
$$


<center>
<img src="https://ncatlab.org/nlab/files/AssociativityDiagram.png" width="300">
</center>

$$
  \array{
    c_2 &\overset{ \phantom{AA}g\phantom{AA} }{\longrightarrow}& c_3
    \\
    {}^{\mathllap{f}}\Big\uparrow 
      & \searrow^{\mathrlap{h \circ g}} & 
    \Big\downarrow{}^{\mathrlap{h}}
    \\
    c_1 &\underset{ (h \circ g) \circ f }{\longrightarrow}& c_4
  }
  \;\;\;\;=\;\;\;\;
  \array{
    c_2 &\overset{ \phantom{AA}g\phantom{AA} }{\longrightarrow}& c_3
    \\
    {}^{\mathllap{f}}\Big\uparrow 
      & {}^{\mathllap{ g \circ f }}\nearrow & 
    \Big\downarrow{}^{\mathrlap{h}}
    \\
    c_1 &\underset{ h \circ (g \circ f) }{\longrightarrow}& c_4
  }
$$

If the category has a single [[object]] it is the [[delooping]] $\mathcal{B} A$ a [[monoid]] $A$, and then this condition is the _associativity_ condition on the binary operation of [[monoids]] such as [[groups]], [[rings]], [[algebras]], etc.

More generally, in [[higher category theory]], _associativity_ of composition of morphisms in an [[n-category]] means that the different ways to use binary composition for composing collections of [[k-morphisms]] form a [[contractible]] [[infinity-groupoid]]. This is a [[coherence law]].

For instance the associativity law in an [[A-infinity algebra]] is the special case of associativity in a 1-object [[A-infinity-category]].


## Examples

* See [[associahedron]].

* In a [[monoidal category]] associativity is the statement that the [[associator]] satisfies its [[coherence law]], which is true by a [[coherence theorem]].

## Related concepts

* [[unitality]]

* [[co-associativity]]

## References

The [[coherence law]] of associativity is stated in 

* [[Hermann Grassmann]], &#167;3 of _[[Ausdehnungslehre]]_, 1844

[[!redirects associativity]]
[[!redirects associativity law]]
[[!redirects associativity laws]]
[[!redirects associative]]
[[!redirects associative law]]
[[!redirects associative laws]]
