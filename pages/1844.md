__Euler numbers__ $E_n$, $n\geq 0$ are defined via generating function

$$
\frac{1}{ch t}= \frac{2}{e^t+e^{-t}} = \sum_{n\geq 0} E_n \frac{t^n}{n!}
$$

Do not mix them with Eulerian numbers (forming a different,  double sequence $A(n,k)$). All odd-numbered members of that sequence vanish: $E_{2k-1}=0$ for $k\in\mathbb{N}$. $E_0=1$, $E_2 = -1$, $E_4 = 5$, see [Euler number at wikipedia](http://en.wikipedia.org/wiki/Euler_number) for more and [Abramowitz-Stegun handbook](http://en.wikipedia.org/wiki/Abramowitz_and_Stegunfor) for many Euler numbers. 
 
Euler numbers generalize to __Euler polynomials__ $E_n(x)$ defined via generating function

$$
\frac{2e^{tx}}{e^t+1}=\sum_{n\geq 0} E_n(x) \frac{t^n}{n!},
$$ 

namely $E_n = 2^n E_n(\frac{1}{2})$. Euler polynomials satisfy recursion $E_n(x+1)+E_n(x)=2x^n$ and may be conversely expressed via Euler numbers as

$$
E_n(x) = \sum_k \left(\array{n\\ k}\right) \frac{E_k}{2^k}\left(x-\frac{1}{2}\right)^{n-k}
$$

There is also a complementarity formula $E_n(1-x)=(-1)^n E_n(x)$. 
See e.g. Louis Comtet, __Advanced combinatorics__, D. Reifel Publ. Co., Dordrecht-Holland, Boston 1974 [djvu](http://ftp.filekeeper.org/download/acm/books/Comtet%20Louis%20-%20Advanced%20Combinatorics.djvu)

[[!redirects Euler polynomial]]
[[!redirects Euler numbers]]
[[!redirects Euler polynomials]]