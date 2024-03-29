### Compactness for locales 

this is a scratch space for where I was working on clarifying

https://ncatlab.org/nlab/show/compact+space#compactness_for_locales

In another context, the definition 2.2 also works for [[locales]], since it refers only to the [[frame]] of open sets.  Here is an equivalent way to phrase it that is often convenient for locale theory. 

Firstly, note that given any open cover, adding to it the closure of all unions of finite opens defines a [[direction]] on any [[open cover]].  This directed open cover is useful for locales.

+-- {: .num_prop #directed}
###### Proposition

A space is compact iff every directed open cover of it has the entire space as one of its opens.

=-- 

+-- {: .proof} 
###### Proof 
For the "only if" case: Let $\mathcal{U}$ be a directed open cover of compact $X$, with the direction defined by unioning. By the open-cover definition of compactness, $X$ is the union of finitely many opens $U_i$ of $\mathcal{U}$. By directedness, these $U_i$ have an upper bound in $\mathcal{U}$. Since the only upper bound of opens unioning to $X$ is $X$, it follows that $X$ belongs to $\mathcal{U}$. 

For the "if" case: given an open cover $\mathcal{U}$ of $X$, let $\mathcal{U}'$ be all the unions of finitely many opens of $\mathcal{U}$. $\mathcal{U}'$ is an open cover of $X$ since $\mathcal{U}$ is. Taking the upper bound for a direction as unioning, clearly $\mathcal{U}'$ is directed. So, by hypothesis, $X$ belongs to $\mathcal{U}'$. So $X$ is a union of finitely many opens of $\mathcal{U}$. This shows $X$ is compact according to Definition \ref{hb}. 
=-- 
