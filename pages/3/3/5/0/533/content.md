A _strict $n$-category_ is a [[strict omega-category]] all whose $k$-morphisms for $k \gt n$ are identities.

The category $n Cat$ of strict $n$-categories can inductively be defined by

* starting with setting $0 Cat :=$ [[Set]]; 

* noticing that [[Set]] is canonically a (symmetric) [[closed monoidal category]] such that one can consider [[enriched category|categories enriched]] over it;

* noticing that for $V$ any closed monoidal category also $V-Cat$ is closed monoidal;

* finally setting, recursively, 

  $$
    (n+1)Cat := n Cat-Cat
    \,.
  $$

