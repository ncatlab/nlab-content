
<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[logic]], the __false__ proposition, called __falsehood__ or __falsity__, is the [[proposition]] which is always false.

The faleshood is commonly denoted $false$, $F$, $\bot$, or $0$.


## Definitions

### In classical logic

In [[classical logic]], there are two [[truth values]]: false and [[true]].  Classical logic is perfectly symmetric between falsehood and truth; see [[de Morgan duality]].


### In constructive logic

In [[constructive logic]], $false$ is the [[bottom element]] in the [[poset]] of [[truth values]].  

Constructive logic is still [[two-valued logic|two-valued]] in the sense that any truth value is false if it is not [[true]].


### In a topos

In terms of the [[internal logic]] of a [[topos]] (or other [[category]]), $false$ is the [[bottom element]] in the [[poset of subobjects]] of any given [[object]] (where each object corresponds to a [[context]] in the internal language).

However, not every topos is [[two-valued topos|two-valued]], so there may be other truth values besides $false$ and $true$.


## Examples

### In the topos $Set$

In the archetypical [[topos]] [[Set]], the terminal object is the [[singleton]] [[set]] $*$ (the [[point]]) and the poset of subobjects of that is classically $\{\emptyset \hookrightarrow *\}$.  Then falsehood is the [[empty set]] $\emptyset$, seen as the [[empty subset]] of the point.  (See [Internal logic of Set](http://ncatlab.org/nlab/show/internal+logic#LogicOfSet) for more details).

The same is true in the archetypical [[(∞,1)-topos]] [[∞Grpd]]. From that perspective it makes good sense to think of

* a set as a 0-[[truncated]] $\infty$-groupoid: a [[0-groupoid]];

* a [[subsingleton]] set as a $(-1)$-[[truncated]] $\infty$-groupoid: a [[(?1)-groupoid]].

In this sense, the object $false$ in [[Set]] or [[∞Grpd]] may canonically be thought of as being [[generalized the|the]] unique [[empty groupoid]].


[[!redirects false]]
[[!redirects False]]
[[!redirects falsity]]
[[!redirects falsehood]]
