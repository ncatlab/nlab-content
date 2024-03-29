
| | [[type theory]] | [[category theory]] |
|--|--|--|
|  | [[syntax]] | [[semantics]] |
|  |  [[natural deduction]] |  [[universal construction]] | 
|  | **[[product type]]** | **[[product]]** |
| [[type formation]] |  $\frac{\vdash \;A \colon Type \;\;\;\;\; \vdash \;B \colon Type}{\vdash A \times B \colon Type}$ | $A,B \in \mathcal{C} \Rightarrow A \times B \in \mathcal{C}$ |
| [[term introduction]] | $\frac{\vdash\; a \colon A\;\;\;\;\; \vdash\; b \colon B}{ \vdash \; (a,b) \colon A \times B}$ | $\array{ && Q\\ & {}^{\mathllap{a}}\swarrow &\downarrow_{\mathrlap{(a,b)}}&  \searrow^{\mathrlap{b}}\\ A &&A \times B&& B }$  |
| [[term elimination]] | $\frac{\vdash\; t \colon A \times B}{\vdash\; p_1(t) \colon A} \;\;\;\;\;\frac{\vdash\; t \colon A \times B}{\vdash\; p_2(t) \colon B}$ | $\array{ && Q\\ &&\downarrow^{t} && \\ A &\stackrel{p_1}{\leftarrow}& A \times B &\stackrel{p_2}{\to}& B}$ |
| [[computation rule]] | $p_1(a,b) = a\;\;\; p_2(a,b) = b$ | $\array{ && Q \\ & {}^{\mathllap{a}}\swarrow &\downarrow_{(a,b)}& \searrow^{\mathrlap{b}}  \\ A &\stackrel{p_1}{\leftarrow}& A \times B& \stackrel{p_2}{\to} & B}$ |

