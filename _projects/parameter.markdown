---
layout: page
title: Parameterization of Li-ion battery
description: Measured or calculated the parameters used in a physics-based model.
img: /assets/img/p4_0.png
importance: 3
project: gitteis
---

This project aims to experimentally obtain the parameters of a graphite-NMC622 cell for a P2D model. 

<!-- For cycling degradation mechanisms, we consider SEI (solid electrolyte interface) growth, lithium plating, electrolyte oxidation, transition metal dissolution and loss of active materials. For calendar aging, we consider SEI growth, electrolyte oxidation and transition metal dissolution.  -->

## Background

Pseudo-two dimensional (P2D) model is a continuous model to describe the electrochemistry and transport of a battery, especially used in lithium ion batteries. To predict the battery performance by P2D model, there are multiple parameters needed in the model, such as electrode thickness, conductivity and so forth. 

<!-- Degradation mechanisms also have paramters such as reaction rate of side reactions. These parameters can be obtained by either measurement techniques or by fitting the experiment curves.  -->

## Methods
**Overview.** The parameters used in P2D model are measured or calculated by the methods below. 

<div class="caption">
    Parameter list and measurement methods (some parameters have more than one method to obtain)
</div>

{:class="table table-hover table-sm"}
<table class='tbl'>
<colgroup>
<col width="6%" />
<col width="46%" />
<col width="48%" />
</colgroup>
<thead>
<tr class="header">
<th>Symbol</th>
<th>Description</th>
<th>Methods</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan = "3" style="text-align:center"><b>Negative electrode (graphite)</b></td>
</tr>
<tr>
<td markdown="span">$$L_{neg}$$</td>
<td>Negative electrode thickness</td>
<td markdown="span">[Micrometer](#micrometer)</td>
</tr>
<tr>
<td markdown="span">$$r_{p,neg}$$</td>
<td markdown="span">Particle radius</td>
<td markdown="span">From manufacturer / Mercury intrusion</td>
</tr>
<tr>
<td markdown="span">$$\varepsilon_{s,neg}$$</td>
<td markdown="span">Solid material volume fraction</td>
<td markdown="span">[Micrometer](#micrometer) / [Mercury intrusion](#mercury-intrusion)</td>
</tr>
<tr>
<td markdown="span">$$a_{s,neg}$$</td>
<td markdown="span">Active surface area per unit electrode volume</td>
<td markdown="span">Assuming sphere ($$3\varepsilon_{s,pos}/r_{p,pos}$$) / [Mercury intrusion](#mercury-intrusion)</td>
</tr>
<tr>
<td markdown="span">$$p_{neg}$$</td>
<td markdown="span">Bruggeman porosity exponent</td>
<td markdown="span">From literature</td>
</tr>
<tr>
<td markdown="span">$$\kappa_{s,neg}$$</td>
<td markdown="span">solid conductivity</td>
<td markdown="span">[Four-probe method](#four-probe-method)</td>
</tr>
<tr>
<td markdown="span">$$D_{s,neg}$$</td>
<td markdown="span">Diffusivity of graphite</td>
<td markdown="span">[GITT](#gitt) / [EIS](#eis)</td>
</tr>
<tr>
<td markdown="span">$$i_{0,neg}$$</td>
<td markdown="span">Exchange current density</td>
<td markdown="span">[EIS](#eis)</td>
</tr>
<tr>
<td markdown="span">$$A_{neg}$$</td>
<td markdown="span">Electrode area (negative area is dominating the cell)</td>
<td markdown="span">From cutting machine</td>
</tr>

<tr>
<td colspan = "3" style="text-align:center"><b>Positive electrode (NMC622)</b></td>
</tr>
<tr>
<td markdown="span">$$L_{pos}$$</td>
<td>Positive electrode thickness</td>
<td markdown="span">[Micrometer](#micrometer)</td>
</tr>
<tr>
<td markdown="span">$$r_{p,pos}$$</td>
<td markdown="span">Particle radius</td>
<td markdown="span">From manufacturer / Mercury intrusion</td>
</tr>
<tr>
<td markdown="span">$$\varepsilon_{s,pos}$$</td>
<td markdown="span">Solid material volume fraction</td>
<td markdown="span">[Micrometer](#micrometer) / [Mercury intrusion](#mercury-intrusion)</td>
</tr>
<tr>
<td markdown="span">$$a_{s,pos}$$</td>
<td markdown="span">Active surface area per unit electrode volume</td>
<td markdown="span">Assuming sphere ($$3\varepsilon_{s,pos}/r_{p,pos}$$) / [Mercury intrusion](#mercury-intrusion)</td>
</tr>
<tr>
<td markdown="span">$$p_{pos}$$</td>
<td markdown="span">Bruggeman porosity exponent</td>
<td markdown="span">From literature</td>
</tr>
<tr>
<td markdown="span">$$\kappa_{s,pos}$$</td>
<td markdown="span">solid conductivity</td>
<td markdown="span">[Four-probe method](#four-probe-method)</td>
</tr>
<tr>
<td markdown="span">$$D_{s,pos}$$</td>
<td markdown="span">Diffusivity of graphite</td>
<td markdown="span">[GITT](#gitt) / [EIS](#eis)</td>
</tr>
<tr>
<td markdown="span">$$i_{0,pos}$$</td>
<td markdown="span">Exchange current density</td>
<td markdown="span">[EIS](#eis)</td>
</tr>


<tr>
<td colspan = "3" style="text-align:center"><b>Others</b></td>
</tr>
<tr>
<td markdown="span">$$\kappa_{e}$$</td>
<td markdown="span">Electrolyte conductivity</td>
<td markdown="span">From manufacturer / From literature / Conductivity Meter</td>
</tr>
<tr>
<td markdown="span">$$L_{sep}$$</td>
<td markdown="span">Separator thickness</td>
<td markdown="span">From manufacturer / [Micrometer](#micrometer)</td>
</tr>
<tr>
<td markdown="span">$$\varepsilon_{e,sep}$$</td>
<td markdown="span">Electrolyte volume fraction in separator</td>
<td markdown="span">From manufacturer</td>
</tr>
</tbody>
</table>


<a name="micrometer"></a>
**Micrometer.** We can use the micrometer to measure the thickness $$L_{neg}$$, $$L_{pos}$$ and $$L_{sep}$$. Then we  calculate the porosity by (taking negative electrode as an example)

$$
\varepsilon_{s,neg}=\frac{V_{dense}}{V_{total}}=\frac{\frac{m_{graphite}}{\rho_{graphite}}+\frac{m_{PVDF}}{\rho_{PVDF}}+\frac{m_{carbon}}{\rho_{carbon}}}{A_{neg}L_{neg}}$$

where the dense density values $$\rho_{graphite}$$, $$\rho_{PVDF}$$, and $$\rho_{carbon}$$ can be found in literature or from manufacturer. 

<a name="mercury-intrusion"></a>
**Mercury intrusion.** Mercury intrusion, or mercury intrusion porosimetry (MIP), is a powerful technique to evaluate the porosity, pore size distribution and particle size distribution of materials. Mercury is squeezed into the material under pressure. Due to the surface tension, the amount of intruded mercury is related to its pressure. The pressure of mercury increases from atmosphere pressure to 60000 psi (413 MPa) above the atmosphere pressure.


<div class="row justify-content-md-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/p4_1.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
  Illustration of mercury intrusion porosimetry. 
</div>

<a name="four-probe-method"></a>
**Four-probe method.** The electrode conductivity can be measured by the four-point method: applying a DC current to the electrode film and measure the voltage between them. Finite element method is then used to help process the current-voltage data to determine the conductivity of electrodes. Specifically, we can measure the effective conductivity by the following steps:
1.	Paste electrode slurry on a glass substrate
2.	Measure resistance (current goes through probes at both ends, measure the voltage between center probes)
3.	Measure dimensions (thickness, probe distance, etc.)
4.	Calculate conductivity by the finite element method

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/p4_2.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/p4_3.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Left: schematic illustration of the four-probe method. Right: experiment picture.
</div>

<a name="gitt"></a>
**GITT.** Galvanostatic Intermittent Titration Technique (GITT) is a  mature method to measure diffusivity. A current pulse is applied to the cell and diffusivity is calculated from the slope of voltage response versus square root of time,

$$
D=\frac{4}{\pi}\left(\frac{IV_M}{SF}\right)^2\left[\left(\frac{\mathrm{d\ }U}{\mathrm{d\ }\delta}\right)/\left(\frac{\mathrm{d\ }V}{\mathrm{d\ }\sqrt{t}}\right)\right],
$$

where, $$I$$ denotes the total current, $$S$$ is the total surface area, $$V$$ is cell voltage after current pulse as a function of time $$t$$, $$V_M$$ is the molar volume of the sample, $$\frac{\mathrm{d\ }U}{\mathrm{d\ }\delta}$$  denotes the derivative of the open circuit voltage with respect to stoichiometry number. $$U^0$$ as a function of $$\delta$$ can be measured from the voltage at each steady state (i.e. lithium ion concentration is uniform in the particle) of a half-cell during the rest period between pulses.


<a name="eis"></a>
**EIS.** Electrochemical Impedance Spectroscopy (EIS) is an electrochemical technique to characterize the performance of cells. The cell is connected to an alternating current (AC) source and the impedance is measured as a function of current frequency. It can measure  **exchange current density** $$i_0$$ and **diffusivity** $$D$$.  Exchange current density $$i_0$$ is measured by 

$$
i_0=\frac{R_{ct}SRT}{F}
$$

where $$R_{ct}$$ is is the charge transfer resistance, $$F$$ is Faraday constant, $$R$$ is gas constant, $$S$$ is the surface area of particles, and $$T$$ is temperature. We assembled a three-electrode cell for EIS (left below) and obtain the plot (right below). 

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/p4_4.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/p4_5.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Left: assembly of three-electrode (graphite/Cu/Li) cell. Right: an example of EIS plot.
</div>

To get the diffusivity, we use the formula

$$
D=\frac{1}{2}\left( \frac{\text{d}U^0}{\text{d}\delta}\frac{V_M}{SF} \right) ^2\left( \frac{\text{dRe}\left( Z \right)}{\text{d}\sqrt{1/\omega}} \right) ^{-2}.
$$

where $$Z$$ denotes impedence, $$\omega$$ denotes frequency.


<h2 id="related-publications">Related publications</h2>

<div class="publications">

  {% bibliography -f papers -q @*[project={{page.project}}]* %}

</div>

All details are written as an internal report (for our sponsor). It is not published but may be shared upon request. 


