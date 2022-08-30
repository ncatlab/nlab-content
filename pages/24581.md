{ ----------------------------- pseudoterms ------------------------------1-- }

pterm : TYPE := PRIM

{ ----------------------------- judgements -------------------------------4-- }

* [A:pterm] type : TYPE := PRIM
* [A:pterm][B:pterm] eq_type : TYPE := PRIM
* [a:pterm][A:pterm] in : TYPE := PRIM
* [a:pterm][b:pterm][A:pterm] eq_in : TYPE := PRIM

{ ----------------------------- equality rules ---------------------------8-- }

* [A:pterm][a:pterm][b:pterm][c:pterm]
A * [B:pterm][C:pterm]

A * [_1:type(A)] refl_type : eq_type(A,A) := PRIM
B * [_1:eq_type(A,B)] sym_type : eq_type(B,A) := PRIM
C * [_1:eq_type(A,B)][_2:eq_type(B,C)] trans_type : eq_type(A,C) := PRIM
a * [_1:in(a,A)] refl : eq_in(a,a,A) := PRIM
b * [_1:eq_in(a,b,A)] sym : eq_in(b,a,A) := PRIM
c * [_1:eq_in(a,b,A)][_2:eq_in(b,c,A)] trans : eq_in(a,c,A) := PRIM

B * [a:pterm][_1:in(a,A)][_2:eq_type(A,B)] conv_in : in(a,B) := PRIM
a * [b:pterm][_1:eq_in(a,b,A)][_2:eq_type(A,B)]
  conv_eq_in : eq_in(a,b,B) := PRIM

{ ----------------------------- congruence rules -------------------------2-- }

* [A:pterm][a:pterm][b:pterm][C:[x,pterm]pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>C)][_3:eq_in(a,b,A)]
  cong_type : eq_type(<a>C,<b>C) := PRIM
C * [c:[x,pterm]pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]in(<x>c,<x>C)][_3:eq_in(a,b,A)]
  cong : eq_in(<a>c,<b>c,<a>C) := PRIM

{ ----------------------------- the empty type ---------------------------4-- }

* '0' : pterm := PRIM
* [a:pterm] R_0 : pterm := PRIM

* '0'_form : type('0') := PRIM
a * [C:[x,pterm]pterm]
  [_1:[x,pterm][_,in(x,'0')]type(<x>C)][_2:in(a,'0')]
  '0'_elim : in(R_0(a),<a>C) := PRIM

{ ----------------------------- the unit type ----------------------------7-- }

* '1' : pterm := PRIM
* star : pterm := PRIM
* [c:pterm][a:pterm] R_1 : pterm := PRIM

* '1'_form : type('1') := PRIM
* '1'_intro : in(star,'1') := PRIM
a * [C:[x,pterm]pterm]
  [_1:[x,pterm][_,in(x,'1')]type(<x>C)][_2:in(a,'1')][_3:in(c,<star>C)]
  '1'_elim : in(R_1(c,a),<a>C) := PRIM
c * [C:[x,pterm]pterm]
  [_1:[x,pterm][_,in(x,'1')]type(<x>C)][_2:in(c,<star>C)]
  '1'_eq : eq_in(R_1(c,star),c,<star>C) := PRIM

{ ----------------------------- the Booleans ----------------------------13-- }

* '2' : pterm := PRIM
* 1 : pterm := PRIM
* 2 : pterm := PRIM
* [c:pterm][d:pterm][a:pterm] R_2 : pterm := PRIM

* '2'_form : type('2') := PRIM
* '2'_intro_1 : in(1,'2') := PRIM
* '2'_intro_2 : in(2,'2') := PRIM
a * [C:[x,pterm]pterm]
  [_1:[x,pterm][_,in(x,'2')]type(<x>C)][_2:in(a,'2')]
  [_3:in(c,<1>C)][_4:in(d,<2>C)]
  '2'_elim : in(R_2(c,d,a),<a>C) := PRIM
d * [C:[x,pterm]pterm]
  [_1:[x,pterm][_,in(x,'2')]type(<x>C)][_2:in(c,<1>C)][_3:in(d,<2>C)]
  '2'_eq_1 : eq_in(R_2(c,d,1),c,<1>C) := PRIM
  '2'_eq_2 : eq_in(R_2(c,d,2),d,<2>C) := PRIM

* [A:pterm][B:pterm][c:pterm][_1:type(A)][_2:type(B)][_3:in(c,'2')]
  '2'_elim_type : type(R_2(A,B,c)) := PRIM
B * [_1:type(A)][_2:type(B)]
  '2'_eq_type_1 : eq_type(R_2(A,B,1),A) := PRIM
  '2'_eq_type_2 : eq_type(R_2(A,B,2),B) := PRIM

{ ----------------------------- product types ----------------------------9-- }

* [A:pterm][B:[x,pterm]pterm] Pi : pterm := PRIM
A * [B':pterm] arrow : pterm := Pi(A,[x,pterm]B')
A * [b:[x,pterm]pterm] lambda : pterm := PRIM
* [f:pterm][a:pterm] app : pterm := PRIM

B * [C:[x,pterm]pterm][_1:type(A)][_2:[x,pterm][_,in(x,A)]eq_type(<x>B,<x>C)]
  Pi_cong : eq_type(Pi(A,B),Pi(A,C)) := PRIM
