---
marp: true
author: Man Hin Tsang
header: '![width:70px height: 70px](../img//cuhk-logo.png) 香港中文大學<br>The Chinese University of Hong Kong'
footer: '30 June, 2022 - Tsang Man Hin - <a href="http://sfg.phy.cuhk.edu.hk/group_page/">SFG@CUHK</a>'
theme: gaia
math: katex
header-includes:
   - \usepackage{bbm}
paginate: true
style: |
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    * {
        color: rgba(255, 255, 255, 0.9) !important;
        font-weight: 100;
        padding: 0;
        margin: 0 !important;
        box-sizing: border-box !important;
    }
    :root {
        background-image: url("../img/background.jpg");
        background-size: contain;
        padding: 3rem;
        cursor: url("../img/star-mod.svg") 25 25,
                url("../img/star-mod.svg") 25 25,
                auto !important;
        z-index: -9999;
    }
    header {
        font-weight: 100;
        font-size: 0.5rem;
        padding-left: 1.4rem;
        display:flex;
        height: 3rem;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        letter-spacing: 1px;
        line-height: 1;
    }
    footer {
        display:flex;
        flex-direction: row;
        width: 100%;
        font-weight: 100;
        padding-left: 1.4rem;
        font-size: 0.4rem;
    }
    footer > a{
        font-size: 0.4rem;
    }
    header > img{
        filter: drop-shadow(0px 0px 0.01px #fff);
    }
    h1 {
        font-size: 1.3rem !important;
    }
    h2 {
        font-size: 1.2rem !important;
    } 
    h3 {
        font-size: 1.1rem !important;
    }
    h4 {
        font-size: 1.3rem !important;
    }
    h5 {
        font-size: 1.2rem !important;
    } 
    h6 {
        font-size: 1.1rem !important;
    }
    h1, h2, h3 {
        text-align: center;
        letter-spacing: 0.01rem;
    }
    h4, h5, h6 {
        letter-spacing: 0.01rem;
    }
    small {
        font-size: 0.5rem !important;
    }
    sup {
        font-size: 0.5em !important;
        display: inline;
    }
    p {
        font-size: 1rem !important;
    }
    a {
        text-decoration: none;
        font-size: 1rem;
        color: rgba(255, 255, 255, 0.7);
    }
    header, footer {
        font-family: 'Noto Sans', sans-serif;
        font-weight: 100;
        letter-spacing: 0em; 
    }
    h1, h2, h3, h4, h5, h6, small, sup, p, a, figcaption, label, ul {
        font-family: 'Noto Sans', sans-serif;
        font-weight: 100;
        letter-spacing: 0em; 
        position: relative;
        display: block;
        width: fit-content;
        transition-duration: 200ms;
    }
    sup {
        display: inline-block!important;
    }
    h1:hover, h2:hover, h3:hover,
    h4:hover, h5:hover, h6:hover,
    sup:hover, p:hover, li:hover,
    small:hover, figcaption:hover {
        color: rgba(255, 255, 255, 1);
        text-shadow: 0 0 rgba(255, 255, 255, 1);
    }
    h1::before, h2::before, h3::before,
    h4::before, h5::before, h6::before, p::before, label::before  {
        position: absolute;
        top: 0;
        left: 0;
        content: '\00a0';
        width: 0rem;
        height: 0.05rem;
        border-radius: 1000px;
        background-color: rgba(255,255,255,0.8);
        transition-duration: 500ms;
    }
    h1:hover::before, h2:hover::before, h3:hover::before,
    h4:hover::before, h5:hover::before, h6:hover::before, p:hover::before, label:hover::before  {
        width: 100%;
        transform: translateX(2000px);
    }
    h1::after, h2::after, h3::after,
    h4::after, h5::after, h6::after, p::after, label:after {
        position: absolute;
        bottom: 0;
        left: 2000px;
        content: '\00a0';
        width: 0rem;
        height: 0.05rem;
        border-radius: 1000px;
        background-color: rgba(255,255,255,0.9);
        transition-duration: 500ms;
    }
    h1:hover::after, h2:hover::after, h3:hover::after,
    h4:hover::after, h5:hover::after, h6:hover::after, p:hover::after, label:hover::after  {
        width: 100%;
        left: 0;
    }
    .row {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .row-sub {
        width: 40%;
        display: flex;
        justify-content: space-between;
    }
    .center-page {
        padding-top: 100px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    section::after { 
        color: rgba(255, 255, 255, 0.8); 
        font-weight: 100; 
        display: flex !important;
        flex-direction: columne;
        font-family: 'Noto Sans', sans-serif;
        text-shadow: 0 0 rgba(0, 0, 0, 1);
        font-size: 0.4em; 
        content: attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
    }
    left {
        justify-self: start;
    }
    #img-center {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        z-index: -100;
    }
    #canvas {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: -999;
    }
    #canvas .circle {
        position: absolute;
        opacity: 0;
        width: 10px;
        height: 10px;
        z-index: -999;
    }
    .star {
        position: relative;
        left: 0;
        right: 0;
        background-color: rgba(255, 255, 255, 1);
        width: 10px !important;
        height: 10px !important;
        border-radius: 100px;
    }
    @keyframes radial {
        0% {
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        20% {
            opacity: 0.5;
            width: 2000px;
            height: 2000px;
        }
        100% {
            opacity: 1;
            width: 2000px;
            height: 2000px;
        }
    }
    #c1{
        transform: rotate(0deg) !important;
        animation: radial 5000ms ease-in 100ms infinite;
        animation-fill-mode: forwards;
    }
    #c2{
        transform: rotate(40deg) !important;
        animation-delay: 2s;
        animation: radial 5000ms ease-in 500ms infinite;
        animation-fill-mode: forwards;
    }
    #c3{
        transform: rotate(70deg) !important;
        animation-delay: 2s;
        animation: radial 5000ms ease-in 1500ms infinite;
        animation-fill-mode: forwards;
    }
    #c4{
        transform: rotate(200deg) !important;
        animation-delay: 2s;
        animation: radial 5000ms ease-in 7500ms infinite;
        animation-fill-mode: forwards;
    }
    #c5{
        transform: rotate(350deg) !important;
        animation-delay: 2s;
        animation: radial 5000ms ease-in 1900ms infinite;
        animation-fill-mode: forwards;
    }
    #c6{
        transform: rotate(270deg) !important;
        animation-delay: 2s;
        animation: radial 5000ms ease-in 3000ms infinite;
        animation-fill-mode: forwards;
    }
    #c7{
        transform: rotate(140deg) !important;
        animation-delay: 2s;
        animation: radial 5000ms ease-in 2000ms infinite;
        animation-fill-mode: forwards;
    }
    figcaption {
        font-size: 0.7rem;
        text-align: center;
        display:flex; 
        flex-direction: column; 
        align-items: center;
    }
    .list-item {
        display: flex;
        align-items: center;
        justify-content: flex-start;
        gap: 1rem;
    }
    .list-item input {
        position: absolute;
        opacity: 0;
        height: 0;
        width: 0;
    }
    .list-bullet {
        height: 0.3rem;
        width: 0.3rem;
        border-radius: 100rem;
        background-color: rgba(255, 255, 255, 0.7);
    }
    .list-item label {
        opacity: 0;
        transform: translate(1rem, 0);
        transition: 500ms;
        cursor: url("../img/star-mod.svg") 25 25,
                url("../img/star-mod.svg") 25 25,
                auto !important;
    }
    input:checked + label {
        transform: translate(0rem, 0);
        text-shadow: 0px 0px 10px rgba(0,0,0,1);
        opacity: 1;
    }
    ul {
        padding-left: 0.8rem;
    }
    li {
        font-size: 0.9em;
    }
    li::marker {
        font-size: 0.9rem;
        color:  rgba(255, 255, 255, 0.7);
    }
    section#12 {
        display: flex;
        flex-direction: column !important;
    }
    
