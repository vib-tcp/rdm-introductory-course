<!--

author:   Alexander Botzki, Bruna Piereck
email:    training@vib.de
version:  2.2.0
language: en
narrator: UK English Female

icon:     https://vib.be/sites/vib.sites.vib.be/files/logo_VIB_noTagline.svg

comment:  This document shall provide an entire compendium and course on the
          development of Open-courSes with [LiaScript](https://LiaScript.github.io).
          As the language and the systems grows, also this document will be updated.
          Feel free to fork or copy it, translations are very welcome...

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
          https://felixhao28.github.io/JSCPP/dist/JSCPP.es5.min.js

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css
link:     https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css
link:     https://raw.githubusercontent.com/vibbits/material-liascript/master/img/org.css
link:     https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.min.css
link:     https://fonts.googleapis.com/css2?family=Saira+Condensed:wght@300&display=swap
link:     https://fonts.googleapis.com/css2?family=Open+Sans&display=swap
link:     https://raw.githubusercontent.com/vibbits/material-liascript/master/vib-styles.css

orcid:    [@0](@1)<!--class="orcid-logo-for-author-list"-->
tutor:    Research Data Management for Life Sciences: essentials

@JSONLD
<script run-once>
  let json = @0 

  const script = document.createElement('script');
  script.type = 'application/ld+json';
  script.text = JSON.stringify(json);

  document.head.appendChild(script);

  // this is only needed to prevent and output,
  // as long as the result of a script is undefined,
  // it is not shown or rendered within LiaScript
  console.debug("added json to head")
</script>
@end

-->

# Introduction to Research Data Management (RDM)

<section>
Hello and welcome to our @tutor course! We are very happy to have you here.

This workshop is jointly organised by the VIB Technologies and ELIXIR Belgium.

> We are using the interactive Open Educational Resource online/offline course infrastructure called LiaScript. 
> It is a distributed way of creating and sharing educational content hosted on github.
> To see this document as an interactive LiaScript rendered version, click on the
> following link/badge:
>
> [![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/rdm.md)

### Lesson overview

> <i class="fa fa-bookmark"></i> **Description**:
> This course is composed by **6 sessions** that complement each other aiming to give an overview of the steps of Research Data Management (RDM) based on **practical and fun activities, as much as discussions**. All along we focus in practical and analytical view on the **impact** of this practices **on writing and publishing** the results of researchers in scientific journals. This course contains generalized examples and life sciences dedicated examples, but the content is easily **applicable to any areas of science** and research.
> 
> <i class="fa fa-arrow-left"></i> **Prerequisites**:  
> To be able to follow this course, learners should have knowledge in:
>
> 1. Basic knowlegde of HTML  
> 2. Basic knowledge of structured data as JSON-LD objects
> 3. Being comfortable working with the CLI (command-line interface) in a Linux-based environment.  
> 
> <i class="fa fa-arrow-right"></i> **Learning Outcomes:**  
> By the end of the course, learners will be able to:






### Complement (Links for materials and Reading)

- Extra material for trainers: [List of material](https://github.com/vibbits/rdm-course-2022/blob/main/activities/Material_4trainers.md)

- Interactive actives links for students: [List of links](https://github.com/vibbits/rdm-introductory-course/blob/main/activities/Material_ACTIVITY_LINKS.md)

- Extra reading material for students: [List of links](https://github.com/vibbits/rdm-introductory-course/blob/main/activities/Material_4trainers.md)

- Course presentation:
  
  - [Latest](https://github.com/vibbits/rdm-introductory-course/tree/main/presentations)
  
  - [Previous courses](https://github.com/vibbits/rdm-introductory-course/tags)

### Learning Outcomes

Find out what you should be able to achieve after each session.

> **Session: No data, no paper: better to start with the end in mind**
> 
> - Define what is research data management.
> - Explain the meaning of FAIR.
> - Differentiate FAIR and open data.
> - Find information and resources about research data management.
> - List the benefits of good data management for the research/er.
> - List the aspects to take into account when implementing data management practices to reach FAIR data as end goal.
> - Find and explain data policy and recommendations of few journals and funders.
>
> **Session: Organising and standardising research data that underpin your publication**
>
> - To implement a system to organise and structure all data and documentation files linked to a publication during and after research.
> - To apply logical, structured and descriptive file names in their project.
> - To implement file versioning in their project (manually).
> - To use suitable data standards to make data interoperable, commonly understandable and reusable.
> 
> **Session: Make writing easier: Document & describe your data**
>
> - Implement SOP (standardoperating procedure) type of approach for your daily documentation of experiments.
> - Discuss the benefitis of make versioning more persistent by using github or related.
> - Apply minimal metadata standards for domain-specific data.
> - Describe the impact of documentation on the publication preparation
>
> **Session 5: Ethical and legal constraints on the sharing of personal data**
> 
> - Recognize and discuss the main GDPR principles.
> - Explain when is a dataset subject to the GDPR.
> - Recognize practical consequences of the GDPR.
> - Differentiate anonymous, pseudonymous and, when are data highly unique.
> - Know how to protect personal data.
> - Apply anonymization to publish/upload onto a repository and share human datasets.
> 
> **Session : A closer look at the repositories world**
> 
> - Recognize generic and discipline specific repositories.
> - Explain the different access levels and access types.
> - List considerations to be taken into account when sharing human data.
> - Mention few domain specific and restricted access repositories.
> - Verify if the data is suitable for reuse.
>
> **Session : Planning for efficiency**
> - Describe what a data management plan (DMP) is.
> - List which areas should be covered in a DMP.
> - Create a plan and select the appropriate template in DMPonline(.be)
> - Describe what types of data exist.
> - Recognize characteristics of data that need specific RDM measures (e.g. confidential data, large data).
>
> <i class="fa fa-user"></i> **Target Audience:** Researchers
> 
> <svg xmlns="http://www.w3.org/2000/svg" height="14" width="16" viewBox="0 0 576 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path d="M384 64c0-17.7 14.3-32 32-32H544c17.7 0 32 14.3 32 32s-14.3 32-32 32H448v96c0 17.7-14.3 32-32 32H320v96c0 17.7-14.3 32-32 32H192v96c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32h96V320c0-17.7 14.3-32 32-32h96V192c0-17.7 14.3-32 32-32h96V64z"/></svg> **Level:** Beginner  
>
> <i class="fa fa-lock"></i> **License:** [Creative Commons Attribution 4.0 International  License](https://creativecommons.org/licenses/by/4.0/)
> 
> <i class="fa fa-money-bill"></i> **Funding:** This project has received funding from ELIXIR Belgium.
> 
> <i class="fa fa-hourglass"></i> **Time estimation**: 12 hours
> 
> <i class="fa fa-envelope-open-text"></i> **Supporting Materials**:
>
>  1. [Exercises and solutions](https://github.com/vibbits/nextflow-workshop)
>  2. Slides
>
>    * [Day 1 Session 1](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov13_Day01_Session01_General-perspective-RDM_intro_.pdf)
>    * [Day 1 Session 2](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov13_Day01_Session02_Standardisation.pptx.pdf)
>    * [Day 1 Session 3](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov13_Day01_Session03_Documentation_and_Metadata_RDM.pdf)
>    * [Day 1 Session 4](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov13_Day01_Session04_DataPublication101.pdf)
>    * [Day 2 Session 1](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov14_Day02_Session01_Management_of_personaldata_RDM.pptx)
>    * [Day 2 Session 2](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov14_Day02_Session02_A-closer-look-at-the-repositories-world.pptx)
>    * [Day 2 Session 3](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov14_Day02_Session03_Data-Reuse-RDM.pptx)
>    * [Day 2 Session 4](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov14_Day02_Session04_Planning-for-efficiency_DMP.pdf) 
>
> <i class="fa fa-asterisk"></i> **Requirements:** The (technical) installation requirements are described in the [installations](https://vibbits-nextflow-workshop.readthedocs.io/en/latest/installations.html) section.
>
> <i class="fa fa-life-ring"></i> **Acknowledgement**: 
>
> * [ELIXIR Belgium](https://www.elixir-belgium.org/)
> * [VIB Technologies](https://www.vib.be/)
>
> <i class="fa fa-anchor"></i> **PURL**:  


### Authors

@[orcid(Alexander Botzki)](https://orcid.org/0000-0001-6691-4233), 
@[orcid(Bruna Piereck)](https://orcid.org/0000-0001-5958-0669), 
@[orcid(Flora D'Anna)](https://orcid.org/0000-0003-4665-6673), 
@[orcid(Laura Standaert)](https://orcid.org/0000-0003-1208-4160), 
@[orcid(Rafael Buono)](https://orcid.org/0000-0002-6675-3836), 
@[orcid(René Custers)](https://orcid.org/0000-0003-1382-3543), 
@[orcid(Veerle Van den Eynden)](https://orcid.org/0000-0003-2542-2747)

|  |  |
|--|--|
|[![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0001-6691-4233) Alexander Botxki | [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0001-5958-0669) Bruna Piereck |
|[![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0003-4665-6673) Flora D'Anna | [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0003-1208-4160) Laura Standaert |
| [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0002-6675-3836) Rafael Buono |[![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0003-1382-3543) René Custers |
| [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0003-2542-2747) Veerle Van den Eynden |[![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0009-0005-0193-5224) Dilza Campos |

</section>

## General context

Welcome to our Research Data Management course material repository! We are very happy to have you here.

### Schedule

Morning 1

| Time  | Session                                                                   |
| ----- | ------------------------------------------------------------------------- |
| 9h00  | No data, no paper: better to start with the end in mind                   |
| 10h30 | Coffee break                                                              |
| 10h45 | A closer look at the repositories world                                   |
| 12h30 | End of the day                                                            |

Morning 2

| Time  | Session                                                                   |
| ----- | ------------------------------------------------------------------------- |
| 9h00  | Planning for efficiency                                                   |
| 10h30 | Coffee break                                                              |
| 10h45 | Organising and standardising research data that underpin your Publication |
| 12h30 | End of the day                                                            |


Morning 3

| Time  | Session                                                                   |
| ----- | ------------------------------------------------------------------------- |
| 9h00  | Make writing easier: Document & describe your data                        |
| 10h30 | Coffee break                                                              |
| 10h45 | Ethical and legal constraints on the sharing of personal data             |
| 12h30 | End of the day                                                            |

## Citing this lesson

Please cite as:

  1. Bruna Piereck, Alexander Botzki. (2023). The training course about using TeSS (v1.0.0). Zenodo. tbc

## References

Here are some great tips for revision of the content and further reading:

- Extra material for trainers: [List of material](https://github.com/vibbits/rdm-course-2022/blob/main/activities/Material_4trainers.md)

- Interactive actives links for students: [List of links](https://github.com/vibbits/rdm-introductory-course/blob/main/activities/Material_ACTIVITY_LINKS.md)

- Extra reading material for students: [List of links](https://github.com/vibbits/rdm-introductory-course/blob/main/activities/Material_4trainers.md)


--------------------------------------------

*About ELIXIR Training Platform*

The ELIXIR Training Platform was established to develop a training community that spans all ELIXIR member states (see the list of Training Coordinators). It aims to strengthen national training programmes, grow bioinformatics training capacity and competence across Europe, and empower researchers to use ELIXIR's services and tools. 

One service offered by the Training Platform is TeSS, the training registry for the ELIXIR community. Together with ELIXIR France and ELIXIR Slovenia, VIB as lead node for ELIXIR Belgium is engaged in consolidating quality and impact of the TeSS training resources (2022-23) (https://elixir-europe.org/internal-projects/commissioned-services/2022-trp3).

The Training eSupport System was developed to help trainees, trainers and their institutions to have a one-stop shop where they can share and find information about training and events, including training material. This way we can create a catalogue that can be shared within the community. How it works is what we are going to find out in this course.

*About VIB and VIB Technologies*

VIB is an entrepreneurial non-profit research institute, with a clear focus on groundbreaking strategic basic research in life sciences and operates in close partnership with the five universities in Flanders – Ghent University, KU Leuven, University of Antwerp, Vrije Universiteit Brussel and Hasselt University.

As part of the VIB Technologies, the 12 VIB Core Facilities, provide support in a wide array of research fields and housing specialized scientific equipment for each discipline. Science and technology go hand in hand. New technologies advance science and often accelerate breakthroughs in scientific research. VIB has a visionary approach to science and technology, founded on its ability to identify and foster new innovations in life sciences.

The goal of VIB Technology Training is to up-skill life scientists to excel in the domains of VIB Technologies, Bioinformatics & AI, Software Development, and Research Data Management.

--------------------------------------------

*Editorial team for this course*

Authors: @[orcid(Alexander Botzki)](https://orcid.org/0000-0001-6691-4233), @[orcid(Bruna Piereck)](https://orcid.org/0000-0001-5958-0669)

Contributors: Finn Bacall, Aitor Apaolaza, Munazah Andrabi, Chris Child, Carole Goble, Olivier Sand

Technical Editors: Alexander Botzki

License: [![CC BY](img/picture003.jpg)](http://creativecommons.org/licenses/by/4.0/)

```json   @JSONLD
{
  "@context": "https://schema.org/",
  "@type": "LearningResource",
  "@id": "https://elixir-europe-training.github.io/ELIXIR-TrP-TeSS/",
  "http://purl.org/dc/terms/conformsTo": {
    "@type": "CreativeWork",
    "@id": "https://bioschemas.org/profiles/TrainingMaterial/1.0-RELEASE"
  },
  "description": "Strategic Use of Generative AI - this is our hands-on course for general use and research-specific use of Generative AI.",
  "keywords": "FAIR, OPEN, Generative AI, Writing, Ethics, Scripting",
  "name": "Strategic Use of Generative AI",
  "license": "https://creativecommons.org/licenses/by/4.0/",
  "educationalLevel": "beginner",
  "competencyRequired": "none",
  "teaches": [
    "Providing a background of the evolution of generative AI models",
    "Providing an overview of the features and capabilities of genAI",
    "Analysing prompt engineering techniques for different purposes",
    "Exploring several applications of genAI in academic research (afternoon session)", 
    "Providing hands-on experience with using different genAI tools for work and research purposes",
    "Critically evaluating the AI generated outcomes"
  ],
  "audience": "researchers",
  "inLanguage": "en-US",
  "learningResourceType": [
    "tutorial"
  ],
  "author": [
    {
      "@type": "Person",
      "name": "Bruna Piereck"
    },
    {
      "@type": "Person",
      "name": "Alexander Botzki"
    }
  ],
  "contributor": [
    {
      "@type": "Person",
      "name": "Christof De Bo"
    }
  ]
}
```


