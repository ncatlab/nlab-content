
\tableofcontents

## Idea

Given a commutative ring $R$, a **paraunital $R$-algebra** is a [[nonunital algebra|nonunital $R$-algebra]] $A$ where there is an element $\iota \in A$ and an [[involution]] $x \mapsto \overline{x}$ such that $x \cdot \iota = \iota \cdot x = \overline{x}$ for all $x \in A$. A paraunital $\mathbb{Z}$-algebra is also called a **paraunital ring**. 

A [[unital algebra]] is a paraunital algebra in multiple different ways: 

* where the element is given by the unit $1$ and the involution is given by the [[identity function]] $x \mapsto x$. 

* where the element is given by the negation of the unit $-1$ and the involution is given by negation $x \mapsto -x$

These were first defined in the specific context of [[composition algebras]] in the [[generalized Hurwitz theorem]] in [Elduque 2021](#Elduque21) but could be generalized from composition algebras to any $R$-algebra. 

## Generalizations

This concept could be generalized from the category of $R$-modules to any [[monoidal category]]:

A **paraunital algebra object** in a [[monoidal category]] $(C, I, \otimes)$ is an object $A \in C$ with morphisms $\iota:I \to A$, $\pi:A \otimes A \to A$, and $j:A \to A$ such that $j \circ j = \mathrm{id}_A$ and the following [[commuting diagram|diagrams commute]]:

   $$
     \array{
       I \otimes A 
         &\overset{\iota \otimes \mathrm{id}_A}{\longrightarrow}&
       A \otimes A
       \\
       \downarrow^{\lambda_A} & & \downarrow^{\pi} 
       \\
       A &\overset{j}{\longrightarrow}& A
     }
     \,,
   $$

   $$
     \array{
       A \otimes I 
         &\overset{\mathrm{id}_A \otimes \iota}{\longrightarrow}&
       A \otimes A
       \\
       \downarrow^{\rho_A} & & \downarrow^{\pi} 
       \\
       A &\overset{j}{\longrightarrow}& A
     }
     \,,
   $$

where $\lambda_A:I \otimes A \to A$ and $\rho_A:A \otimes I \to A$ are the left and right [[unitors]] of the [[monoidal category]]. 

In the [[category of sets]], paraunital algebra objects are called **paraunital magmas**, and in the [[category of abelian groups]], paraunital algebra objects are called **paraunital rings**. 

## Related concepts

* [[magma]], [[unital magma]]

* [[nonunital algebra]], [[nonunital ring]]

* [[composition algebra]] 

* [[generalized Hurwitz theorem]]

## References

* {#Elduque21} [[Alberto Elduque]], *Composition algebras*, Chapter 2 in:  Abdenacer Makhlouf (ed.), *Algebra and Applications I: Non-associative Algebras and Categories*, Sciences-Mathematics, ISTEWiley (2021) 27-57 &lbrack;[arXiv:1810.09979](https://arxiv.org/abs/1810.09979), [ISBN:978-1-789-45017-0](https://www.wiley.com/en-ae/Algebra+and+Applications+1:+Non+associative+Algebras+and+Categories-p-9781789450170)&rbrack;

[[!redirects paraunital algebra]]
[[!redirects paraunital algebras]]
[[!redirects para-unital algebra]]
[[!redirects para-unital algebras]]

[[!redirects paraunital ring]]
[[!redirects paraunital rings]]
[[!redirects para-unital ring]]
[[!redirects para-unital rings]]

[[!redirects paraunital algebra object]]
[[!redirects paraunital algebra objects]]
[[!redirects para-unital algebra object]]
[[!redirects para-unital algebra objects]]

[[!redirects paraunital magma]]
[[!redirects paraunital magmas]]
[[!redirects para-unital magma]]
[[!redirects para-unital magmas]]