A $k$-character, $k \in \mathbb{N}$, of a group $G$ is a certain function 
$$
  \chi^{(k)} : G^k \to \mathbb{C}
$$
which descends to a function of _$k$-conjugacy classes_.

A $k$-conjugacy class in $G^k$ is a minimal subset of $G^k$ which is closed under $k$-fold conjugation in the following sense:

$$
  [g_1, \cdots, g_k]
  :=
  \{
    (g'_1, \cdots, g'_k) \in G^k |
    \exists (h_1, \cdots h_k) \in G^k :
    g'_1 = h_1 g_1 h_2^{-1} \vee
    g'_2 = h_2 g_2 h_3^{-1} \vee \cdots
    g'_k = h_k g_2 h_1^{-1}
  \}
  \,.
$$

The quotient map which sends elements in $G^k$ to their $k$-conjugacy class is called (at least for $k=2$) the [[weak Cayley table]] of $G$.

#Remarks#

* Evidently, on any $k$-conjugacy class of $G$ we canonically obtain $k$ different commuting actions of $G$.

#Reference#

For a brief review and a collection of many relevant references see

* Kenneth W. Johnson, Sandro Mattarei and Surinder K. Sehgal, _Weak Cayley tables_, [Journal of the London Mathematical Society 2000 61(2):395-411](http://jlms.oxfordjournals.org/cgi/content/abstract/61/2/395) ([pdf](http://journals.cambridge.org/download.php?file=%2FJLM%2FJLM61_02%2FS0024610799008571a.pdf&code=e119cd0ef145cd79d298f403f4d38dc7))

#Functorial reformulation#

There is a succinct functorial reformulation of $k$-conjugacy classes. This is described at [[schreiber:higher group characters]].


[[!redirects higher group characters]]