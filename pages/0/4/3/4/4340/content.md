
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

In [[logic]], the __true__ proposition, or __truth__, is the [[proposition]] which is always true.

The truth is commonly denoted $true$, $T$, $\top$, or $1$.  These may be pronounced 'true' even where it would be ungrammatical for an adjective to appear in ordinary English.


## Definitions

In [[natural deduction]] the [[inference rules]] for true is given by

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \top \; \mathrm{prop}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Xi \vdash \top \; \mathrm{true}}$$ 

### In classical logic

In [[classical logic]], there are two [[truth values]]: true and [[false]].  Classical logic is perfectly symmetric between truth and falsehood; see [[de Morgan duality]].


### In constructive logic

In [[constructive logic]], $true$ is the [[top element]] in the [[poset]] of [[truth values]].  

Constructive logic is still [[two-valued logic|two-valued]] in the sense that any truth value which is not true is [[false]].

### In linear logic

In [[linear logic]], there is both _additive_ truth, denoted $\top$, and _multiplicative_ truth, denoted $1$.  As the notation suggests, it is $\top$ that is the [[top element]] of the lattice of linear truth values.  (In particular, $1 \vdash \top$ but $\top \nvdash 1$.)


### In a topos

In terms of the [[internal logic]] of a [[topos]] (or other [[category]]), $true$ is the [[top element]] in the [[poset of subobjects]] of any given [[object]] (where each object corresponds to a [[context]] in the internal language).

However, not every topos is [[two-valued topos|two-valued]] (even if it is [[boolean topos|boolean]], so there may be other truth values besides $true$ and $false$.


### In type theory

In [[type theory]] with [[propositions as types]], truth is represented by the [[unit type]].


### In homotopy type theory

In [[homotopy type theory]], truth is represented by any [[contractible type]].


## Examples

### In the topos $Set$

In the archetypical [[topos]] [[Set]], the terminal object is the [[singleton]] [[set]] $\{*\}$ (the [[point]]) and the poset of subobjects of that is classically $\{\emptyset \hookrightarrow *\}$.  Then truth is the singleton set $\{*\}$, seen as the [[improper subset]] of itself.  (See [Internal logic of Set](http://ncatlab.org/nlab/show/internal+logic#LogicOfSet) for more details).

The same is true in the archetypical [[(∞,1)-topos]] [[∞Grpd]]. From that perspective it makes good sense to think of

* a set as a 0-[[truncated]] $\infty$-groupoid: a [[0-groupoid]];

* a [[subsingleton]] set as a $(-1)$-[[truncated]] $\infty$-groupoid: a [[(−1)-groupoid]];

* the singleton set as the $(-2)$-[[truncated]] $\infty$-groupoid: the unique (up to equivalence) [[(−2)-groupoid]].

In this sense, the object $true$ in [[Set]] or [[∞Grpd]] may canonically be thought of as being [[generalized the|the]] unique [[(−2)-groupoid]].


## Related concepts

* **true**, [[unit type]]

* [[false]], [[empty type]]

* [[contradiction]], [[inconsistency]], [[consistency]]

* [[correspondence theory of truth]]

[[!include homotopy n-types - table]]

category: logic

[[!redirects true]]
[[!redirects True]]
[[!redirects true proposition]]
[[!redirects true propositions]]
[[!redirects true statement]]
[[!redirects true statements]]
[[!redirects true sentence]]
[[!redirects true sentences]]

[[!redirects truth]]
[[!redirects Truth]]
[[!redirects the truth]]
