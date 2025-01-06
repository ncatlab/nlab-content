
### Braid groups as mapping class groups of [[punctured]] surfaces
 {#AsMappingClassGroupOfAPuncturedDisk}


The [[braid groups]] are equivalently given by [[mapping class groups]] of punctured [[surfaces]]. &lbrack;[Birman 1969](#Birman69)&rbrack;



#### For plain braid groups


The plan braid group $Br(n)$ may be alternatively described as the [[mapping class group]] of a [[2-disk]] $D^2$ with $n$ [[puncture|punctures]].  

(review includes [Birman 1975 §4](braid+group#Birman75), [González-Meneses 2011 §1.4](braid+group##González-Meneses11), [Massuyeau 2021 §3.3](braid+group##Massuyeau21), [Abadie 2022 §1.3](braid+group##Abadie22))

Concretely, consider 

1. $D^2 \setminus \{z_1, \cdots, z_n\}$ 

   denoting the [[complement]] of $n$ distinct points in the [[closed disk]] (with [[boundary]] the [[circle]]);

1. $Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)$ 

   denoting the [[mapping space]] of [[automorphism|auto]]-[[homeomorphisms]] which restrict to the [[identity]] on the [[boundary]] [[circle]], regarded with its canonical [[group]] [[structure]] under [[composition]];

1. $Homeo^{\partial}_id\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)$ 

   denoting the [[subgroup]] which is the [[connected component]] of the [[identity]] (which is readily seen to be a [[normal subgroup]]).

Then the [[mapping class group]] is the [[quotient group]]:

$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)
  \;\coloneqq\;
  Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
  \Big/
  Homeo^{\partial}_{id}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
  \,.
$$

Now observe that 

1. for the case that $n = 0$ this group is [[trivial group|trivial]], by *[[Alexander's trick]]*. 

1. continuous extension yields an [[injection]]

   $$
     Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
     \xhookrightarrow{\phantom{-}\iota\phantom{-}}
     Homeo^{\partial}\big(D^2\big)
     \,.
   $$

Combining this implies that for every $[\phi] \,\in\, MCG\big(D^2 \setminus \{z_1, \cdots, z_n\}\big)$ there is an [[isotopy]] to the [[identity]], $\iota[\phi] \to id$, under which the locations of the punctures trace out a [[braid]] (in the sense of a [[loop]] in the symmetrized [[configuration space of points]]). This construction constitutes a [[group homomorphism]] from the [[mapping class group]] to the [[braid group]]
$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)
  \xrightarrow{\;\;\sim\;\;}
  Br(n) 
  \,.
$$
and this is an [[isomorphism]].


\begin{remark}\label{ActionOfBraidGroupOnFundamentalGroupOfPuncturedDisk}
**(action of braid group on fundamental group of $n$-punctured disk)**
\linebreak
It follows in particular that the braid group $Br(n)$ has a canonical [[group action]] on the [[fundamental group]] of the $n$-punctured disk. Since the latter is [[isomorphism|isomorphic]] to the [[free group]] on $n$ [[generators and relations|generators]], this leads to the purely algebraic characterization of the braid group [below](#AsAutomorphismsOfAFreeGroup).

See also eg. [Margalit & Winarski (2021), §7](#MargalitWinarski21), [Amram, Lawrence & Vishne (2012), §7](#AmramLawrenceVishne12).
\end{remark}

#### For surface braid groups

More generally, let $\Sigma$ be a ([[connected topological space|connected]]) [[closed manifold|closed]], [[orientation|oriented]] [[surface]], possibly with [[boundary of a manifold|boundary]] and let $x_1, \cdots, x_n \in \Sigma$ a [[finite set]] of [[interior]] points.

Then the [[mapping class groups]] ($MCG(-) \coloneqq \pi_0 Homeo^{+,\partial}(-)$)

* $MCG(\Sigma)$ (of $\Sigma$ itself, presering orientation and the boundary pointwise)

* $MCG(\Sigma, \{x_1, \cdots, x_n\})$ (of $\Sigma$ with "indistinguishable" punctures)

* $MCG(\Sigma, \{x_1\}, \cdots, \{x_n\})$ (of $\Sigma$ with "distinguishable" punctures)

relate to the [[surface braid groups]]

* $Br_n(Sigma)$ (ordinary braid group)

* $PBr_n(Sigma)$ (pure braid group)

* $Sym_n$ (the [[symmetric group]])

by forming the following [[commuting diagram]] of [[group homomorphisms]] where all rows and all columns are [[exact sequences]]:

\begin{tikzcd}
  & 
  1 \ar[d]
  & 
  1 \ar[d]
  \\
  \pi_1\big(
    \mathrm{Homeo}^{+,\partial}(\Sigma)
  \big)
  \ar[r]
  \ar[d, equals]
  &
  \mathrm{PBr}_n(\Sigma)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(\Sigma, \{x_1\}, \cdots, \{x_n\}\big)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(\Sigma\big)
  \ar[r]
  \ar[d, equals]
  &
  1
  \\
  \pi_1\big(
    \mathrm{Homeo}^{+,\partial}(\Sigma)
  \big)
  \ar[r]
  &
  \mathrm{Br}_n(\Sigma)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(
    \Sigma, \{x_1, \cdots, x_n\}
  \big)
  \ar[r]
  \ar[d]
  & 
  \mathrm{MCG}(\Sigma)
  \ar[r]
  &
  1
  \\
  & \mathrm{Sym}_n 
  \ar[r, equals]
  & \mathrm{Sym}_n
  \\
  & 1 & 1
\end{tikzcd}


