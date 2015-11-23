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
{% include toc.html %}

## Installation

Fred2 can simply be installed via <b>pip</b> with:

<code>pip install git+https://github.com/FRED-2/Fred2</code>

### Installation of External Tools

For a fully functioning Fred2 installation, several external tools have to be installed. These tools can not be shipped
with Fred2 due to Licensing issues or due to complex installation procedures.

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

We provide a wealth of tutorials for any level, from basic user, to advanced developer. These tutorials are provided as interactive [IPython Notebooks](http://ipython.org/notebook.html) and can be directly viewed online on our GitHub repository or can be executed offline via [IPython](http://ipython.org/index.html). To view the tutorials online, please [enable JavaScript](https://support.microsoft.com/en-us/gp/howtoscript), otherwise the notebooks will not render.


### For Users
- [Epitope Prediction](https://github.com/FRED-2/Fred2/blob/master/Fred2/tutorials/EpitopePrediction.ipynb) - This tutorial gives a good overview of the basic functionality covering the core objects, epitope prediction, and manipulation of the prediction results.
- [Polymorhpic Epitope Prediction](https://github.com/FRED-2/Fred2/blob/master/Fred2/tutorials/PolymorphicEpitopePrediction.ipynb) - This tutorial exemplifies how to incorporate mutations into epitope prediction.
- [Antigen Processing](https://github.com/FRED-2/Fred2/blob/master/Fred2/tutorials/CleavageAndTAPPrediction.ipynb) - The tutorial exemplifies the usage of proteasomal cleavage, TAP, and epitope prediction methods and how to combine these methods for T-cell epitope prediction.
- [Vaccine Design](https://github.com/FRED-2/Fred2/blob/master/Fred2/tutorials/VaccineDesign.ipynb) - The tutorial covers all steps in rational vaccine design, from epitope discovery, epitope selection, as well as epitope delivery in the form of string-of-beads vaccines.
- [HLA Typing](https://github.com/FRED-2/Fred2/blob/master/Fred2/tutorials/HLATyping.ipynb) - This short tutorial shows how to use FRED2 for HLA typing exemplified by the usage of [OptiType](https://github.com/FRED-2/OptiType).

### For Advanced Users and Developers
- [Databases](https://github.com/FRED-2/Fred2/blob/master/Fred2/tutorials/DBAdapterUsage.ipynb) - This tutorial familiarizes the advanced users with internal functionalities of FRED2's data base adapters.
- [Interfaces](https://github.com/FRED-2/Fred2/blob/master/Fred2/tutorials/ImplementingNewMethods.ipynb) - This tutorial gives an overview of all abstract base classes relevant for implementing new prediction methods, or data base adapters.

