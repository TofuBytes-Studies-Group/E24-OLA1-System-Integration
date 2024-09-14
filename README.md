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

So, from watching the video [Enterprise Architecture vs Solution Architecture](https://www.youtube.com/watch?v=v6xBGN2A0hM) he mentions that there are quite a few differences between **Enterprise Architecture (EA)** and **Solution Architecture (SA)** as far as we’ve been able to pick up. In frameworks he also mentions like TOGAF, architecture is split into four key levels. Three of these levels function within Enterprise Architecture:

1. **Strategic Architecture**
2. **Segment Architecture**
3. **Capability Architecture**

And then there’s the 4th level, which is **Solution Architecture**. Before diving into Solution Architecture, let’s go over the differences between these roles.

Enterprise Architecture, especially within the first three levels, is all about strategy, long-term planning, and ensuring that the technology systems align with the business’s overall objectives. Think of **Strategic Architecture** as the top-level vision, defining where the organization wants to go. Then, **Segment Architecture** breaks this down into different parts or "segments" of the business, each with its own needs but all aligned with that top-level strategy. Finally, **Capability Architecture** focuses on what the organization *can* do, identifying the core competencies it needs to develop to meet those strategic goals.

Now, when we get to **Solution Architecture**, the focus shifts from high-level planning to actual products and solutions. This is the stage where we specify the detailed implementation of the capabilities defined earlier in the enterprise architecture. Unlike the **Capability Architecture**, which defines what the organization needs to be capable of, **Solution Architecture** deals with the actual "how." It's where we start talking about the real-world systems and applications needed to deliver those capabilities.

For example, in **Enterprise Architecture**, you wouldn’t necessarily discuss the specific details of an application. You’d instead focus on ensuring the right capabilities are in place, like moving towards cloud computing or building strong data management systems. However, when we step into **Solution Architecture**, we’re no longer just talking strategy—we’re specifying which technologies, platforms, or applications are required to bring those capabilities to life. This is where the **Solution Architect** comes in, designing systems that align with the broader goals laid out by the enterprise architects.

In simple terms, **Enterprise Architecture** is about laying the roadmap, while **Solution Architecture** is about building the car that drives on that roadmap. EA operates at a higher, long-term strategic level, whereas SA gets into the nitty-gritty of delivering specific projects or products.

 ### When designing large-scale systems, Enterprise Architecture (EA) and Solution Architecture (SA) contribute at different levels but are both essential.
#### Enterprise Architecture (EA):
EA focuses on the strategic, long-term vision, ensuring that all technology systems align with business objectives. It defines company-wide principles, such as system integration, technology standards, and security requirements. In large-scale systems, EA sets the architectural framework, ensuring that the system will integrate seamlessly into the organization’s broader ecosystem.

#### Solution Architecture (SA):
SA operates on a project-specific level, designing the technical solutions for individual systems within the framework set by EA. It specifies the technology stack, APIs, and detailed functional requirements, ensuring the system meets the business needs while adhering to enterprise guidelines.

#### Collaboration:
EA provides the roadmap, while SA delivers the detailed solutions that fit within that roadmap. Together, they ensure systems are scalable, aligned with - business goals, and technically sound.

So to sum it up, **Enterprise Architecture** ensures the organization is heading in the right direction from a technology perspective. It defines the capabilities and frameworks that guide everything. **Solution Architecture**, on the other hand, takes those ideas and turns them into actionable solutions, detailing how specific technologies and systems will be implemented to meet the organization’s needs.



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
- **Objective**: Identify and describe five messaging integration patterns, including the *Pipes and Filters* and *Request-Reply* patterns.
  - Use the PowerPoint slides on integration patterns as your reference.
  - Provide real-world use cases and, optionally, code examples for these patterns.

### Q7: Messaging vs Conversation Architectures
- **Objective**: Discuss the difference between messaging and conversation architectures as explained by Gregor Hohpe.
  - Focus on challenges like pub-sub vs. subscribe-notify models (starting at 18 minutes in *Enterprise Integration Patterns 2*).

### Q8: Pattern Languages
- **Objective**: Summarize the core concepts of pattern languages as described by Gregor Hohpe.

  - For patterns to be truly useful, they need to be clear and understandable, allowing practitioners to easily grasp and communicate the ideas they represent. They must be proven solutions, drawn from real-world experiences, demonstrating their effectiveness in addressing recurring problems. It’s crucial that patterns are context-aware, clearly defining the situations where they are most applicable, so they are used appropriately. Additionally, useful patterns should document both their benefits and potential trade-offs, helping practitioners make informed decisions. Reusability is also key—patterns should be general enough to apply across different scenarios while still providing specific, actionable guidance. Finally, patterns are most effective when they are part of a larger pattern language, connecting with other patterns to provide a comprehensive roadmap for solving complex problems.

### Q9: Strangler Pattern
- **Objective**: Explain the *Strangler Pattern* as described in Simon Rohrer’s article.
  - Discuss why it is considered complex and how it helps in moving away from legacy systems.

### Q10: Core Architecture Diagrams
- **Objective**: List and explain the three core architecture diagrams described by Jesper Lowgren.
  - Provide examples of each diagram and explain their roles in solution architecture.


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