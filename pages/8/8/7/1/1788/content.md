
$D^{\triangledown}$

```coq
CoInductive conat : Set :=
| cozero : conat
| cosuc : conat -> conat.

CoFixpoint omega: conat := cosucc omega.
```

\[
x = y \quad\text{Some text $X$ with math in it}
\]