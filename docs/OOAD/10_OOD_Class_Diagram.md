# OOD – Class Diagram

> OOAD 객체지향개발방법론 · 슬라이드 137–180 · 원본: [PDF](../../original/2026%20AA%204차%20-%20OOAD%20(20261126).pdf)

[← 이전: Practice #3 OOD – Sequence Diagram](09_Practice3_OOD_Sequence_Diagram.md) · [← 목차](README.md) · [다음: OOD – SOLID →](11_OOD_SOLID.md)

## 슬라이드 목록

- [137. Class Diagram](#s137)
- [138. Common Class Diagram Notation](#s138)
- [139. Design Class Diagram](#s139)
- [140. Object](#s140)
- [141. From Object to Class](#s141)
- [142. Attribute Syntax - Visibility](#s142)
- [143. Attribute Syntax - Derived Attribute](#s143)
- [144. Attribute Syntax - Name](#s144)
- [145. Attribute Syntax - Type](#s145)
- [146. Attribute Syntax - Multiplicity](#s146)
- [147. Attribute Syntax - Default Value](#s147)
- [148. Attribute Syntax - Properties](#s148)
- [149. Operation Syntax - Parameters](#s149)
- [150. Operation Syntax - Type](#s150)
- [151. Operations and Methods](#s151)
- [152. Note Symbols](#s152)
- [153. Class Variable and Operation](#s153)
- [154. Operations to Access Attributes in DCDs](#s154)
- [155. Types of Class Relationship](#s155)
- [156. Dependency](#s156)
- [157. Dependency - Example](#s157)
- [158. Association](#s158)
- [159. Binary Association](#s159)
- [160. Binary Association - Navigability](#s160)
- [161. Navigability - UML Standard vs. Best Practice](#s161)
- [162. Binary Association as Attribute](#s162)
- [163. Ways to Show UML Attributes](#s163)
- [164. Attribute Text vs. Association Lines for Attributes](#s164)
- [165. Association Class](#s165)
- [166. Singleton Classes](#s166)
- [167. Active Class](#s167)
- [168. Interfaces](#s168)
- [169. Aggregation](#s169)
- [170. Shared Aggregation](#s170)
- [171. Composition](#s171)
- [172. Shared Aggregation and Composition](#s172)
- [173. Shared Aggregation and Composition](#s173)
- [174. Generalization](#s174)
- [175. Generalization - Abstract Class](#s175)
- [176. Generalization - Multiple Inheritance](#s176)
- [177. With and Without Generalization](#s177)
- [178. What’s the Relationship between Sequence and Class Diagrams?](#s178)
- [179. The Relationship to Other Artifacts](#s179)
- [180. (이미지 슬라이드)](#s180)

---

<a id="s137"></a>

## 137. Class Diagram

<img src="img/p137.jpg" alt="슬라이드 137" width="720">

---

<a id="s138"></a>

## 138. Common Class Diagram Notation

<img src="img/p138.jpg" alt="슬라이드 138" width="720">

---

<a id="s139"></a>

## 139. Design Class Diagram

<img src="img/p139.jpg" alt="슬라이드 139" width="720">

- The same UML class diagrams can be used in multiple perspectives.
  - In a conceptual perspective, Domain model
  - In a design perspective, Design Class Diagram (DCD)

---

<a id="s140"></a>

## 140. Object

<img src="img/p140.jpg" alt="슬라이드 140" width="720">

- Individuals of a system

- Alternative notation : · Object name · Class

Anonymous objects  
Attribute · Current value · = No object name  

---

<a id="s141"></a>

## 141. From Object to Class

<img src="img/p141.jpg" alt="슬라이드 141" width="720">

- A class is a construction plan for a set of similar objects of a system.
  - Objects are instances of classes.

- Attributes: structural characteristics of a class
  - Different value for each instance (object)

- Operations: behavior of a class
  - Identical for all objects of a class → not depicted in object diagram

Class · Object of the Person class  

---

<a id="s142"></a>

## 142. Attribute Syntax - Visibility

<img src="img/p142.jpg" alt="슬라이드 142" width="720">

- Who is permitted to access the attribute.
  - \+ ... public: everybody
  - - ... private: only the object itself
  - \# ... protected: class itself and subclasses
  - ~ ... package: classes that are in the same package

---

<a id="s143"></a>

## 143. Attribute Syntax - Derived Attribute

<img src="img/p143.jpg" alt="슬라이드 143" width="720">

- Attribute value is derived from other attributes or associations.
  - age: calculated from the date of birth

---

<a id="s144"></a>

## 144. Attribute Syntax - Name

<img src="img/p144.jpg" alt="슬라이드 144" width="720">

- Name of the attribute

---

<a id="s145"></a>

## 145. Attribute Syntax - Type

<img src="img/p145.jpg" alt="슬라이드 145" width="720">

- Types of attributes
  - Data types
    - Primitive data type
      - Pre-defined: Boolean, Integer, Unlimited Natural, String
      - User-defined: «primitive»
      - Composite data type: «datatype»
    - Enumerations: «enumeration»

  - User-defined classes

---

<a id="s146"></a>

## 146. Attribute Syntax - Multiplicity

<img src="img/p146.jpg" alt="슬라이드 146" width="720">

- Number of values which an attribute may contain
  - Default value: 1

- Notation: [min..max]
  - no upper limit: [\*] or [0..\*]

---

<a id="s147"></a>

## 147. Attribute Syntax - Default Value

<img src="img/p147.jpg" alt="슬라이드 147" width="720">

- Default value
  - Used if the attribute value is not set explicitly by the user

---

<a id="s148"></a>

## 148. Attribute Syntax - Properties

<img src="img/p148.jpg" alt="슬라이드 148" width="720">

- Pre-defined properties
  - {readOnly} … value cannot be changed
  - {unique} … no duplicates permitted
  - {non-unique} … duplicates permitted
  - {ordered} … fixed order of the values
  - {unordered} … no fixed order of the values

- Attribute specification
  - Set: {unordered, unique}
  - Multi-set (Bag): {unordered, non-unique}
  - Ordered set: {ordered, unique}
  - List: {ordered, non-unique}

---

<a id="s149"></a>

## 149. Operation Syntax - Parameters

<img src="img/p149.jpg" alt="슬라이드 149" width="720">

- Notation similar to attributes

- Direction of the parameter
  - in … input parameter
    - When the operation is used, a value is expected from this parameter
  - out … output parameter
    - After the execution of the operation, the parameter has adopted a new value
  - inout : combined input/output parameter

---

<a id="s150"></a>

## 150. Operation Syntax - Type

<img src="img/p150.jpg" alt="슬라이드 150" width="720">

- Types of the return value

---

<a id="s151"></a>

## 151. Operations and Methods

<img src="img/p151.jpg" alt="슬라이드 151" width="720">

- Operations
  - The full official format of the operation syntax :
    - visibility name (parameter-list) {property-string}
    - visibility name (parameter-list) : return-type {property-string} ← UML1.X
  - Guidelines
    - Assume that the new version includes a return type.
    - Operations are usually assumed public if no visibility is shown.

- An operation is not a method.
  - A UML operation is a declaration, with a name, parameters, return type, exceptions list, and possibly a set of constraints of pre-and post-conditions.
  - Not an implementation - rather, methods are implementations.

---

<a id="s152"></a>

## 152. Note Symbols

<img src="img/p152.jpg" alt="슬라이드 152" width="720">

- A UML note symbol may represent several things, such as:
  - UML note or comment, which by definition have no semantic impact
  - UML constraint, in which case it must be encased in braces '{…}’
  - Method body : the implementation of a UML operation

---

<a id="s153"></a>

## 153. Class Variable and Operation

<img src="img/p153.jpg" alt="슬라이드 153" width="720">

- Instance variable (= instance attribute) : attributes defined on instance level

- Class variable (= class attribute, static attribute)
  - Defined only once per class, i.e., shared by all instances of the class
  - Example: counters for the number of instances of a class

- Class operation (= static operation)
  - Can be used, if no instance of the corresponding class was created
  - Example: constructors, counting operations, etc.

class Person {  

public String firstName;  
Class · public String lastName;  
private Date dob;  
variable · protected String[ ] address;  
private static int pNumber;  

public static int getPNumber() {…}  
Class · public Date getDob() {…}  
operation · }  

---

<a id="s154"></a>

## 154. Operations to Access Attributes in DCDs

<img src="img/p154.jpg" alt="슬라이드 154" width="720">

- Accessing operations to retrieve or set all (private) attributes
  - Example: getPNumber() and setPNumber()

  - Often excluded (or filtered) from the class diagram, since they are too many.
    - For n attributes, there may be 2n uninteresting getter and setter operations.

  - Most UML tools support filtering their display.

- Getter/Setter are a big obstacle for securing “Object Data Encapsulation”.
  - The fastest and easiest way to summon the “Maintenance Nightmare”.

Maintenance Nightmares  

---

<a id="s155"></a>

## 155. Types of Class Relationship

<img src="img/p155.jpg" alt="슬라이드 155" width="720">

This is the Default Basic Relationship !!!  

---

<a id="s156"></a>

## 156. Dependency

<img src="img/p156.jpg" alt="슬라이드 156" width="720">

- Dependency models weakest possible relationships between classes
  - A class needs to know about another class to use objects of that class briefly.
  - Not used often in class diagram but does in component diagram.

---

<a id="s157"></a>

## 157. Dependency - Example

<img src="img/p157.jpg" alt="슬라이드 157" width="720">

- Example:
  - The updatePriceFor method receives a ProductDescription parameter object and then sends it a getPrice message.
  - Therefore, the Sale object has parameter visibility to the ProductDescription, and message-sending coupling, and thus a dependency on the ProductDescription.
  - If the latter class changed, the Sale class could be affected.

public class Sale  
{  
public void updatePriceFor( ProductDescription description )  
{  
Money basePrice = description.getPrice();  
//…  
}  
// …  
}  

---

<a id="s158"></a>

## 158. Association

<img src="img/p158.jpg" alt="슬라이드 158" width="720">

- Association models possible relationships between instances of classes
  - When objects of one class work with objects of another class for some prolonged amount of time.
  - A basic and default relationship

---

<a id="s159"></a>

## 159. Binary Association

<img src="img/p159.jpg" alt="슬라이드 159" width="720">

- Connects instances of two classes with one another

Navigability Association name · Reading direction  

Multiplicity  

Non-navigability  

Visibility · Role  

---

<a id="s160"></a>

## 160. Binary Association - Navigability

<img src="img/p160.jpg" alt="슬라이드 160" width="720">

- Navigability
  - An object knows its partner objects and can therefore access their visible attributes and operations.
  - Indicated by open arrow-head or cross

- Example:
  - “A can access the visible attributes and operations of B”
  - “B cannot access any attributes and operations of A”

- Navigability undefined
  - Bidirectional navigability is assumed.

---

<a id="s161"></a>

## 161. Navigability - UML Standard vs. Best Practice

<img src="img/p161.jpg" alt="슬라이드 161" width="720">

UML Standard · Best Practice  

---

<a id="s162"></a>

## 162. Binary Association as Attribute

<img src="img/p162.jpg" alt="슬라이드 162" width="720">

Preferable  
Our general usage  

\=  

- Java-like notation: class Professor {…}

class Student {  
public Professor[] lecturer;  
…  
}  

---

<a id="s163"></a>

## 163. Ways to Show UML Attributes

<img src="img/p163.jpg" alt="슬라이드 163" width="720">

- Attributes can be shown in three ways:

1\. attribute text (with line)  
  - visibility name : type multiplicity = default {property-string}

2\. association line  
  - a navigability arrow
  - multiplicity
  - a role name

3\. both together  

---

<a id="s164"></a>

## 164. Attribute Text vs. Association Lines for Attributes

<img src="img/p164.jpg" alt="슬라이드 164" width="720">

- Use the attribute text notation for data type objects, while the association line notation for others.
  - Both are semantically equal.
  - But showing an association line to another class box in the diagram gives visual emphasis.

public class Register  
{  
private int id;  
private Sale currentSale;  
private Store location;  
// …  
}  

---

<a id="s165"></a>

## 165. Association Class

<img src="img/p165.jpg" alt="슬라이드 165" width="720">

- Association class
  - Assign attributes to the relationship between classes rather than to a class itself.
  - Treat an association itself as a class, and model it with attributes, operations, and other features.
    - Illustrated with a dashed line from the association to the association class.
    - Necessary when modeling n:m Associations

  - Example : If a Company employs many Persons, modeled with an Employs association, you can model the association itself as the Employment class, with attributes such as salary and startDate.

---

<a id="s166"></a>

## 166. Singleton Classes

<img src="img/p166.jpg" alt="슬라이드 166" width="720">

- Singleton class has only one instance of the class.
  - "singleton" instance
  - In a UML diagram, it is marked with a '1' in the upper right corner of the name compartment.
  - The Singleton design pattern

---

<a id="s167"></a>

## 167. Active Class

<img src="img/p167.jpg" alt="슬라이드 167" width="720">

- An active object runs and controls on its own thread of execution.
  - The class of an active object is an active class.
  - In the UML, it may be shown with double vertical lines on the left and right sides of the class box.

---

<a id="s168"></a>

## 168. Interfaces

<img src="img/p168.jpg" alt="슬라이드 168" width="720">

- The UML provides several ways to show interface implementation.
  - Formally called interface realization

  - 3 Notations:
    - Socket + lollipop notation
    - Dependency line notation
    - Interface implementation

---

<a id="s169"></a>

## 169. Aggregation

<img src="img/p169.jpg" alt="슬라이드 169" width="720">

- Special form of association
  - Used to express that a class is part of another class.

- Properties of the aggregation association:
  - Transitive: if B is part of A and C is part of B, C is also part of A
  - Asymmetric: it is not possible for A to be part of B and B to be part of A simultaneously.

- Two types:
  - Shared aggregation
  - Composition

---

<a id="s170"></a>

## 170. Shared Aggregation

<img src="img/p170.jpg" alt="슬라이드 170" width="720">

- Expresses a weak belonging of the parts to a whole
  - Parts also exist independently of the whole.

- Multiplicity at the aggregating end may be &gt;1.
  - One element can be part of multiple other elements simultaneously.
  - Spans a directed acyclic graph.
  - Syntax: Hollow diamond at the aggregating end

- Example:
  - Student is part of LabClass.
  - Course is part of StudyProgram.

---

<a id="s171"></a>

## 171. Composition

<img src="img/p171.jpg" alt="슬라이드 171" width="720">

- Existence dependency between the composite object and its parts
  - One part can only be contained in at most one composite object at one specific point in time.
  - If the composite object is deleted, its parts are also deleted.
  - Multiplicity at the aggregating end is max. 1 → The composite objects form a tree.
  - Syntax: Solid diamond at the aggregating end

- Example:
  - Beamer is part of LectureHall which is part of Building.

If the Building is deleted, · The Beamer can exist without the LectureHall,  
the LectureHall is also deleted. · but if it is contained in the LectureHall, while it is deleted,  
the Beamer is also deleted.  

---

<a id="s172"></a>

## 172. Shared Aggregation and Composition

<img src="img/p172.jpg" alt="슬라이드 172" width="720">

- Which model applies?

---

<a id="s173"></a>

## 173. Shared Aggregation and Composition

<img src="img/p173.jpg" alt="슬라이드 173" width="720">

- Which model applies?

----Yes--- ---------No-------- ----Yes---  
A Tire can exist without a Car. A  
Tire belongs to one Car at most.  

A Tire cannot exist without a Car.  

A Tire can belong to multiple Cars  

A Car has one or two types of  
Tires. Several Cars may have  
the same Type of Tires.  

---

<a id="s174"></a>

## 174. Generalization

<img src="img/p174.jpg" alt="슬라이드 174" width="720">

- Everything of a general class are passed on to its subclasses.
  - Every instance of a subclass is simultaneously an indirect instance of the superclass.
  - Subclass inherits all characteristics (attributes and operations), associations, and aggregations of the superclass except private ones.
  - Subclass may have further characteristics, associations, and aggregations.

- Generalizations are transitive. Superclass

Subclasses inherit  
characteristics, associations,  
and aggregations  

A Secretary is  
an Employee and a Person  

---

<a id="s175"></a>

## 175. Generalization - Abstract Class

<img src="img/p175.jpg" alt="슬라이드 175" width="720">

- Used to highlight common characteristics of their subclasses
- Used to ensure that there are no direct instances of the superclass
  - Only its non-abstract subclasses can be instantiated.

- Notation: keyword {abstract} or class name in italic font.

No Person-object possible  

Two types of Person: Man and Woman  

---

<a id="s176"></a>

## 176. Generalization - Multiple Inheritance

<img src="img/p176.jpg" alt="슬라이드 176" width="720">

- UML allows multiple inheritance.
  - A class may have multiple super classes.
  - Not allowed for JAVA programming language

- Example:

A Tutor is both an Employee and a Student  

---

<a id="s177"></a>

## 177. With and Without Generalization

<img src="img/p177.jpg" alt="슬라이드 177" width="720">

vs.  

---

<a id="s178"></a>

## 178. What’s the Relationship between Sequence and Class Diagrams?

<img src="img/p178.jpg" alt="슬라이드 178" width="720">

- From sequence diagrams, class diagrams can be generated iteratively.
  - When we draw sequence diagrams, a set of classes and their methods that are necessary emerge.
  - Two complementary dynamic and static views are drawn concurrently and iteratively. → Dynamic Model-Driven Approach !!!

  - Example:
    - If we started with the makePayment sequence diagram, we see that a Register and Sale class definition in a class diagram can be obviously derived.

---

<a id="s179"></a>

## 179. The Relationship to Other Artifacts

<img src="img/p179.jpg" alt="슬라이드 179" width="720">

\`  

from “Applying UML and Patterns (2nd)” · 179  
from “Applying UML and Patterns (3rd)”  

---

<a id="s180"></a>

## 180. (이미지 슬라이드)

<img src="img/p180.jpg" alt="슬라이드 180" width="720">

---

[← 이전: Practice #3 OOD – Sequence Diagram](09_Practice3_OOD_Sequence_Diagram.md) · [← 목차](README.md) · [다음: OOD – SOLID →](11_OOD_SOLID.md)
