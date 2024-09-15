# OLA 2: Distributed Architecture – Modern Enterprise Architecture
 - Group: **TofuBytes**
 - Members: **Isak, Jamie & Helena**
## Objective
This assignment is focused on exploring the concepts of Enterprise and Solution Architecture as well as understanding the role of teams, integration patterns, and modern architectural practices. It also aims to provide a foundation for the exam project by allowing students to research relevant tools and technologies for building scalable, service-based enterprise applications.

---

## Table of Contents
1. [Overview](#overview)
2. [Study Materials](#study-materials)
3. [Assignment Questions](#assignment-questions)
   - [Q1: Enterprise vs Solution Architecture](#q1-enterprise-vs-solution-architecture)
   - [Q2: Role of Teams in Modern Architecture](#q2-role-of-teams-in-modern-architecture)
   - [Q3: Centralization in Architecture](#q3-centralization-in-architecture)
   - [Q4: ABCDE of Modern Architecture](#q4-abcde-of-modern-architecture)
   - [Q5: Continuous Conversation and DevOps](#q5-continuous-conversation-and-devops)
   - [Q6: Messaging Integration Patterns](#q6-messaging-integration-patterns)
   - [Q7: Messaging vs Conversation Architectures](#q7-messaging-vs-conversation-architectures)
   - [Q8: Pattern Languages](#q8-pattern-languages)
   - [Q9: Strangler Pattern](#q9-strangler-pattern)
   - [Q10: Core Architecture Diagrams](#q10-core-architecture-diagrams)
4. [Submission Guidelines](#submission-guidelines)
5. [Resources](#resources)

---

## Overview
This assignment focuses on the different aspects of modern enterprise architecture, including comparisons between enterprise and solution architectures, the role of teams, architectural centralization, and key integration patterns. The answers to the questions will provide a deep understanding of how to build and scale enterprise systems in distributed environments.

---

## Study Materials
Before answering the questions, ensure you have gone through the following resources:
- Moodle videos on Enterprise Architecture
- PowerPoint slides on Enterprise Architecture and Integration Patterns
- Suggested readings: *Team Topologies* by Matthew Skelton, *Enterprise Integration Patterns* by Gregor Hohpe, and the article by Simon Rohrer on modern enterprise architecture.

---

## Assignment Questions

### Q1: Enterprise vs Solution Architecture
- **Objective**: Explain the differences between Enterprise Architecture and Solution Architecture.
  - Describe how these roles contribute to the design of large-scale systems.
  - Reference the video: *Enterprise Architecture vs Solution Architecture*.

### Q2: Role of Teams in Modern Architecture
- **Objective**: Discuss Stefan Tilkov's views on team roles in architecture.
  - Reference the video *Practical Architecture*.
  - Summarize how *Team Topologies* views team structures and whether you agree with the importance of teams in project success.

### Q3: Centralization in Architecture
- **Objective**: Explain the reasoning behind Stefan Tilkov’s argument for centralizing certain architectural decisions.
  - Focus on his claims around centralization benefits (starting at 23:30 in *Practical Architecture*).

### Q4: ABCDE of Modern Architecture
- **Objective**: Analyze Simon Rohrer’s ABCDE comparison of modern vs. legacy architectures.
  - Provide your opinion on whether his arguments for modern architecture are persuasive.

### Q5: Continuous Conversation and DevOps
- **Objective**: Summarize Simon Rohrer’s explanation of the “Continuous Conversation” and its benefits to Saxo Bank.
  - Explain its connection to the DevOps Infinity Loop.

### Q6: Messaging Integration Patterns

#### 1. Pipes and Filters
**Description**: In the pipes and filters pattern, data is processed through a series of filters (processing stages) connected by pipes (communication channels). Each filter performs a specific transformation or processing task on the data.

**Use Case**: Data Processing Pipeline
- **Scenario**: An ETL (Extract, Transform, Load) system for data warehousing.
- **Example**: Data is extracted from various sources (pipes), passed through filters for cleaning, transformation, and enrichment, and then loaded into a database. Each filter handles a distinct processing step, such as removing duplicates, converting formats, or aggregating data.

#### 2. Request-Reply
**Description**: In the request-reply pattern, a sender sends a request message to a service and expects a reply message in return. This is a synchronous interaction where the sender waits for the response before continuing.

**Use Case**: Online Payment Processing
- **Scenario**: A web application processes credit card payments.
- **Example**: When a user submits payment details, the application sends a request to a payment gateway for authorization. The payment gateway processes the request and replies with a confirmation or error message. The web application waits for this response before informing the user of the payment status.

#### 3. Message Routing
**Description**: In the message routing pattern, messages are directed to specific destinations based on criteria such as message content, metadata, or routing rules. This helps in directing messages to appropriate services or endpoints.

**Use Case**: Order Processing System
- **Scenario**: An e-commerce platform with different fulfillment centers.
- **Example**: When an order is placed, the system routes the order message to the appropriate fulfillment center based on factors like the customer’s location or the type of product. Routing rules ensure that each order is processed by the correct center.

#### 4. Publish-Subscribe
**Description**: In the publish-subscribe pattern, a publisher sends messages to a topic or channel without knowing the subscribers. Subscribers express interest in specific topics and receive messages related to those topics.

**Use Case**: News Distribution
- **Scenario**: A news website distributing updates to subscribers.
- **Example**: A news publisher posts updates on various topics (e.g., sports, politics) to different channels. Subscribers interested in sports receive updates on sports news, while those interested in politics get updates on political news.

#### 5. Point-to-Point
**Description**: In the point-to-point pattern, messages are sent directly from a sender to a specific receiver. Each message has a single destination, and the receiver processes the message.

**Use Case**: Task Management System
- **Scenario**: An application for managing background tasks or jobs.
- **Example**: A job scheduling system sends task messages to specific worker services. Each task message is intended for one worker, which processes the task and reports back the result. This ensures that each task is handled by a single worker service.


### Q7: Messaging vs Conversation Architectures

#### Messaging Patterns (E-mail System, for example):
- **Focus on the message**: Messaging architectures emphasize the delivery of individual messages.
- **Follows the message**: The path or flow of the message is what matters, rather than the participants involved.
- **One-way communication**: In traditional messaging systems, like email, messages are sent from sender to receiver without the expectation of an immediate response.
- **Transport layer-centric**: The concern is with the reliable delivery of messages across transport mechanisms (e.g., message queues).
- **'Stateless'**: Each message is independent, and the system does not retain the state of the conversation or the participants.

#### Conversation Patterns (Chatbot System, for example):
- **Focus on participants**: Conversation architectures are concerned with the entities participating in the communication, such as people or systems.
- **Follows time**: Conversations are temporal; they involve a sequence of exchanges over time, where each message depends on previous interactions.
- **Two-way or multi-way**: Unlike messaging, conversations involve ongoing exchanges between participants.
- **Resource-centric**: Conversations focus on managing resources such as session state, participant roles, and context.
- **'Stateful'**: Conversations retain state over time, tracking the context of the communication, which makes it necessary to manage the state of the interaction.

#### Challenges for Conversation-Based Patterns:
One of the key challenges Gregor Hohpe describes is that **conversation-based patterns require waiting for a response** before the next action can be taken. This introduces complexities such as:
- **Latency**: A conversation cannot proceed without responses, making it sensitive to delays.
- **State management**: Conversations are stateful, meaning that systems must keep track of the ongoing exchange, which adds overhead compared to stateless messaging.
- **Coordination**: Managing multiple participants in a conversation can become complicated, especially in distributed systems.

#### Difference Between Pub-Sub and Subscribe-Notify:
- **Pub-sub (Publish-Subscribe)**: This messaging pattern allows publishers (senders) to send messages without knowing who the subscribers (receivers) are. Subscribers are interested in certain topics and receive messages from those topics via an intermediary, like a broker. The key here is the decoupling of publishers and subscribers.
  
  - **Example**: In a financial market system, a stock price publisher sends updates to a broker, and all subscribers interested in that stock (e.g., traders) receive the updates. The publisher does not know which traders are subscribed.

- **Subscribe-notify**: This pattern is more specific to event-driven communication. Clients subscribe to certain events or changes, and they are **notified** when there is an update. The emphasis is on notifying subscribers about specific state changes.
  
  - **Example**: In a software update system, a client subscribes to updates for a particular application. When a new update is available, the client is notified directly, triggering a download of the new version.

While both patterns involve subscriptions, the **pub-sub** pattern is more general and message-oriented, while **subscribe-notify** tends to focus on event-based, state change notifications.

### Q8: Pattern Languages
- **Objective**: Summarize the core concepts of pattern languages as described by Gregor Hohpe.

  - For patterns to be truly useful, they need to be clear and understandable, allowing practitioners to easily grasp and communicate the ideas they represent. They must be proven solutions, drawn from real-world experiences, demonstrating their effectiveness in addressing recurring problems. It’s crucial that patterns are context-aware, clearly defining the situations where they are most applicable, so they are used appropriately. Additionally, useful patterns should document both their benefits and potential trade-offs, helping practitioners make informed decisions. Reusability is also key—patterns should be general enough to apply across different scenarios while still providing specific, actionable guidance. Finally, patterns are most effective when they are part of a larger pattern language, connecting with other patterns to provide a comprehensive roadmap for solving complex problems.

### Q9: Strangler Pattern
- **Objective**: Explain the *Strangler Pattern* as described in Simon Rohrer’s article.
  - Discuss why it is considered complex and how it helps in moving away from legacy systems.

### Q10: Core Architecture Diagrams

Jesper Lowgren explains three core diagrams that are essential for describing an architecture: the Solution Overview Diagram, the Landscape Diagram, and the Solution Design Diagram. Each of these plays a distinct role in mapping the solution from different perspectives: business, infrastructure, and technical design.

Jesper Lowgren explains three core diagrams that are essential for describing an architecture: the **Solution Overview Diagram**, the **Landscape Diagram**, and the **Solution Design Diagram**. Each of these plays a distinct role in mapping the solution from different perspectives: business, infrastructure, and technical design.

#### 1. Solution Overview Diagram
**Role**: This diagram translates high-level business requirements into use cases and conceptual architectures. It provides an overview of the core business processes and shows the interactions between people, systems, and technologies at a conceptual level.

- **Purpose**: To help business owners or project managers understand the system’s functionality and how it aligns with business needs.
- **Content**: It highlights major components and interactions without going into too much technical detail. The diagram is often high-level and shows entities such as business functions, system components, user interactions, and data flow.

**Example**: A solution overview for a banking application may show how different customer segments interact with the system (e.g., loan processing, account management). It would represent customers, banking services, and communication channels (web, mobile, etc.) without going into technical implementation details.

#### 2. Landscape Diagram
**Role**: This diagram provides a more detailed view of the technical infrastructure and how the application interacts with databases, servers, and other components. It’s typically used to describe the architecture's physical or deployment aspects.

- **Purpose**: To map out the underlying infrastructure, including hardware, software, networks, and external systems, ensuring that all components are aligned and properly integrated.
- **Content**: The diagram includes databases, servers, networks, firewalls, and how they all connect. It often shows interactions between different applications and databases.

**Example**: For a healthcare system, the landscape diagram might show the integration between the hospital's internal patient records database, external cloud services for storage, and third-party APIs for insurance processing. It would also map the physical locations of servers and the flow of data across secure networks.

#### 3. Solution Design Diagram
**Role**: The solution design diagram dives deeper into how specific components within the architecture interact. It is more detailed than the solution overview and includes a more technical perspective, showing interactions between people, processes, data, applications, and technical infrastructure.

- **Purpose**: To provide a detailed representation of the solution’s functionality and technical execution. This diagram is typically used by technical architects and developers.
- **Content**: It outlines the detailed interactions between the various systems, components, and data flows. It includes specifics such as APIs, services, business logic, and how data is exchanged between systems.

**Example**: In a logistics management system, the solution design diagram would show how different systems—such as the warehouse management system, delivery tracking, and customer interface—communicate through APIs, how data flows between them, and what protocols are used for each interaction.


### Due Date:
- **Submission Deadline**: 16 September 2024

---

## Resources
- Moodle videos on Enterprise and Solution Architecture.
- PowerPoint slides on Enterprise Architecture and Integration Patterns.
- Books:
  - *Team Topologies* by Matthew Skelton
  - *Enterprise Integration Patterns* by Gregor Hohpe
- Additional reading:
  - Simon Rohrer’s article on [Modern Enterprise Architecture](https://modernenterprisearchitecture.substack.com/p/modern-enterprisearchitecture-a)

---
