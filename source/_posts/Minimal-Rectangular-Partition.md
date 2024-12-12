---
title: Minimal Rectangular Partition
date: <%- date(Date.now()) %>
tags: Geometry
categories: Misc
---

   <h3 class="sectionHead"><span class="titlemark">1   </span> <a id="x1-10001"></a>Introduction</h3>
<!--l. 13--><p class="noindent">This article is mainly based on L Ferrari, P.V Sankar and J SKlansky’s paper[<a id="x1-1001"></a><a href="#cite.0@mrpdb">1</a>]. In
that paper they derive an algorithm that partitions finite four-connected subset of
an infinite rectangular array(or ”mosaic”) R into a minimum number of
rectangular subregions whose edges are parallel to the coordinate axes of
R.
<!--l. 15--></p><p class="noindent">
   </p><h3 class="sectionHead"><span class="titlemark">2   </span> <a id="x1-20002"></a>Definitions from Geometry</h3>
<!--l. 17--><p class="noindent">Let <span class="cmmi-10">R </span>denote a rectangular mosaic
   </p><div class="newtheorem">
<!--l. 19--><p class="noindent"><span class="head">
<a id="x1-2001r1"></a>
<span class="cmbx-10">Definition 1.</span>  </span><span class="cmti-10">A </span><span class="cmbxti-10">blob </span><span class="cmti-10">on R is a four-connected finite region in R.</span>
   </p></div>
<!--l. 21--><p class="indent">
   </p><div class="newtheorem">
<!--l. 22--><p class="noindent"><span class="head">
<a id="x1-2002r2"></a>
<span class="cmbx-10">Definition 2.</span>  </span><span class="cmti-10">Two  concave  vertices  </span><span class="cmmi-10">V</span> <sub><span class="cmr-7">1</span></sub>  =  (<span class="cmmi-10">x</span><sub><span class="cmr-7">1</span></sub><span class="cmmi-10">,y</span><sub><span class="cmr-7">1</span></sub>)  <span class="cmti-10">and  </span><span class="cmmi-10">V</span> <sub><span class="cmr-7">2</span></sub>  =  (<span class="cmmi-10">x</span><sub><span class="cmr-7">2</span></sub><span class="cmmi-10">,y</span><sub><span class="cmr-7">2</span></sub>)  <span class="cmti-10">on</span>
<span class="cmti-10">the  boundary  of  a  blob  </span><span class="cmmi-10">B  </span><span class="cmti-10">on  </span><span class="cmmi-10">R  </span><span class="cmti-10">are  </span><span class="cmbxti-10">cogrid </span><span class="cmti-10">if  </span>(<span class="cmmi-10">x</span><sub><span class="cmr-7">1</span></sub>   =  <span class="cmmi-10">x</span><sub><span class="cmr-7">2</span></sub>  <span class="cmsy-10">∨ </span><span class="cmmi-10">y</span><sub><span class="cmr-7">1</span></sub>   =  <span class="cmmi-10">y</span><sub><span class="cmr-7">2</span></sub>) <span class="cmsy-10">∧</span>
(<span class="overline"><span class="cmmi-10">V</span> <sub><span class="cmr-7">1</span></sub><span class="cmmi-10">V</span> <sub><span class="cmr-7">2</span></sub></span> <span class="cmti-10">is a chord of</span> <span class="cmmi-10">B</span>)<span class="cmti-10">.</span>
   </p></div>
<!--l. 24--><p class="indent">
   </p><div class="newtheorem">
