
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

# Quasi-topological spaces
* table of contents
{: toc}

## Idea 

The [[category]] of *quasi-topological spaces* was proposed in [Spanier 1963](#Spanier63) as a substitute for the category [[Top]] of ordinary [[topological spaces]], in order to serve as a [[convenient category of topological spaces|convenient category]] for the purposes of [[algebraic topology]]. In particular, quasi-topological spaces form a [[complete category|complete]] and [[cocomplete category|cocomplete]] [[cartesian closed category]]. 

Today, quasi-topological spaces seem to be regarded mostly as a historical curiosity, perhaps because working topologists were never comfortable with the [[set theory|set-theoretic]] issues that accompany them. In retrospect, however, they are an impressive testament to the conceptual insight of [[Edwin Spanier|Spanier]] into ideas of [[topos theory]] which were at the time (early 1960's) barely in the air, and even not quite born yet (being an early example of [[quasitopos]], whose name perhaps derives from Spanier's notion, compare [Dubuc & Español 2006, p. 12](#DubucEspanol06)). 


## Definition 

Let $\mathcal{C H}$ be the [[category]] of [[compact Hausdorff spaces]]. This may be regarded as a (large) [[site]] when equipped with the [[Grothendieck topology]] of [[finite open covers]], in fact a [[concrete site]]. 

+-- {: .un_defn}
###### Definition 
A **quasi-topological space** is a (small-set valued) [[concrete sheaf]] on $\mathcal{C H}$. 
=-- 

The (super-large) category of quasi-topological spaces is a [[quasitopos]] (although this is not immediately obvious for [[size issues|size reasons]] --- in particular, it is probably not a [[Grothendieck quasitopos]]).  In particular, it is a [[locally cartesian closed category]].


## References 

* {#Spanier63} [[Edwin Spanier]], _Quasi-topologies_, Duke Mathematical Journal **30**, number 1 (1963) pp 1–14 ([doi:10.1215/S0012-7094-63-03001-1](https://doi.org/10.1215/S0012-7094-63-03001-1))


* {#DubucEspanol06} [[Eduardo Dubuc]], [[Luis Español]], _Quasitopoi over a base category_  ([arXiv:math.CT/0612727](http://arxiv.org/abs/math.CT/0612727))


[[!redirects quasi-topological space]]
[[!redirects quasi-topological spaces]]
[[!redirects quasitopological space]]
[[!redirects quasitopological spaces]]
