
| $k \,\backslash\, n$ | $-1$ | $0$ | $1$ | $2$ | $\cdots$ | $\infty$ |
|--|--|--|--|--|--|--|
| $0$ | trivial | [[pointed set]] | [[pointed object|pointed]] [[groupoid]] | [[pointed object|pointed]] [[2-groupoid]] | $\cdots$ | [[pointed infinity-groupoid|pointed $\infty$-groupoid]] | 
| $1$ | trivial | [[pointed set]] | [[pointed object|pointed]] [[groupoid]] | [[pointed object|pointed]] [[2-groupoid]] | $\cdots$ | [[pointed infinity-groupoid|pointed $\infty$-groupoid]] <br/> [[A1-space|$A_1$-space]] | 
| $2$ | trivial | [[unital magma]] | [[H-spatial groupoid|magmoidal groupoid with unit]] | [[magmoidal 2-groupoid with unit]] | $\cdots$ | [[H-space]]/[[A2-space]] |
| $3$ | " | [[monoid]] | [[H-monoidal groupoid]] | [[H-monoidal 2-groupoid]] | $\cdots$ | [[H-monoid]]/[[A3-space]] |
| $4$ | " | " | [[A4-spatial groupoid]] | [[A4-spatial 2-groupoid]] | $\cdots$ | [[A4-space]] | 
| $5$ | " | " | " | [[A5-spatial 2-groupoid]] | $\cdots$ | [[A5-space]] | 
| $\vdots$ | " | " | " | " | $\ddots$ | $\vdots$ |  
| $\infty$ | trivial | [[monoid]] | [[monoidal groupoid]] | [[monoidal 2-groupoid]] | $\cdots$ | [[A-infinity space|$A_\infty$-space]] | 


</th><th>-1</th><th>0</th><th>1</th><th>2</th><th>...</th><th>\infty</th></tr>
<tr><th>0</th><td>trivial</td><td>[[pointed set]]</td><td>[[pointed object|pointed]] [[groupoid]]</td><td>[[pointed object|pointed]] [[2-groupoid]] </td><td>...</td><td>[[pointed object|pointed]] [[∞-groupoid]]</td></tr>
<tr><th>1</th><td>trivial</td><td>[[pointed set]]</td><td>[[pointed object|pointed]] [[groupoid]]</td><td>[[pointed object|pointed]] [[2-groupoid]] </td><td>...</td><td>[[pointed object|pointed]] [[∞-groupoid]]/[[A1-space]]</td></tr>
<tr><th>2</th><td>trivial</td><td>[[unital magma]]</td><td>[[magmoidal groupoid with unit]]</td><td>[[magmoidal 2-groupoid with unit]]</td><td>...</td><td>[[H-space]]/[[A2-space]]</td></tr>
<tr><th>3</th><td>\"</td><td>[[monoid]]</td><td>[[H-monoidal groupoid]]</td><td>[[H-monoidal 2-groupoid]]</td><td>...</td><td>[[H-monoid]]/[[A3-space]]</td></tr>
<tr><th>4</th><td>\"</td><td>\"</td><td>[[A4-spatial groupoid]]</td><td>[[A4-spatial 2-groupoid]]</td><td>...</td><td>[[A4-space]]</td></tr>
<tr><th>5</th><td>\"</td><td>\"</td><td>\"</td><td>[[A5-spatial 2-groupoid]]</td><td>...</td><td>[[A5-space]]</td></tr>
<tr><th>&#8942;</th><td>\"</td><td>\"</td><td>\"</td><td>\"</td><td>&#8945;</td><td>&#8942;</td></tr>
<tr><th>\infty</th><td>trivial</td><td>[[monoid]]</td><td>[[monoidal groupoid]]</td><td>[[monoidal 2-groupoid]] </td><td>...</td><td>[[A-∞-space]]</td></tr></table>



\linebreak



[[!redirects Onsager-Machlup]]
#Onsager-Machlup
The [[Onsager-Machlup function]] is a generalization of a density (Radon-Nikodym derivative) to non locally compact spaces. Rather than comparing a probability measure to a translation invariant measure, the idea is to compare a probability measure to translations of itself. 

More precisely, consider a locally compact metric group $(G, d)$ with Borel probability measure $\mu$.  Then there exists Haar measure $\lambda$, and we may thus consider the limit 
\[f(z):=\lim_{\varepsilon\to 0} \frac{\mu(B_\varepsilon(z))}{\lambda(B_\varepsilon(z))}.\]

If this limit exists, then $f(z)$ is called the Radon-Nikodym derivative or density of $\mu$. However if $G$ is not locally compact (for instance, an infinite dimensional Banach space), then there is not a Haar measure. Therefore, we may consider the limit 
\[f(z):=\lim_{\varepsilon\to 0} \frac{\mu(B_\varepsilon(z))}{\mu(B_\varepsilon(0))}.\] 

If this limit exists, then $f(z)$ can be viewed as a fictitious density of the measure $\mu$. By convention, we call $\operatorname{OM}_\mu(z)=- \log (f(z))$ the Onsager-Machlup function for $\mu$.

#Mode
The Onsager-Machlup is the minimization objective for the mode of the measure $\mu$. That is, by minimizing $\operatorname{OM}_\mu(z)$, we maximize $f(z)$ which yields the modes of $\mu$. 

#Example
The Onsager-Machlup function for an infinite dimensional centered Gaussian measure $\mu$ on Banach space $B$ with Cameron-Martin space $H_\mu$ is 
\[\operatorname{OM}_\mu(z)=
\frac{1}{2}\|z\|_{\mu}^2 .\]

if $z\in H_\mu$ and $\infty$ otherwise. 