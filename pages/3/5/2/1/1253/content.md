
# The axiom of extensionality
* table of contents
{: toc}

## Idea

In material [[set theory]], the _axiom of extensionality_ says that the global membership relation $\in$ is an [[extensional relation]] on the class of all [[pure sets]].

Since any relation becomes extensional on its [[extensional quotient]], one can interpret this axiom as a definition of [[equality]].  However, because the extensional quotient map need not reflect the relation, there is still content to the axiom: if two sets would be identified in the extensional quotient, then they must be members of the same sets and have the same sets as members.

If one models [[pure sets]] in structural [[set theory]], then this property may be made to hold by construction.


## Statements

### Weak extensionality

In the context of the [[axiom of foundation]], we may use [[weak extensionality]], simplifying the statement.

Taking [[equality]] as a primitive:

+-- {: .un_defn}
###### Axiom

If two sets have the same members, then they are equal.
=--

Or taking equality as defined:

+-- {: .un_defn}
###### Axiom

If two sets have the same members, then they are members of the same sets.
=--

Here we define two sets to be equal if they have the same members.

Note that we may prove, using the [[axiom of separation]] (bounded separation is enough), the converse: two sets must be equal if they are members of the same sets (as long as we have something, such as the [[axiom of pairing]] or [[axiom of power sets|power sets]], to guarantee that each set is a member of some set).


### Strong extensionality

Let $\sim$ be a [[bisimulation]], a binary relation such that for all sets $A$ and $B$ such that $A \sim B$, the following conditions hold:

* for all sets $C$ such that $C \in A$, there exists a set $D$ such that $D \in B$ and $C \sim D$
* for all sets $D$ such that $D \in B$, there exists a set $C$ such that $C \in A$ and $C \sim D$

The **axiom of extensionality** states that for every bisimulation $\sim$ and for every set $A$ and $B$, $A \sim B$ implies that $A = B$. 

If the set theory does not have [[equality]] as a primitive, we could define equality as the [[terminal]] [[bisimulation]], as the bisimulation $=$ such that for every bisimulation $\sim$ and for every set $A$ and $B$, $A \sim B$ implies that $A = B$.

## See also

* [[extensionality]]

category: foundational axiom

[[!redirects axiom of extensionality]]