---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<div class="center-page">
    <h3>Project Presentation</h3>
    <h1>Possible Existence of Parallel Oriented Molecular Cloud in Gould Belt in Numerical Aspect</h1>
    <br><br><br>
    <div class="row">
        <div class="row-sub">
            <small class='left'>MPhil student @ CUHK</small>
            <small>Tsang Man Hin</small>
        </div>
        <div class="row-sub">
            <small class='left'>Supervisor @ CUHK</small>
            <small>Prof. Li, Hua Bai</small>
        </div>
        <small>30 June 2022</small>
    </div>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4>Stars</h4>

<div id="img-center">
    <img height="60%" src="../img/sun.png"/>
    <small>Image adoped from Helioviewer.org</small>
</div>


<!--
    - funcamental building blocks of the astronomical objects.
    - ages clusters
    - distributions & composition trace the history of the galaxy.
    - HR diagram -> ages of clusters.
    - Giant fusion reactor - pp chain, CNO cycles, 
    - 
-->

<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb1-1" />
    <label for="cb1-1">Atom of the universe <small>(Mckee, 2017)</small></label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb1-2" />
    <label for="cb1-2">Origin ?</label>
</div>
<!-- 
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb2" />
    <label for="cb2"></label>
</div> -->


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4>Inter staller Medium</h4>

