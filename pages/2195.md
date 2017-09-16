Let $G$ be a locally compact abelian group with invariant (= Haar) measure $\mu$. Then for each $f\in L_1(G,\mu)$ define its __Fourier transform__ $\hat{f}$ as a function on its [[Pontrjagin dual]] group $\hat{G}$ given by

$$
\hat{f}(\chi) = \int_G f(x) \widebar{\chi(x)} d\mu(x),\,\,\,\chi\in\hat{G}.
$$

The Fourier transform of $f\in L_1(G,\mu)$ is always continuous and bounded on $\hat{G}$; the transform of the convolution of two functions is the product of the transforms of each of the functions separately. In the classical case of __Fourier series__, where $G=\mathbb{Z}$ and $\hat{G}=S^1$, the Fourier transform restricts to a unitary operator from $L_2(S^1,dt)$ to $l_2(\mathbb{Z})$ and the Fourier coefficients are the numbers 

$$c_n := \hat{f}(\chi_n) = \int_0^1 f(t) e^{-2\pi i n t} dt,$$

for $n\in\mathbb{Z}$, where the functions $\chi_n(t)= e^{2\pi i n t}$ form an orthonormal basis of $L_2(S^1,dt)$. The Fourier transform $\hat{\chi_n}$ is then viewed as the  $\mathbb{Z}$-series $\delta_n$ which on $n$-th space has $1$ and elsewhere $0$. The Fourier transform replaces the operator of differentiation $d/dx$ by the operator of the multiplication by the series $\{2\pi i n\}_{n\in\mathbb{Z}}$.

In general if $G$ is compact abelian group whose Pontrjagin dual is discrete, one can normalize the invariant measure by $\mu(G)=1$ and $\hat{\mu}(X)=card(X)$ for $X\subset\hat{G}$. Then the Fourier transform is a unitary operator from $L_2(X,\mu)$ to $L_2(\hat{G},\hat{\mu})$. 

Fourier transform of functions on the real line $\mathbb{R}$ is called the __Fourier integral__: $\hat{f}(\lambda)=\int_{-\infty}^\infty f(x) e^{-2\pi i\lambda x} dx.$ It is usually defined as a linear automorphism of the Schwarz space $S(\mathbb{R})\to S(\mathbb{R})$; there is also an appropriate extension to the space of distributions $S'(\mathbb{R})$ by $\langle \hat{f},\phi\rangle := \langle f, \hat{\phi}\rangle$ where $f\in S'(\mathbb{R})$ and $\phi\in S(\mathbb{R})$. The Fourier transform and the inverse Fourier transforms are continuous mutually inverse operators $S'(\mathbb{R})\to S'(\mathbb{R})$. 
There is a unitary operator on $L_2(\mathbb{R},dx)$ which when restricted to $L_2(\mathbb{R},dx)\cap L_1(\mathbb{R},dx)$ agrees with the Fourier transform. 

The study of Fourier transform and its generalizations is the main subject of harmonic analysis. 
For noncommutative topological groups instead of continuous characters one should consider irreducible unitary representations what makes the subject much more difficult. There are also generalizations in [[noncommutative geometry]].  

