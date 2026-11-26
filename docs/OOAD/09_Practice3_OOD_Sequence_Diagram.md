# Practice #3 OOD – Sequence Diagram

> OOAD 객체지향개발방법론 · 슬라이드 112–136 · 원본: [PDF](../../original/2026%20AA%204차%20-%20OOAD%20(20261126).pdf)

[← 이전: Practice #2 OOA – System Sequence Diagram, Domain Model](08_Practice2_OOA_SSD_Domain_Model.md) · [← 목차](README.md) · [다음: OOD – Class Diagram →](10_OOD_Class_Diagram.md)

## 슬라이드 목록

- [112. Practice #3](#s112)
- [113. [Activity #3] OOD](#s113)
- [114. Layered Architecture](#s114)
- [115. Connections Between SSDs, System Operations and Layers](#s115)
- [116. Designing Objects: Static vs. Dynamic](#s116)
- [117. Sequence Diagram](#s117)
- [118. 4 UML Interaction Diagrams](#s118)
- [119. Sequence and Communication Diagram](#s119)
- [120. Basic Sequence Diagram Notations](#s120)
- [121. Lifeline Boxes](#s121)
- [122. 3 Types of Messages](#s122)
- [123. Order of Messages](#s123)
- [124. Message Syntax](#s124)
- [125. Other Types of Messages](#s125)
- [126. Singleton Objects](#s126)
- [127. Instance Creation and Destruction](#s127)
- [128. Messages to Classes to Invoke Static (or Class) Methods](#s128)
- [129. Combined Fragments and Operators](#s129)
- [130. alt Fragment](#s130)
- [131. opt Fragment](#s131)
- [132. loop Fragment](#s132)
- [133. break Fragment](#s133)
- [134. loop and break Fragment - Example](#s134)
- [135. The Relationship to Other Artifacts](#s135)
- [136. (이미지 슬라이드)](#s136)

---

<a id="s112"></a>

## 112. Practice #3

<img src="img/p112.jpg" alt="슬라이드 112" width="720">

OOD  

---

<a id="s113"></a>

## 113. [Activity #3] OOD

<img src="img/p113.jpg" alt="슬라이드 113" width="720">

System  
Architecture  

Component Diagram  
one by one  

Traceability Table  
System Operations + SSDs  

Sequence Diagrams · copy of  

Database  
1  
-Title: Map  
\+Item: Map · Title  
\+Borrower: Map  
1..\* · +Loan: Map · +name: String  
\+Reservation: Map · +isbn: ISBNType  
\+price: Flot  
Item · +searchTitleDB(isbn: ISBNType): Title · +loanPeriod: Integer  
\+addTtileDB(titleRef: Title): Void · +numOfItem: Integer  
\+itemID: String · +removeTitleDB(titleRef: Title): Void  
\+available: Boolean · +availalbeCount: Integer  
\+updateTitleDB(titleRef: Title): Void · +reservationCount: Integer  
\+lost: Boolean · +searchItemDB(itemID: String): Item  
\+addItemDB(itemRef: Item): Void · Magazine  
\+isBorrowed(): Boolean · Manages · +increaseAvailableCount(): Void  
\+removeItemDB(itemRef: Item): Void · +decreaseAvailableCount(): Void  

Use Cases  
\+setLost(flag: Boolean): Void · 1 · \* · +publishCycle: String  
\+searchItem(itemID: String): Item · +updateItemDV(itemRef: Item): Void · +increaseNumOfItem(): Void · +month: String  
Controller · \* · 1  
\+addItem(itemRef: Item): Void · +searchBorrowerDB(ssn: String): Borrower · Manages · +decreaseNumOfItem(): Void  
\+updateItem(itemRef: Item): Void · +addBorrowerDB(borrowerRef: Borrower): Void · +getNumOfItem(): Integer  
\+mkaeReservation() · +removeItem(itemRef: Item): Void · +removeBorrowerDB(borrowerRef: Borrower): Void · +getPrice(): Float  
\+removeReservation() · +setAvailable(flag: Boolean): Void · +updateBorrowerDB(borrowerRef: Borrower): Void · +getLoanPeriod(): Integer  
\+LendItem() · +getTitle(itemRef: Item): Title · +searchLoanDB(itemID: String): Loan · +getNewItemID(): String  
\+returnItem() · +searchLoanDB(borrwerRef: Borrower): Loan · +searchTitle(isbn: ISBNType): Title  
\+getReplacementFee() · +addLoanDB(loanRef: Loan): Void · +addTitle(titleRef: Title): Void  
\+addTitle() · 1 · +updateLoanDB(loanRef: Loan): Void · +removeTitle(titleRef: Title): Void · Book  
\+removeTitle() · +searchReservationDB(isbn: ISBNType): Reservation · +updateTitle(titleRef: Title): Void  
\+updateTitle() · +searchReservationDB(titleRef: Title): Reservation · +isReserved(titleRef: Title): Boolean · +author: String  
\+addItem() · +searchReservationDB(borrowerRef: Borrower): Resrvation[] · +increaseReservationCount(): Void  
\+removeItem() · Refer To · +addReservationDB(reservationRef: Reservation): Void · +decreaseReservationCount(): Void  
\+updateItem() · 1 +removeReservationDB(reservationrRef: Reservation): Void  
Manages · +validateDB(userID: String, password: String): Void  
\+addBorrower()  
\+removeBorrower() · 1  
\+updateBorrower() · 0..1  
\* · 1 · 1  
\+log-In() · Manages  
\+1  
\+log-Out() · Loan  
\+countLoans()  
\+checkInDate: Date · Manages · Refer to  
\+checkOutDate: Date  
\+lateReturnFee: Integer  
\+validLoan: Boolean  
\+LoanCount: Long · \*  

\+setValidLoan(flag: Boolean): Void · 0..\*  
Librarian  
\+calculateLateReturnFee(loanPeriod: Integer): Integer · +\*  
\+calculateReplacementFee(price: Float): Integer · +name: String · Manages  
Reservation  
\+searchLoan(itemID: String): Loan · +userId: String  
\+searchLoan(borrowerRef: Borrower): Loan · +password: String · +reserveDate: Date  
\+addLoan(loanRef: Loan): Void · +logInFlag: Boolean  
\+searchReservation(isbn: ISBNType): Reservation  
\+updateLoan(loanRef: Loan): Void  
\+validate(userI: String, password: String) · +searchReservation(titleRef: Title): Reservation  
\+decreaseLoanCount(): Void  
\+logOut(userID: String) · +searchReservation(borrowerRef: Borrower): Reservation[]  
\+increaseLoanCount(): Void  
\+addReservation(reservationRef: Reservation): Void  
\+getNumOfLoan(): Void  
\+removeReservation(reservationRef: Reservation): Void  
\+getItem(LoanRef: Loan): Item  
\+printNotifyCard(titleRef: Title): Void  
\+printCard(resrvationRef: Reservation): Void  
\*  
0..\* · +getTitle(reservationRef: Reservation): Title  

Borrower  
0..\*  
\+name: String  

Domain Model  
\+ssn: String  

Class Diagram · Has  
\+address: String  
\+reservationCount: Integer  
\+loanCount: Integer  
\+increaseLoanCount(): Void · Has  

1 · +decreaseLoanCount(): Void · 1  
\+increaseReservationCount(): Void  
\+decreaseReservationCount(): Void  
\+searchBorrower(ssn: String): Borrower  
\+addBorrower(borrowerRef: Borrower): Void  
\+removeBorrower(ssn: String): Void  
\+updateBorrower(borrwerRef: Borrower): Void  

---

<a id="s114"></a>

## 114. Layered Architecture

<img src="img/p114.jpg" alt="슬라이드 114" width="720">

- UML Package Diagrams illustrate the logical architecture.
  - Logical architecture: a large-scale organization of the software classes into packages, subsystems, and layers
  - Can also be summarized as Views in a Software Architecture Document (AD)

- Typical layers in object-oriented systems: 1. User Interface layer 2. Application Logic and Domain Objects layer 3. Technical Services layer

Our focus  

A partial package diagram of NextGen POS  

---

<a id="s115"></a>

## 115. Connections Between SSDs, System Operations and Layers

<img src="img/p115.jpg" alt="슬라이드 115" width="720">

- In a well-designed layered architecture,
  - The UI layer objects will forward the requests from the UI layer (system operations) onto the domain layer for handling.
  - The messages sent from the UI layer to the domain layer will be the messages illustrated on the SSDs.

---

<a id="s116"></a>

## 116. Designing Objects: Static vs. Dynamic

<img src="img/p116.jpg" alt="슬라이드 116" width="720">

- Two kinds of object models:
  - Static models help design the definition of packages, class names, attributes, and method signatures.
    - Example: UML Class diagram
  - Dynamic models help design the logic, the code, or the method bodies. (How they collaborate via messages and methods)
    - Example: UML Interaction diagrams (Sequence diagram, Communication diagram)

- Relationship between static and dynamic modeling:
  - Spend a short period of time on interaction diagrams, then switch to a wall of related class diagrams.

---

<a id="s117"></a>

## 117. Sequence Diagram

<img src="img/p117.jpg" alt="슬라이드 117" width="720">

---

<a id="s118"></a>

## 118. 4 UML Interaction Diagrams

<img src="img/p118.jpg" alt="슬라이드 118" width="720">

Sequence diagram · Timing diagram  

Communication diagram · Interaction Overview diagram  

---

<a id="s119"></a>

## 119. Sequence and Communication Diagram

<img src="img/p119.jpg" alt="슬라이드 119" width="720">

- Sequence diagrams public class A
  - Modeling the collaboration of objects based on a time sequence · { private B myB = new B();

public void doOne()  
{  
- Communication diagrams · myB.doTwo(); myB.doThree();
  - Focusing on showing the collaboration of objects rather than the time sequence · } // …

}  

---

<a id="s120"></a>

## 120. Basic Sequence Diagram Notations

<img src="img/p120.jpg" alt="슬라이드 120" width="720">

- Lifeline boxes and lifelines
- Messages
- Execution specification

---

<a id="s121"></a>

## 121. Lifeline Boxes

<img src="img/p121.jpg" alt="슬라이드 121" width="720">

- Lifeline boxes
  - Represent the participants in the interaction, informally and practically
    - object(s), class, subsystem, component, etc.
  - Usually called roles

---

<a id="s122"></a>

## 122. 3 Types of Messages

<img src="img/p122.jpg" alt="슬라이드 122" width="720">

- Synchronous message
  - Sender waits until it has received a response message before continuing.
  - An execution specification is inserted at target.

- Response message
  - Corresponding to a synchronous message like acknowledgement
  - May be omitted if content and location are obvious

- Asynchronous message
  - Sender continues without waiting for a response message.

---

<a id="s123"></a>

## 123. Order of Messages

<img src="img/p123.jpg" alt="슬라이드 123" width="720">

… on one lifeline · … on different lifelines · … on different lifelines  
which exchange messages  

&lt;&lt; Happens before &gt;&gt;  

---

<a id="s124"></a>

## 124. Message Syntax

<img src="img/p124.jpg" alt="슬라이드 124" width="720">

return = message (parameter: parameterType) : returnType  

- For example: initialize(code) initialize d = getProductDescription(id) d = getProductDescription(id:ItemID) d = getProductDescription(id:ItemID) : ProductDescription

Recieve event  
aDate = getDate( )  

getDate( ) · Execution specification  
Send event  

---

<a id="s125"></a>

## 125. Other Types of Messages

<img src="img/p125.jpg" alt="슬라이드 125" width="720">

- Found message
  - Sender of a message is unknown or not relevant.

- Lost message
  - Receiver of a message is unknown or not relevant.

- Time-consuming message
  - Message with duration : Express that time elapses between the sending and the receipt of a message
  - Usually, messages are assumed to be transmitted without any loss of time.

---

<a id="s126"></a>

## 126. Singleton Objects

<img src="img/p126.jpg" alt="슬라이드 126" width="720">

- There is only one instance of a class instantiated : a singleton object
  - Implying to the Singleton design pattern

---

<a id="s127"></a>

## 127. Instance Creation and Destruction

<img src="img/p127.jpg" alt="슬라이드 127" width="720">

- To create an instance of a class
  - The UML mandates dashed line.
  - The message name create is not required;
    - Anything is legal, but it's a UML idiom.

- To show explicit destruction of an object
  - The &lt;&lt;destroy&gt;&gt; stereotyped message, with the large X and short lifeline indicates explicit object destruction

---

<a id="s128"></a>

## 128. Messages to Classes to Invoke Static (or Class) Methods

<img src="img/p128.jpg" alt="슬라이드 128" width="720">

- You can show class or static method calls by
  - using a lifeline box label that indicates the receiving object is a class, or
  - more precisely, an instance of a metaclass

public class Foo  
{  
public void doX()  
{  
// static method call on class Calendar  
Locale[] locales = Calendar.getAvailableLocales();  
// …  
}  
// …  
}  

---

<a id="s129"></a>

## 129. Combined Fragments and Operators

<img src="img/p129.jpg" alt="슬라이드 129" width="720">

- 12 predefined types of operators
  - Model various control structures with frames
    - Frames : regions or fragments of the diagrams, which has an operator and a guard
  - Frames are nested freely.

---

<a id="s130"></a>

## 130. alt Fragment

<img src="img/p130.jpg" alt="슬라이드 130" width="720">

- To model alternative sequences

- Similar to switch statement in Java
  - Guards are used to select the one path to be executed.
  - Multiple operands

- Guards
  - Modeled in square brackets
  - default: true
  - predefined: [else]

- Guards have to be disjoint to avoid non-deterministic behavior.

---

<a id="s131"></a>

## 131. opt Fragment

<img src="img/p131.jpg" alt="슬라이드 131" width="720">

- To model an optional sequence

- Similar to if statement without else branch
  - Exactly one operand
  - Actual execution at runtime is dependent on the guard.

---

<a id="s132"></a>

## 132. loop Fragment

<img src="img/p132.jpg" alt="슬라이드 132" width="720">

- To model repeatedly-executed sequences
  - Exactly one operand
- Keyword loop followed by the minimal/maximal number of iterations
  - (min..max) or (min,max)
  - default: (\*) .. no upper limit
- Guard
  - Evaluated as soon as the minimum number of iterations has taken place
  - Checked for each iteration within the (min,max)limits
  - If the guard evaluates to false, the execution of the loop is terminated.

Max  
Min  
Guard · Notation alternatives:  
loop(3,8) = loop(3..8)  
loop is executed at least once, · loop(8,8) = loop (8)  
as long as a&lt;1 is true. · loop = loop(\*) = loop(0,\*)  

---

<a id="s133"></a>

## 133. break Fragment

<img src="img/p133.jpg" alt="슬라이드 133" width="720">

- Similar to exception handling
  - Exactly one operand with a guard

- If the guard is true:
  - Interactions within this operand are executed.
  - Remaining operations of the surrounding fragment are omitted.
  - Interaction continues in the next higher level fragment.

Not executed if break is executed  

---

<a id="s134"></a>

## 134. loop and break Fragment - Example

<img src="img/p134.jpg" alt="슬라이드 134" width="720">

---

<a id="s135"></a>

## 135. The Relationship to Other Artifacts

<img src="img/p135.jpg" alt="슬라이드 135" width="720">

\`  

from “Applying UML and Patterns (3rd)” · from “Applying UML and Patterns (2nd)”  

---

<a id="s136"></a>

## 136. (이미지 슬라이드)

<img src="img/p136.jpg" alt="슬라이드 136" width="720">

---

[← 이전: Practice #2 OOA – System Sequence Diagram, Domain Model](08_Practice2_OOA_SSD_Domain_Model.md) · [← 목차](README.md) · [다음: OOD – Class Diagram →](10_OOD_Class_Diagram.md)