<div id="img-center">
    <img height="60%" src="../img/ism.jpg"/>
</div>

<!-- 
    - Gas filling the space
    - Hydrogen, atoms molecules or ions.
    - Dust.
    - Ions -> H II emission, (n = 3 -> 2: red) (n = 4 -> 2: blue).
    - Atoms -> H I region (wavelength = 21 cm) (spin flip)
    - Molecules -> didn't emit -> observe CO emission line (2.6 mm).
 -->

<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb2-1" />
    <label for="cb2-1">Gas filling the space</label>
</div>
<br>
<!-- <div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb2-2" />
    <label for="cb2-2">Origin ?</label>
</div> -->

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4>Molecular Cloud</h4>

<div id="img-center" style="padding-left:10rem;">
    <img height="60%" src="../img/musca.png"/>
    <figcaption>Herschel 250 µm dust emission map of Musca <small>(A. Tritsis & K. Tassis, 2018)</small>
    </figcaption>
</div>

<!-- 
    - Dense and cold gas, composite of molecules.
    - Hydrogen, atoms molecules or ions.
 -->

<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb3-1" />
    <label for="cb3-1">Elongated</label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb3-2" />
    <label for="cb3-2">Magnetized</label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb3-3" />
    <label for="cb3-3">Turbulent</label>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4>Magnetic Field</h4>

<div id="img-center" style="flex-direction: row; gap: 1rem;">
    <div style="width: 40%; height: 40%; display: flex; flex-direction: column; align-items: center;">
        <img height="100%" src="../img/musca-b.png"/>
        <figcaption>Musca <small>(ESA/Herschel/Planck; J. D. Soler, MPIA)</small>
        </figcaption>
    </div>
    <div style="width: 40%; height: 40%; display: flex; flex-direction: column; align-items: center;">
        <img height="100%" src="../img/taurus.png"/>
        <figcaption>Taurus <small>(ESA/Herschel/Planck; J. D. Soler, MPIA)</small>
        </figcaption>
    </div>
</div>

<!-- 
    - Dense and cold gas, composite of molecules.
    - Herschel 250, 350, 500 microns
    - PLANCK - Magnetic field.
 -->
<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb4-1" />
    <label for="cb4-1">Ordered</label>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4>Turbulent</h4> 

<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb5-1" />
    <label for="cb5-1">Emittion line width (FWHM ~ km/s) </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb5-2" />
    <label for="cb5-2">Larson's relation σ ∝ POW(L, 0.38) </label>
</div>


 <!-- Too Basic -->

<!-- - What is ISM. & Molecular cloud (big picture).

- Base to build the research.

- Elongated properties of MC. (Examples, from PLANCK | QL) (-> idea to study the long-axis orientation.)

- Turbulent & Magnetic field (Examples, shows some figures).

- linewidth observed is much wider then thermal emission (~10K), preventing from cloud from free-falling.

- Gas pressure is some how isotropic, but not for the magnetic field pressure. 

- B-field (ordered) & elongated -> something to do to the SFE. (Li 2017)
 -->


---


<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4>Motivation</h4> 

