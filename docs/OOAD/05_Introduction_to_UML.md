# An Introduction to UML

> OOAD 객체지향개발방법론 · 슬라이드 44–74 · 원본: [PDF](../../original/2026%20AA%204차%20-%20OOAD%20(20261126).pdf)

[← 이전: UP, RE, OOAD and Architecture Design](04_UP_RE_OOAD_Architecture.md) · [← 목차](README.md) · [다음: The Team Practice Overview →](06_Team_Practice_Overview.md)

## 슬라이드 목록

- [44. An Introduction to UML](#s44)
- [45. UML](#s45)
- [46. UML](#s46)
- [47. The UML Semantics](#s47)
- [48. UML 2.0 Diagrams](#s48)
- [49. 1\. Use Case Diagram](#s49)
- [50. Example: Uses Cases](#s50)
- [51. Use Cases (Planning / OOA)](#s51)
- [52. 2\. Class Diagram](#s52)
- [53. Example: Domain Model to DCD](#s53)
- [54. Provided Interface](#s54)
- [55. 3\. Object Diagram](#s55)
- [56. 4\. Package Diagram](#s56)
- [57. 5\. Component Diagram (+ 6. Composite Structure Diagram)](#s57)
- [58. Component Diagram](#s58)
- [59. Component Diagram은](#s59)
- [60. 7\. Deployment Diagram](#s60)
- [61. A Single Main Server](#s61)
- [62. Multiple Application Servers](#s62)
- [63. Microservice Architecture](#s63)
- [64. 8\. Sequence Diagram](#s64)
- [65. Example: Use Case → System Sequence Diagram](#s65)
- [66. System Sequence Diagram → Sequence Diagram](#s66)
- [67. The System under Consideration · External Entities](#s67)
- [68. 9\. Communication Diagram](#s68)
- [69. 10\. State (Statechart) Diagram](#s69)
- [70. 11\. Activity Diagram](#s70)
- [71. 12\. Timing Diagram](#s71)
- [72. 13\. Interaction Overview Diagram](#s72)
- [73. 13 UML Diagrams](#s73)
- [74. (이미지 슬라이드)](#s74)

---

<a id="s44"></a>

## 44. An Introduction to UML

<img src="img/p044.jpg" alt="슬라이드 44" width="720">

---

<a id="s45"></a>

## 45. UML

<img src="img/p045.jpg" alt="슬라이드 45" width="720">

- Unified Modeling Language for
  - Visualizing , Specifying , Constructing and
  - Documenting the artifacts of software-intensive systems.

- Offer vocabulary and rules for communication
  - http://www.uml.org/

- Combine the best of the best from
  - Data Modeling (Entity Relationship Diagrams)
  - Business Modeling (workflow)
  - Object Modeling
  - Component Modeling (development and reuse - middleware, COTS)

A de facto industry standard for OO development  

---

<a id="s46"></a>

## 46. UML

<img src="img/p046.jpg" alt="슬라이드 46" width="720">

- 3 ways to apply (use) UML

  - Sketch
    - Conceptual perspective
    - Informal and incomplete diagrams are created to discuss with each other.
    - Used at the Inception and OOA phases

  - Blueprint
    - Specification perspective
    - Relatively detailed design diagrams can be used for code generation.
    - Used at the OOA and OOD phases

  - Programming language
    - Implementation perspective
    - Complete executable code will be automatically generated.
    - Still under development in terms of theory, tool robustness and usability.

---

<a id="s47"></a>

## 47. The UML Semantics

<img src="img/p047.jpg" alt="슬라이드 47" width="720">

- 4-layer metamodel architecture
  - instance → model → meta model → meta-meta model

- MOF (Meta Object Facility) defines a four-layer meta model hierarchy.
  - Layer M3: Meta-meta model layer (The MOF model)
  - Layer M2: Meta model layer (The UML meta model)
  - Layer M1: Model layer (The UML model)
  - Layer M0: Information layer (the Application)

- MOF and UML are aligned.
  - The UML infrastructure contains all the concepts needed for the specification of UML and MOF.

---

<a id="s48"></a>

## 48. UML 2.0 Diagrams

<img src="img/p048.jpg" alt="슬라이드 48" width="720">

- 13 UML diagrams

---

<a id="s49"></a>

## 49. 1\. Use Case Diagram

<img src="img/p049.jpg" alt="슬라이드 49" width="720">

- Use case diagrams illustrate the name of use cases and actors, and the relationships between them.
  - Use case
    - A collection of related success and failure scenarios
    - Describing how an actor uses the system to achieve a goal (= the name of the use case)
  - Actor : something with behavior, such as a person, computer, or organization

Use Case : Process Sale  

---

<a id="s50"></a>

## 50. Example: Uses Cases

<img src="img/p050.jpg" alt="슬라이드 50" width="720">

System  

1\. Make Reservation  

Library Management System  
2\. Remove Reservation  

3\. Lend Item  
5\. Calculate Late-Return-Fee  

4\. Retuen Item  
7\. Notify Availability  

6\. Get Replacement Fee  

Librarian  
8\. Add Title  

9\. Remove Title  

10\. Update Title  

11\. Add Item  

12\. Remove Item  

13\. Update Item  

14\. Add Borrower  

15\. Remove Borrower  

16\. Update Borrower  

17\. Log-In  

18\. Log-Out  

19\. Count Loans  
Use Cases (Planning / OOA)  

Use Case Diagram  

---

<a id="s51"></a>

## 51. Use Cases (Planning / OOA)

<img src="img/p051.jpg" alt="슬라이드 51" width="720">

Use Cases (OOA / OOD)  

---

<a id="s52"></a>

## 52. 2\. Class Diagram

<img src="img/p052.jpg" alt="슬라이드 52" width="720">

- Class diagrams show the classes of the system, their inter-relationships, and the operations and attributes of the classes.
  - Domain model
  - Design class diagram (DCD)

Object / Class  
Definition  

Interfaces  
    - Provided IF · 5 Relationships
    - Required IF · between Objects / Classes

---

<a id="s53"></a>

## 53. Example: Domain Model to DCD

<img src="img/p053.jpg" alt="슬라이드 53" width="720">

Domain Model (OOA)  

Desing Class Diagram (OOD)  

---

<a id="s54"></a>

## 54. Provided Interface

<img src="img/p054.jpg" alt="슬라이드 54" width="720">

Bridge Design Pattern  

Required Interfaces  

---

<a id="s55"></a>

## 55. 3\. Object Diagram

<img src="img/p055.jpg" alt="슬라이드 55" width="720">

- Object diagrams are useful for exploring real world examples of objects and the relationships between them.
  - Shows instances of classes at a specific point of time. (i.e., snapshot)

---

<a id="s56"></a>

## 56. 4\. Package Diagram

<img src="img/p056.jpg" alt="슬라이드 56" width="720">

- Package diagrams group classes into packages and simplify complex class diagrams.
  - A package is a collection of logically related UML elements.
  - Easy to describe the layered architecture style and their composition.

(at the early iterations) · 56  
(at the later iterations)  

---

<a id="s57"></a>

## 57. 5\. Component Diagram (+ 6. Composite Structure Diagram)

<img src="img/p057.jpg" alt="슬라이드 57" width="720">

- Component diagrams depicts how components are wired together to form larger components or software systems.
  - Illustrate the logical structure and inter-dependency of arbitrarily complex systems
  - Show the internal structure (including parts and connectors) of components
  - Show run-time instances of interconnected instances collaborating over communications links

Port  

Assembly Connector  
Provided Interface  
Required Interface  

---

<a id="s58"></a>

## 58. Component Diagram

<img src="img/p058.jpg" alt="슬라이드 58" width="720">

\+  

Package Diagram  

---

<a id="s59"></a>

## 59. Component Diagram은

<img src="img/p059.jpg" alt="슬라이드 59" width="720">

논리적 구조(Logical Structure)를 표현하며,  
물리적 배치(Physical Deployment)는 고려하지 않음.  

서버 內, layer 간 프로세스 호출  

서버 간  
네트워크 통신  

---

<a id="s60"></a>

## 60. 7\. Deployment Diagram

<img src="img/p060.jpg" alt="슬라이드 60" width="720">

- Deployment diagrams depict a static view of the run-time configuration of hardware nodes and the software components running on those nodes.
  - Showing the reflected QAs like performance, availability, and scalability
  - Reflecting various deployment patterns and tactics

---

<a id="s61"></a>

## 61. A Single Main Server

<img src="img/p061.jpg" alt="슬라이드 61" width="720">

(Omitted Below)  

---

<a id="s62"></a>

## 62. Multiple Application Servers

<img src="img/p062.jpg" alt="슬라이드 62" width="720">

(Omitted Below)  

---

<a id="s63"></a>

## 63. Microservice Architecture

<img src="img/p063.jpg" alt="슬라이드 63" width="720">

(Omitted Below)  

---

<a id="s64"></a>

## 64. 8\. Sequence Diagram

<img src="img/p064.jpg" alt="슬라이드 64" width="720">

- Sequence diagrams model the collaboration of objects based on a time sequence.
  - Show how objects (or components) interact with others in a particular scenario of a use case.

  - System Sequence Diagram (SSD)
    - at system level

  - Sequence Diagram (SD)
    - at object level
    - at system components level (architecture Design)

A Sequence Diagram  
(at system level)  

---

<a id="s65"></a>

## 65. Example: Use Case → System Sequence Diagram

<img src="img/p065.jpg" alt="슬라이드 65" width="720">

System Sequence Diagram  
Use Case  
(at system level)  

---

<a id="s66"></a>

## 66. System Sequence Diagram → Sequence Diagram

<img src="img/p066.jpg" alt="슬라이드 66" width="720">

System Sequence Diagram (OOA)  

Sequence Diagram (OOD)  

---

<a id="s67"></a>

## 67. The System under Consideration · External Entities

<img src="img/p067.jpg" alt="슬라이드 67" width="720">

Port P1 with  
Provided Interface  

Port P2 with  
Required Interface  

(Omitted Below)  

Sequence Diagram (at system component level, architecture design)  

---

<a id="s68"></a>

## 68. 9\. Communication Diagram

<img src="img/p068.jpg" alt="슬라이드 68" width="720">

- Communication diagrams are used to model the dynamic behavior of the use case.
  - Called collaboration diagram
  - ≈ Sequence diagram
  - Not widely used for designing objects behaviors but explaining and documenting them.
  - More focus on showing the collaboration of objects rather than the time sequence.

\=  

Sequence Diagram  

---

<a id="s69"></a>

## 69. 10\. State (Statechart) Diagram

<img src="img/p069.jpg" alt="슬라이드 69" width="720">

- State diagrams can show different states of an entity and how an entity responds to various events by changing from one state to another.
  - Originated from the Statechart formalism
  - The history of an entity is modeled by a finite state diagram.

---

<a id="s70"></a>

## 70. 11\. Activity Diagram

<img src="img/p070.jpg" alt="슬라이드 70" width="720">

- Activity diagrams help to describe the flow of control of the target system.
  - Exploring complex business rules and operations, describing the use case and the business process.
  - It is an object-oriented equivalent of flow-charts and DFDs (data flow diagrams).

---

<a id="s71"></a>

## 71. 12\. Timing Diagram

<img src="img/p071.jpg" alt="슬라이드 71" width="720">

- Timing diagrams show the behavior of the objects in a given period of time.
  - A special form of a sequence diagram
  - The time increases from left to right and the lifelines are shown in separate compartments arranged vertically.

---

<a id="s72"></a>

## 72. 13\. Interaction Overview Diagram

<img src="img/p072.jpg" alt="슬라이드 72" width="720">

- Interaction overview diagrams focus on the overview of the flow of control of the interactions.
  - A variant of the Activity Diagram, where the nodes are the interactions or interaction occurrences.

---

<a id="s73"></a>

## 73. 13 UML Diagrams

<img src="img/p073.jpg" alt="슬라이드 73" width="720">

---

<a id="s74"></a>

## 74. (이미지 슬라이드)

<img src="img/p074.jpg" alt="슬라이드 74" width="720">

---

[← 이전: UP, RE, OOAD and Architecture Design](04_UP_RE_OOAD_Architecture.md) · [← 목차](README.md) · [다음: The Team Practice Overview →](06_Team_Practice_Overview.md)
