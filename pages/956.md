A (binary) [[relation]] $\sim$ on a set $A$ is __tight__ if any two elements that are related in neither order are equal:
$$\forall (x, y: A),\; x \nsim y \;\wedge\; y \nsim x \;\Rightarrow\; x = y$$

The term 'tight' here comes from the theory of [[apartness relation]]s, although this is also a property of [[linear order]]s.

## Discussion ##

This discussion is from when the article was at [[linear relation]].

+--{.query}
I\'m not aware of any standard name for this property, even in the constructive literature.  (Constructive mathematicians mostly think of it as antisymmetry of the negation; classical mathematicians mostly think of it as half of trichotomy, with asymmetry being the other half.)  The high-school meaning of 'linear relation' referred to above (which is what you find on Google) is unlikely to cause confusion, but an unambiguous name might be better.

The alternative is 'tight relation'.  I\'ve never seen that used (in mathematics) except in reference to an [[apartness relation]].  One could therefore argue that the symmetrised form here has never appeared in the literature; since an apartness relation is symmetric, you only have to list one of the conjuncts in the hypothesis (and people always list the left one, since that looks most natural).

Perhaps this is such an unimportant concept that it doesn\'t matter, but I wonder if there are any opinions?

_Mike_: I think it is so unimportant that it doesn't matter.  (-:  I would actually prefer to avoid calling it anything, especially something that has other meanings and  could create needless confusion.

_Toby_:  I think that I\'ll take the last clause as a vote for 'tight'.  (The best that I can find for 'tight relation' is a usage in combinatorics that seems pretty informal; one sometimes says that there\'s a tight relation between $A$ and $B$ if $A$ provides a tight bound for $B$; here 'tight bound' is the only notion that requires definition.)  The main reason that I want a word is so that I can put it in the table at [[linear order]].

_Toby_:  OK, it\'s all 'tight relation' now.

=--