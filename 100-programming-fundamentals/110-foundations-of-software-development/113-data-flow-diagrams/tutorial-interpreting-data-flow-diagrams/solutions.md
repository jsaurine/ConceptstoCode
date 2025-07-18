# Solutions

### Question 1

Define the following terms relating to data flow diagrams and give examples: external entity, data store, and process.

<details>

<summary>See answer</summary>

* **External Entity**\
  In DFDs, an external entity represents sources or data destinations outside the system, such as users or external systems. \
  &#xNAN;_&#x45;xample:_ In a banking system, a Customer is an external entity.

- **Data Store**\
  A data store in DFDs symbolizes where data is stored within the system, like databases or files. \
  &#xNAN;_&#x45;xample:_ A Customer Database storing user information.

* **Process**\
  Processes in DFDs depict activities that transform inputs into outputs. \
  &#xNAN;_&#x45;xample:_ Process Payment converts payment details into transaction records.

</details>

### Question 2

Discuss the nested hierarchy of data flow diagrams.

<details>

<summary>See answer</summary>

Data flow diagrams begin with a high-level Context Diagram (Level 0) showing the system’s interaction with external entities. Subsequent levels (Level 1, Level 2, etc.) break down processes into more detailed subprocesses, providing a deeper understanding of data flows within the system.

</details>

### **Questions 3-7 are based on the Level 1 DFD below for a railway reservation system.**

<figure><img src="../../../../.gitbook/assets/102-hacksheet-dfd (1).jpg" alt=""><figcaption></figcaption></figure>

### Question 3

Prepare a Level 0 DFD (context diagram) for this system.

<details>

<summary>See answer</summary>

![](<../../../../.gitbook/assets/image (23).png>)

</details>

### Question 4

List the external entities, data stores, and processes in the Level 1 DFD.

<details>

<summary>See answer</summary>

* **External Entities**\
  Passenger, Reservation Clerk
* **Data Stores**\
  Passenger Data Store, Reservation Data Store, Train Schedule Data Store
* **Processes**\
  Enter Passenger Details, Create Reservation, Cancel Reservation, Check Availability, Update ReservationAnswer

</details>

### Question 5

Explain the flow of passenger reservation data from when a passenger enters their details until the reservation is stored. Include the processes and data stores involved.

<details>

<summary>See answer</summary>

1. **Enter Passenger Details**\
   The passenger provides personal and travel information, which is sent to the Enter Passenger Details process.
2. **Check Availability**\
   The system verifies seat availability by consulting the Train Schedule Data Store.
3. **Create Reservation**\
   If seats are available, the Create Reservation process records the reservation details into the Reservation Data Store.
4. **Confirmation**\
   The system sends a confirmation to the passenger, completing the reservation process.

</details>

### Question 6

Describe the relationship between the 'create reservation' and 'check availability' processes. How does the system ensure a reservation is only made for available trains and seats?

<details>

<summary>See answer</summary>

The Create Reservation process depends on the Check Availability process to confirm seat availability before booking. The system workflow is as follows:

1. **Check Availability**\
   Assesses seat availability using data from the Train Schedule Data Store.
2. **Create Reservation**\
   Proceeds with booking only if Check Availability confirms availability, ensuring reservations are made exclusively for available trains and seats.Answer

</details>

### Question 7

How does the 'reservation clerk' interact with the system? What processes can the clerk initiate, and what data flows result from their interaction?

<details>

<summary>See answer</summary>

The Reservation Clerk serves as an external entity in the Railway Reservation System and interacts with the system by performing key reservation-related tasks. The clerk’s role involves handling passenger requests, managing reservations, and ensuring that data is accurately processed within the system.

The Reservation Clerk can create, cancel and modify reservations, but cannot access customer details.

</details>
