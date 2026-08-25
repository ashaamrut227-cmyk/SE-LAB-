# Warehouse Inventory & Pallet Location Tracker

## PES University – Department of CSE
NAME : Asha
SRN : PES2UG24AM030
SECTION : 5-A(AIML)

### Lab 1: Requirements Engineering & UML Use-Case Modelling

**Problem Statement #27 – Smart Cities, Transport & Logistics**
---

## 1. Problem Context & Overview

The **Warehouse Inventory & Pallet Location Tracker** is an automated warehouse management system designed to track pallet locations in a 3D shelf environment, enforce maximum rack weight limits, and maintain accurate records of stock movements.

The system uses **barcode/RFID scanning** to identify pallets and records their movement between different warehouse locations. It also allows warehouse personnel to search inventory, track pallet locations, monitor rack capacity, and generate inventory reports.

---

## 2. Objectives

The main objectives of the system are:

* Track the exact 3D location of pallets in the warehouse.
* Validate pallet placement against rack maximum weight limits.
* Identify pallets using barcode/RFID scanning.
* Record all stock movements for traceability.
* Allow authorized users to search and monitor inventory.
* Provide inventory and movement information to the Logistics Supervisor.

---

## 3. Target Stakeholders / Actors

### Warehouse Operator

The Warehouse Operator is responsible for day-to-day warehouse activities such as:

* Scanning barcode/RFID tags.
* Storing and assigning pallets.
* Moving pallets between locations.
* Tracking pallet locations.
* Searching for inventory.

### Logistics Supervisor

The Logistics Supervisor is responsible for monitoring warehouse operations and can:

* View inventory status.
* View stock movement history.
* Search inventory information.
* Generate inventory reports.

---

## 4. Functional Requirements

The system contains exactly **5 Functional Requirements**.

| ID     | Requirement                                                   | Priority |
| ------ | ------------------------------------------------------------- | -------- |
| FR-001 | Validate pallet placement against rack maximum load capacity. | High     |
| FR-002 | Scan and identify pallets using barcode/RFID.                 | High     |
| FR-003 | Track and retrieve the current 3D location of stored pallets. | High     |
| FR-004 | Record every pallet movement with relevant movement details.  | High  |
| FR-005 | Provide inventory monitoring and reporting facilities.        | High   |

Detailed requirements are available in:

`requirements/requirements-table.md`

---

## 5. Non-Functional Requirements

The system contains exactly **2 Non-Functional Requirements**.

| ID      | Type        | Requirement                                                                                                        | Priority |
| ------- | ----------- | ------------------------------------------------------------------------------------------------------------------ | -------- |
| NFR-001 | Performance | SKU/pallet location lookup across 100,000 bins shall be completed within 100 ms under normal operating conditions. | High     |
| NFR-002 | Security    | Only authenticated and authorized warehouse personnel shall be allowed to perform restricted inventory operations. | High     |

Detailed acceptance criteria and rationale are available in:

`requirements/requirements-table.md`

---

## 6. UML Use-Case Diagram

The UML Use-Case Diagram represents the interaction between the system and its two main actors:

* **Warehouse Operator**
* **Logistics Supervisor**

The diagram includes the required:

* `«include»` relationship
* `«extend»` relationship
* System boundary
* Primary use cases
* Actor associations

### Diagram

![UML Use-Case Diagram](uml/use-case-diagram.png)

---

## 7. Main Use Cases

The major use cases represented in the system are:

1. Scan Barcode/RFID
2. Store/Assign Pallet
3. Validate Pallet Placement
4. Record Stock Movement
5. Track Pallet Location
6. Search Inventory
7. View Inventory Status
8. View Movement History
9. Generate Inventory Report

---

## 8. Use-Case Relationships

### Include Relationship

**Store/Assign Pallet** `«include»` **Validate Pallet Placement**

Whenever a pallet is assigned to a rack, the system must validate that the proposed placement does not exceed the rack's maximum load capacity.

**Record Stock Movement** `«include»` **Scan Barcode/RFID**

The pallet must be identified using its barcode/RFID before the movement can be recorded.

### Extend Relationship

**Search Inventory** `«extend»` **Track Pallet Location**

When an operator searches for a particular SKU or pallet, the system can provide its current tracked location as an extended behavior.

---

## 9. Use-Case Flow Specification

### Core Use Case

**Use Case:** Store / Assign Pallet
**Use Case ID:** UC-01
**Primary Actor:** Warehouse Operator

The flow specification contains:

* Preconditions
* Postconditions
* Main Success Scenario
* Alternate Flow

The complete specification is available in:

`use-case-flow/store-assign-pallet.md`

---

## 10. Repository Structure

```text
warehouse-inventory-pallet-tracker/
│
├── README.md
│
└── requirements-table.md
│
└── use-case-diagram.png
│
└── store-assign-pallet.md
```

---

## 11. Technologies / Modelling Tools

This lab focuses on **Requirements Engineering and UML Use-Case Modelling**.

Suggested tools for creating the UML diagram:

* Draw.io
* StarUML
* Lucidchart
* PlantUML

---

## 12. Lab Information

**University:** PES University
**Department:** Computer Science and Engineering
**Lab:** Requirements Engineering & UML Use-Case Modelling
**Problem Statement:** #27
**Domain:** Smart Cities, Transport & Logistics
**System:** Warehouse Inventory & Pallet Location Tracker

---

