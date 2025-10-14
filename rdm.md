<!--

author:   Alexander Botzki, Bruna Piereck, Flora D'Anna, Laura Standaert, Rafael Buono, René Custers, Veerle Van den Eynden, Matheus Lourenco
email:    training@vib.de
version:  1.0.1
language: en
narrator: UK English Female

icon:     https://raw.githubusercontent.com/vibbits/nextflow-workshop/2024-liascript/docs/img/logo_VIB_noTagline.svg
logo:     https://raw.githubusercontent.com/vibbits/nextflow-workshop/2024-liascript/docs/img/logo_VIB_noTagline.svg

comment:  This document provide the resources for the Research Data Management Course

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
          https://felixhao28.github.io/JSCPP/dist/JSCPP.es5.min.js

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css
link:     https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css
link:     https://raw.githubusercontent.com/vibbits/material-liascript/master/img/org.css
link:     https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.min.css

@orcid: [@0](@1)<!--class="orcid-logo-for-author-list"-->

-->

# Introduction to Research Data Management (RDM)

<section>
Hello and welcome to our Research Data Management course! We are very happy to have you here.

This is the May 2025 edition of this workshop, jointly organised by the VIB Technologies and ELIXIR Belgium.

> We are using the interactive Open Educational Resource online/offline course infrastructure called LiaScript. 
> It is a distributed way of creating and sharing educational content hosted on github.
> To see this document as an interactive LiaScript rendered version, click on the
> following link/badge:
>
> [![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/rdm.md)

### Lesson overview

> <i class="fa fa-bookmark"></i> **Description**:
> This course is composed by **8 sessions** that complement each other aiming to give an    overview of the steps of Research Data Management (RDM) based on **practical activities and discussions**. All along we focus in practical and analytical view on the **impact** of this practices **on writing and publishing** the results of researchers in scientific journals. This course contains generalized examples and life sciences dedicated examples, but the content is easily **applicable to any areas of science** and research.
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
>
> **Session 1:** **No data, no paper: better to start with the end in mind**
> 
> - Define what is research data management.
> - Explain the meaning of FAIR.
> - Differentiate FAIR and open data.
> - Find information and resources about research data management.
> - List the benefits of good data management for the research/er.
> - List the aspects to take into account when implementing data management practices to reach FAIR data as end goal.
> - Find and explain data policy and recommendations of few journals and funders.
>
> **Session 2: A closer look at the repositories world**
>
> - Recognize generic and discipline specific repositories.
> - Explain the different access levels and access types.
> - List considerations to be taken into account when sharing human data.
> - Mention few domain specific and restricted access repositories.
> 
> **Session 3: Planning for efficiency**
>
> - Describe what a data management plan (DMP) is.
> - List which areas should be covered in a DMP.
> - Create a plan and select the appropriate template in DMPonline(.be)
> - Describe what types of data exist.
> - Recognize characteristics of data that need specific RDM measures (e.g. confidential data, large data).
>   
> **Session 4: Organising and standardising research data that underpin your publication**
> 
> - To implement a system to organise and structure all data and documentation files linked to a publication during and after research.
> - To apply logical, structured and descriptive file names in their project.
> - To implement file versioning in their project (manually).
> - To use suitable data standards to make data interoperable, commonly understandable and reusable.
> 
> **Session 5: Make writing easier: Document & describe your data**
>
> - Implement SOP (standardoperating procedure) type of approach for your daily documentation of experiments.
> - Discuss the benefitis of make versioning more persistent by using github or related.
> - Apply minimal metadata standards for domain-specific data.
> - Describe the impact of documentation on the publication preparation
>
> **Session 6: Ethical and legal constraints on the sharing of personal data**
> - Recognize and discuss the main GDPR principles.
> - Explain when is a dataset subject to the GDPR.
> - Recognize practical consequences of the GDPR.
> - Differentiate anonymous, pseudonymous and, when are data highly unique.
> - Know how to protect personal data.
> - Apply anonymization to publish/upload onto a repository and share human datasets.**>
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
>    * [Day 1 Session 2](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov14_Day02_Session02_A-closer-look-at-the-repositories-world.pptx)
>    * [Day 2 Session 3](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov14_Day02_Session04_Planning-for-efficiency_DMP.pdf) 
>    * [Day 2 Session 4](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov13_Day01_Session02_Standardisation.pptx.pdf)
>    * [Day 3 Session 5](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov13_Day01_Session03_Documentation_and_Metadata_RDM.pdf)
>    * [Day 3 Session 6](https://github.com/vibbits/rdm-introductory-course/blob/main/presentations/2023nov14_Day02_Session01_Management_of_personaldata_RDM.pptx)
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
@[orcid(Matheus Pereira da Cruz Gomes Lourenço)](https://orcid.org/0000-0001-5478-4857)

</section>

## Installations

Please read this page carefully **before** the start of the workshop.

There are two options for following this workshop: 

  1. do the installations yourself & be in control of everything, 
  2. use the setup that we have provided with the installations already done. In the former case, you will have to download [Nextflow](https://www.nextflow.io/docs/edge/getstarted.html) and [Apptainer](https://apptainer.org/). In the latter case, you can follow the instructions below.

### Provided infrastructure

We will be using the Gent section of the [Flemish Supercomputing Center](https://www.vscentrum.be/), you should have already recieved instructions for creating an account. Specifically, we will be using the [Interactive and Debug](https://docs.hpc.ugent.be/Linux/interactive_debug/) cluster. The cluster is already equipped with the latest version of Nextflow, and Apptainer.

To connect to the cluster, there are two options. For the first option, there is no local setup needed, we will use the Web Interface to access the Gent VSC.

#### Option 1: Web Interface

This utilizes the OnDemand infrastructure at the VSC to launch a web-based version of VSCode for us. Using this, we don't need to make any connections to the clutser other than through the browser.

_If you normally use VSCode locally, this setup is completely seperate and won't have your usual extensions etc._

- Navigate to [https://login.hpc.ugent.be/](https://login.hpc.ugent.be/) and login with your credentials.
- Select "Interactive Apps" from the top bar -> "Code Server"
- Fill in the following settings:
  - Cluster: `donphan (interactive/debug)`
  - Time: 8 (hours)
  - Nodes: 1
  - Cores: 8
  - Select Path -> $VSC_DATA (on the left)
  - Click "Launch"!
- Wait for your job to start -> "Connect to VS Code"

This runs fully in your browser and will continue to run even when your laptop is off etc. Your job will automatically end after 8 hours. **Make sure to save your work.**

#### Option 2: Local Installation

We will be using an SSH connection in VSCode which we can create by following these instructions:

- Download Visual Studio Code ([link](https://code.visualstudio.com/download))
- Add the following extensions for a seamless integration of Nextflow and the VM in VScode:
  - In VSCode, navigate to the 'Extensions' tab, search for the SSH remote package and install it:
  - 'Remote - SSH' (ms-vscode-remote.remote-ssh).
- Modify your local `.ssh/config` file to add the configuration for the cluster - If you already connect to the Gent VSC with this machine, you don't need to do this
  - `Ctrl-Shift-P` will bring up the "command palette"
  - Type `ssh config` and select the option to modify the configuration file (select the first file)
  - Add the following code to your config file:
    ```
    Host login-gent
        User vscXXXXX # Replace Xs with your VSC ID
        HostName login.hpc.ugent.be
        IdentityFile ~/.ssh/id_rsa # This should be replaced with the path to your private key ( windows users might look like this: C:\Users\KrisDavie\Documents\VSC\vsc_id_rsa)
    ```
- Start a terminal in VSCode (select Terminal and then New Terminal)
- Connect to the cluster with the following command: `ssh login-gent`
- Optional: Start `screen` or `tmux` and do the following in the new terminal - This will keep your session alive even when you disconnect from the cluster
- Load the modules for connecting to the interactive cluster: `module swap cluster/donphan`
- Start a job using qsub: `qsub -I -l walltime=08:00:00,nodes=1:ppn=8`
- Note the node you are connected to (e.g. `node4006.donphan.os`)
- Add the following code to your config file:
  ```
  Host node4006
      User vscXXXXX # Replace Xs with your VSC ID
      HostName node4006.donphan.os
      ProxyCommand ssh login-gent -W %h:%p
      # On windows you should use
      # ProxyCommand C:\Windows\System32\OpenSSH\ssh.exe login-gent -W %h:%p
  ```
- Finally you can open a this host in VSCode by typing `Ctrl-Shift-P` and selecting `Remote-SSH: Connect to Host...` and selecting the host you just added.
  - If you didn't run qsub in a screen or tmux session, you will need to use an entire new VSCode window to connect to the host, otherwise when VSCode refreshes, the original connection will be lost and the job will end.

#### Option 3: Custom Installation

You are free to connect to the cluster however you want, but the above 2 methods are the only ones we will support in the session.

### Common Setup

- Install the Nextflow VSCcode Package - This will give you syntax highlighting and linting for Nextflow
- Open a new terminal within VSCode: Terminal -> New Terminal
- Create a new folder for the workshop
- Clone this repository into the folder: `git clone git@github.com:VIBbits/nextflow-workshop.git`
- Load the nextflow module: `module load Nextflow/23.10.0`

## Citing this lesson

Please cite as:

  1. Bruna Piereck, Olivier Sand, Yasmine Maes, Alexander Botzki. (2023). The training course about using TeSS (v1.0.0). Zenodo. tbc

## References

Here are some great tips for revision of the content and further reading:

- Extra material for trainers: [List of material](https://github.com/vibbits/rdm-course-2022/blob/main/activities/Material_4trainers.md)

- Interactive actives links for students: [List of links](https://github.com/vibbits/rdm-introductory-course/blob/main/activities/Material_ACTIVITY_LINKS.md)

- Extra reading material for students: [List of links](https://github.com/vibbits/rdm-introductory-course/blob/main/activities/Material_4trainers.md)

- Course presentation:
  
  - [Latest](https://github.com/vibbits/rdm-introductory-course/tree/main/presentations)
  
  - [Previous courses](https://github.com/vibbits/rdm-introductory-course/tags)


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
