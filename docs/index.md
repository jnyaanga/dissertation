---
title: Mechanisms of Larval Growth Control in _Caenorhabditis elegans_
author: 
- |
    | Joy Nyaanga
    |    
    | PhD Dissertation 
    | Northwestern University
    |
    | Repository: https://github.com/jnyaanga/dissertation    

date: "June 2022"
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

*Though she be but little, she is fierce - Shakespeare*

</center>

# Acknowledgements {.unnumbered}

<style type="text/css">
h1 {
  text-align: center;
}
</style>

<center>

<em>

Six years ago, inspired by the incredible scientists who'd mentored me and the research I'd been immersed in, I made the decision to pursue a graduate degree. Five years ago, I left undergrad feeling empowered and excited about a future studying science.

Four years ago, I left a graduate program at Princeton University feeling broken by the deceptively pristine atmosphere of the ivory tower. Uncertain about any future studying science.

Three years ago, I joined the Andersen Lab cautious but hopeful about my future studying science.

Three years later, I write this dissertation as a testament to the scientific journey that reinvigorated my love for science and shaped me into a stronger writer, researcher and person.

</em>
</center>

------------------------------------------------------------------------
  
It takes a village to raise a Ph.D. candidate and this journey would not have been possible without the support I???ve received from my village. 
  
Were it not for my undergraduate academic advisors, Drs. Jim Lissemore and Chrystal Bruce, and my undergraduate research advisor, Dr. Michael Nichols, I would never have considered a career in research. I am forever grateful to the patience they showed me as a young scientist, the incessant curiosity they imparted upon me, and the respect they taught me I deserved. They each, in their own way, showed me the very best of academia and for that I am thankful.
  
Above all, I would like to acknowledge my advisor, Dr. Erik Andersen. Throughout my four years as a graduate student at Northwestern University, Erik has been a constant source of support going above and beyond to ensure I had what I needed to be successful. I believe, without a doubt in my mind, that Erik has found his calling as a scientist, teacher, and mentor. His passion for science is infectious, his commitment to research inspiring, and his sheer determination unmatched. I look forward to seeing where his career takes him.
  
My time in graduate school would not have been the same without the many colleagues and friends I???ve made along the way. First, I would like to acknowledge Dr. Gaotian Zhang who helped me find my place in the laboratory during my rotation. Gaotian???s secret power is his enduring positivity and confidence. I am so fortunate to have worked with him and witness his experimental skill firsthand ??? I am convinced there is no experiment too difficult for Gaotian. I will carry his calmness with me through all future stressful situations. 

Two other people I would like to mention are Drs. Tim Crombie and Sam Widmayer. I had the pleasure of building the easyXpress package with these incredibly talented postdocs. They have both been a constant source of positive feedback and constructive criticism. My progress over the last four years would not have been possible without our daily collaboration and conversation. Unknowingly, they have pushed and mentored me to be a better programmer and scientist. Above all, they give me hope for the future of academia ??? I look forward to seeing the product of their hard work and dedication to science. 

Next, I would like to thank Dr. Katie Evans. Katie???s extensive knowledge and computational prowess intimidated me for the longest time. I soon found that we were incredibly similar and I have been fortunate enough to lean on her experience and advice in the last year as I explored careers in industry. As she makes her own transition to industry, I am certain she will continue to make great contributions to her field.  

The data in this dissertation would not exist were it not for the help of two talented technicians, Nicole Roberto and Sophia Gibson. They both shared the burden of my 72-hour time course experiments, allowing me to get a few hours of shut eye while knowing my animals would be in good hands. I would also be remiss if I did not mention Dr. Robyn Tanny. Robyn???s tireless management of all aspects of the laboratory, especially the CeNDR strain collection, is both impressive and inspiring. Her kindness and hospitality is infectious, and her birthday treats are delicious!

I am grateful to my committee members, Drs. John Marko, Marco Gallio, Shelby Blythe, Niall Mangan, and Erik Andersen, who have provided helpful comments and advice regarding my scientific and career journey. I have sincerely appreciated the support they???ve shown me as I???ve pursued a non-academic career path. In particular, I would like to thank Niall for the time I???ve spent as part of her group. The experience has shaped me into a better communicator and deepened my respect for the field of mathematics. 

During my time in graduate school, I had the fortune of an incredibly supportive cohort. Loraina Stinson, Emily Pujadas, and Emily Czajkowski have shared in the joys and struggles of grad school from day one (\*cough\* Quant Bio \*cough\*). I am grateful for their continued support and friendship throughout this journey. In addition to my fellow scientists, I am thankful for my network of family and friends. My parents and three younger siblings remain a constant reminder of the privilege I have to pursue my passion for science. My close friend (and soon to be fellow Dr.!), Sara Martinko, was always a short call away when I needed a sympathetic ear to vent about graduate school. And of course my cat, Spooky, who???s unconditional love and soft purrs have brightened every morning and eased every evening.    

Last, but certainly not least, my graduate school journey would not have been possible without the love and support of my partner, Austin McIlvaine. Austin has been my rock for the last seven years, keeping me sane amidst the trials of graduate school admissions, candidacy exams, and now this ??? the doctoral dissertation and defense. I am grateful for the countless hours spent listening to me talk on-and-on about science, time spent driving me to campus for late night experiments, and many many words of encouragement. All of this would not have been possible without him.

