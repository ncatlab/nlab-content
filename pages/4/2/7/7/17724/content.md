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

##Example 
(from [ForsSetz](#ForsSetz))

The universe a la Tarski is an example of an inductive-recursive definition,
where a set $U$ is defined inductively together with a recursive function $T: U \to
Set$. The constructors for $U$ may depend negatively on $T$ applied to
elements of $U$, as is the case if $U$, for example, is closed under dependent function spaces:

$$
\frac{a:U \;\;\;\;\;\;b : T(a) \to U}{\pi(a, b) : U}
$$

with $T(\pi(a, b)) = \prod_{x:T(a)} T(b(x))$.

Here, $T:U \to Set$ is defined recursively. Sometimes, however, one might
not want to give $T(u)$ completely as soon as $u:U$ is introduced, but instead
define $T$ inductively as well. This is the principle of [[induction-induction]].

##Related concepts

* [[inductive-inductive type]]

* [[algebraically compact category]]

##References 

* {#ForsSetz} [[Fredrik Nordvall Forsberg]] and [[Anton Setzer]], _A finite axiomatisation of inductive-inductive definitions_, ([pdf](http://cs.swan.ac.uk/~csfnf/papers/indind_finite.pdf))

[[!redirects induction-recursion]]
