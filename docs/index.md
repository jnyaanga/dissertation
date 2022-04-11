---
title: Mechanisms of Larval Growth Control in _Caenorhabditis elegans_
author: 
- |
    | Joy Nyaanga
    |    
    | PhD Dissertation 
    | Northwestern University
    |
    | Repository: https://github.com/jnyaanga/thesis    

date: "April 2022"
cover-image: "img/NU_seal.png"
classoption: openany
geometry: "left=1in,right=1in,top=1.5in,bottom=1in"
fontsize: 12pt
linestretch: 1.5
site: bookdown::bookdown_site
output: 
  bookdown::pdf_book:
    latex_engine: xelatex
  bookdown::gitbook:
    split_by: chapter
    split_bib: false
documentclass: book
link-citations: true
bibliography: bibliography.bib
csl: plos-biology.csl
github-repo: jnyaanga
description: "Nyaanga PhD Dissertation"
always_allow_html: yes
header-includes:
  - \usepackage{float}
  - \usepackage{titling}
  - \pretitle{\begin{center}
    \includegraphics[width=2.5in,height=2.5in]{img/NU_seal.png}\LARGE\\}
  - \posttitle{\end{center}}
  - \AtBeginDocument{\frontmatter}
---



# Abstract {.unnumbered}

Body size is one of the most discernible ways in which animal species vary. The blue whale (*Balaenoptera musculus*), the largest animal on earth, can reach up to 30 m in length and weigh up to 200 tonnes. At the other extreme, a species of frog called *Paedophryne amauensis* is among the smallest animals on earth with adults measuring just 8 mm in length, about the size of a pea. Understanding how organisms grow to their characteristic sizes is a fundamental biological question. Although a larger body size can increase an organism's competitive advantage, an increased body size also requires added time and nutrients to develop. As such, organisms must have mechanisms to both sense and adjust growth during development. Studies of single cells have revealed that growth regulation can be achieved using time or size sensing control methods. In multicellular organisms, however, regulatory mechanisms must not only control single cell growth but also integrate it across organs and tissues during development. In this dissertation, I investigate growth control in the roundworm nematode *Caenorhabditis elegans*. I first optimize a high-throughput phenotyping platform that facilitates quantitative assessment of thousands of individuals at high precision. Using this platform, I quantify changes in animal size and shape throughout development, and explore how genetics and natural genetic variation contribute to differences in animal growth. The results of this work lay the foundation for a mechanistic dissection of organismal growth control.


# Dedication {.unnumbered} 
<style type="text/css">
h1 {
  text-align: center;
}
</style>

<center>
  
  
  For my family, and the little black girl who always aspired to be great.

  _Though she be but little, she is fierce - Shakespeare_
</center>




