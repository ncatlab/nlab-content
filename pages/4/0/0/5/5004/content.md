[[!redirects relational structures]]

#Contents#
* table of contents
{:toc}

## Relational structures ## 

### Idea### 
Relational structures are models for a relational theory, that is, a logical theory whose [[signature (in logic)|signature]] is **relational**.

+--{: .un_defn}
######Definition ######
A __relational structure__ is a tuple $\mathfrak{F}$ whose first component $W$, is a non-empty set, and whose remaining components are relations on $W$. (We assume that there is at least one relation given.) 
=--
In their use in the Kripke semantics of [[modal logics]], the set $W$ is sometimes called the _universe_ (perhaps better the _domain_) and the  elements of $W$ are called 'worlds', amongst a host of other names! This leads to the terminology 'possible world semantics' which is sometimes used.

### Examples### 

1.  [[partial order|poset]], $(W;\leq)$ or more generally a set, $W$, with a family of partial orders, $\{\leq_i\}$, on it;

1. [[transition system]], $(S; \{R_e\mid e\in E\})$, (see discussion on the transition system's page);

1.  a rooted [[tree]] can be considered as a relational structure on its set of nodes, by specifying properties of a successor relation;

1. an [[arrow structure]] is a relational structure proposed in [[modal logic]] to handle relational versions of [[groupoids]];

1.  a set $W$ with, on it, an equivalence relation, $\sim$, or, more generally, a family of equivalence relations, $\sim_i$, for $i$ is some indexing set.