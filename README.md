<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>

# Build a CI/CD Pipeline
<!-- TABLE OF CONTENTS -->
<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#introduction">Introduction</a></li>
    <li>
      <a href="#course-information">Course Information</a>
    </li>
    <li>
      <a href="#information-about-the-project">Information about the Project</a>
      <ul>
        <li><a href="#general">General</a></li>
        <li><a href="#tech-stack">Tech Stack</a></li>
      </ul>
    </li>
    <li>
      <a href="#what-i-have-done-as-part-of-the-project">What I have done as part of the project</a></li>
      <ul>
        <li><a href="#setup-of-github-actions-and-creation-of-workflow-yaml-file">Setup of GitHub Actions and creation of workflow YAML file</a></li>
        <li><a href="#implementing-workflow-steps">Implementing workflow steps</a></li>
      </ul>
    </li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>
<br>


## Introduction
This repository was created as part of IBM's "Continuous Integration and Delivery (CI/CD)" course.<br>
It's a project about building a CI/CD pipeline.<br>
Much of the code was cloned from the IBM repository: https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode<br>
<br>
TODO: Insert short intro with picture of pipeline

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>


## Course Information
Title: Continuous Integration and Delivery (CI/CD)<br>
Type: Practice Project<br>
Course Provider: IBM<br>
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>


## Information about the Project
### General
- Client: Myself
- Project Goal: Building a CI/CD pipeline. Gain a deeper understanding of Continous Integration and Continous Delivery.
- Number of Project Participants: 1 (Cloned repository of IBM. Developed the rest on my own)
- Time Period: November, 2024
- Industry / Area: DevOps
- Role: Developer
- Languages: English
- Result: CI/CD pipeline successfully built. Improved understanding of implementing Continous Integration and Continous Delivery.
<br>

### Tech Stack
With regard to my role:
TODO: Insert Tech Stack
- GitHub Actions
- XXXXX
- IBM Cloud IDE (based on Theia and Container)
- XXXXX
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>



## What I have done as part of the project

### Setup of GitHub Actions and creation of workflow YAML file
First implemented the setup for GitHub Actions: The creation of a .github/workflows folder with a workflow YML file.<br>
The name of the workflow as well as the events, the job and the runner including the container were defined.<br>

![Implement empty workflow](https://github.com/user-attachments/assets/d3d3f45d-a6e6-4123-ba7c-97f773486752)

If you check the Actions tab on the GitHub website, you will see failed workflows, as the workflow has been triggered but not yet fully implemented.

![Failed workflows](https://github.com/user-attachments/assets/c0988e0a-4227-4744-bcfa-7da8ee302a27)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>


### Implementing workflow steps
After the workflow file was created, the steps were added:

![3 Adding Steps to workflow](https://github.com/user-attachments/assets/7be106b4-808f-4422-b555-3a19ca4ce973)

The changes were pushed into the repository. This triggered the workflow again.<br>
It is now running successfully thanks to the implemented steps:

![4 Workflow successful](https://github.com/user-attachments/assets/3f758410-a722-4f49-bfaf-b319a38ba068)

After clicking on the build job, exact details of the individual steps can be viewed:

![5 Details of Workflow Steps](https://github.com/user-attachments/assets/f1720b37-6542-4e02-b174-59a6d89d619f)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>



## Getting Started
The code was only executable with the help of the IBM Cloud IDE.<br>
The IDE had many necessary tools and accesses preconfigured. These include, for example, Kubernetes installation or IBM Cloud Container Registry.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>



## Contact
If you have any questions, please feel free to reach out via email: christian-schwanse (at) gmx.net<br>
<p align="right">(<a href="#readme-top">back to top</a>)</p>
