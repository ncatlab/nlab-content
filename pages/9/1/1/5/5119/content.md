
#Contents#
* table of contents
{:toc}

##Algebraic semantics for modal logics##

##Idea##
Classical [[propositional calculus]] has an algebraic model, namely a Boolean algebra. With a bit of imagination, one can give it a combinatorial model on the line of Kripke semantics. As this ordinary propositional logic has no modal operators, then the corresponding [[frame(in modal logic)|frames]] have no relations, so are just sets.  If $W$ is such a set, (of worlds), a valuation $V: Prop \to 2^W$ just assigns to each $p \in Prop$ and $w\in W$ a truth value, $\top$ or $\bot$, (true or false).  We know however that there is a Boolean algebra structure around in that power set $2^W$ and the semantics extends the assignment given by $V$ to a map of algebras, from the term algebra based on the basic propositional language to the Boolean algebra of subsets of $W$. That is just to say that it builds up that extension of $V$ bit-by-bit on the terms. This gives an algebraic interpretation or representation of the terms of the logic in terms of the algebra of subsets of $W$, in other words an algebraic semantics.

Modal logics also have an algebraic semantics based on a Boolean algebra, but with additional operators that model the modal operators.

##Boolean algebras with operators (BAOs)##

###[[Boolean algebras]]###
We will, here, write a Boolean algebra, $\mathbb{B }$ as an algebra, and in the notation,

$$\mathbb{B} = (B, +, ., {}^-,0,1)$$