<!--l. 25--><p class="noindent"><span class="head">
<a id="x1-2003r3"></a>
<span class="cmbx-10">Definition 3.</span>  </span><span class="cmti-10">A </span><span class="cmbxti-10">rectangular partition </span><span class="cmti-10">of a blob </span><span class="cmmi-10">B </span><span class="cmti-10">is a partition </span><span class="cmsy-10">{</span><span class="cmmi-10">P</span><sub><span class="cmmi-7">i</span></sub><span class="cmsy-10">}</span><sub><span class="cmmi-7">i</span><span class="cmr-7">=1</span></sub><sup><span class="cmmi-7">M</span></sup>
<span class="cmti-10">such that </span>(<span class="cmsy-10">∪</span><sub><span class="cmmi-7">i</span></sub><span class="cmmi-10">P</span><sub><span class="cmmi-7">i</span></sub> = <span class="cmmi-10">B</span>) <span class="cmsy-10">∧ </span>(<span class="cmmi-10">P</span><sub><span class="cmmi-7">i</span></sub> <span class="cmsy-10">∩ </span><span class="cmmi-10">P</span><sub><span class="cmmi-7">j</span></sub> = <span class="cmsy-10">∅</span><span class="cmmi-10">,i</span><span class="cmmi-10">≠</span><span class="cmmi-10">j</span>) <span class="cmsy-10">∧ </span>(<span class="cmmi-10">P</span><sub><span class="cmmi-7">i</span></sub> <span class="cmti-10">is a rectangular for all</span> <span class="cmmi-10">i</span>)<span class="cmti-10">. </span><span class="cmmi-10">M</span>
<span class="cmti-10">is defined as the order of the partition </span><span class="cmsy-10">{</span><span class="cmmi-10">P</span><sub><span class="cmmi-7">i</span></sub><span class="cmsy-10">}</span><span class="cmti-10">.</span>
   </p></div>
<!--l. 27--><p class="indent">
                                                                  

                                                                  
<!--l. 29--></p><p class="noindent">
   </p><h3 class="sectionHead"><span class="titlemark">3   </span> <a id="x1-30003"></a>Geometrical Properties of Digital Blobs</h3>
   <div class="newtheorem">
<!--l. 31--><p class="noindent"><span class="head">
<a id="x1-3001r1"></a>
<span class="cmbx-10">Lemma 1.</span>  </span><span class="cmti-10">For a blob on R whose boundary contains </span><span class="cmmi-10">N  </span><span class="cmti-10">noncogrid concave</span>
<span class="cmti-10">vertices and no cogrid concave vertices, there exists a minimum order rectangular</span>
<span class="cmti-10">partition of order </span><span class="cmmi-10">N </span>+ 1<span class="cmti-10">.</span>
   </p></div>
<!--l. 33--><p class="indent">
   </p><div class="proof">
<!--l. 35--><p class="indent">   <span class="head">
<span class="cmti-10">Proof.</span> </span>trival and skipped.                                                                   __
   </p></div>
<!--l. 38--><p class="noindent">By convenience, <span class="cmmi-10">MP</span><sub><span class="cmmi-7">B</span></sub> denote a minimum order rectangular partition of blob <span class="cmmi-10">B</span>,
which partition <span class="cmmi-10">B </span>into <span class="cmsy-10">|</span><span class="cmmi-10">MP</span><sub><span class="cmmi-7">B</span></sub><span class="cmsy-10">| </span>rectangulars.
<!--l. 40--></p><p class="indent">   Let <span class="cmmi-10">C </span>denote a set of nonintersecting chords connecting points on the boundary
of a blob <span class="cmmi-10">B</span>. Let <span class="cmsy-10">|</span><span class="cmmi-10">C</span><span class="cmsy-10">′| </span>= <span class="cmmi-10">L</span><span class="cmsy-10">′</span>, and <span class="cmmi-10">c</span><span class="cmsy-10">′</span><sub><span class="cmmi-7">i</span></sub> denote an element of <span class="cmmi-10">C</span><span class="cmsy-10">′</span><span class="cmmi-10">,i </span>= 1<span class="cmmi-10">,</span>2<span class="cmmi-10">,</span><span class="cmmi-10">…</span><span class="cmmi-10">,L</span><span class="cmsy-10">′</span>.
<!--l. 42--></p><p class="indent">   Let <span class="cmmi-10">c </span>denote a chord connecting two points on the boundary of <span class="cmmi-10">B </span>such that <span class="cmmi-10">c </span>and
<span class="cmmi-10">C</span><span class="cmsy-10">′ </span>share <span class="cmmi-10">b </span>boundary points. Let <span class="cmmi-10">x </span>denote the number of intersections of <span class="cmmi-10">c </span>with <span class="cmmi-10">C</span><span class="cmsy-10">′</span>.
Then
   </p><div class="newtheorem">
