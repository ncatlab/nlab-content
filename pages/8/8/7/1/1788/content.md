
$D^{\triangledown}$

```coq
CoInductive conat : Set :=
| cozero : conat
| cosuc : conat -> conat.

CoFixpoint omega: conat := cosucc omega.
```