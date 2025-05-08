

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

$\phantom{-----------}$Monday, May 19:

| Time | Speaker |
|------|---------|
| 08:00-08:45 | &lbrack;Breakfast&rbrack; |
| 09:00-09:45 | [[Andrei Bernevig]] (Princeton University) |
| 09:50-10:35 | [[Meng Cheng]] (Yale) |
| 10:35-11:00 |	\[Break\] |
| 11:00-11:45 | [[Sankar Das Sarma]] (University of Maryland) |
| 11:45-13:00 |	\[Lunch\] |
| 12:00-13:45 |	[[Sophia Economou]] (Virginia Tech) |
| 13:50-14:35 |	[[Tudor Stanescu]] (West Virginia) |
| 14:35-15:00 |	\[Break\] |
| 15:00-15:45 |	[[Abhay Pasupathy]] (Columbia University) |
| 15:50-16:35 |	[[Yi Li]] (Johns Hopkins University) |
| 16:35-17:00 |	\[Break\] |
| 17:00-18:00 |	Microsoft |
| 18:00       |	\[Dinner\]

$\phantom{-----------}$Tuesday, May 20

| Time | Speaker |
|------|---------|
| 08:00-08:45 | \[Breakfast\] $\phantom{-------------}$ |
| 09:00-9:45  |	[[Hisham Sati]] (NYU Abu Dhabi) |
| 09:50-10:35 |	[[Tim Byrnes]] (NYU Shanghai) |
| 10:35-11:00 |	\[Break\] |
| 11:00-11:45 |	[[Pouyan Ghaemi]] (CUNY) |
| 11:45-13:00 |	\[Lunch\] |
| 13:00-13:45 | [[Emil Prodan]] (Yeshiva University) |
| 13:50-14:35 | [[Javad Shabani]] (NYU) |
| 14:35-15:00 |	\[Break\] |
| 15:00-15:45 |	[[Urs Schreiber]] (NYU Abu Dhabi) |
| 15:50-16:35 |	[[Andrei Vrajitoarea]] (NYU New York) |
| 17:00       | \[Closing\] |







$$   
  \mathbb{C}[\mathbb{Z}^n]
  \underset{
    \mathbb{Z}\big[\mathbb{Z}^n_{[\sum] = 0}\big]
  }{\otimes}
  \mathbf{1}_{\zeta^{1/n}}
$$

$$
  shift 
  \sum_{i=0}^{n-1}
  \zeta^{-i/n} (i, 0, \cdot)
  \;=\;
  \sum_{i=0}^{n-1}
  \zeta^{-i/n} (i+1, 0, \cdot)
  \;=\;
  \zeta^{1/n}
  \sum_{i=0}^{n-1}
  \zeta^{-i/n} (i, 0, \cdot)
$$

\linebreak



Let $\mathbb{Z}^n_{\sum= [0]_k } \hookrightarrow \mathbb{Z}^n$ be the subgroup on those [[n-tuple|$n$-tuples]] of [[integers]] $(n_i)_{i = 1}^n$ whose [[sum]] is a multiple of $k \in \mathbb{Z}$, hence whose sum vanishes [[modulo]] $k$: $\sum_i n_i = 0 \,mod\, k$.

The [[cosets]] of this [[subgroup]] inclusion are clearly indexed by $C_k \equiv \mathbb{Z}/k$, and an element $(n_i)_{i=1}^k \,\in\,\mathbb{Z}^n$ belongs to the coset $r \,mod\, k$ if $\sum_i n_i = r \,mod\, k$. Hence we have a [[short exact sequence]] 

$$
  0 
    \to 
  \mathbb{Z}^n_{\sum = [0]_k}
    \longrightarrow
  \mathbb{Z}^n
    \xrightarrow{\sum \,\mathrm{mod}\, k}
  C_k
    \to 
  0
$$





(...)