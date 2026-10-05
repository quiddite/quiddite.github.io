---
title: Some frequently used  constructions (functors) and tools in AT
date: 2025-05-25 23:40:27
tags: at
categories: math
# mathjax: true
# katex: true
---
### spaces

##### &sect; concerning groups

<details>
<summary>Moore space $M(G,n)$</summary>
<ul>

- definition
    $M(G,n):=$the CW complex with $H_i(-)=\left.\begin{cases}
        0&,i\neq n\\
        G&,i=n
    \end{cases}\right.$, we may also assume $\pi_1(-)=0$ if $n>0$.
- basic results
- applications
<!-- 
- definition
- basic results
- applications -->
</ul>
</details>

<details>
<summary>EM space $K(G,n)$</summary>
<ul>

- definition
    $K(G,n):=$the CW complex with $\pi_i(-)=\left.\begin{cases}
        0&,i\neq n\\
        G&,i=n
    \end{cases}\right.$.
- basic results
  - unique up to (weak) homotopy equivalence;
  - product: $K(G,n)\times K(H,n)\simeq K(G\times H,n)$
  - representation results: Let $G$ be an Ab-grp, $X$ a CW complex, then $$\langle{X,K(G,n)}\rangle\leftrightarrow H^n(X;G),[f]\mapsto f^*\alpha$$ where $\alpha\in H^n(K;G))=Hom(H_n(K),G)$ is given by the inverse of Hurewitz isomorphism $G\to H_n(K)$.
  - cohomology: $H^*(K(\mathbb{Z},n);\mathbb{Q})=\left.\begin{cases}
    \mathbb{Q}[x_n]&,n\text{ is even}\\
    \mathbb{Q}[x_n]/(x_n^2)&,n\text{ is odd}
  \end{cases}\right.$, using SSS with loopspace fibration, see page 11 of [AT-all](https://quiddite.github.io/files/AT-all.pdf "page 11").

- applications
  - motivations of (complex) universal bundles: $K(\mathbb{Z},1)=S^1,K(\mathbb{Z}/2,1)=\mathbb{R}\mathbb{P}^\infty,K(\mathbb{Z},2)=\mathbb{C}\mathbb{P}^\infty$.
  - (co)homology of groups: $H^n(G)=H^n(K(G,n))$
</ul>
</details>

<details>
<summary>classifying space $BG$</summary>
<ul>

- definition
	- $BG$ is the CW complex such that there is a principle $G$-bundle $EG\to BG$, with $EG$ weakly contractible
	- construction (Milnor): for a topo-grp $G$, there is a accenting chain via topological join: $$G\subset G^{\star 2}\subset \cdots \subset G^{\star n}\cdots$$ Let $EG=\cup G^{\star n}$, $BG=EG /G$.

- basic results
	- uniqueness up to homotopy equivalence
	- bijection: $[B,BG]\leftrightarrow Bun_{G}(B)=\left.\begin{cases}\text{principal } G-\\\text{bundles over B}\end{cases}\right\} /\cong$

- applications 
</ul>
</details>

<details>
<summary>Postnikov Towers</summary>
<ul>
</ul>
</details>

##### &sect; (direct) constructions


<details>
<summary>connected sum $\cdot \#\cdot$</summary>
<ul>
</ul>
</details>

<details>
<summary>topological join $\cdot \star\cdot$</summary>
<ul>

- definition
    $M\star N=M\times[0,1]\times N/\sim$, where $(x,0,y_1)\sim(x,0,y_2),(x_1,1,y)\sim(x_2,1,y)$

- basic results
  - if $M$ is $m$-connented, $N$ is $n$-connected, then $M\star N$ is $(m+n+2)$-connected.
  - $S^0\star S^0=S^1,\, S^m\star S^n=S^{m+n+1}$.
  - $M^{\star n}$ is always $(n-2)$-connected.
  
- applications
  - Milnor's construction of classifying space:
    $EG=\cup G^{\star n},\,BG=EG/G$
</ul>
</details>

<details>
<summary>suspension $\Sigma X$</summary>
<ul>
</ul>
</details>


<details>
<summary>wedge sum $\cdot \vee\cdot$</summary>
<ul>
</ul>
</details>


<details>
<summary>smash product $\cdot\wedge\cdot$</summary>
<ul>
</ul>
</details>

<details>
<summary>path space $PX$</summary>
<ul>
</ul>
</details>

<details>
<summary>loop space $\Omega X$</summary>
<ul>
</ul>
</details>



<details>
<summary>Thom space $TE$</summary>
<ul>
</ul>
</details>


<details>
<summary>Configuration space $\mathrm{Conf}_nX$</summary>
<ul>
</ul>
</details>


<details>
<summary>Čech nerve</summary>
<ul>
</ul>
</details>


##### &sect; concerning mappings

<details>
<summary>mapping cylinder</summary>
<ul>
</ul>
</details>

<details>
<summary>mapping cone $Cf$</summary>
<ul>
</ul>
</details>


<details>
<summary>mapping torus</summary>
<ul>
</ul>
</details>


<details>
<summary>lens space $S^-/\mathbb{Z}_\bullet$</summary>
<ul>
</ul>
</details>


<details>
<summary>Hopf torus</summary>
<ul>
</ul>
</details>

### tools

- fiber bundle
- Gysin sequence
- Leray-Hirsch
- Thom class
- Steenrod square


<!-- 
<details>
  <summary>Click to reveal more details</summary>
  <p>This is the hidden content.</p>
</details> -->
