
\linebreak

* [[Gonzalo Reyes]], _Topos Theory in Montréal in the 1970s: My Personal Involvement_,  History and Philosophy of Logic Volume 40, 2019 - Issue 4 (2019) ([doi:10.1080/01445340.2018.1554471](https://doi.org/10.1080/01445340.2018.1554471))

> **2. Completeness theorems**

> Model theory tells us what a set-theoretical model of a theory is. What is the corresponding notion of model of a category in Categorical Logic? As mentioned already (see the first table) it should be just a functor from the category into Sets which preserves this extra structure. In particular, a model of a coherent category is a functor from the category into Sets which preserves finite limits, finite sups (of subobjects) and images. Such a functor is called a coherent functor. And indeed, we have a bi-univocal correspondence between the models of a coherent theory (in the model-theoretical sense) and the coherent functors from the (coherent) category associated with the theory.

> Since every coherent category $\mathbb{T}$ is obtained from a coherent theory, Gödel's theorem gives a completeness theorem for coherent categories. By putting together all the set-theoretical models of the category one obtains an embedding $e \colon \mathbb{T} \to Sets^{\left\vert \Mod(\mathbb{T})\right\vert}$ into the category of families of sets indexed by the models of the theory, namely the evaluation defined on objects by $e(A)(M) = M(A)$. (The definition of $e$ on morphisms should be clear)

> Using these techniques, one can prove several completeness theorems, by just transferring those proved in logic. Let us give two examples:

> Kripke's completeness theorem for an intuitionistic theory (Kripke 1965) shows that any Heyting category $\mathbb{H}$ has an embedding $e \colon \mathbb{H} \to Sests^{\mathbb{P}}$ into the category of set-valued functors from the dual of a poset $\mathbb{P}$ (on which further conditions could be imposed).

> On the other hand, Mansfield's completeness theorem for geometric theories (Mansfield 1972) (i.e. whose sequents are of the form $\phi \vdash \psi$ with $\phi$ and $\psi$ formulas in the language whose connectives are $\wedge, \top, \vee, \bottom, \exists$) shows that every geometric theory $\mathbb{T}$ has an embedding $e \colon \mathbb{T} \to V^{(\mathbb{B})}$ in the category of Boolean-valued sets of Scott–Solovay (with $\mathbb{B}$ a complete Boolean algebra) (Bell 1977).

> Now, all of these "target" categories are Grothendieck topos and the point is that these embeddings preserve the corresponding structure of the ‘source’ categories. Thus, the first is coherent, the second is Heyting and the last is geometric (i.e. it is coherent and preserves arbitrary $\vee$). Furthermore, it should be clear that these embeddings are models of the corresponding theories. But how do we interpret formulas and sequents directly in a topos? For these particular toposes, the answer had been given by Kripke and Cohen, but a general solution to this problem was missing. It is interesting to notice that the Grothendieck school was confronted with this problem when trying to define structures like ‘local ring’ or ‘separably real-closed local rings’ in a topos. Their method was to use points. Thus a ring R was local provided that for every point $p$, $p^\ast(R)$ is a local rings in $Sets$. 

> There were problems with this solution, however. Some toposes had no points at all. Even worse, for some structures, this solution was not correct. In fact, it was OK for structures defined in coherent logic only. The correct solution was obtained by Joyal using a generalization of the **forcing** of Kripke. Since then, this general notion is called the Kripke–Joyal forcing ([Johnstone 1977](sheaf+and+topos+theory#Johnstone77)).



\linebreak