<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb6-1"/>
    <label for="cb6-1">Correlation between MCs orientation & b-field direction ?</label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb6-2" />
    <label for="cb6-2">Does parallel orientated molecular cloud could explain the result better?</label>
</div>


---


<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4>Bimodal Cloud Orientation</h4> 


<div id="img-center" style="padding-left: 50%;">
    <img height="60%" src="../img/bimodal.png"/>
    <figcaption>
        Cloud versus B-field directions
    </figcaption>
    <small>
        Adopted from Li, Fang, Henning & Kainulainen (2013)
    </small>
    
</div>


<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb8-1"/>
    <label for="cb8-1">
        Study of the Gould Belt MCs.
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb8-2" />
    <label for="cb8-2" style="max-width: 60%;"> 
        Cloud alignment - autocorrelation contour of the extinction map.
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb8-3" />
    <label for="cb8-3" style="max-width: 60%;"> 
        B-field alignment - equal weight Stokes mean. 
        <small>Optical polarimetry data Heiles (2000)</small>
    </label>
</div>

<!-- 
    IRAS-based extinction maps 
        from Schlegel, Finkbeiner & Davis (SFD; 1998)
    
    near-infrared color-excess 2MASS-based extinction maps 
        from Rowles & Froebrich (RF; 2009)
        and from Dobashi (2011).
 -->


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center" style="">
    <img height="60%" src="../img/bimodal-2.png"/>
    <figcaption>
        Pipe nebula (left) and Ophichus (right) with B-field overlapped.
    </figcaption>
    <small>
        Adopted from Li, Jiang, Fan, Gu & Zhang (2017),  background: ESO/S Guisard
    </small>
    <small>
        Red: Alves, Franco & Girart (2008), Yellow: Heiles (2000)
    </small>
</div>

--- 



<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4 style="max-width: 65%">Magnetic flux for different cloud alignment</h4>

<div id="img-center" style="padding-left: 60%">
    <img height="60%" src="../img/para-vs-perp.png"/>
    <figcaption style="text-align: center;">
        Illustration of magnetic flux vary with filamentary cloud orientation.
    </figcaption>
    <small>
        Adopted from Li, Jiang, Fan, Gu & Zhang (2017)
    </small>
</div>
<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb10-1"/>
    <label for="cb10-1">
        Different of cross-section area.
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb10-2" />
    <label for="cb10-2" style="max-width: 60%;"> 
        ∥: smaller flux, ⟂: larger flux.
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb10-3" />
    <label for="cb10-3" style="max-width: 60%;"> 
        Different collapsing efficiency?
    </label>
</div>

--- 

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4 style="">Effect of Alignment on Mass Cumulative Functions</h4>

<div id="img-center" style="padding-left: 60%; padding-top: 10%;">
    <img height="60%" src="../img/paul-mcf.png"/>
    <figcaption style="text-align: center; max-width: 80%;">
        MCF of 13 Gould Belt MCs.
    </figcaption>
    <small>
        Adopted from Law (2020)
    </small>
</div>
<br>

<p style="font-size: 0.7rem; margin-bottom: 1rem !important;"> Mass Cumulative function (MCF) </p>


$$MCF(\tilde A_V)\;=\;\mu m_H C \sum_{A_V > \tilde A_V} A_V \times A_{pixel}$$

<br>

<p style="font-size: 0.7rem; margin-bottom: 1rem !important;"> MCF Slope </p>

$$MCF.Slope = \frac{1}{|A_{Vtrs} - A_{V 10\%}|}$$

<br>

<p style="font-size: 0.7rem; margin-bottom: 0.5rem !important; max-width: 60%;">
    ↑ MCF Slope  → more mass accumulate at the high dense region
</p>

<style scoped>
    span.katex-display {
        transform: scale(1.1) translateX(40%);
    }
</style>



---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4 style="">Effect of Alignment on MCF cont'd</h4>

<div id="img-center" style="padding-left: 60%; padding-top: 10%;">
    <img height="60%" src="../img/paul-mcf-slope-vs-offset.png"/>
    <figcaption style="text-align: center; max-width: 80%;">
        MCF Slope versus cloud-field offset of 13 Gould Belt MCs.
    </figcaption>
    <small>
        Adopted from Law (2020)
    </small>
