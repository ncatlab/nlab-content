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