---
layout: article
title: "Getting Started with FRED2"
date: 2014-06-25T13:57:25-04:00
modified:
excerpt:
tags: []
image:
  feature: HIV-infected_H9_T_cell_45h.png
  teaser: mhc.png
  thumb: mhc.png
share: false
---

## Installation

Fred2 can simply be installed via <b>pip</b> with:

<code>pip install git+https://github.com/FRED-2/Fred2</code>

### Installation of External Tools

For a fully functioning Fred2 installation, several external tools have to be installed. These tools can not be shipped
with Fred2 due to Licencing issues or due to complex installation procedures.

The following tools are not provided by Fred2 and have to be downloaded and installed:

<html>

<h3> Epitope Prediction </h3>
<br></br>
<table>
<tr>
<th>Method</th><th>Link</th>
</tr>
<tr>
<td>NetMHC</td><td> <a href="http://www.cbs.dtu.dk/services/NetMHC/">http://www.cbs.dtu.dk/services/NetMHC/</a></td>
</tr>
<tr>
<td>NetMHCpan</td><td> <a href="http://www.cbs.dtu.dk/services/NetMHCpan/">http://www.cbs.dtu.dk/services/NetMHCpan</a></td>
</tr>
<tr>
<td>NetMHCII</td><td><a href="http://www.cbs.dtu.dk/services/NetMHCII/">http://www.cbs.dtu.dk/services/NetMHCII/</a></td>
</tr>
<tr>
<td>NetMHCIIpan</td><td><a href="http://www.cbs.dtu.dk/services/NetMHCIIpan/">http://www.cbs.dtu.dk/services/NetMHCIIpan</a></td>
</tr>
<tr>
<td>NetCTLpan</td><td><a href="http://www.cbs.dtu.dk/services/NetCTLpan">http://www.cbs.dtu.dk/services/NetCTLpan</a></td>
</tr>
<tr>
<td>PickPocket</td><td><a href="http://www.cbs.dtu.dk/services/PickPocket/">http://www.cbs.dtu.dk/services/PickPocket</a></td>
</tr>
</table>

<br></br>
<h3> Cleavage Prediction </h3>
<table>
<tr>
<th>Method</th><th>Link</th>
</tr>
<tr>
<td>NetChop</td><td><a href="http://www.cbs.dtu.dk/services/NetChop/">http://www.cbs.dtu.dk/services/NetChop</a></td>
</tr>
</table>
<br></br>

<h3> HLA Typing </h3>
<table>
<tr>
<th>Method</th><th>Link</th>
</tr>
<tr>
<td>OptiType</td><td><a href="https://github.com/FRED-2/OptiType/">https://github.com/FRED-2/OptiType</a></td>
</tr>
<tr>
<td>Polysolver</td><td><a href="https://www.broadinstitute.org/cancer/cga/polysolver/">https://www.broadinstitute.org/cancer/cga/polysolver</a></td>
</tr>
<tr>
<td>seq2HLA</td><td><a href="https://bitbucket.org/sebastian_boegel/seq2hla/">https://bitbucket.org/sebastian_boegel/seq2hla</a></td>
</tr>
<tr>
<td>ATHLATES</td><td><a href="https://www.broadinstitute.org/scientific-community/science/projects/viral-genomics/athlates/">https://www.broadinstitute.org/scientific-community/science/projects/viral-genomics/athlates/</a></td>
</tr>
</table>
</html>

### Installation of ILP Solver

It is necessary to install a ILP solver such as CBC, CPLEX, Gurobi, or GLPK when using the epitope selection and 
assembly approaches of Fred2. We recommend CBC, an open-source solver supported by the COIN-OR community 
(<a href="https://projects.coin-or.org/Cbc">https://projects.coin-or.org/Cbc</a>).

Although modern ILP solver are quit fast, some models and especially the ones used for epitope assembly are still very time consuming even for small input sizes. 
Therefore, Fred2 offers also methods to approximate the solution. For doing so, Fred2 resorts to the Lin-Kernighan Helsgaun TSP heuristic, which has to be installed separately and can be found here <a href="http://www.akira.ruc.dk/~keld/research/LKH/">http://www.akira.ruc.dk/~keld/research/LKH</a>. 

## Tutorials:



