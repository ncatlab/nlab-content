Given a [[set]] $S$ and an [[equivalence relation]] $\equiv$ on $S$, the __quotient set__ of $S$ by $\equiv$ is the set $S/{\equiv}$ whose elements are the elements of $S$ but where two elements are now considered [[equality|equal]] if in $S$ they were merely equivalent.

If changing the definition of equality like this is not allowed in your [[foundations]] of mathematics, then you can still define $S/{\equiv}$ as an element of the [[power set]] of $S$ as follows:
\[\label{setdef}
A \in S/{\equiv} \;\Leftrightarrow\; \exists (x: S),\; A = \{y: S \;\mid\; x \equiv y\}\]
If you don\'t have (extensional) power sets either, then you\'ll have to use [[setoid]]s instead (but perhaps you\'d do better to change your terminology as described there).

In any case, the element of $S/{\equiv}$ that comes from the element $x$ of $S$ may be denoted $[x]_\equiv$, or simply $[x]$ if $\equiv$ is understood, or simply $x$ if there will be no confusion as to which set it is an element of.  This $[x]$ is called the __equivalence class__ of $x$ with respect to $\equiv$; the term 'class' here is an old word for 'set' and refers to the definition (eq:setdef) above, where $[x]$ is literally the set $A$.

Quotient sets in [[Set]] generalise to [[quotient object]]s in other categories.  In particular, an [[exact category]] is a [[regular category]] in which every (internal) equivalence relation on every object has a quotient object.