
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


# Epsilontic analysis
* table of contents
{: toc}

## Idea

Epsilontic analysis is the now standard rigorous approach to [[analysis]], developed by [[Bernard Bolzano]], [[Augustin Cauchy]], [[Karl Weierstraß]], [[Richard Dedekind]], and others in the mid-to-late 19th century.  It contrasts with [[infinitesimal analysis]], both the less-than-rigorous analysis that preceded it and the rigorous [[nonstandard analysis]] (and other approaches to infinitesimals, such as [[synthetic differential geometry]]) that followed it.

Ironically, [[classical mathematics|classical]] epsilontic analysis is not rigorous enough for [[constructive mathematics]], which requires it to be applied using [[intuitionistic logic]].  This was developed thoroughly by [[Errett Bishop]]; see [[constructive analysis]].


## History

Epsilontic analysis developed out of the practical problems of finding errors of [[approximation]].  Taking the basic principles of calculus for granted, 18th-century mathematicians discovered various methods to approximate the values of [[limit of a sequence|limits]], [[derivatives]], [[integrals]], and [[series]] with an error guaranteed to be bounded above by whatever [[positive number]] $\epsilon$ (for 'error') one wished.

Epsilontic analysis turns these results around into definitions: the value of a limit, derivative, integral, or series is *defined* to be the (necessarily unique) [[real number]] $L$ such that, given any positive number $\epsilon$, one can produce an approximation within $\epsilon$ of $L$.

[[Augustin Cauchy]] is often credited with promoting this approach, in his 1821 _[[Cours d'Analyse]]_.  However, Cauchy also used [[infinitesimal number|infinitesimals]], and he did not actually *define* concepts with epsilontics.  Cauchy did, however, use epsilontic arguments in many proofs.

Other mathematicians used epsilontics to clarify Cauchy\'s work.  [[Bernard Bolzano]] gave epsilontic definitions and proofs even earlier than Cauchy, but his work was largely ignored at the time.  This later came to the attention of [[Karl Weierstraß]], who set out a systematic treatment of epsilontic analysis, the basis of the standard analysis of today.


## Topological vs uniform properties

The precise post-Cauchy development of epsilontics was necessary to clarify the difference between (as we now see them) [[topological property|topological]] and [[uniform property|uniform properties]], which show up in the order of [[quantifiers]] in the definitions.

Typically, topological properties apply at a point, although one can then require them at all points.  Doing so, one has a definition of the form
$$ \forall x,\; \forall \epsilon,\; \exists M,\; \phi(M,x,\epsilon) ,$$
where $M$ is some parameter for a method of approximation and $\phi(M,x,\epsilon)$ states that the method, applied with the parameter $M$, approximates a value of interest at $x$ to within an error $\epsilon$.  Equivalently, one may write
$$ \forall \epsilon,\; \forall x,\; \exists M,\; \phi(M,x,\epsilon) ,$$
but we cannot shift the quantifiers further.

In contrast, a uniform property necessarily refers to a range of points and typically takes the form
$$ \forall \epsilon,\; \exists M,\; \forall x,\; \phi(M,x,\epsilon) ,$$
which is stronger.

It is difficult to make this distinction without the $\epsilon$.  It is not impossible to do this otherwise, as [[Abraham Robinson]] showed with infinitesimals, but it\'s telling that nobody did so before epsilontics.  Even Cauchy\'s definitions are difficult to understand in this respect, since he used epsilontics only for proofs (and not always even then) and not for definitions.  (In this regard, see the [[Cauchy sum theorem]].)

## Examples

* for an epsilontic proof that [[polynomials are continuous]] see for instance ([Miller 14](#Miller14))

## References

The extent to which Cauchy anticipated modern epsilontics is debated.  For arguments pro and contra (respectively), see:

* {#Grabiner1983} Judith Grabiner (1983). Who Gave You the Epsilon? Cauchy and the Origins of Rigorous Calculus. The American Mathematical Monthly 90:3 (1983). [pdf](http://www.maa.org/pubs/Calc_articles/ma002.pdf).
   

* {#BKS2012} Piotr B&#322;aszczyk, Mikhail G. Katz, David Sherry (2012). Ten Misconceptions from the History of Analysis and Their Debunking. [arXiv](http://arxiv.org/abs/1202.4153). Foundations of Science 18:1 (2013), 43--74. [doi](http://dx.doi.org/10.1007/s10699-012-9285-8).
   

On Bolzano, this looks promising, but I have not read it:

*  {#Rusnock2000} Paul Rusnock (2000).  Bolzano\'s Philosophy and the Emergence of Modern Mathematics.  Rodopi (2000).
   

Examples of epsilontic proofs include

* {#Miller14} Kyle Miller, _Polynomials are continuous functions_, 2014 ([pdf](https://math.berkeley.edu/~kmill/math1afa2014/poly.pdf))



[[!redirects epsilontic analysis]]
[[!redirects epsilontics]]
[[!redirects epsilontic]]
[[!redirects epsilon-delta analysis]]
[[!redirects epsilon--delta analysis]]
[[!redirects epsilon-delta analysis]]
[[!redirects ε-δ analysis]]
[[!redirects epsilon-delta]]
[[!redirects epsilon--delta]]
[[!redirects epsilon-delta]]
[[!redirects ε-δ]]