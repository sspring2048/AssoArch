# Object-Oriented Software Development

> OOAD 객체지향개발방법론 · 슬라이드 23–35 · 원본: [PDF](../../original/2026%20AA%204차%20-%20OOAD%20(20261126).pdf)

[← 이전: UP (Unified Process)](02_Unified_Process.md) · [← 목차](README.md) · [다음: UP, RE, OOAD and Architecture Design →](04_UP_RE_OOAD_Architecture.md)

## 슬라이드 목록

- [23. Object-Oriented Software Development](#s23)
- [24. Software Development Methodology (SW개발방법론)](#s24)
- [25. Procedural Programming](#s25)
- [26. A Procedural Program](#s26)
- [27. Structured Analysis and Structured Design](#s27)
- [28. An Object-Oriented Programming](#s28)
- [29. Object-Oriented Program](#s29)
- [30. Object-Oriented Analysis and Design (OOAD)](#s30)
- [31. Domain Model → Design Class Diagram](#s31)
- [32. System Sequence Diagram → Sequence Diagram](#s32)
- [33. An OOAD Example – Dice Game](#s33)
- [34. UP - OOAD](#s34)
- [35. (이미지 슬라이드)](#s35)

---

<a id="s23"></a>

## 23. Object-Oriented Software Development

<img src="img/p023.jpg" alt="슬라이드 23" width="720">

---

<a id="s24"></a>

## 24. Software Development Methodology (SW개발방법론)

<img src="img/p024.jpg" alt="슬라이드 24" width="720">

- Methods helping software development (i.e., implementation / coding)
  - Ensuring that sufficient requirements analysis and design are conducted prior to implementation/coding/testing

  - Procedural programming : SASD (Structured Analysis and Structured Design, 구조적 분석설계 방법론)
  - Object-Oriented programming : OOAD (Object-Oriented Analysis and Design, 객체지향 개발 방법론)

( C , Python ) · &lt; SW 개발방법론 &gt;  

Software Development · Procedural Programming · SASD  
Object-Oriented Programming · OOAD  
( C++ , JAVA , Python)  

---

<a id="s25"></a>

## 25. Procedural Programming

<img src="img/p025.jpg" alt="슬라이드 25" width="720">

- A program is organized with procedures.
  - Procedure/Function
    - Building-block of procedural programs
    - Statements changing values of variables
  - Focusing on data structures, algorithms, and sequencing of steps
    - Algorithm : a set of instructions for solving a problem (Control-Centric)
    - Data structure : a construct used to organize data in a specific way (Data-Centric)

  - Most computer languages (from FORTRAN to C) are procedural ones.

struct account {  
Procedure 1: Deposit( ) {...} · char name;  
int accountId;  
Procedure 2: Withdraw( ) {...} · float balance;  
float interestYTD;  
Procedure 3: Transfer( ) {...} · &lt;&lt;Use&gt;&gt; · char accountType;  
};  
Procedures (with Algorithms) · Data Structure  

---

<a id="s26"></a>

## 26. A Procedural Program

<img src="img/p026.jpg" alt="슬라이드 26" width="720">

Read /  
WRITE  
WRITE  

READ  

---

<a id="s27"></a>

## 27. Structured Analysis and Structured Design

<img src="img/p027.jpg" alt="슬라이드 27" width="720">

- SASD (Structured Analysis and Structured Design)
  - A traditional software development methodology for procedural programs like C
  - Structural modeling in Top-Down Divide &amp; Conquer manner
    - Divide large, complex problems into smaller, more easily handled ones
  - Functional view of the problem using DFD (Data Flow Diagram)
    - Control functionalities using FSM (Finite State Machine)

DFD Level 0  

…  

An FSM for 2.1.1 Controller  

DFD Level 3  

---

<a id="s28"></a>

## 28. An Object-Oriented Programming

<img src="img/p028.jpg" alt="슬라이드 28" width="720">

- A program is organized with objects.
  - Objects
    - Consisting of data and operations
    - Encapsulation (→ Information Hiding), Inheritance, Polymorphism
  - Providing system functionalities through object communications
    - Object communication : an object calls an operation of other objects with its data

Professor  

-name: String  
-age: Integer · client · yoo : Professor  
Class · -speciality: String  
\+getName(): String · What’s your name?  
\+getAge(): Integer  
\+getSpeciality(): String · yoo.getName()  
1 : getName()  
client · Prof. Yoo  
name  
yoo : Professor  

Object · name = Yoo  
age = 43  
speciality = Software Engineering  

---

<a id="s29"></a>

## 29. Object-Oriented Program

<img src="img/p029.jpg" alt="슬라이드 29" width="720">

Object를 (다수) 만들지 않고 기능을 구현한 경우.  

---

<a id="s30"></a>

## 30. Object-Oriented Analysis and Design (OOAD)

<img src="img/p030.jpg" alt="슬라이드 30" width="720">

- OO (Object-Oriented)
  - “Providing system functionalities through object communications”

- OOAD (Object-Oriented Analysis and Design, 객체지향개발방법론)
  - “Identifying your requirements and creating a domain model, and then add methods to the appropriate classes, and define the messaging between the objects to fulfill the requirements”

  - Object-Oriented Analysis (OOA)
    - Identify requirements → Use-Case model
    - Discover the domain concepts/objects → Domain model
  - Object-Oriented Design (OOD)
    - Define software objects (static model) → Class diagram
    - Define how they collaborate to fulfill requirements (dynamic model) → Sequence diagram

  - Applicable to various development process models : Waterfall, UP (Iterative, Agile)

- OOAD should be a dynamic model-driven approach to avoid “maintenance nightmare”
  - OOAD involves deep principles (e.g., SOLID).
  - Deciding what methods belong to where and how objects should interact carries consequences should be undertaken seriously. Maintenance Nightmare

---

<a id="s31"></a>

## 31. Domain Model → Design Class Diagram

<img src="img/p031.jpg" alt="슬라이드 31" width="720">

Domain Model (OOA)  

Design Class Diagram (OOD)  

---

<a id="s32"></a>

## 32. System Sequence Diagram → Sequence Diagram

<img src="img/p032.jpg" alt="슬라이드 32" width="720">

System Sequence Diagram (OOA)  

Sequence Diagram (OOD)  

---

<a id="s33"></a>

## 33. An OOAD Example – Dice Game

<img src="img/p033.jpg" alt="슬라이드 33" width="720">

OOA · OOD  

Use Case : Play a Dice Game  
- Player requests of the system to roll the dice.
- System rolls the dice.
- System presents results.
- If the dice’s face value totals seven, player wins; otherwise, player loses.

Sequence Diagram  

Dynamic model-driven !!!  

Domain Model · Design Class Diagram  

---

<a id="s34"></a>

## 34. UP - OOAD

<img src="img/p034.jpg" alt="슬라이드 34" width="720">

Domain Model  

Use-Case Model  
(+System Sequence Diagram)  

OOA  
OOD  

Sequence Diagrams  

Class Diagram  

The dynamic model-driven approach!!! · OOI  

---

<a id="s35"></a>

## 35. (이미지 슬라이드)

<img src="img/p035.jpg" alt="슬라이드 35" width="720">

---

[← 이전: UP (Unified Process)](02_Unified_Process.md) · [← 목차](README.md) · [다음: UP, RE, OOAD and Architecture Design →](04_UP_RE_OOAD_Architecture.md)
