---
author-meta:
- Finlay Maguire
- Michael A. Graven
- Noni E. MacDonald
date-meta: '2019-10-17'
keywords:
- markdown
- publishing
- manubot
lang: en-GB
title: 'Data Ordinality: An Important Concept in Reducing Medical and Research Errors'
...






<small><em>
This manuscript
([permalink](https://fmaguire.github.io/data_ordinality_paper/v/9d6ebf6f4710528db2aa2d81464de76324c139d7/))
was automatically generated
from [fmaguire/data_ordinality_paper@9d6ebf6](https://github.com/fmaguire/data_ordinality_paper/tree/9d6ebf6f4710528db2aa2d81464de76324c139d7)
on October 17, 2019.
</em></small>

## Authors



+ **Finlay Maguire**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0002-1203-9514](https://orcid.org/0000-0002-1203-9514)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [fmaguire](https://github.com/fmaguire)
    · ![Twitter icon](images/twitter.svg){.inline_icon}
    [finlaym](https://twitter.com/finlaym)<br>
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



## Data Ordinality {.page_break_before}

Adverse effects of medical treatment are responsible for 2.8% of all deaths in the US [@140XZkS8r].
A major cause of these adverse medical outcomes is error in the transmission and communication of information between healthcare workers (HCW) [@1EgScuf8f].
These types of errors are very common, with manually entered pathology data having errors in 76% of patients records [@UwDcTEu8], up to 26.9% error rate in some medical database fields [@184pUTqaA], and 2-14% of medication errors caused by prescription transcription errors [@DhnNgERL].

While errors in patient data can have disastrous consequences for that patient, these mistakes can also have much more wide-ranging impacts.
Retrospective and prospective analysis of datasets derived from patient chart data make up a huge proportion of clinical research publications [@EJpntCLW,@UwDcTEu8].
These datasets are often used to construct or update research databases that are then re-used by large numbers of later studies. 
Observed error rates of individual entries in clinical research databases have ranged from 2.3% to 26.9% [@184pUTqaA].
Therefore, the errors in this clinical data (whether introduced in the underlying patient data or in the later extraction and cleaning) can and likely does lead to erroneous study outcomes [@r2B04jOT].
One recent high-profile example of this involved errors in the large and well-respected UK Biobank database [@xSLvif2A].
These distorted study results have the potential to harm huge numbers of patients by contributing to incorrect changes in the standards of care.

It is generally cheaper and easier to prevent the introduction of errors into data than to retrospectively attempt to correct the data.
If we want to try and prevent these adverse medical and experimental outcomes we need to minimise the number of opportunities for error to be introduced.
Humans, even well trained ones, are fallible.
The more humans involved in communicating a piece of data, the more likely it is to acquire errors.
An intuitive example of this effect is that of the childhood "whisper game".
In this, a message is whispered from person to person down a line of people.
Upon the last person in the line speaking the message aloud the message is typically drastically different from the original message.
Essentially, each brain the information passes through causes the original information to become increasingly distorted and warped.
Medical information, which requires sharing between large networks of HCWs over extended periods of times is particularly prone to these types of distortions.
Therefore, minimising the number of error-prone human links in these chains of data transmission is the easiest way to mitigate this type of error.

To help researchers and clinicians understand and conceptualise this we present the idea of "data ordinality".
Ordinality is a mathematical term denoting the order of objects within a sequence, e.g., 1st, 2nd, 3rd.
We can apply this idea to data, by using it describe how many times a piece of data has been manually recorded or entered into a system.
For example, 1st order data would be data that has been directly extracted or printed out from a device such as a digital thermometer.
When this temperature is written down by a HCW into a patient’s chart it would now be 2nd order data. 
Finally, when a researcher extracts this temperature from the chart it is now 3rd order data.
In our intuitive example, data ordinality would increase every time one person whispers the message to the next person. 
Errors increase as data ordinality increases, much as the distortion of the message becomes greater the more people are playing the whisper game.

![Propagation of Error with Data Ordinality. Assuming an arbitrary uniform 5% chance of error in the copying of each data-point at each stage of copying. In reality different pieces of data and different stages will have drastically different error rates.](images/error_prop.png){#fig:errorprop}

An effective way to reduce data ordinality is the adoption of clinical information technology (IT) such as electronic health records, electronic prescription systems, and so on.
The adoption of systems like this have been shown to reduce hospital-related morbidity, mortality, and costs [@1DvlBqvBW,@X1io6jjf].
With immediate input of data into these systems, ideally directly from the medical equipment, we can greatly reduce data ordinality because all subsequent users of the information can access the original information on the database. 

It is, however, not sufficient to just enter the information into any digital format.
Without careful planning the ordinality and thus error rate of digital data can still increase.
For example, a dataset could be entered into a spreadsheet and shared with a collaborator.
That researcher could make some accidental changes due to either user-error or computer glitches (partial data transfer, bugs, automated reformatting).
The now mangled data is then sent to another collaborator who introduces their own errors before finally uploading the data to a publication database with all the accumulated data ordinality and errors.
A pervasive example of this in the life sciences is the mangling of gene names through automated formatting of them as dates by Excel [@HkW6SMFg,@UOgYpEcx].
These mangled names are uploaded to central databases where they continue to proliferate as other researchers make use of them.
Therefore, whether it is a physical or an IT system, it is vital to have a single authoritative source that can only be changed in a restricted audited way.
These datasets and any updates to them should be tracked using a version control system and be thoroughly backed-up in order to ensure data integrity.
Indeed, this kind of data integrity and versioning requirements are enumerated in many national laws and regulations governing clinical trials and pharmaceutical manufacture (e.g. US Federal Drug Association's 21CFR11).

While most researchers, hospital administrators, and clinicians will understand the general implicit idea of data ordinality, we believe explicitly codifying the idea will be useful in many areas of practice and system design.
Errors are inevitable but by thinking about data ordinality the utility of interventions that generate authoritative carefully controlled and preserved information sources becomes clear.
A conception of data ordinality also makes it much easier to identify dangerous practices that lead to the medical "whisper game".
Without this concept it is much harder to build these ideas into the design of clinical systems and research protocols.
Ultimately, we believe that the concept of data ordinality is a very useful mental framework that will help clinicians be more mindful of data provenance in both practice and research.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