</div>
<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb12-1"/>
    <label for="cb12-1">
        ↑ offset → ↑ MCF Slope
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb12-2" />
    <label for="cb12-2" style="max-width: 60%;"> 
        Statistically significant (p-value = 0.01)
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb12-3" />
    <label for="cb12-3" style="max-width: 60%;"> 
        Projection effect!
    </label>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<h4 style="">Effect of Alignment on Star Formation Efficiency <small>Li(2017)</small></h4>

<div id="img-center" style="padding-left: 50%; padding-top: 10%;">
    <img height="60%" src="../img/li-sfe.png"/>
    <figcaption style="text-align: center; max-width: 80%;">
        SFE versus cloud-field offset of 13 Gould Belt MCs.
    </figcaption>
    <small>
        Adopted from Li (2017)
    </small>
</div>
<br>

<h3 style="margin-bottom: 1rem !important;">SFR estimated by</h3>
    
$$ 
SFR = N_{YSO} \times \frac{Median-mass}{0.5 M_{\odot}} \times 
\left(\frac{Typical-age}{2 Myr} \right)^{-1}
$$

<br>

<h3>SFR rate<sup>-1</sup> (SFE) estimated by</h3>

- SFR divided by cloud mass
    - Mass above $A_V = 2$ mag for Ref <sup>4</sup>
    - Mass above $A_V = 7$ mag for Ref <sup>3</sup>



<style scoped>
    p:hover::before {
        display: none;
    }
    p:hover::after  {
        display: none;
    }
    p span.katex-display {
        transform: scale(1.5) translateX(30%);
    }
    h3 {
        text-align: left;
        font-size: 1rem !important;
    }
    
</style>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


# Our Goal

<br>

<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb14-1"/>
    <label for="cb14-1" style="max-width: 100%;">
        Offset is caused by projections.
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb14-2" />
    <label for="cb14-2" style="max-width: 100%;">
        Best fit of the observed result including parallel clouds.
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb14-3" />
    <label for="cb14-3" style="max-width: 100%;">
        Statistical analysis with MHD simulated result. 
    </label>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<div id="img-center" style="padding-left:35rem;">
    <img height="60%" src="../img/03-orszag-tang-vortex.png"/>
    <figcaption style="display:flex; flex-direction: column; align-items: center;">
        Example test case - OT vortex<small> (Orszag & Tang, 1998)</small>
        <a href="http://sfg.phy.cuhk.edu.hk/group_page/scorpio.php"><small>
            find more test cases in sfg.phy.cuhk.edu.hk/group_page/scorpio.php
        </small></a>
    </figcaption>
</div>



# MHD simulation

<br>

Scorpio

<br>

<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb15-1"/>
    <label for="cb15-1" style="max-width: 100%;">
        Initiated by Hsiang-Hsu Wang
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb15-2" />
    <label for="cb15-2" style="max-width: 100%;">
        Two fulid MHD-AD solver
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb15-3" />
    <label for="cb15-3" style="max-width: 40%;">
        Open source & publication in the future
    </label>
</div>



---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


# Initial conditions

<div id="img-center" style="padding-bottom:10%;">
    <img width="60%" src="../img/init.png"/>
    <figcaption>
        Initial column density of the clouds.
    </figcaption>
</div>

<br>
<br>
<br>
<br>
<br>

- $960 \times 480^2$ grid cells $20 \times 10^2$ pc<sup>3</sup> box.
    - cloud scales ~ 10 pc.


- Plammer Profile
    - $\rho(r) = \rho_c \left( 1 + r^2/a^2\right) ^{-p/2}$ 
    - $p = 2$, $a = 2.5$ pc,  $\rho_c=57.5$ M$_⊙$ pc$^{−3}=1110$ cc$^{−1}$
     - exponential decay at $r > \pm 7.5$ pc, $\rho_{min} = 0.2 \rho_c$  


<style scoped> 
    p {
        font-size: 0.8rem !important;
        margin-top: 0.5rem !important; 
    }
    li {
        font-size: 0.8em !important;
    }
