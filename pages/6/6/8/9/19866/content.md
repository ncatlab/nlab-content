operator | sort | vars | type args | term args | scoping              | sugared syntax
---------|------|------|-----------|-----------|----------------------|--------------------
$\Pi$    | $ty$ | $x$  | $A$, $B$  |           | $B\lhd x$            | $\Pi(x:A).B$
$\lambda$| $tm$ | $x$  | $A$, $B$  | $M$       | $B\lhd x$, $M\lhd x$ | $\lambda(x:A.B).M$
$App$    | $tm$ | $x$  | $A$, $B$  | $M$, $N$  | $B\lhd x$            | $App^{(x:A).B}(M,N)$
