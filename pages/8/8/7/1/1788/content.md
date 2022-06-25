* [[Guiseppe Peano]], *Sur une courbe, qui remplit toute une aire plane*, Mathematische Annalen, **36** (1890) 157–160 &#x5B;[doi:10.1007/BF01199438](https://doi.org/doi:10.1007/BF01199438)]
| $k \,\backslash\, n$ | $-1$ | $0$ | $1$ | $2$ | $\cdots$ | $\infty$ |
|--|--|--|--|--|--|--|
| $0$ | trivial | [[pointed set]] | [[pointed object|pointed]] [[groupoid]] | [[pointed object|pointed]] [[2-groupoid]] | $\cdots$ | [[pointed infinity-groupoid|pointed $\infty$-groupoid]] | 
| $1$ | trivial | [[group]] | [[2-group]] | [[3-group]] | $\cdots$ | [[infinity-group|$\infty$-group]] |
| $2$ | " | [[abelian group]] | [[braided 2-group]] | [[braided 3-group]] | $\cdots$ | [[braided infinity-group|braided $\infty$-group]] | 
| $3$ | " | " | [[symmetric 2-group]] | [[sylleptic 3-group]] | $\cdots$ | groupal [[E3-algebra|$E_3$-space]] |
| $4$ | " | " | " | [[symmetric 3-group]] | $\cdots$ | groupal  [[E4-algebra|$E_4$-space]] |  
| $\vdots$ | " | " | " | " | $\ddots$ | $\vdots$ |
| $\infty$ | " | " | " | " | $\cdots$ | groupal [[E-infinity space|$E_\infty$-space]] <br/> / [[abelian infinity-group|abelian $\infty$-group]]  | 

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