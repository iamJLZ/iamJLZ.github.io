---
title: Minimal Rectangular Partition
date: <%- date(Date.now()) %>
tags: Geometry
categories: Misc
mathjax: true
---

# Introduction

This article is mainly based on L Ferrari, P.V Sankar and J SKlansky's paper[<a id="x1-1001"></a><a href="#cite.0@mrpdb">1</a>]. In that paper they derive an algorithm that partitions finite four-connected subset of an infinite rectangular array(or "mosaic") $R$ into a minimum number of rectangular subregions whose edges are parallel to the coordinate axes of $R$.

# Definitions from Geometry

Let $R$ denote a rectangular mosaic

**definition 1.**
	*A **blob** on $R$ is a four-connected finite region in $R$.*

**definition 2.**
	*Two concave vertices $V_1=(x_1,y_1)$ and $V_2=(x_2,y_2)$ on the boundary of a blob $B$ on $R$ are **cogrid** if $(x_1=x_2\lor y_1=y_2)\land (\overline{V_1V_2} \text{ is a chord of } B)$.*

**definition 3.**
	*A **rectangular partition** of a blob $B$ is a partition $\{P_i\}_{i=1}^M$ such that $(\cup_iP_i = B)\land (P_i\cap P_j=\emptyset, i\ne j)\land (P_i \text{ is a rectangular for all } i)$. $M$ is defined as the *order* of the partition $\{P_i\}$.*

# Geometrical Properties of Digital Blobs

**lemma 1.**
	*For a blob on $R$ whose boundary contains $N$ noncogrid concave vertices and no cogrid concave vertices, there exists a minimum order rectangular partition of order $N+1$.*

*proof.*
	trival and skipped.

By convenience, $MP_B$ denote a minimum order rectangular partition of blob $B$, which partition $B$ into $|MP_B|$ rectangulars.

Let $C$ denote a set of nonintersecting chords connecting points on the boundary of a blob $B$. Let $|C'|=L'$, and $c'_i$ denote an element of $C', i=1, 2, \ldots, L'$.

Let $c$ denote a chord connecting two points on the boundary of $B$ such that $c$ and $C'$ share $b$ boundary points. Let $x$ denote the number of intersections of $c$ with $C'$. Then

**lemma 2.**
	*The set $C'$ and the chord $c$ partition $B$ into $L'+x+2-b$ regions.*

*proof.*
	trival and skipped.

**theorem 1.**
	$|MP_B|=N-L+1$. $N$ *is the total number of concave vertices on the boundary of $B$. $L$ is the maximum number of nonintersecting chords that can be drawn between cogrid concave vertices.*

WIP

# Reference

<dl class="thebibliography"><dt id="X0-mrpdb" class="thebibliography">
[1]  </dt><dd id="bib-1" class="thebibliography">
    <!--l. 58--><p class="noindent"><a id="cite.0@mrpdb"></a>L Ferrari, P.V Sankar, and J Sklansky. “Minimal rectangular partitions of
    digitized blobs”. In: <span class="cmti-10">Computer Vision, Graphics, and Image Processing </span>28.1
    (1984), pp.&nbsp;58–71. <span class="cmcsc-10"><span class="small-caps">i</span><span class="small-caps">s</span><span class="small-caps">s</span><span class="small-caps">n</span></span>: 0734-189X. <span class="cmcsc-10"><span class="small-caps">d</span><span class="small-caps">o</span><span class="small-caps">i</span></span>: <a href="https://doi.org/https://doi.org/10.1016/0734-189X(84)90139-7">https://doi.org/10.1016/0734-189X(84)90139-7</a>.
    <span class="cmcsc-10"><span class="small-caps">u</span><span class="small-caps">r</span><span class="small-caps">l</span></span>: <a href="https://www.sciencedirect.com/science/article/pii/0734189X84901397" class="url"><span class="cmtt-10">https://www.sciencedirect.com/science/article/pii/0734189X84901397</span></a>
    (cit. on p.&nbsp; <a href="#x1-1001">1</a>).</p></dd></dl>