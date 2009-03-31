#Idea#

The _IPC-property_ ("inductive limit product commutation property") is a technical condition on a [[category]] $A$ which ensures that [[presheaf|presheaves]] with values in $A$ have a good notion of [[sheafification]].

#Definition#

A [[category]] $A$ is said to satisfy the **IPC-property** if

* it admits small [[product]]s and [[filtered category|filtered]] [[colimit]]s;

* for 

  * every family $\{I_s\}_{s \in S}$ of [[small category|small]] [[filtered category|filtered]] categories 

  * and for any family $\{\alpha_s : I_s \to A\}$ of [[functor]]s

  * indexed by a [[Grothendieck universe|small set]] $S$ 

the canonical morphism

$$
  colim \left(
    \prod_s I_s \stackrel{k \mapsto \prod_s \alpha_s(\pi_s(j))}{\to} A
  \right)
  \to
  \prod_s colim \alpha_s
$$

is an [[isomorphism]].

#References#

The IPC property is definition 3.1.10 in 

* Kashiwara-Schapira, [[Categories and Sheaves]].

It is invoked for [[sheafification]] in section 17.4 there.