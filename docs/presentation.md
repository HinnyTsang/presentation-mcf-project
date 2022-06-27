---
marp: true
author: Man Hin Tsang
header: ''
theme: gaia
math: katex
paginate: true
style: |
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    * {
        font-family: 'Noto Sans', sans-serif;
        color: rgba(255, 255, 255, 0.9);
        font-weight: 100;
        letter-spacing: 0em; 
        padding: 0;
        margin: 0;
        box-sizing: border-box !important;
    }
    :root {
        background-image: url("../img/background.jpg");
        background-size: contain;
        padding: 3rem;
        cursor: url("../img/star.svg"), auto;
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
        font-size: 0.6rem !important;
    }
    sup {
        font-size: 0.9em !important;
    }
    p {
        font-size: 1rem !important;
    }
    a {
        text-decoration: none;
        font-size: 1rem;
        color: rgba(255, 255, 255, 0.7);
    }
    h1, h2, h3, h4, h5, h6, small, sup, p, a {
        position: relative;
        display: inline-block;
        transition-duration: 200ms;
    }
    h1:hover, h2:hover, h3:hover,
    h4:hover, h5:hover, h6:hover,
    sup:hover, p:hover, li:hover,
    small:hover {
        color: rgba(255, 255, 255, 1);
        text-shadow: 0 0 rgba(255, 255, 255, 1);
    }
    h1::before, h2::before, h3::before,
    h4::before, h5::before, h6::before, p::before {
        position: absolute;
        top: 0;
        left: 0;
        content: '\00a0';
        width: 0rem;
        height: 0.1rem;
        background-color: rgba(255,255,255,0.5);
        transition-duration: 500ms;
    }
    h1:hover::before, h2:hover::before, h3:hover::before,
    h4:hover::before, h5:hover::before, h6:hover::before, p:hover::before  {
        width: 100%;
    }
    .row {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
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
        font-family: 'Noto Sans', sans-serif;
        text-shadow: 0 0 rgba(0, 0, 0, 1);
        font-size: 0.4em; 
        content: 'Page ' attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
    }
    section {
        cursor: crosshair;
    }
    .test {
        width: 20px;
        height: 20px;
        background: red;
    }
---

<div class="center-page">
    <h3>Presentation</h3>
    <h1>Possible Existence of Parallel Oriented Molecular Cloud in Gould Belt in Numerical Aspect</h1>
    <br><br>
    <div class="row">
        <small>Tsang Man Hin</small>
        <small>21 <sup>th</sup> July, 2022</small>
    </div>
    <div class="test">
    </div>
</div>



---

---

1. Why SFE so low? candidates are b-field & turbulent.

2. Disk formation & IMF

---

<h4>Background</h4> 

 <!-- Too Basic -->

- What is ISM. & Molecular cloud (big picture).

- Base to build the research.

- Elongated properties of MC. (Examples, from PLANC | QL) (-> idea to study the long-axis orientation.)

- Turbulent & Magnetic field (Examples, shows some figures).

- linewidth observed is much wider then thermal emission (~10K), preventing from cloud from free-falling.

- Gas pressure is some how isotropic, but not for the magnetic field pressure. 

- B-field (ordered) & elongated -> something to do to the SFE. (Li 2017)



---

#### Background 
- Orientation of molecular clouds.

- Probing the Magnetic field.

    1. Zeeman measurement (LOS field strength)

    2. Polarmetary (Orientations).

- Defination of Cloud-field alignment.

---

#### Background 

<!-- Logic flow -->

- Li 2013 Discovery of bimodal cloud-field alignemnt.

- Seifried 2015 MHD study of Cloud orientation.

- Law 2020 MCF slope study of mass accumulation

- Li 2017 study of star-formation effeciency.

--- 

#### Project details.

1. Simulation setup

2. Projections

3. MCF & SFE.

4. Statistical test.

5. Result.

---

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

Same result if repeating Balsara's result.

Ask's ZY opinion.

Draine 1986.


A numerical scheme and benchmark tests for non-isothermal two-fluid
ambipolar diffusion
David A. Tilley
, Dinshaw S. Balsara, Chad Meyer


New Astronomy 17 (2012) 368–376
