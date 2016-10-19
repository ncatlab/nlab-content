[[!redirects inductive-recursive types]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##


In [[type theory]], _induction-recursion_ is a principle for mutually defining [[types]] of the form 


$$
  A \colon Type\,,\;\;\; and \;\;\; B \colon A \to Type
  \,,
$$ 

where $A$ is defined as an [[inductive type]] and $B$ is defined by [[recursion]] on $A$. Crucially, the definition of $A$ may use $B$. Without this last requirement, we could first define $A$ and then separately $B$.

##Related concepts

* [[inductive-inductive type]]