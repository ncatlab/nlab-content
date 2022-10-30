This page is meant to provide a general example and template for new
[[nLab:HomePage|nLab]]-pages. You can look at **[its source
code](http://ncatlab.org/nlab/source/Template+page)** to see how the
various parts are done. A minimal template is given first which
can be copy-and-pasted into newly created pages.  See [[HowTo]] for more details.

category: meta
[[!redirects Template page]]
[[!redirects Template pages]]
[[!redirects template page]]
[[!redirects template pages]]
[[!redirects page template]]
[[!redirects page templates]]


## Minimal Template Code

Remove any sections that you don\'t use.

~~~~

# Contents (or put a title here)
* the following line creates the automatic table of contents
{: toc}

## Idea ##

...


## Abstract ##

...


## Definition ##

...


## Properties ##

...


## Examples ##

...


## References ##

...


[[!redirects <put page name here>]]
[[!redirects <put page name here>s]]

~~~~

A longer example follows.

****


# Contents
* the following line creates the automatic table of contents
{: toc}

## Idea

It is an old observation that xyz. One notices that from the [[nPOV]] this is just an abc. This leads to the  definition of a uvw. It is useful for doing klm and provides the basis for the more general theory of &#228;&#246;&#252;.


## Abstract

A uvw is effectively a uv together with a w. Its main property is encoded in Somebody's Theorem which says that it consists of precisely three letters. The archetypical example of a uvw is $\mu \nu \omega$, details will be explained in the [special examples paragraph](/nlab/show/template+page#Specific_examples).


## Definition

As Jacques Distler said,

> See [more about definition/theorem/proof-environments](http://golem.ph.utexas.edu/wiki/instiki/show/Theorems)


+-- {: .un_defn}
###### Definition
**(uvw)**

A **uvw** is a UVW in which all letters are lower case.
=--


This may be summed up in the slogan:

+-- {: .standout}
A uvw is just what it looks like.
=--


## Properties

+-- {: .un_lemma }
###### Lemma

Every uvw contains at least one letter.
=--

+-- {: .proof}
###### Proof

By inspection.
=--


+-- {: .un_prop}
###### Proposition

Every uvw contains strictly more than one letter.
=--

+-- {: .proof}
###### Proof

Use the above lemma and continue counting:

\[
  1 + 1 = 2  \label{firstequation}
  \,.
\]
=--


+-- {: .un_theorem}
###### Theorem

Every uvw contains exactly three letters.
=--

+-- {: .proof}
###### Proof

Along the lines of the above proposition, we use equation \eqref{firstequation} and then conclude with

$$
  2 + 1 = 3
  \,.
$$

Notice that this is indeed independent of in which order we sum up the letters, in that the diagram

$$
  \array{
    \mathbb{N}\times \mathbb{N} \times \mathbb{N}
    &\stackrel{Id \times + }{\to}&
    \mathbb{N} \times \mathbb{N} 
    \\
    {}^{\mathllap{+ \times Id}}\downarrow && \downarrow^{\mathrlap{+}}
    \\
    \mathbb{N} \times \mathbb{N}
    &\underset{+}{\to}&
    \mathbb{N}
  }
  \,.
$$

commutes.
=--


+-- {: .un_corollary}
###### Corollary

No uvw contains more than three letters.
=--


## Examples

### Special cases

*  First case

*  Second case

*  Third case

+-- {: .query}
_[[Urs Schreiber|First person]]_:  I listed all of the special cases that I know above, but didn\'t Grothendieck study an important version too?

_[[Toby Bartels|Second person]]_:  No, you\'re thinking of Lawvere.  When I find the reference, I\'ll put it here.
=--


### Specific examples
{#Specific_examples}

For ease of reference, we will number the examples.

1.  The first example is obvious.

2.  The second example is a slight variation of (1).

3.  The third example is completely different from either (1) or (2).


## References  

The original definition appeared in section 3 of

* FirstName LastName, _Title_ Journal ([arXiv](http://put.url/here), [pdf](http://another.url/)) .


[[!redirects uvw]]
[[!redirects uvws]]
