---
title: "Software"
layout: gridlay
sitemap: false
permalink: /software/
---

<style>
img{
  border-radius: 10px;
}
iframe {
  width: 175px;
  display: inline;
  vertical-align:middle;
  <!-- margin-bottom:5px; -->
  <!-- margin-left:5px; -->
  <!-- border: 1px solid red; -->
}
.col-md-3 {
  margin:0;
  padding:0;
  margin-top:10px;
  margin-bottom:10px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  height: auto;
  float: none;
  background:white;
  border-radius:20px;
  <!-- border: 1px solid black; -->
}
</style>

## Software

<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-12 col-sm-12">
<h4><b>RAIRE (Python)</b></h4>
<a href="https://github.com/michelleblom/rairepy" target="_blank"><button class="btn btn-info btn-sm">GIT</button></a>
<a href="https://arxiv.org/pdf/1903.08804.pdf" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> 

<b>Michelle Blom, Peter J. Stuckey,  and Vanessa J. Teague</b>

RAIRE or <i><b>R</b>isk-limiting <b>A</b>udits for <b>I</b>nstant <b>R</b>unoff voting (IRV) <b>E</b>lections</i> is a methodology for conducting risk-limiting audits (RLAs) for IRV elections (commonly referred to as Ranked Choice Vote, RCV, elections in the United States).  Risk-limiting post election audits guarantee a high probability of correcting incorrect reported election results, independent of why the result was incorrect. Risk-limiting audits for first-past-the-post elections are well understood, and used in some US elections. RAIRE represents the first, and currently only, practical technique for conducting  RLAs of IRV/RCV elections. Several pilot audits using RAIRE have been conducted since 2019, including for the 2019 San Francisco District Attorney's race, and three Democratic National Convention (DNC) primaries in 2020 (Alaska, Wyoming, and Kansas). 

RAIRE works by taking cast vote records (CVRs) -- digitised representations of the ballots cast in an election -- and returning a set of what we call <i>assertions</i>. Each assertion is a pairwise comparison between the tallies of two candidates in a specific <i>context</i>. This context defines whether we include a ballot in one, or neither, of the candidates tallies. One example of an assertion is 'Darius has more votes than Domenic in the context where Connie has been eliminated'. RAIRE finds a set of assertions that, if shown to hold, rule out all outcomes in which someone other than the reported winner wins the election. In other words, we demonstrate that the reported winner is indeed the correct winner. 

Originally implemented in C++, a more recent python version of RAIRE has been developed. The <i>rairepy</i> repository (linked above) contains the RAIRE algorithm for generating assertions, and code demonstrating how that algorithm can be called. An associated repository (<i>rairepy-data</i>) contains data sets, in formats suitable for RAIRE, for a range of election instances. 
</div>
</div>
</div>

<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-12 col-sm-12">
<h4><b>IRV Margin Computation (C++)</b></h4>
<a href="https://github.com/michelleblom/margin-irv" target="_blank"><button class="btn btn-info btn-sm">GIT</button></a>
<a href="https://dl.acm.org/doi/10.3233/978-1-61499-672-9-480" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> 

<b>Michelle Blom, Peter J. Stuckey,  Vanessa J. Teague, and Ron Tidhar</b>

This software implements the branch-and-bound margin computation algorithm described by Blom et al. in "Efficient Computation of Exact IRV Margins" presented at ECAI in 2016. Computing the margin of victory (MOV) in an Instant Runoff Voting (IRV) election is NP-hard. In an IRV, also known as Ranked Choice Vote (RCV), election with winning candidate <i>w</i>, the MOV defines the smallest number of cast ballots that, if modified, result in the election of a candidate other than <i>w</i>. The ability to compute such margins has significant value. Arguments over the correctness of an election outcome usually rely on the size of the electoral margin. This software provides an efficient branch-and-bound algorithm for computing exact margins, improving upon on prior branch-and-bound method by Magrino, Rivest, Shen, and Wagner ("Computing the margin of victory in IRV elections", presented at the 2011 USENIX Accurate Electronic Voting Technology Workshop: Workshop on Trustworthy Elections). Although exponential in the worst case, our algorithm runs efficiently in practice, computing margins in instances that could not be solved by prior methods in a reasonable time frame.
</div>
</div>
</div>

<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-12 col-sm-12">
<h4><b>2-seat STV RLAs (Python)</b></h4>
<a href="https://github.com/michelleblom/stv-rla" target="_blank"><button class="btn btn-info btn-sm">GIT</button></a>
<a href="https://arxiv.org/pdf/2112.09921.pdf" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> 

<b>Michelle Blom, Peter J. Stuckey,  Vanessa J. Teague, and Damjan Vukcevic</b>

Single Transferable Vote (STV) refers to a multi-winner preferential election scheme, used widely in Australia to elect representatives to the upper houses of state and federal parliaments. No methods currently exist for conducting risk limiting audits (RLAs) for such elections in general, however this work represents a first attempt. We present two methods for conducting RLAs for 2-seat STV elections -- one that applies only when the first seat is awarded in the first round of counting (on the basis of first preference tallies), and a second that can be used in more general cases where this isn't the case. We show that the first method is in general quite practical. The second, more general, approach is far less successful. This software accompanies our paper on the topic, presented at the 7th Workshop on Advances in Secure Electronic Voting (VOTING'21), and linked above. 
</div>
</div>
</div>


<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-12 col-sm-12">
<h4><b>RLAs for Hamiltonian Elections (C++)</b></h4>
<a href="https://github.com/michelleblom/primaries" target="_blank"><button class="btn btn-info btn-sm">GIT</button></a>
<a href="https://arxiv.org/pdf/2102.08510.pdf" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> 

<b>Michelle Blom, Philip B. Stark, Peter J. Stuckey,  Vanessa J. Teague, and Damjan Vukcevic</b>

Presidential primaries are a critical part of the United States Presidential electoral process, since they are used to select the candidates in the Presidential election. While methods differ by state and party, many primaries involve proportional delegate allocation using the so-called Hamilton method. In this work, we show how to conduct risk-limiting audits for delegate allocation elections using variants of the Hamilton method where the viability of candidates is determined either by a plurality vote or using instant runoff voting. Experiments on real-world elections show that we can audit primary elections to high confidence (small risk limits) usually at low cost. This software accompanies our paper on the topic, presented at the 7th Workshop on Advances in Secure Electronic Voting (VOTING'21), and linked above. 
</div>
</div>
</div>