The concept of Cauchy completeness, ordinarily thought of as applying to [[metric space]]s, was vastly generalized by Bill Lawvere in his influential paper "Metric spaces, generalized logic, and closed categories". It is now seen by category theorists as a concept of [[enriched category]] theory, with close ties to the concept of [[Morita equivalence]] in the theory of modules. 

The basic idea is that the Cauchy completion of a category is the closure of a category under what are called "absolute limits", i.e., limits that are preserved by any functor whatsoever. Equivalently, the Cauchy completion is the closure with respect to absolute colimits. If $C$ is small, the Cauchy completion $\bar{C}$ of $C$ lies between $C$ and its "free cocompletion", aka presheaf category

$$C \hookrightarrow \bar{C} \hookrightarrow Set^{C^{op}}$$ 

(see the entry at [[presheaf]] for "free cocompletion"), and consists of those presheaves $F$ dubbed "tiny" by Lawvere, meaning those presheaves which are connected and projective: the functor 

$$hom_{Set^{C^{op}}}(F, -): Set^{C^{op}} \to Set$$ 

preserves small coproducts and coequalizers. All of these concepts generalize straightforwardly to the context of general $V$-enriched categories, where $V$ is a complete, cocomplete, symmetric monoidal closed category. 


## Discussion 

_Todd_: I envision starting with the example $V = [0, \infty]$ before treating other bases $V$ such as $Set$ and $Ab$.

_Toby_: Although the term comes from $[0,\infty]$, readers might find it easier to understand in $\Set$, where we usually study limits first. That said, you should write whichever you want, and people will add to it.

_Todd_: Um, I _think_ I understand how the wiki works, Toby, so I while I appreciate your giving me permission to write however I please, I wasn't actually asking for any. I was just stating some intent. That said, some things are easier for the $Set$ case, and some are easier for the case $[0, \infty]$. I'll get back to this in a bit. Thanks. 

_Toby_: Sorry, I interpreted it more broadly as a suggestion for future development rather than individual intent. (That is, 'I envision that we should start with ...' rather than 'I envision that I shall start with ...'.) So I added my own suggestion; but then it sounded like I might be telling you what to do, so I disclaimed that. In other words, of course you don\'t need my permission, but I didn\'t want to leave you with the impression that I was trying to stop you either.

_Todd_: Okay, that makes sense. It would have been clearer had I said "I plan to...": in a sense I was both thinking to myself and also letting people know what I was thinking. Anyway, thanks for clarifying, and I promise to try to add some more intellectual content to this so far scintillating conversation we're having. ;-) 

_Toby_:  I just read this again after a couple of months, and I think that I was just completely stupid.  Of course one should start with $[0, \infty]$!


[[!redirects Cauchy complete categories]]
[[!redirects Cauchy completion]]