</style>
---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


#### Initial conditions cont'd.

<br>

- Equipartition of energy - $KE = U_G = U_B$

- Mach number 10 at the ~10 pc scale 
- $T = 25$ K, $\mu = 2.3$ ~ typical value of MC.
- $|\vec{B}| = 20.79$ 𝜇𝐺
- identical initial turb velocity field $P(k) \propto k^{-2} \{k \geq 5\}, 0 \{k < 5\}$.


<style scoped> 
    p {
        padding-bottom: 0.2rem !important;
    }  
</style>

---


<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


#### Simulation result

<div id="img-center" style="padding-left:60%;">
    <img height="60%" src="../img/column-density-example.png"/>
    <figcaption>
        Column density at the end of the simulation
    </figcaption>
</div>


<br>


<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb18-1"/>
    <label for="cb18-1" style="max-width: 100%;">
        End at 1.58 Myr
    </label>
</div>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb18-2" />
    <label for="cb18-2" style="max-width: 100%;">
        <p>Projections</p>
        <ul>
            <li>10000 times each</li>
            <li>Random & uniform (Fibonacci Lattice)</li>
            <li>Equal mass maximum closed contour</li>
        </ul>
    </label>
</div>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb18-3" />
    <label for="cb18-3" style="max-width: 100%;">
        <p>Generate observables</p>
        <ul>
            <li>Orientations of cloud and b-field</li>
            <li>MCF Slope</li>
            <li>Estimate SFE by dense gas fraction</li>
        </ul>
    </label>
</div>

<style scoped> 
    li::marker {
        content: '-';
        letter-spacing: 0.5rem;
        font-size: 1rem;
    }
    .list-item {
        margin-bottom: 0.7rem !important;
    }
</style>



---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


#### Orientations

<div id="img-center" style="padding-left:60%;">
    <img height="60%" src="../img/orientation.png"/>
    <figcaption style="display:flex; flex-direction: column; align-items: center;">
    <p style="font-size: 1em !important;">Cloud orientation (red line)</p>
    <p style="font-size: 1em !important;">Mean b-field direction (Black arrow)</p>
    </figcaption>
</div>


<br>

Cloud orientation
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb19-1"/>
    <label for="cb19-1" style="max-width: 60%; font-size: 0.8em;">
        Column density weighted principle component 
    </label>
</div>
<br>

Mean B-field direction 
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb19-2" />
    <label for="cb19-2" style="max-width: 100%; font-size: 0.8em;">
        Density weighted Stoke's mean
    </label>
</div>

<style scoped> 
    li::marker {
        content: '-';
        letter-spacing: 0.5rem;
        font-size: 1rem;
    }
    .list-item {
        margin-bottom: 1rem !important;
    }
    p {
        padding-bottom: 0.5em;
    }
</style>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


#### Orientations cont'd.

<br>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb20-1"/>
    <label for="cb20-1" style="max-width: 90%;">
        9934/10000 parallel cloud's projections with offset smaller than 45 deg
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb20-2" />
    <label for="cb20-2" style="max-width: 100%;"> 
        3051/10000 perpendicular cloud's projections with offset smaller than 45 deg
    </label>
</div>


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


#### Orientations analysis

<br>

Compare with $13$ Gould belt MCs in Li(2017, 2013) and Law(2020) 
$5$ clouds are parallel, and $8$ clouds are perpendicular to the b-field.

- Assume $k$ clouds in 13 is intrinsically parallel, 
    - select $k$ projection from intrinsically parallel cloud.
    - select $13 - k$ projection from intrinsically perpendicular cloud.
    - relative likelihood of $k$ to see the observed propotion (5:8)


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


#### Orientations analysis cond't

<br>

<div id="img-center" style="padding-left:40rem;">
    <img height="60%" src="../img/fib_10000/proj_test.png"/>
    <figcaption>
        Result of the orientation test.
    <small></small>
    </figcaption>
</div>

- Maximum likelihood estimate of $k$ is
    - $k = 2 \in [0, 5]$ for PLANCK data

<br>

