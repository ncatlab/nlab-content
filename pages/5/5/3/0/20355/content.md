[[!redirects functorially finite]]
##Functorially finite subcategories of abelian categories##

Let $\mathcal{A}$ be an abelian category and $\mathcal{C}$ a full subcategory. Given an object $X$ of $\mathcal{A}$, a morphism $f: C \to X$ from $C \in \mathrm{Ob}(\mathcal{C})$ is called a **right $\mathcal{C}$ approximation of X** if, for any $C' \in \mathrm{Ob}(\mathcal{C})$ and any morphism $f': C' \to X$, we can factor $f'$ and $f \circ g$. 

For example, suppose that we have finitely many objects $C_1$, $C_2$, ..., $C_n$ and $\mathcal{C}$ is the full subcategory on direct sums of $C_j$'s. Suppose also that our category is $k$ linear for some field $k$ and that $\mathrm{Hom}(C_j, X)$ is finite dimensional over $k$. Then $\bigoplus_j \Hom(C_j, X) \otimes_k C_j \longrightarrow X$ will be a right approximation of $X$.

As an example where we do NOT have a left approximation, let $\mathcal{A}$ be finitely generated abelian groups and let $\mathcal{C}$ be finite abelian groups. Take $X = \mathbb{Z}$. For any finite abelian group $C$ and map $\mathbb{Z} \to C$, we can choose a prime $p$ not dividing $|C|$, then $\mathbb{Z} \to \mathbb{Z}/p \mathbb{Z}$ will not factor through $\mathbb{Z} \to C$.

The full subcategory $\mathcal{C}$ is called **right functorially finite** if every object in $\mathcal{A}$ has a **right $\mathcal{C}$ approximation**. We define **left $\mathcal{C}$ approximation** and **left functorially finite** in a dual manner. A full subcategory which is both right and left functorially finite is called functorially finite.