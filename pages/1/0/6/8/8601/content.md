
| [[type theory]] | [[category theory]] |
|--|--|
| [[syntax]] | [[semantics]] |
| **[[judgment]]** | **[[diagram]]** | 
| [[type]] | [[object]] in [[category]] |
| $\vdash\; A \; \mathrm{type}$ | $A \in \mathcal{C}$ |
| [[term]] | [[element]] |
| $\vdash\; a \colon A$ | $* \stackrel{a}{\to} A$ |
| [[dependent type]] |  [[object]] in [[slice category]] |
| $x \colon X \;\vdash\; A(x) \; \mathrm{type}$ | $\array{A \\ \downarrow \\ X} \in \mathcal{C}_{/X}$ |
| [[term in context]] | [[generalized elements]]/[[element]] in [[slice category]] |
| $x \colon X \;\vdash \; a(x)\colon A(x)$ | $\array{X &&\stackrel{a}{\to}&& A \\ & {}_{\mathllap{id_X}}\searrow && \swarrow_{\mathrlap{}} \\ && X}$ |
| $x \colon X \;\vdash \; a(x)\colon A$ | $\array{X &&\stackrel{(id_X,a)}{\to}&& X \times A \\ & {}_{\mathllap{id_X}}\searrow && \swarrow_{\mathrlap{p_1}} \\ && X}$ |



