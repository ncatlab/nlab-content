
<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[logic]], the __true__ proposition, or __truth__, is the [[proposition]] which is always true.

The truth is commonly denoted $true$, $T$, $\top$, or $1$.


## Definitions

### In classical logic

In [[classical logic]], there are two [[truth values]]: true and [[false]].  Classical logic is perfectly symmetric between truth and falsehood; see [[de Morgan duality]].


### In constructive logic

In [[constructive logic]], $true$ is the [[top element]] in the [[poset]] of [[truth values]].  

Constructive logic is still [[two-valued logic|two-valued]] in the sense that any truth value which is not true is [[false]].


### In a topos

In terms of the [[internal logic]] of a [[topos]] (or other [[category]]), $true$ is the [[top element]] in the [[poset of subobjects]] of any given [[object]] (where each object corresponds to a [[context]] in the internal language).

However, not every topos is [[two-valued topos|two-valued]], so there may be other truth values besides $true$ and $false$.


## Examples

### In the topos $Set$

In the archetypical [[topos]] [[Set]], the terminal object is the [[singleton]] [[set]] $\{*\}$ (the [[point]]) and the poset of subobjects of that is classically $\{\emptyset \hookrightarrow *\}$.  Then truth is the singleton set $\{*\}$, seen as the [[improper subset]] of itself.  (See [Internal logic of Set](http://ncatlab.org/nlab/show/internal+logic#LogicOfSet) for more details).

The same is true in the archetypical [[(∞,1)-topos]] [[∞Grpd]]. From that perspective it makes good sense to think of

* a set as a 0-[[truncated]] $\infty$-groupoid: a [[0-groupoid]];

* a [[subsingleton]] set as a $(-1)$-[[truncated]] $\infty$-groupoid: a [[(?1)-groupoid]];

* the singleton set as the $(-2)$-[[truncated]] $\infty$-groupoid: the unique (up to equivalence) [[(?2)-groupoid]].

In this sense, the object $true$ in [[Set]] or [[∞Grpd]] may canonically be thought of as being [[generalized the|the]] unique [[(?2)-groupoid]].


[[!redirects true]]
[[!redirects True]]
[[!redirects truth]]