<!--l. 44--><p class="noindent"><span class="head">
<a id="x1-3002r2"></a>
<span class="cmbx-10">Lemma 2.</span>  </span><span class="cmti-10">The set </span><span class="cmmi-10">C</span><span class="cmsy-10">′ </span><span class="cmti-10">and the chord </span><span class="cmmi-10">c </span><span class="cmti-10">partition </span><span class="cmmi-10">B </span><span class="cmti-10">into </span><span class="cmmi-10">L</span><span class="cmsy-10">′ </span>+ <span class="cmmi-10">x </span>+ 2 <span class="cmsy-10">- </span><span class="cmmi-10">b </span><span class="cmti-10">regions.</span>
   </p></div>
<!--l. 46--><p class="indent">
   </p><div class="proof">
<!--l. 48--><p class="indent">   <span class="head">
<span class="cmti-10">Proof.</span> </span>trival and skipped.                                                                   __
   </p></div>
   <div class="newtheorem">
<!--l. 51--><p class="noindent"><span class="head">
<a id="x1-3003r1"></a>
                                                                  

                                                                  
<span class="cmbx-10">Theorem 1.</span>  </span><span class="cmsy-10">|</span><span class="cmmi-10">MP</span><sub><span class="cmmi-7">B</span></sub><span class="cmsy-10">| </span>= <span class="cmmi-10">N </span><span class="cmsy-10">- </span><span class="cmmi-10">L </span>+ 1<span class="cmti-10">. </span><span class="cmmi-10">N </span><span class="cmti-10">is the total number of concave vertices</span>
<span class="cmti-10">on the boundary of </span><span class="cmmi-10">B</span><span class="cmti-10">. </span><span class="cmmi-10">L </span><span class="cmti-10">is the maximum number of nonintersecting chords that</span>
<span class="cmti-10">can be drawn between cogrid concave vertices.</span>
   </p></div>
<!--l. 53--><p class="indent">
<!--l. 55--></p><p class="indent">   WIP
<!--l. 58--></p><p class="noindent">
   </p><h3 class="sectionHead"><a id="x1-4000"></a>References</h3>
<!--l. 58--><p class="noindent">
    </p><dl class="thebibliography"><dt id="X0-mrpdb" class="thebibliography">
[1]  </dt><dd id="bib-1" class="thebibliography">
    <!--l. 58--><p class="noindent"><a id="cite.0@mrpdb"></a>L Ferrari, P.V Sankar, and J Sklansky. “Minimal rectangular partitions of
    digitized blobs”. In: <span class="cmti-10">Computer Vision, Graphics, and Image Processing </span>28.1
    (1984), pp.&nbsp;58–71. <span class="cmcsc-10"><span class="small-caps">i</span><span class="small-caps">s</span><span class="small-caps">s</span><span class="small-caps">n</span></span>: 0734-189X. <span class="cmcsc-10"><span class="small-caps">d</span><span class="small-caps">o</span><span class="small-caps">i</span></span>: <a href="https://doi.org/https://doi.org/10.1016/0734-189X(84)90139-7">https://doi.org/10.1016/0734-189X(84)90139-7</a>.
    <span class="cmcsc-10"><span class="small-caps">u</span><span class="small-caps">r</span><span class="small-caps">l</span></span>: <a href="https://www.sciencedirect.com/science/article/pii/0734189X84901397" class="url"><span class="cmtt-10">https://www.sciencedirect.com/science/article/pii/0734189X84901397</span></a>
    (cit. on p.&nbsp; <a href="#x1-1001">1</a>).</p></dd></dl>