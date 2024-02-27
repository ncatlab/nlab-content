
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[inverse function|inverse]] operation to [[multiplication]].

## Definition

### In an Euclidean domain

See [[Euclidean domain]]...

### In a field

Given a [[Heyting field]] $F$, let us define the type of all terms in $F$ apart from 0:

$$F_{#0} \coloneqq \{a \in F \vert a # 0\}$$

The **division function** is a [[binary function]] $\frac{(-)}{(-)}:F \times F_{#0} \to F$ defined as 

$$\frac{x}{y} \coloneqq x \cdot \frac{1}{y}$$

where 

$$\frac{1}{y}$$

is the [[reciprocal function]]. 

## Division of finite sets

Given finite set $A$ and [[pointed set]] $B$ with an element $p:B$, one can construct finite sets $A \div B$ and $A\ \%\ B$ with a bijection 
$$A \simeq ((B \times (A \div B)) + (A\ \%\ B))$$
and a bijection
$$(B \hookrightarrow A\ \%\ B) \simeq \emptyset$$

A finite [[pointed set]] $B$ is a divisor of $A$ if there is a bijection $(A\ \%\ B) \simeq \emptyset$:

$$A \vert B \coloneqq (A\ \%\ B) \simeq \emptyset$$

## Related concepts

* [[arithmetic]]

* [[division ring]]

* [[division algebra]]

* [[localization of a ring]], [[field of fractions]]

* [[fraction]],  [[rational numbers]]

* [[reciprocal function]], [[rational function]]

