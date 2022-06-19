
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


In [[type theory]], *type checking* refers to the problem whether the [[judgment]] $\Gamma\vdash a \colon A$ is derivable in a given type theory. 

## Properties

### Decidability

For instance, [[intensional type theory]] has [[decidability|decidable]] type checking, but [[extensional type theory]], which adds the rule of [[equality reflection]], does not. For an exposition of this result, see [Hofmann 1995](#Hofmann95). 

In more expressive type theories, we can also ask whether [[judgmental equality]] (also called _computational_ or _definitional_ equality) is [[decidability|decidable]]. Since deciding the judgmental equality is often a prerequisite for deciding type checking, systems with decidable type checking often have decidable judgmental equality.


## Related entries

* [[software verification]]

## References

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. dissertation, University of Edinburgh (1995). ([link](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/)) 


See also:

* Wikipedia, *[Type system](https://en.wikipedia.org/wiki/Type_system)* 


