
# Frames in Modal Logics
* table of contents
{:toc}

## Idea

This entry is about the notion of *frame* in [[modal logic]], also called _Kripke frames_, after the philosopher and logician [[Saul Kripke]].

Beware that this is an entirely  different concept than that of the same name used in [[geometric logic]], where the concept of *[[frames]]* (see there) refers to an abstraction of the algebraic structure of [[lattices of open subsets]] of a [[topological space]].


## Frames in Monomodal Logics

We will start with the simplest case, namely a frame for the basic [modal language](modal+logic#modal+language), $\mathcal{L}_\omega(1)$, (so with _one_ _unary_ [[modal operator]], denoted $\Diamond$).

+-- {: .un_defn}
###### Definition

A _frame_ for $\mathcal{L}_\omega(1)$ is a [[pair]] $\mathfrak{F} = (W,R)$ with 

* $W$ a [[inhabited set|non-empty set]] 

* $R$ a binary [[relation]] on $W$.

=--


In usual terminology 

* $W$ is referred to as the set of *[[possible worlds]]*.  Its [[elements]] are sometimes called _worlds_, sometimes _states_, sometimes _points_, depending on the context and the whim of the writer.  

* $R$ is called the _accessibility relation_, so $ R w v$ is read as "$v$ is accessible from $w$".


## Frames in Multimodal Logics

(N.B.  Here we are still restricting to multimodal logics in which the [[modal operators]] are unary. The generalisation to allowing more general $n$-ary modalities will be considered later.)

The generalisation is not difficult. In $\mathcal{L}_\omega(1)$, the single unary modality $\Diamond$ is modeled by one _binary_ relation.  In $\mathcal{L}_\omega(n)$, there are $n$ unary modalities so the frames have $n$ binary relations.  Explicitly we have 

+-- {: .un_defn}
###### Definition

A _frame_ for $\mathcal{L}_\omega(n)$ is a [[tuple|$(n+1)$-tuple]] $\mathfrak{F} = \big(W,\{R_i\}_{\{i=1,\ldots, n\}}\big)$ with 

* $W$ a [[inhabited set|non-empty set]] 

* $R_i$ a binary [[relation]] on $W$, for each $i=1,\ldots, n$.

=--


(More to go here ... frames with unary and more general relations.)


## Models in Modal Logics
 
To give the standard (geometric) semantics of modal logics one needs the models and these will be discussed in the entry [[geometric models for  modal logics]] and the companion [[algebraic models for  modal logics]].
 

## References

Generally this entry is based on

* {#BlackburnDeRijkeVenema01} [[Patrick Blackburn]], [[Maarten de Rijke]], [[Yde Venema]], *Modal Logic*, Cambridge Tracts in Theoretical Computer Science **53**, Cambridge University Press  (2001) &lbrack;[doi:10.1017/CBO9781107050884](https://doi.org/10.1017/CBO9781107050884)&rbrack;

(any mistakes or errors of interpretation are due to ....!)


[[!redirects Kripke frame]]
[[!redirects Kripke frames]]
[[!redirects frame (Kripke)]]
[[!redirects frames (Kripke)]]
[[!redirects frame (modal logic)]]
[[!redirects frames (modal logic)]]
