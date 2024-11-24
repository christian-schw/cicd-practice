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
        <li><a href="#task-1---setup-of-github-actions-and-implement-a-workflow">Task 1 - Setup of GitHub Actions and implement a workflow</a></li>
        <li><a href="#task-2---building-a-tekton-pipeline">Task 2 - Building a Tekton Pipeline</a></li>
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
With regard to my role:<br>
TODO: Insert Tech Stack
- CI/CD Tool: GitHub Actions
- CI/CD Tool: Tekton
- Container Orchestration: Kubernetes
- IBM Cloud IDE (based on Theia and Container)
- XXXXX
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>



## What I have done as part of the project

### Task 1 - Setup of GitHub Actions and implement a workflow
First implemented the setup for GitHub Actions: The creation of a .github/workflows folder with a workflow YML file.<br>
The name of the workflow as well as the events, the job and the runner including the container were defined.<br>

![Implement empty workflow](https://github.com/user-attachments/assets/d3d3f45d-a6e6-4123-ba7c-97f773486752)

If you check the Actions tab on the GitHub website, you will see failed workflows, as the workflow has been triggered but not yet fully implemented.

![Failed workflows](https://github.com/user-attachments/assets/c0988e0a-4227-4744-bcfa-7da8ee302a27)

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


### Task 2 - Building a Tekton Pipeline
The first step of the task was to create a traditional Hello World program / pipeline in Tekton.<br>
<br>
The Tekton object "Task" is used for this.<br>
According to the Tekton documentation, a Task is a collection of Steps that you define and arrange in a specific order of execution as part of your continuous integration flow.<br>
<br>
The corresponding Task has been implemented in the tasks.yaml file:<br>

![Implement tasks yaml](https://github.com/user-attachments/assets/30aea9c6-0edb-43df-8f59-cd2fec5dfa5e)

It is then applied to the cluster with the following command:<br>

```
kubectl apply -f tasks.yaml
```

The Task has been successfully created:<br>

![2 Task created](https://github.com/user-attachments/assets/505756ef-3db7-44ba-8242-5aa85265b1db)

Next, a Tekton object called "Pipeline" is created that uses and executes the Task object.<br>
The implementation is in the pipeline.yaml:<br>

![3 Implement pipeline yaml](https://github.com/user-attachments/assets/dfa30ea1-423c-4bb8-8059-e14211e1b187)

It is then applied to the cluster with the following command:<br>

```
kubectl apply -f pipeline.yaml
```

The Pipeline has been successfully created:<br>

![4 Pipeline created](https://github.com/user-attachments/assets/2c57f1a8-3427-44ba-843a-ff273dd3030d)

The Pipeline is now executed with the following command:<br>

```
tkn pipeline start --showlog hello-world-pipeline
```

Output of the Pipeline:

![5 Run pipeline and display output](https://github.com/user-attachments/assets/ffafdd0b-b44f-4341-ae94-328388339d2a)

Parameters are now added to make the pipeline more flexible.<br>
Both the task and the pipeline are changed for this.<br>
<br>
The modified tasks.yaml file:<br>

![6 Add params to task](https://github.com/user-attachments/assets/a20a242e-1ad7-4f01-a71e-44a01a111414)

The changes are then applied to the cluster with the following command:<br>

```
kubectl apply -f tasks.yaml
```

The Task has been successfully created:<br>

![7 Task created](https://github.com/user-attachments/assets/2c3c3eca-24ab-4c3e-9326-fed60f870597)

The modified pipeline.yaml file:<br>

![7 5 Add params to pipeline yaml](https://github.com/user-attachments/assets/3419235b-9cb6-47f7-b614-d5dafd1ee0b0)

The changes are then applied to the cluster with the following command:<br>

```
kubectl apply -f pipeline.yaml
```

The Pipeline has been successfully created:<br>

![8 Pipeline update configured](https://github.com/user-attachments/assets/a8ca390e-5347-416a-a8dd-846b652f42b3)

The Pipeline is now executed with the following command:<br>

```
tkn pipeline start hello-world-pipeline \
  --showlog \
  -p message="Hello Tekton! I added params to pipeline!"
```

Output of the Pipeline:<br>

![9 Output of updated pipeline](https://github.com/user-attachments/assets/af834715-e163-4a79-b51e-14cdce40ef29)

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
