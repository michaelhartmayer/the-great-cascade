# 🌊 The Great Cascade (TGC) Planning

TGC Planning is a comprehensive, flexible, and scalable project planning approach designed to break down complex tasks into smaller, more manageable containers. It is particularly well-suited for software development projects but can be applied to a wide range of projects that require subdividing tasks into smaller units. The key constructs in TGC Planning are Containers, Input Assets, Output Assets, Transformers, and Transformation Cost.

## 📝 Overview

A project is structured using the following constructs:

- **📦 Containers:** The units representing tasks or subtasks within a project. Containers have a Name and a Goal and serve as a "black box" where the transformation process occurs. Containers are composed of Input Assets, Output Assets, Transformers, and Transformation Cost.

  - **📥 Input Assets:** The resources required to begin a transformation process within a container.
  
  - **📤 Output Assets:** The desired results or products of the transformation process within a container.
  
  - **⚙️ Transformers:** The agents or resources responsible for transforming Input Assets into Output Assets within a container. Transformers are self-assembling and can dynamically join and leave tasks based on their skillset and the project's current needs.
  
  - **💰 Transformation Cost:** The cost associated with transforming Input Assets into Output Assets using the given Transformer(s) within a container. This cost can be calculated as a summation of internal components for subdivided containers or as an estimation for indivisible containers.

### 🔪 Subdividing Containers

Containers should be subdivided based on the complexity of tasks and the number of transformers needed. The goal is to break down containers until only one transformer is needed, representing a manageable task that can be accomplished by a single resource. To ensure a smooth flow of work between containers, subdivisions should minimize dependencies and ensure efficient resource allocation.

### 🧩 Dependencies Management

Dependencies are clearly defined as Input Assets and can be either aggregated to the parent container or maintained within a container as a list of internal dependencies. This structure allows for easy tracking and management of dependencies within the project, and any changes or removals of containers will automatically update the dependency requirements.

### 💰 Transformation Cost

1. If a container has been subdivided into smaller containers, the Transformation Cost for the parent container should be the summation of the Transformation Cost of its internal components (i.e., the smaller containers). This allows for accurate cost aggregation and a clear understanding of the total cost for that parent container.

2. If a container is indivisible (i.e., it cannot be further subdivided and requires only one transformer), the Transformation Cost should be estimated based on the effort, time, or resources required to complete the transformation. This can be expressed in terms of transformer-days, hours, or any other suitable metric.

By incorporating Transformation Cost into the TGC Planning framework, project managers can better estimate project costs, allocate resources more efficiently, and make more informed decisions about project timelines and priorities.

### 🐝 Swarming and Parallelism

TGC Planning facilitates swarming and parallelism, leading to more efficient project execution. By subdividing containers into smaller, atomic units that require only one transformer, TGC Planning allows multiple team members with the same skillset (e.g., React JS Programmers) to work on different containers simultaneously. This approach helps distribute the workload evenly across the team and make better use of available resources.

### 🌐 Self-Assembling Transformers and Elimination of Fixed Teams

TGC Planning promotes a flexible approach to resource allocation, where team members can work on any compatible task, regardless of their predefined team affiliations. In TGC Planning, transformers (team members) are self-assembling, meaning that they can dynamically join and leave tasks based on their skillset and the project's current needs.

By focusing on compatibility between transformers and containers, TGC Planning eliminates the need for fixed teams. Instead, resources can be allocated based on their skills and the specific requirements of each container. This approach encourages cross-functional collaboration and allows for a more adaptable and responsive project environment.

## 🌟 Example

Here is an example using TGC Planning:

Container Name: Customer Support Form
Goal: Add a customer support form to our landing page

Inputs:
- PRD
- TDD
- Repository with code of landing page

Outputs:
- Customer Support Form on Landing Page

Transformers:
- 1 Product Manager
- 1 Project Manager
- 2 Designers
- 1 Front-End Engineer
- 1 Back-End Engineer
- 1 QA

Transformation Cost:
- Estimated in terms of transformer-days, hours, or other suitable metrics.

This container would be further subdivided into smaller containers, such as "Add Form to Front End Code," which requires only one engineer (transformer). Dependencies are managed by connecting the outputs of previous containers to the inputs of subsequent containers.
