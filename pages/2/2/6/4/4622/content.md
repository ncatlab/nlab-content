
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[logic]], the __false__ proposition, called __falsehood__ or __falsity__, is the [[proposition]] which is always false.

The faleshood is commonly denoted $false$, $F$, $\bot$, or $0$.  These may be pronounced 'false' even where it would be ungrammatical for an adjective to appear in ordinary English.


## Definitions

### In classical logic

In [[classical logic]], there are two [[truth values]]: false and [[true]].  Classical logic is perfectly symmetric between falsehood and truth; see [[de Morgan duality]].


### In constructive logic

In [[constructive logic]], $false$ is the [[bottom element]] in the [[poset]] of [[truth values]].  

Constructive logic is still [[two-valued logic|two-valued]] in the sense that any truth value is false if it is not [[true]].

In [[natural deduction]] the [[inference rules]] for falsehood are given as 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \bot \; \mathrm{prop}} \quad \frac{\Gamma \vdash P \; \mathrm{prop}}{\Gamma, \bot \; \mathrm{true} \vdash P \; \mathrm{true}}$$ 

### In linear logic

In [[linear logic]], there is both _additive_ falsity, denoted $0$, and _multiplicative_ falsity, denoted $\bot$.  Despite the notation, it is $0$ that is the [[bottom element]] of the lattice of linear truth values.  (In particular, $0 \vdash \bot$ but $\bot \nvdash 0$.)


### In a topos

In terms of the [[internal logic]] of a [[topos]] (or other [[category]]), $false$ is the [[bottom element]] in the [[poset of subobjects]] of any given [[object]] (where each object corresponds to a [[context]] in the internal language).

However, not every topos is [[two-valued topos|two-valued]], so there may be other truth values besides $false$ and $true$.


### In type theory

In [[type theory]] with [[propositions as types]], falsehood is represented by the [[empty type]].


### In homotopy type theory

In [[homotopy type theory]], falsehood is represented by the [[empty space]].


## Examples

### In the topos $Set$

In the archetypical [[topos]] [[Set]], the terminal object is the [[singleton]] [[set]] $*$ (the [[point]]) and the poset of subobjects of that is classically $\{\emptyset \hookrightarrow *\}$.  Then falsehood is the [[empty set]] $\emptyset$, seen as the [[empty subset]] of the point.  (See [Internal logic of Set](http://ncatlab.org/nlab/show/internal+logic#LogicOfSet) for more details).

The same is true in the archetypical [[(∞,1)-topos]] [[∞Grpd]]. From that perspective it makes good sense to think of

* a set as a 0-[[truncated]] $\infty$-groupoid: a [[0-groupoid]];

* a [[subsingleton]] set as a $(-1)$-[[truncated]] $\infty$-groupoid: a [[(-1)-groupoid]].

In this sense, the object $false$ in [[Set]] or [[∞Grpd]] may canonically be thought of as being [[generalized the|the]] unique [[empty groupoid]].


## Related concepts

* [[true]], [[unit type]]

* [[empty type]], [[ex falso quodlibet]]

* [[contradiction]], [[inconsistency]], [[consistency]]


[[!redirects false]]
[[!redirects False]]
[[!redirects false proposition]]
[[!redirects false propositions]]
[[!redirects false statement]]
[[!redirects false statements]]
[[!redirects false sentence]]
[[!redirects false sentences]]

[[!redirects falsity]]
[[!redirects falsehood]]