B * [b:[x,pterm]pterm][c:[x,pterm]pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]eq_in(<x>b,<x>c,<x>B)]
  lambda_cong : eq_in(lambda(A,b),lambda(A,c),Pi(A,B)) := PRIM

B * [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)]
  Pi_form : type(Pi(A,B)) := PRIM
B * [b:[x,pterm]pterm][_1:type(A)][_2:[x,pterm][_,in(x,A)]in(<x>b,<x>B)]
  Pi_intro : in(lambda(A,b),Pi(A,B)) := PRIM
B * [a:pterm][f:pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)][_3:in(f,Pi(A,B))][_4:in(a,A)]
  Pi_elim : in(app(f,a),<a>B) := PRIM
a * [b:[x,pterm]pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]in(<x>b,<x>B)][_3:in(a,A)]
  Pi_eq {beta} : eq_in(app(lambda(A,b),a),<a>b,<a>B) := PRIM

{ ----------------------------- sum types -------------------------------11-- }

* [A:pterm][B:[x,pterm]pterm] Sigma : pterm := PRIM
* [a:pterm][b:pterm] pair : pterm := PRIM
a * pi_1 : pterm := PRIM
a * pi_2 : pterm := PRIM

B * [C:[x,pterm]pterm][_1:type(A)][_2:[x,pterm][_,in(x,A)]eq_type(<x>B,<x>C)]
  Sigma_cong : eq_type(Sigma(A,B),Sigma(A,C)) := PRIM

B * [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)]
  Sigma_form : type(Sigma(A,B)) := PRIM
B * [a:pterm][b:pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)][_3:in(a,A)][_4:in(b,<a>B)]
  Sigma_intro : in(pair(a,b),Sigma(A,B)) := PRIM
B * [c:pterm][_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)]
  [_3:in(c,Sigma(A,B))]
  Sigma_elim_1 : in(pi_1(c),A) := PRIM
  Sigma_elim_2 : in(pi_2(c),<pi_1(c)>B) := PRIM
b * [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)][_3:in(a,A)][_4:in(b,<a>B)]
  Sigma_eq_1 : eq_in(pi_1(pair(a,b)),a,A) := PRIM
  Sigma_eq_2 : eq_in(pi_2(pair(a,b)),b,<a>B) := PRIM

{ ----------------------------- W types ----------------------------------8-- }

* [A:pterm][B:[x,pterm]pterm] W : pterm := PRIM
* [a:pterm][f:pterm] sup : pterm := PRIM
* [b:pterm][e:pterm] rec : pterm := PRIM

B * [C:[x,pterm]pterm][_1:type(A)][_2:[x,pterm][_,in(x,A)]eq_type(<x>B,<x>C)]
  W_cong : eq_type(W(A,B),W(A,C)) := PRIM

B * [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)]
  W_form : type(W(A,B)) := PRIM
B * [a,pterm][f:pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)][_3:in(a,A)]
  [_4:in(f,arrow(<a>B,W(A,B)))]
  W_intro : in(sup(a,f),W(A,B)) := PRIM
B * [C:[z,pterm]pterm]
    [x:pterm][u:pterm]
    D : pterm := arrow(Pi(<x>B,[y,pterm]<app(u,y)>C),<sup(x,u)>C)
C * [b:pterm][e:pterm]
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)]
  [_3:[z,pterm][_,in(z,W)]type(<z>C)]
  [_4:in(b,Pi(A,[x,pterm]Pi(arrow(<x>B,W),[u,pterm]D(x,u))))][_5:in(e,W)]
  W_elim : in(rec(b,e),<e>C) := PRIM
b * [a:pterm][f:pterm]
    g : pterm := lambda(<a>B,[y,pterm]rec(b,app(f,y)))
  [_1:type(A)][_2:[x,pterm][_,in(x,A)]type(<x>B)]
  [_3:[z,pterm][_,in(z,W)]type(<z>C)]
  [_4:in(b,Pi(A,[x,pterm]Pi(arrow(<x>B,W),[u,pterm]D(x,u))))]
  [_5:in(a,A)][_6:in(f,arrow(<a>B,W))]
  W_eq : eq_in(rec(b,sup(a,f)),app(app(app(b,a),f),g),<sup(a,f)>C) := PRIM

{ ----------------------------- extensionality --------------------------10-- }

* [A:pterm][a:pterm][b:pterm] Eq : pterm := PRIM
b * [_1:type(A)][_2:in(a,A)][_3:in(b,A)] Eq_form : type(Eq(A,a,b)) := PRIM
b * [_1:eq_in(a,b,A)] Eq_intro : in(star,Eq(A,a,b)) := PRIM
b * [c:pterm][_1:in(c,Eq(A,a,b))] Eq_elim : eq_in(a,b,A) := PRIM
  Eq_eq : eq_in(c,star,Eq(A,a,b)) := PRIM

A * [B:pterm] EQ : pterm := PRIM
B * [_1:type(A)][_2:type(B)] EQ_form : type(EQ(A,B)) := PRIM
B * [_1:eq_type(A,B)] EQ_intro : in(star,EQ(A,B)) := PRIM
B * [c:pterm][_1:in(c,EQ(A,B))] EQ_elim : eq_type(A,B) := PRIM
  EQ_eq : eq_in(c,star,EQ(A,B)) := PRIM
