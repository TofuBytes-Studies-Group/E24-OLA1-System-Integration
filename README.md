# E24-OLA1-System-Integration
Research Task

## Table of Contents
1. [Introduction](#introduction)
2. [Technology Stack](#technology-stack)
3. [What is Enterprise Integration?](#what-is-enterprise-integration)
4. [Architectural Styles](#architectural-styles)
    - [Monolithic Architecture](#monolithic-architecture)
    - [Microservices Architecture](#microservices-architecture)
5. [Integration Patterns](#integration-patterns)
    - [Pipes and Filters](#pipes-and-filters)
    - [Message Broker](#message-broker)
    - [Other Patterns](#other-patterns)
6. [Diagramming Standards](#diagramming-standards)
    - [UML](#uml)
    - [DrawIO Diagrams](#DrawIO-diagrams)
    - [Mermaid Diagrams](#Mermaid-diagrams)
7. [Code Examples](#code-examples)
    - [Pipes and Filters Implementation](#pipes-and-filters-implementation)
    - [Other Patterns Implementation](#other-patterns-implementation)
8. [Conclusion](#conclusion)
9. [References](#references)

---

## Introduction
Provide an overview of the report. Briefly explain the purpose, scope, and importance of Enterprise Integration in modern software architecture. 

## Technology Stack
This section outlines the tools and technologies used throughout the project for research, documentation, development, and collaboration.
- **Git**: Used for version control to track changes, manage contributions, and maintain the history of the project.
- **GitHub/GitLab**: The platform for hosting the repository, managing issues, and collaborating with team members.
- **Visual Studio Code**: The primary text editor used for writing the report in Markdown, embedding diagrams, and formatting code snippets.
- **Markdown**: Chosen for writing the report due to its simplicity, readability, and compatibility with version control systems.
- **Mermaid**: Used for creating diagrams directly within Markdown files, allowing for easy visualization of integration patterns and architectural concepts.
- **DrawIO**: An online tool used for collaborative diagramming, especially for more complex diagrams that require interactive editing.
- **Messenger/Discord**: Used for team communication, coordinating research efforts, and sharing resources.
- **Google Scholar, YouTube, Medium**: Sources for gathering current information on Enterprise Integration and related topics.
- **Docker**: Utilized for containerizing and testing microservices to demonstrate integration patterns like Pipes and Filters.
- **C#, osv osv**: Programming language and framework chosen for implementing integration patterns and providing working examples.
- **IPhone 11 Pro Max Camera, Cap Cut for Editing**: Used to record the 5-minute video presentation summarizing the key findings from the report.
- **Google Slides**: For creating slides and visual aids to enhance the presentation.

## What is Enterprise Integration?
Define Enterprise Integration and discuss its significance in building scalable, distributed applications. Include key concepts and goals, such as interoperability, scalability, and flexibility.
#### Event Driven Integration
- **Promotes Loose couplings between components**, allowing them to operate independently. Scalability. Suitable for Micro Services.
#### Application-centric Integration
- **Particularly relevant in modern software development**, where building applications as a set of loosely coupled and independently deployable **components** is essential for scalability, maintainability and agility. It aligns well with **contemporary microservices (breaking larger problems into smaller chunks/services** architecture and API-driven development practices.

#### Summary
- **Data-centric integration** focuses on a single source of truth, ensuring data consistency and accuracy, ideal for scenarios requiring reliable data for decision making.

- **Event-driven integration** excels in environments needing real-time responsiveness and scalability, perfect for dynamic, fast-changing conditions.

- **Application-centric integration** emphasizes modularity and reusability, suited for scalable, maintainable applications, often aligning with microservices architecture and API-driven development.

## Architectural Styles
### Monolithic Architecture
Explain what Monolithic Architecture is, including its benefits and challenges. Provide examples of where it might still be relevant today.

### Microservices Architecture
Discuss the Microservices approach, focusing on its advantages over monolithic systems, such as scalability and independence of services. Include examples of industries or companies where Microservices are heavily used.

## Integration Patterns
### Pipes and Filters
- **Overview**: Describe the Pipes and Filters pattern. 
- **Diagram**: Insert a diagram illustrating how Pipes and Filters work.
- **Use Cases**: Explain where and why this pattern might be used.
  
### Message Broker
- **Overview**: Describe the Message Broker pattern.
- **Diagram**: Include a diagram to represent the Message Broker pattern.
- **Use Cases**: Provide scenarios where this pattern is applicable.

### Other Patterns
Briefly mention other common integration patterns, such as:
- **Publish-Subscribe**
- **Request-Reply**

## Diagramming Standards
### UML
- **Explanation**: Describe UML (Unified Modeling Language) and its relevance in Enterprise Integration.
- **Examples**: Provide a simple UML diagram relevant to our topic.

### Mermaid Diagrams
- **Explanation**: Explain how Mermaid can be used to create diagrams directly in Markdown.
- **Examples**: Include a Mermaid diagram example within the markdown using Mermaid syntax.

## Code Examples
### Pipes and Filters Implementation
- **Overview**: Explain the code provided.
- **Code Snippets**: Include the relevant code snippets.
- **Explanation**: Walk through the code, explaining key components and how they implement the pattern.

### Other Patterns Implementation
Follow the same format as above for any additional patterns we implement.

## Conclusion
Summarize the key points discussed in the report. Reinforce the importance of understanding and applying Enterprise Integration principles in real-world scenarios.

## References
Provide a list of all the sources we used for our research, including blogs, articles, videos, and any academic papers. Use a consistent citation style (e.g., APA, MLA) to format our references.

