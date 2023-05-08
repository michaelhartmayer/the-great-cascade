# The Great Cascade (TGC) Planning

TGC Planning is a comprehensive and flexible project planning approach designed to break down complex tasks into smaller, more manageable containers. It is particularly well-suited for software development projects but can be applied to a wide range of projects that require subdividing tasks into smaller units. The key constructs in TGC Planning are Containers, Input Assets, Output Assets, Transformers, and Transformation Cost Out.

## Overview

A project is structured using the following constructs:

- **Containers:** The units representing tasks or subtasks within a project. Containers have a Name and a Goal and serve as a "black box" where the transformation process occurs. Containers are composed of Input Assets, Output Assets, Transformers, and Transformation Cost Out.

  - **Input Assets:** The resources required to begin a transformation process within a container.
  
  - **Output Assets:** The desired results or products of the transformation process within a container.
  
  - **Transformers:** The agents or resources responsible for transforming Input Assets into Output Assets within a container.
  
  - **Transformation Cost Out:** The cost associated with transforming Input Assets into Output Assets using the given Transformer(s) within a container. This cost can be calculated as a summation of internal components for subdivided containers or as an estimation for indivisible containers.

### Subdividing Containers

Containers should be subdivided based on the complexity of tasks and the number of transformers needed. The goal is to break down containers until only one transformer is needed, representing a manageable task that can be accomplished by a single resource. To ensure a smooth flow of work between containers, subdivisions should minimize dependencies and ensure efficient resource allocation.

### Dependencies Management

Dependencies are clearly defined as Inputs and can be either aggregated to the parent container or maintained within a container as a list of internal dependencies. This structure allows for easy tracking and management of dependencies within the project, and any changes or removals of containers will automatically update the dependency requirements.

### Transformation Cost Out

1. If a container has been subdivided into smaller containers, the Transformation Cost Out for the parent container should be the summation of the Transformation Cost Out of its internal components (i.e., the smaller containers). This allows for accurate cost aggregation and a clear understanding of the total cost for that parent container.

2. If a container is indivisible (i.e., it cannot be further subdivided and requires only one transformer), the Transformation Cost Out should be estimated based on the effort, time, or resources required to complete the transformation. This can be expressed in terms of transformer-days, hours, or any other suitable metric.

By incorporating the Transformation Cost Out into the TGC Planning framework, project managers can better estimate project costs, allocate resources more efficiently, and make more informed decisions about project timelines and priorities.

## Example

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

Transformation Cost Out:
- Estimated in terms of transformer-days, hours, or other suitable metrics.

This container would be further subdivided into smaller containers, such as "Add Form to Front End Code," which requires only one engineer (transformer). Dependencies are managed by connecting the outputs of previous containers to the inputs of subsequent containers.
