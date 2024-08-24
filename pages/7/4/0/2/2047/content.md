+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

###Context###

#### Algebra
+--{: .hide}
[[!include algebra - contents]]

=--
=--
=--

## Definition

Given a [[ring]] $R$, the __socle__ $Soc(M)$ of a left $R$-[[module]] $M$ is the [[internal sum]] of all [[simple object|simple]] [[subobject|submodules]] of $M$. 

## Properties

Given a ring $R$, the correspondence $M\mapsto Soc(M)$ is clearly a subfunctor of the identity functor ${}_R Mod\to {}_R Mod$. It is moreover left exact (but not a [[kernel functor]] in the sense of Goldman in general). 

By the definition, the socle is a [[semisimple module|semisimple]] $R$-module. If we assume the axiom of choice, then the socle of $M$ can be presented as a direct sum of some subfamily of all simple submodules of $M$.

The notion of socle is important in [[representation theory]]. 

Notice that the notion is dual to the notion of the radical $Rad(M)$ which is the intersection of all maximal submodules of $M$. 

## Literature 

* Louis H. Rowen, _Ring theory -- Student edition_, Academic Press (1991, 2012)
* [[Joachim Lambek]], _Lectures on rings and modules_, Waltham Mass. 1966
* wikipedia [socle (mathematics)](http://en.wikipedia.org/wiki/Socle_%28mathematics%29)

category: algebra