- Maximum likelihood estimate of $k$ is
    - $k = 4 \in [0, 6]$ for starlight data


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


#### MCF Slope

<div id="img-center" style="padding-left:60%;">
    <img height="60%" src="../img/mcf-sample.jpg"/>
    <figcaption style="display:flex; flex-direction: column; align-items: center;">
    <p style="font-size: 1em !important;">5 randomly selected MCF from the two simulated clouds</p>
    </figcaption>
</div>


<br>

Law, 2020 MCF Slope $= \frac{1}{|A_{Vtrs} - A_{V 10\%}|}$

<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb23-1"/>
    <label for="cb23-1" style="max-width: 60%; font-size: 0.8em;">
        Turning point is not resolved in our simulation 
    </label>
</div>

Our simulation:  MCF Slope $= \frac{1}{|\sigma_{min} - \sigma_{10\%}|}$
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb23-2" />
    <label for="cb23-2" style="max-width: 100%; font-size: 0.8em;">
        similar trends as Law (2020)
    </label>
</div>

<style scoped> 
    li::marker {
        content: '-';
        letter-spacing: 0.5rem;
        font-size: 1rem;
    }
    .list-item {
        margin-bottom: 1rem !important;
    }
    p {
        padding-bottom: 0.5em;
    }
</style>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

# Intuition

<div id="img-center" style="flex-direction: row; gap: 1rem;">
    <div style="width: 40%; height: 45%; display: flex; flex-direction: column; align-items: center;">
        <img height="100%" src="../img/paul-mcf.png"/>
        <figcaption> 
            MCF of 13 Gould belt MCs.    
        <small>Law (2020)</small>
        </figcaption>
    </div>
    <div style="width: 40%; height: 45%; display: flex; flex-direction: column; align-items: center;">
        <img height="100%" src="../img/mcf-sample.jpg"/>
        <figcaption>
            5 randomly selected MCF from the two simulated clouds
        </figcaption>
    </div>
</div>

<br><br><br><br><br><br><br><br>
Larger offset trend to have a more flatten MCF.


---


<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

# MCF Slope cont'd

<div id="img-center" style="padding-left:40%;">
    <img height="70%" src="../img/fib_10000/mcf_slope_versus_b_offset.png"/>
    <figcaption>
        MCF Slope versus cloud-field offset
    </figcaption>
</div>

<br>

<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb22-1" />
    <label for="cb22-1" style="max-width: 100%;"> 
        ↑ offset → ↑ MCF Slope
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb22-2" />
    <label for="cb22-2" style="max-width: 40%;"> 
        small variation of offset for intrinsically parllel cloud
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb22-3" />
    <label for="cb22-3" style="max-width: 40%;"> 
        smaller MCF slope for intrinsically parllel cloud
    </label>
</div>


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

# MCF Slope Analysis

<br>

- Calculate mean MCF slope $\theta$ > 45 - mean MCF slope $\theta$ < 45 based on the observation (Relative MCF slope difference)

- Assume $k$ over 13 clouds is intrinsically parallel, 
    - select $k$ projection from intrinsically parallel cloud.
    - select $13 - k$ projection from intrinsically perpendicular cloud.
    - calculate Relative MCF slope difference
    - repeat 10000 times to estimate the likelihood to reach the observed value. 

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center" style="padding-left:40rem;">
    <img height="60%" src="../img/fib_10000/mcf_slope_test.png"/>
    <figcaption>
        MCF test's bootstrapped result.
    </figcaption>
</div>


# MCF Slope Analysis Result

<br>

- Maximum likelihood estimate of $k$ is
    - $k = 5 \in [0, 12]$ for PLANCK data

<br>

- Maximum likelihood estimate of $k$ is
    - $k = 3 \in [0, 11]$ for starlight data


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center" style="padding-left:0rem; z-index: -9900;">
    <img height="100%" src="../img/dgf-.jpg"/>
    <figcaption>
    </figcaption>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center" style="padding-left:0rem; z-index: -9900;">
    <img height="100%" src="../img/dgf-2.jpg"/>
    <figcaption>
    </figcaption>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

# DGF Analysis Cont'd.

<br>

