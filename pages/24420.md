
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## General idea

The notions of *[[posets]]* and *[[prosets]]* (in [[order theory]]),  and of *[[thin categories]]*, *[[truth-value]]-[[enriched categories]]* and *[[(0,1)-categories]]* (in [[category theory]] and [[higher category theory]]) are all closely related and yet possibly subtly but crucially different:


In [[category theory]]-language:

* a *[[preordered set]]* (or *[[proset]]*, for short) is 

  a [[strict category|strict]] and [[thin]] [[category]].

* a *[[partially ordered set]]* (or *[[poset]]*, for short) is 
  
  a [[strict category|strict]] and [[thin]] **and [[skeletal category|skeletal]]** [[category]].

Now, while every [[poset]] is in particular a [[proset]], 
a [[proset]] need not be [[isomorphism|isomorphic]] (namely as a [[strict category]]) to a [[poset]]. 

On the other hand, if we disregard [[strict category|strictness]] and assume the [[axiom of choice]], then every [[proset]] is *[[equivalence of categories|equivalent as a category]]* to a [[poset]]: This is the statement that every category has a [[skeletal category|skeleton]].

Finally, if [[prosets]] are regarded as actual [[categories]] this way (i.e. disregarding their [[strict category|strictness]]) then as such they are, equivalently:

1. [[thin categories]], 

1. [[truth value]]-[[enriched categories]], 

1. [[(0,1)-categories]].

Conversely, since the notion of [[skeletal category]] implies that of a [[strict category]], one may say that [[posets]] are the *[[skeletal category|skeletal]]* [[truth value]][[enriched category|-]]/[[thin category|thin-]]/[[(0,1)-categories|$(0,1)$-categories]].

In doing so, one should just keep in mind that in various contexts (such as in various [[foundations of mathematics]]) [[strict category|strictness]] may matter and/or the [[axiom of choice]] may fail, in which case [[prosets]] are *not* equivalently [[posets]] and neither may be really equivalent to [[thin categories]]/[[(0,1)-categories]].

Finally, beware that even these notions of categories may not always be equivalent: A context which uses the terminology  "[[(0,1)-category]]" is less likely to even consider the notion of a [[strict category]] than a context using the terminology "[[thin category]]" or "[[truth value]]-[[enriched category]]", which might even regard [[strict categories]] as the default notion.

## In Type theory

(...)



