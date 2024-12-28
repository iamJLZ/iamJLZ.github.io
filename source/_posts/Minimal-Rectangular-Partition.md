---
title: Minimal Rectangular Partition
date: <%- date(Date.now()) %>
tags: Geometry
categories: Misc
---

# Introduction

This article is mainly based on L Ferrari, P.V Sankar and J SKlansky's paper[<a id="x1-1001"></a><a href="#cite.0@mrpdb">1</a>] but greatly simplified. In that paper they derive an algorithm that partitions finite four-connected subset of an infinite rectangular array(or "mosaic") $R$, $D$, into a minimum number of rectangular subregions whose edges are parallel to the coordinate axes of $R$.

# Definitions

Let $R$ denote a rectangular mosaic

**Definition 1.**
	*A **blob** on $R$ is a four-connected finite region in $R$.*

**Definition 2.**
	*Two concave vertices $V_1=(x_1,y_1)$ and $V_2=(x_2,y_2)$ on the boundary of a blob $B$ on $R$ are **cogrid** if $(x_1=x_2\lor y_1=y_2)\land (\overline{V_1V_2} \text{ is a chord of } B)$.*

**Definition 3.**
	*A **rectangular partition** of a blob $B$ is a partition $\{P_i\}_{i=1}^M$ such that $(\cup_iP_i = B)\land (P_i\cap P_j=\emptyset, i\ne j)\land (P_i \text{ is a rectangular for all } i)$. $M$ is defined as the *order* of the partition $\{P_i\}$.*

**Definition 4.**
	***Extension**. For each concave vertex, we select and extend to the blob's interior one of its edges. The extension will terminate at the digital blob's boundary or extension from another vertex.*

# Partition

We will talk about a digitized blob $B$ on rectangular mosaic $R$, with $H$ holes, and the set of its concave vertex is $C$, $|C|=N$. The maximum number of nonintersecting chords that can be drawn between cogrid vertices is $L$.

**Lemma 1.**
	If we draw $k$ extensions on blob $B$ and each concave vertex is an end of only one extension, Then the $k$ extensions partition $B$ into $k-H+1$ rectangulars.

This is obvious.

**Theorem 1.**
	$B$ has a minimum order rectangular partition of order $N-L+1-H$.

*proof.*
Let $P$ denote the order of minimum rectangular partition of $B$.Then 
	
$P\le N-L+1-H$. For a partition of $B$ consists of $L'$ nonintersecting chords, each concave vertex of $B$ is either an end of a nonintersecting chord or an extension. By Lemma 1. $B$ is partitioned into $P'=N-L'+1-H$ rectangulars. $P\le P'$, '=' holds when and only when $L'=L$.

$P\ge N-L+1-H$. Each concave vertex of $B$ is an end of at least one extension. By Lemma 1, we get $P\ge N-L+1-H$.

Then we get $P=N-L+1-H$.

# Algorithm

So the key is to find the maximum number of nonintersecting chords of $B$.

Let $V$ denote the set of chords between concave vertices of $B$. $E=\{(v_1,v_2)|v_1\text{ intersects with }v_2, v_1,v_2\in V, v_1\ne v_2\}$. Graph $G=<V,E>$ is a bipartite graph. Let $V_1\subset V$ be the set of cohorizontal chords of $B$, while $V_2=V\setminus V_1$ is the set of covertical chords of $B$. Then $G$ can be represented as $G=<V_1,E,V_2>$.

So the problem is to find the maximum independent set of bipartite graph $G$.



WIP

# Reference

<dl class="thebibliography"><dt id="X0-mrpdb" class="thebibliography">
[1]  </dt><dd id="bib-1" class="thebibliography">
    <!--l. 58--><p class="noindent"><a id="cite.0@mrpdb"></a>L Ferrari, P.V Sankar, and J Sklansky. “Minimal rectangular partitions of
    digitized blobs”. In: <span class="cmti-10">Computer Vision, Graphics, and Image Processing </span>28.1
    (1984), pp.&nbsp;58–71. <span class="cmcsc-10"><span class="small-caps">i</span><span class="small-caps">s</span><span class="small-caps">s</span><span class="small-caps">n</span></span>: 0734-189X. <span class="cmcsc-10"><span class="small-caps">d</span><span class="small-caps">o</span><span class="small-caps">i</span></span>: <a href="https://doi.org/https://doi.org/10.1016/0734-189X(84)90139-7">https://doi.org/10.1016/0734-189X(84)90139-7</a>.
    <span class="cmcsc-10"><span class="small-caps">u</span><span class="small-caps">r</span><span class="small-caps">l</span></span>: <a href="https://www.sciencedirect.com/science/article/pii/0734189X84901397" class="url"><span class="cmtt-10">https://www.sciencedirect.com/science/article/pii/0734189X84901397</span></a>
    (cit. on p.&nbsp; <a href="#x1-1001">1</a>).</p></dd></dl>