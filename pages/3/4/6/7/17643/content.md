
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[propositional logic]], the __contrapositive__ of an [[implication]] $P\to Q$ is the converse implication  $(\neg Q) \to (\neg P)$ of [[negations]].

The __contrapositive rule__ states that it is valid to derive the contrapositive $\neg{Q} \to \neg{P}$ from the original statement $P \to Q$ (where $\neg$ is [[negation]] and $\to$ is [[implication]]).  In symbols:
$$ 
  \frac 
    {P \to Q} 
    {\neg{Q} \to \neg{P}} 
  \;CP 
  \mathrlap{\,.}
$$
The combination of this rule, followed by [[modus ponens]] (MP, the [[elimination rule]] for implication) was traditionally called _modus tollens_:
$$ 
  \frac{
    \displaystyle 
    \frac
      {P \to Q} 
      {\neg{Q} \to \neg{P}} 
    \;CP 
    \;\;\; 
    \neg{Q}
  } 
  {\neg{P}} 
  \;\;
  MP
  \mathrlap{\,.}
$$

The contrapositive rule is valid in [[intuitionistic logic]], not just in [[classical logic]]; however, the reverse rule is valid only in classical logic. 

Another intuitionistically valid rule, this one reversible, is
$$ 
  \frac 
    {P \to \neg{Q}} 
    {Q \to \neg{P} \mathrlap{\,,}} 
$$
as both statements are [[logical equivalence|equivalent]] to the negation of $P \wedge Q$ (where $\wedge$ is [[conjunction]]).  However, the superficially similar
$$ 
  \frac 
    {\neg{P} \to Q} 
    {\neg{Q} \to P} 
$$
is again valid only [[classical logic|classically]].


## Related concepts

* [[implication]]

* [[negation]]

[[!redirects contrapositive]]
[[!redirects contrapositives]]

[[!redirects contrapositive rule]]
[[!redirects contrapositive rules]]

[[!redirects contraposition]]
[[!redirects contrapositions]]

[[!redirects modus tollens]]

