---
author-meta:
- Finlay Maguire
- Michael A. Graven
- Noni E. MacDonald
date-meta: '2019-10-07'
keywords:
- markdown
- publishing
- manubot
lang: en-GB
title: 'Data Ordinality: An Important Concept in Reducing Medical and Research Errors'
...






<small><em>
This manuscript
([permalink](https://fmaguire.github.io/data_ordinality_paper/v/20551e02eba049de5bdbe027a9378bc44fae7cf7/))
was automatically generated
from [fmaguire/data_ordinality_paper@20551e0](https://github.com/fmaguire/data_ordinality_paper/tree/20551e02eba049de5bdbe027a9378bc44fae7cf7)
on October 7, 2019.
</em></small>

## Authors



+ **Finlay Maguire**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0002-1203-9514](https://orcid.org/0000-0002-1203-9514)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [fmaguire](https://github.com/fmaguire)
    · ![Twitter icon](images/twitter.svg){.inline_icon}
    [fmaguire](https://twitter.com/fmaguire)<br>
  <small>
     Faculty of Computer Science, Dalhousie University
     · Funded by Donald Hill Family Fellowship in Computer Science
  </small>

+ **Michael A. Graven**<br><br>
  <small>
     Department of Paediatrics, Faculty of Medicine, Dalhousie University
  </small>

+ **Noni E. MacDonald**<br><br>
  <small>
     Department of Paediatrics, Faculty of Medicine, Dalhousie University
  </small>



## Abstract {.page_break_before}




## Data Ordinality {.page_break_before}


//% of medical errors that are related to transcription
//The majority of medical research is retrospective 
//The more times data is copied the more errors
//Different types of data have different error rates 
//Easier to avoid errors than fix them
//Humans are always going to make errors


Adverse effects of medical treatment are responsible for 2.8% of all deaths in the US [@140XZkS8r].
ICU patients experience an 1.7 medical errors a day of which 29% were errors classed as having the potential to cause severe harm or death [@wKBeXrtj] 
A major source of these adverse outcomes is errors in the transmission and communication of information between healthcare workers (HCW).
For example, transcription errors (misinterpreation of written/spoken orders and mistakes copying prescriptions) are responsible for 2-14% of medication errors across a range of contexts [@DhnNgERL].
Humans, even very well trained ones, are fallible.
This means human error is inevitable. 

While errors in patient care can have disastorous consequences for that patient, these errors can and do propagate into clinical research.
In some cases these errors distort the results of clinical trials leading harming potentially huge numbers of patients by leading to incorrect changes in the standards of care.
Unfortunately, these errors aren't evenly and randomly distributed across the entire dataset with some bits of data having discrepancy rates as high as 26.9% [@184pUTqaA].
With some analyses showing that an error on a page greatly increased the risk of another error appearing on the same page [@184pUTqaA].

The more times a piece of data is copied the more likely it is to have errors introduced.
An intuitive example of this effect is that of the childhood "whisper game".
In this, a message is whispered from person to person down a line of people.
Upon the last person in the line speaking the message aloud the message is typically drastically different from the original message.
Each person listening and repeating this message allows the original information to become increasingly distorted and warped.
Medical research is particularly affected by this especially as a significant quantity of all clinical research involves retrospective review of patient charts (1/4 of emergency medicine research studies [@EJpntCLW]).

To help researchers and clinicians understand and conceptualise this we present the principle of “data ordinality”.  
Ordinality is a term used in maths to denote the order of objects within a sequence, e.g., 1st, 2nd, 3rd.  
We can apply this idea to data, by using it describe how many times a piece of data has been manually entered or written down.
For example, 1st order data would be data that has been directly extracted or printed out from a device such as a digital thermometer.  
When this temperate is written down by a HCW into a patient’s chart it would now be 2nd order data. Finally, when a researcher extracts this temperature from the chart it is now 3rd order data.
In our intuitive example, data ordinality would be the number of whisper events in the game of telephone/whisper.
Errors increase as data ordinality increases, much as the distortion of the message becomes greater the more people are playing the whisper game.

This is an analogous generalisation of the concept of historigraphical primary, secondary, and tertiary sources.

![Propagation of Error with Data Ordinality. Assuming an arbitrary uniform 5% chance of error in the copying of each data-point at each stage of copying. In reality different pieces of data and different stages will have drastically different error rates.](images/error_prop.png){#fig:errorprop}

One way to reduce data ordinality is the adoption of clinical information technology (IT) such as electronic health records, electronic prescription systems etc.
The adoption of these systems have been shown to reduce hospitality mortality, complications, and costs [@1DvlBqvBW,@X1io6jjf].
However, just because data has been entered into a computer does not mean its ordinality cannot still increase.
A dataset can be sent to one researcher, who then makes some accidental changes due to either user error or computer glitches (partial data transfer, bugs, automated reformatting).

Typically, it is always easier and cheaper to prevent errors and adverse situations than to retroactively attempt to fix them.

A pervasive example of this in the life sciences is the mangling of gene names through automated formatting of them as dates by Excel [@HkW6SMFg,@UOgYpEcx].
These mangled names are then uploaded to central databases where they continue to proliferate as other researchers make use of them.

Data ordinality can be controlled by having a single authoritative source copy of any dataset with restricted audited ability to change it.
This dataset and any updates to it should be tracked using a version control system and kept thoroughly backed-up in order to maintain data integrity.
Indeed, these are a requirements enumerated in many national laws and regulations governing clinical trials and pharamceutical manufacture (e.g. US Federal Drug Association's 21CFR11).

Ultimately, we belive that the concept of data ordinality is a useful mental framework that clinicians should be mindful of in both practice and research.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
