
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Differential cohesive homotopy type theory_ is the [[modal type theory]] obtained by adding to [[cohesive homotopy type theory]] an [[adjoint triple]] of [[idempotent monad|idempotent (co)monadic]] [[modalities]]:

$$
  \Re \dashv \Im \dashv \&
$$

called

* [[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]].

{#AlsoCalledElastic} (Also called *elastic* homotopy theory $[$[[schreiber:Proper Orbifold Cohomology|SS20, §3.1.2]]$]$, see at *[[geometry of physics -- categories and toposes]]* the sections on *[elastic toposes](geometry+of+physics+--+categories+and+toposes#ElasticToposes)* and *[elastic $\infty$-toposes](geometry+of+physics+--+categories+and+toposes#ElasticInfinityToposes)*.)

By the discussion at _[[cohesive (infinity,1)-topos -- infinitesimal cohesion]]_ this language can express at least the following notions

* [[reduced type]], [[infinitesimal path ∞-groupoid]], [[de Rham space]], [[jet bundle]], [[D-geometry]], [[∞-Lie algebra]] (synthetically), [[Lie differentiation]], hence "Formal [[Moduli Problems and DG-Lie Algebras]]" , [[formally etale morphism]], [[formally smooth morphism]], [[formally unramified morphism]], [[smooth etale ∞-groupoid]], hence [[∞-orbifold]] etc. 

## Overview ##

Differential cohesive homotopy type theory is a three-sorted dependent type theory of __spaces__, __infinitesimal neighborhoods__, and __homotopy types__, where there exist judgments 

* for __spaces__
$$\frac{\Gamma}{\Gamma \vdash S\ space}$$

* for __infinitesimal neighborhoods__
$$\frac{\Gamma}{\Gamma \vdash I\ infinitesimal\ neighborhood}$$

* for __homotopy types__
$$\frac{\Gamma}{\Gamma \vdash T\ homotopy\ type}$$

* for __points__
$$\frac{\Gamma \vdash S\ space}{\Gamma \vdash s:S}$$

* for __infinitesimals__
$$\frac{\Gamma \vdash I\ infinitesimal\ neighborhood}{\Gamma \vdash i:I}$$

* for __terms__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash t:T}$$

* for __fibrations__
$$\frac{\Gamma \vdash S\ space}{\Gamma, s:S \vdash A(s)\ space}$$

* for __infinitesimal fibrations__
$$\frac{\Gamma \vdash I\ infinitesimal\ neighborhood}{\Gamma i:I\vdash A(i)\ infinitesimal\ neighborhood}$$

* for __dependent types__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma, t:T \vdash B(t)\ homotopy\ type}$$

* for __sections__
$$\frac{\Gamma \vdash S\ space}{\Gamma, s:S \vdash a(s):A(s)}$$

* for __infinitesimal sections__
$$\frac{\Gamma \vdash I\ infinitesimal\ neighborhood}{\Gamma i:I\vdash a(i):A(i)}$$

* for __dependent terms__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma, t:T \vdash b(t):B(t)}$$

Differential cohesive homotopy type theory has the following additional judgments, two for turning spaces into homotopy types, two for turning homotopy types into spaces, two for turning infinitesimal neighborhoods into homotopy types, two for turning homotopy types into infinitesimal neighborhoods, two for turning infinitesimal neighborhoods into spaces, and two for turning spaces into infinitesimal neighborhoods:

* Every space has an __underlying homotopy type__
$$\frac{\Gamma \vdash S\ space}{\Gamma \vdash p_*(S)\ homotopy\ type}$$

* Every space has a __fundamental homotopy type__
$$\frac{\Gamma \vdash S\ space}{\Gamma \vdash p_!(S)\ homotopy\ type}$$

* Every homotopy type has a __discrete space__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash p^*(T)\ space}$$

* Every homotopy type has an __indiscrete space__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash p^!(T)\ space}$$

* Every infinitesimal neighborhood has an underlying homotopy type
$$\frac{\Gamma \vdash I\ infinitesimal\ neighborhood}{\Gamma \vdash q_*(I)\ homotopy\ type}$$

* Every infinitesimal neighborhood has a fundamental homotopy type
$$\frac{\Gamma \vdash I\ infinitesimal\ neighborhood}{\Gamma \vdash q_!(I)\ homotopy\ type}$$

* Every homotopy type has a __discrete infinitesimal neighborhood__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash q^*(T)\ infinitesimal\ neighborhood}$$

* Every homotopy type has an __indiscrete infinitesimal neighborhood__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash q^!(T)\ infinitesimal\ neighborhood}$$

I am not sure what the official names of these functors are:

* Every space has an infinitesimal neighborhood 
$$\frac{\Gamma \vdash S\ space}{\Gamma \vdash i_*(S)\ infinitesimal\ neighborhood}$$

* Every space has an infinitesimal neighborhood
$$\frac{\Gamma \vdash S\ shape}{\Gamma \vdash i_!(S)\ infinitesimal\ neighborhood}$$

* Every infinitesimal neighborhood has a space whereby that infinitesimal neighborhood is contracted away. 
$$\frac{\Gamma \vdash I\ infinitesimal\ neighborhood}{\Gamma \vdash i^*(I)\ space}$$

* Every infinitesimal neighborhood has a space
$$\frac{\Gamma \vdash I\ infinitesimal\ neighborhood}{\Gamma \vdash i^!(I)\ space}$$

## Modalities ##

From these judgements one could construct the [[reduction]] [[modality]] as 
$$\mathfrak{R}(S) \coloneqq i_!(i^*(S))$$
the [[infinitesimal shape]] modality as 
$$\mathfrak{J}(S) \coloneqq i_*(i^*(S))$$
and the [[infinitesimal flat]] modality as 
$$\&(S) \coloneqq i_*(i^!(S))$$
for a space $S$. 

## Related concepts

* [[differential cohesive (infinity,1)-topos]]

* [[differential geometry]]

[[!redirects differential homotopy type theory]]
