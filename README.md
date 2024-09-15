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
Stefan mentions in regard to role of teams in modern architecture he highlights the crucial role of team **organization** in modern architecture. 
Tilkov argues that successful architecture goes beyond technical solutions and emphasizes the importance of how teams are structured and how they collaborate. 
Essentially what he says is that he Values Explicit **Team-first approach** which is when you have larger teams of 50 or 25 people this Team-first idea enables the teams to do something that makes sense, that has purpose is the most motivating thing he continues.
He also Values that the book is completely **technology agnostic** meaning no need micro services to do and the ability to choose any other techonology choice. the Book doesn't try to sell you anything in that regard.
**Long-Lived teams instead of project thinking** is essentlially a shift form companies wherea project is something that is looked upon as an expection thats supposed to end as quickly as possible so you can get to the "state" of having no projects running. The shift he mentions is how the focus now is more on how "we" always can improve and always add new thing or features because the buisness is essentially depending on innovation within the services they support.
And finally how **the book focuses on actual experiences, research and collaboration** is a key point he values.

Stefan mentioned the book **Team Topologies.**
now, **what Team topologies does the book describe and do we agree with from our own experience that the team is a core part of a successfull project?**
Well, to build on that,the book describes four key team types:

1. **Stream-aligned Teams**: These teams are responsible for a specific stream of work, such as a particular product or service.
2. **Enabling Teams**: They focus on helping other teams gain skills and improve their capabilities without directly delivering software themselves.
3. **Complicated Subsystem Teams**: These handle complex or specialized subsystems that require deep technical expertise.
4. **Platform Teams**: They provide internal services and support, creating and maintaining the platforms used for software delivery.

The book also introduces three key interaction modes between teams:

1. **Collaboration**: Teams work closely together for short periods to achieve specific goals.
2. **X-as-a-Service**: One team provides a service to another, often with a formal service contract.
3. **Facilitation**: One team helps another improve its capabilities by offering guidance and support.

**From our own experience**, we can confirm that these concepts are somwhat spot on. Effective team organization and interactions are indeed central to project success and for the team chemistry. When teams are well-structured and collaborate effectively, they can address challenges more efficiently, share and leverage specialized knowledge, and deliver better outcomes. So, aligning team roles and interactions with the principles described in **Team Topologies** **can** greatly enhance the success of a project. That being said. Its not as easy as just saying we agree or disagree. Yes this is true to a degree that allows and enables such teams to develop and prosper but this also depends on the members of the team themselves. all these points can collapse if the team doesn't know how to synchronize or collaborate and grow as a team. Our experiences do infact lean on the agreeable side, as when speaking of school projects and exam projects Teams obviously (meaning us the students delivering the projects) is a core part of the successfull project if not integral.




### Q3: Centralization in Architecture 
***Stefan Tilkov explains why some things are best done centrally (for example at 23 min 30 seconds). Why do you think he is saying this? What does he claim are the benefits?***

From what we could gather from his [presentation](https://www.youtube.com/watch?v=BNTt2aLB1tg&t=7s), is what he means by this is that some things are best done centrally. He suggests that doing so helps address challenges in complex, large-scale systems and organizations. The key benefits he outlines were:

- **Consistency**: Ensuring uniform quality and standards across the organization.
- **Efficiency**: Reducing duplication and costs by managing resources centrally.
- **Specialization and Expertise**: Centralizing knowledge and skills to handle complex tasks.
- **Coordination**: Improving alignment and integration of complex systems.

Stefan also highlights how centralization can enable individuals or small teams to act independently and make quick, efficient decisions. This decentralized decision-making is possible because the core functions are centralized, allowing for more focused, consistent guidance across the organization.

Essentially, he advocates for centralizing specific areas to achieve consistency, efficiency, and specialization, ultimately improving quality, reducing costs, and enhancing security and coordination.

In summary, he thinks centralization is important because it ensures uniform quality and compliance with standards, enables more efficient use of resources, pools specialized expertise, and enhances coordination across different parts of the organization. This leads to better collaboration and smoother functioning within large systems and a happy Stefan (rip bless his soul).

### Q4: ABCDE of Modern Architecture
Do you find his arguments persuasive and if so why?

- A) **Aligning values, people, and technology.** This makes sense—if the whole team is aligned, it leads to better cooperation within the team and across areas of expertise, ensuring that all team members are on the same page.

- B) **Better, value, sooner, safer, happier.** "Better" means delivering the best possible quality of the product. In the video, he explains "value" as what makes you special. "Sooner" refers to learn faster and delivering value faster. "Safer" obviously refers to security and privacy. "Happier" means making everyone involved with the product happier, not just the customer, but also the employees and even the environment/climate.

- C) **Continuous Conversational Governance.** This is about having ongoing conversations about the architecture and involving every member in the discussion. This approach allows for a more agile design of the architecture.

- D) **DevOps at enterprise scale.** This refers to implementing DevOps on a large, enterprise-wide scale.

- E) **Evolutionary enterprise architecture.** This focuses on continuous improvement over time.

His arguments are persuasive, and even without having used them, they make a lot of sense. They focus heavily on community within the team and on CI/CD (continuous integration and continuous delivery/deployment).

### Q5: Continuous Conversation and DevOps
what ways does he say it benefits Saxo Bank? How does he connect the Continuous Conversation to the Devops Infinity Loop.

He says it helps to talk about what makes a better design, less complex, and more simple design. He says this works well in the DevOps loop because of it is a continuous conversation, the conversation will follow around the DevOps loop. He also says it works well at large scale, where you have teams of teams (teams within larger teams).


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
he goes in to more detail about the ABCDE of modern EA he discusses the ‘strangler’ pattern for moving away from legacy systems – why is this seen as a complex problem and what does the 
strangler pattern do to help?

Going from a legacy system to modern enterprise architecture is complex because you often want the system to work while transitioning, and it takes time transitioning. However, the Strangler Pattern, in combination with refactoring and anti-corruption layers, helps to upgrade a legacy system to modern enterprise architecture. This is done in small pieces at a time to reduce complexity, all while the legacy system still runs the functionalities that have not been upgraded yet.
 

### Q10: Core Architecture Diagrams

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
  - [Strangler pattern wikipedia](https://en.wikipedia.org/wiki/Strangler_fig_pattern)

---
