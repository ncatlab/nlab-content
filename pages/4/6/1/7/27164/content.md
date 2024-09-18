# ontology log
* this block creates the table of contents, leave as is
{: toc}

## Idea

An **ontology log** ("olog", spoken like "o log") is a labeled [[graph]] with [[concept with an attitude|an attitude]]: [[vertices]] are labeled with ontological types and [[edges]] are labeled with aspects of ontological relationships. The [[path category]] of an ontology log is a [[diagram]] with an attitude, representing an ontology which can be interpreted in a chosen setting. Non-trivial ontological facts can be added as path equivalences.

Ontology logs provide a basis for [[database]] construction. In particular, an ontology log can serve as the schema for structured data.

As originally introduced in ([Spivak & Kent 2012](#SpivakKent12)), ologs are [[diagrams]] into **[[Set]]** or another [[topos]]. However, as they anticipated, and as later realized by ([Patterson 2017](#Patterson17)), ologs can be generalized to diagrams into **[[Rel]]** or another [[bicategory of relations]].


## Definition 

An ontology log is a [[commuting diagram]] into a topos or a bicategory of relations. In the former case, they are known as **functional ologs**, and in the latter case, they are known as **relational ologs**. The labels of the diagram are expected to adhere to language-specific good practices. Labeled objects, arrows, and equivalences are called **types**, **aspects**, and **facts** respectively.

Target categories are called **data categories** and functors from ontology logs to data categories are called **instance data**. ([Patterson 2017](#Patterson17), p. 26)


### English

These rules are enumerated in ([Spivak & Kent 2012](#SpivakKent12)) as "good practices" which should be followed but may be distorted or ignored as part of authorial intent.

#### Types

Type labels should:

1. begin with "a" or "an",
1. refer to a distinction which the author can demonstrate,
1. also refer to a distinction which is [[inhabited]] and definable,
1. not end in punctuation, and
1. declare any variables or free parameters using subordinate "where" clauses.

#### Aspects

Aspect labels should:

1. begin with a verb,
1. yield a grammatical sentence when prefixed by its source label and suffixed by its target label, and
1. express a [functional dependency](https://en.wikipedia.org/wiki/Functional_dependency).

#### Facts

Facts do not need to be labeled, but the author should indicate as many of them as they know about, even facts which seem simple or trivial.


## Properties

(...)


## Examples

(...)


## References

* {#SpivakKent12} [[David Spivak|DI Spivak]], RE Kent, _Ologs: A Categorical Framework for Knowledge Representation_, PLoS ONE **7(1)** 2012 &lbrack;[arxiv:1102.1889](https://arxiv.org/abs/1102.1889), [doi:10.1371/journal.pone.0024274](https://doi.org/10.1371/journal.pone.0024274)&rbrack;
* {#Patterson17} E Patterson, _Knowledge Representation in Bicategories of Relations_, 2017 [arxiv:1706.00526](https://arxiv.org/abs/1706.00526)