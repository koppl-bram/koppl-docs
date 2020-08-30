# Basics


Koppl automation consist of 4 components:


- Workflows
- Nodes
- Data

## Workflows

Workflows are directed acyclyc graphs consisting of nodes and connections. The nodes execute in order and forward the data that is retrieved to the next node in line. It works similarly to an algorithm.
There are several ways to start a workflow:
  - A workflow can be manually triggered by clicking the "execute workflow" button.
  - A workflow can be automatically triggered by making the workflow active, which is a toggle in the top right corner.
  - A workflow can be automatically started from another workflow by using the "Execute workflow" node. 
  
  ## Nodes
  
  Nodes make up your workflow. They contain instructions for a single purpose. Nodes have to be configured by putting in the right credentials and parameters.
  
  
  For example: 
  
  The "Send Email" node has to be configured with the right SMTP credentials, and parameters have to be filled in such as the destination email address and the email body. When this node is executed it will send the email to the specified address using the specified credentials.
  
  ## Data
  
  All data is represented at the root as a JSON array. Each item has their own node execution. This means that if a trigger receives 3 data points at the same time, each node will be executed 3 times with their respective data input. Koppl works like this out-of-the-box so there is no need to worry about the amount of data points that are coming in at any given point. 