- Calculate mean SFE $\theta$ > 45 - mean SFE $\theta$ < 45 based on the observation (Relative SFE difference, Li 2017)

- Assume $k$ over 13 clouds is intrinsically parallel, 
    - select $k$ projection from intrinsically parallel cloud.
    - select $13 - k$ projection from intrinsically perpendicular cloud.
    - calculate Relative DGF slope difference
    - repeat 10000 times to estimate the likelihood to reach the observed SFE difference. 

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center" style="padding-left:40rem;">
    <img height="60%" src="../img/fib_10000/dgf_test.png"/>
    <figcaption>
        DGF test's bootstrapped result.
    </figcaption>
</div>


# DGF Analysis Result

<br>

- Maximum likelihood estimate of $k$ is
    - $k = 10 \in [1, 12]$ for PLANCK data

<br>

- Maximum likelihood estimate of $k$ is
    - $k = 9 \in [1, 11]$ for starlight data


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center" style="padding-left:40rem;">
    <img height="60%" src="../img/fib_10000/total_likelihood.png"/>
    <figcaption>
        DGF test's bootstrapped result.
    </figcaption>
</div>


# Total Likelihood

<br>

- Maximum likelihood estimate of $k$ is
    - $k = 2 \in [1, 5]$ for PLANCK data

<br>

- Maximum likelihood estimate of $k$ is
    - $k = 4 \in [1, 6]$ for starlight data


---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

#### Discussion 

<br>
<br>

<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb33-1"/>
    <label for="cb33-1" style="max-width: 100%;">
        Estimation of DGF
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb33-2" />
    <label for="cb33-2" style="max-width: 100%;">
        Contridiction with S&W 2015
    </label>
</div>
<br>
<div class="list-item">
    <span class="list-bullet"></span>
    <input type="checkbox" id="cb33-3" />
    <label for="cb33-3" style="max-width: 100%;"> 
        Non log-normal
    </label>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>

<div class="center-page">
    <p>Thank You!</p>
</div>

---


<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center">
    <img height="60%" src="../flow-chart/main.svg"/>
</div>

---

<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center">
    <img height="60%" src="../flow-chart/bootstrapping.drawio.svg"/>
</div>

---


<div id="canvas">
    <div class="circle" id="c1"><div class="star"></div></div>
    <div class="circle" id="c2"><div class="star"></div></div>
    <div class="circle" id="c3"><div class="star"></div></div>
    <div class="circle" id="c4"><div class="star"></div></div>
    <div class="circle" id="c5"><div class="star"></div></div>
    <div class="circle" id="c6"><div class="star"></div></div>
    <div class="circle" id="c7"><div class="star"></div></div>
</div>


<div id="img-center">
    <img height="60%" src="../flow-chart/projection.drawio.svg"/>
</div>

---

<!-- 
#### Discussion 

Why Solar can't see the Li17 trends.

- Density threshold.

(Go through this paper)

- Solar use the density threshold above the critical density $A_V = 8$, a range that cloud mass is linearly correlated with the star-formation rate.

    - Li 2017 analyzed using cloud mass above $A_V= 2$, not only focusing on the high density region.


--- 

Collisional Coefficient. (WG Appendix)
Drag force term.

WG-tests with realistic collisional coefficient (inconsistence result) 
Too big friction (drag) force pointing outward. (not collapsing)

 Same result if repeating Balsara's result. (Teley) (1/2 order smaller)

Ask's ZY opinion.

Draine 1986. (realistic value)

Same problems in Tilley & Balsare see if real collision coef 


A numerical scheme and benchmark tests for non-isothermal two-fluid
ambipolar diffusion
David A. Tilley
, Dinshaw S. Balsara, Chad Meyer


New Astronomy 17 (2012) 368–376


---

Goal of the paper.

reperform SW15 paper, Scale with the observed cloud.

Observe the MCF slope and SFE from the simulated observation.

Comparing this with the observation and judge the most propably ratio between para and perp

---

#### References

A. Tritsis, K. Tassis, Magnetic seismology of interstellar gas clouds: Unveiling a hidden dimension. Science 360, 635-638 (2018) -->