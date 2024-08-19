
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[setoid]] or [[Bishop set]] whose [[quotient set]] is a [[field]]. 

“Field setoid” and "Bishop field" are placeholder names for a concept which may or may not have another name in the mathematics literature. 

## Definition

Let $R$ be a [[commutative ring setoid]]. An element $a \in R$ is [[invertible element|invertible]] if there exists an element $b \in R$ such that $a \cdot b \sim 1$. 

A **field setoid** or **Bishop field** is a [[commutative ring setoid]] $F$ in which for every element $a \in F$, $a$ is invertible if and only if $a \sim 0$ is false. 

### Constructive notions

Similarly to the case for [[fields]], there are different notions for field setoids in constructive mathematics. These include

* discrete field setoids

* Heyting field setoids 

* weak Heyting field setoids

* Kock field setoids

\begin{definition}
A **discrete field setoid** is a [[commutative ring setoid]] $F$ in which for every element $a \in F$, either $a \sim 0$ or $a$ is invertible. 
\end{definition}

\begin{definition}
A **weak Heyting field setoid** is a [[commutative ring setoid]] $F$ in which for every element $a \in F$, $a$ is not invertible if and only if $a \sim 0$. 
\end{definition}

\begin{definition}
A **Heyting field setoid** is a weak Heyting field setoid which is also a [[local ring setoid]]. 
\end{definition}

## Examples

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is a field setoid. In constructive mathematics, the set of Cauchy sequences in $F$ is only a Heyting field setoid. 

* Given any [[Archimedean ordered field]] $F$, the set of all [[locators]] of all elements of $F$ is a field setoid. In constructive mathematics, the set of all [[locators]] of all elements of $F$ is only a Heyting field setoid. 

## Related concepts

* [[setoid]], [[Bishop set]]

* [[field]]

* [[ring setoid]]

* [[local ring setoid]]

* [[ordered field setoid]]

[[!redirects field setoid]]
[[!redirects field setoids]]

[[!redirects Bishop field]]
[[!redirects Bishop fields]]

[[!redirects discrete field setoid]]
[[!redirects discrete field setoids]]

[[!redirects Bishop discrete field]]
[[!redirects Bishop discrete fields]]

[[!redirects discrete Bishop field]]
[[!redirects discrete Bishop fields]]

[[!redirects Heyting field setoid]]
[[!redirects Heyting field setoids]]

[[!redirects Bishop Heyting field]]
[[!redirects Bishop Heyting fields]]

[[!redirects weak Heyting field setoid]]
[[!redirects weak Heyting field setoids]]

[[!redirects Bishop weak Heyting field]]
[[!redirects Bishop weak Heyting fields]]