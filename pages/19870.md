$$
\frac{\Gamma \vdash A \, type \qquad \Gamma, x:A \vdash B\,type}{\Gamma \vdash \Pi(x:A) .B \, type}
$$

$$\,$$

$$
\frac{\Gamma \vdash A \, type \qquad \Gamma, x:A \vdash B\,type \qquad \Gamma \vdash M \Leftarrow \Pi(x:A). B \qquad \Gamma \vdash N \Leftarrow A}{\Gamma \vdash App^{x:A.B}(M,N) \Rightarrow B[N/x]}
$$

$$\,$$

$$
\frac{\Gamma \vdash A \, type \qquad \Gamma,x:A \vdash B \,type \qquad \Gamma,x:A \vdash M \Leftarrow B}{\Gamma \vdash \lambda(x:A.B).M \Rightarrow \Pi(x:A). B}
$$

$$\,$$

$$
\frac{\Gamma\vdash A \equiv A' \, type \qquad \Gamma, x:A \vdash B \equiv B' \, type}{\Gamma \vdash App^{x:A.B}(\lambda(x:A'.B').M,N) \equiv M[N/x] : B[N/x]}
$$

$$\,$$

$$
\frac{\Gamma, y:A \vdash App^{x:A.B}(M,y) \equiv App^{x:A.B}(M',y) : B[y/x]}{\Gamma \vdash M \equiv M' : \Pi(x:A).B }
$$

$$\,$$

$$
\frac{\Gamma \vdash A \equiv A' \qquad \Gamma, x:A \vdash B \equiv B'}{\Gamma \vdash \Pi(x:A)B \equiv \Pi(x:A')B'}
$$

$$\,$$

$$\frac{
   \Gamma \vdash A \equiv A' \qquad
   \Gamma, x:A \vdash B \equiv B' \qquad
   \Gamma, x:A \vdash M \equiv M' : B
}
{\Gamma \vdash \lambda(x:A.B).M \equiv \lambda(x:A'.B').M' : \Pi(x:A).B}
$$

$$\,$$

$$\frac{
   \Gamma \vdash A \equiv A'              \qquad
   \Gamma, x:A \vdash B \equiv B'         \qquad 
   \Gamma \vdash M \equiv M' : \Pi(x:A)B  \qquad 
   \Gamma \vdash N \equiv N' : A
}
{\Gamma \vdash App^{x:A.B}(M, N) \equiv App^{x:A'.B'}(M', N') : B[N/x]}
$$
