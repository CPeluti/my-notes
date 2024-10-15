---
title: Conjuntos
publish: true
---

# Conjuntos

## Números Naturais
$\mathbb{N}=\{1,2,3,4,...\}$
$\mathbb{Z}=\{-2,-1,0,1,2,...\}$
$\mathbb{Q}=\{\frac{a}{b}/a,b \in \mathbb{Z}, b \neq 0\}$
 $\mathbb{N}  \subseteq \mathbb{Z} \subseteq \mathbb{Q}$

### Definição
Sejam $a,b \in \mathbb{Z}$. Diremos que "a divide b" se existir $c \in \mathbb{z}$ tal que $b = a.c$
#### Notação: a/b
#### Exemplo
15/45, pois $45 = 15*3$
7!/22 pois não existe $c \in \mathbb{Z}$ tal que $22=7*c$

As expressões "a divide b", "a é divisor de b", "b é múltiplo de a" representam o mesmo conceito.

## Lema (1)
Sejam $a,b,c \in \mathbb{Z}$. se $\frac{a}{b}$ e $\frac{b}{c}$ então $\frac{a}{c}$.
### Demonstração
Segue das hipóteses que :

$\frac{a}{b}$ então existe $m \in \mathbb{Z}$ tal que $b=a.m$
$\frac{b}{c}$ então existe $n \in \mathbb{Z}$ tal que $c=b.n$

logo

$c=b.n = (a.m).n = a.(m.n)$
como $m,n \in \mathbb{Z}$, o produto $m.n \in \mathbb{Z}$
portanto, $\frac{a}{c}$
$\square$
#### Demonstração utilizando [[Símbolos Lógicos]]
$$
\begin{aligned}
\frac{a}{b} \Rightarrow \exists m\in\mathbb{Z} tq b=m.a\\
\frac{b}{c} \Rightarrow \exists n\in\mathbb{Z} tq c=n.b
\end{aligned}
$$
Portanto
$$
c=a(m.n) \Rightarrow \frac{a}{c}
$$

## Lema (2)
Sejam $a,b,c \in \mathbb{Z}$. Se $\frac{a}{b}$ e $\frac{a}{c}$, então $\frac{a}{br+cs}$, para todo par $r,s\in\mathbb{Z}$
### Demonstração
temos que
$$
\begin{aligned}
\frac{a}{b} \Rightarrow \exists m\in\mathbb{Z}\text{ tq }b=a.m\\
\frac{a}{c} \Rightarrow \exists n\in\mathbb{Z} \text{ tq } c=a.n
\end{aligned}
$$
Agora
$$
br+cs = (am)r + (an)s = a(mr+ns)
$$
Logo
$$
\frac{a}{(br+cs)}
$$
$\square$

## Teorema (Algoritmo de Euclides)
Sejam $a,b \in \mathbb{N}$. Então existem únicos $q,r\in\mathbb{Z}$ tais que $a=bq+r$, com $0\leq r < b$
### Demonstração
#### (i) Existência
Se $a<b$ escreva $a=b.0+a, a\leq a<b$
Se $a \leq b$ escreva $a=b.1+0$
Vamos supor que $a>b$.
Considere o conjunto $M = \{a-bx|x\in \mathbb{Z}\} = \{...,a-2b,a-b,a,a+b,...\}$
Considere $M+=\{m\in M|m\geq0\} \subseteq \mathbb{N}\cup\{0\}$
Pelo #PBO, $\exists r \in M+ \text{ tq r é o menos elemento}$
Como $r\exists M+ \Rightarrow r \geq 0$, e como $r \in M$, $\exists q \in \mathbb{Z}$ tal que $r=a-bq$
Portanto $a = bq +r$ e $r\geq 0$
Vamos supor que $r \geq b$. Seja $r*=r-b\geq 0$
$$
r* = (a-bq)-b = a-b(q+1) \in M \Rightarrow r* \in M+
$$
Mas $r*=r-b<r$ um absurdo, pois r é o menor elemento de $M+$. Portanto, r<b.
#### (ii) Unicidade
Vamos supor que 
$$
a = bq +r\text{ e }a=bq*+r*,\text{ com }0\leq r, r*< b
\tag{*}
$$

Sem perda de generalidade (SPG) vamos supor que $r*\geq r \Rightarrow r*-r \geq 0$
Segue de (*) que
$b(q-q*) = r*-r \geq 0$

(1) supor $r* = r \Rightarrow b(q-q*) = 0 \Rightarrow q-q* = 0 \Rightarrow q=q*$ pois $b\in\mathbb{N}$
(2) supor $r* > r \Rightarrow 0<r*-r < b$
logo $0<b(q*-q) = r*-r <b$
Como isso é um absurdo, então $r=r*$ e $q=q*$
