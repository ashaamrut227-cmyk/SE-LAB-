# Use-Case Flow Specification – Store/Assign Pallet

## Use Case ID

UC-01

## Use Case Name

Store / Assign Pallet

## Primary Actor

Warehouse Operator

## Supporting Actor

Warehouse Inventory & Pallet Location Tracker System

## Preconditions

1. The Warehouse Operator is authenticated and authorized.
2. The pallet has a valid barcode or RFID tag.
3. The target rack and 3D shelf coordinates are available in the system.
4. The rack's maximum load capacity is recorded in the system.
5. The inventory system is operational.

## Postconditions

**Success:**

* The pallet is assigned to the selected rack, shelf, and 3D position.
* The pallet's location is updated in the inventory database.
* The rack's current load is updated.
* The stock movement is recorded with pallet ID, source location, destination location, timestamp, and operator ID.

**Failure:**

* The pallet is not assigned to the selected location.
* No invalid placement is recorded.
* The system displays the reason for rejection.

## Main Success Scenario

1. The Warehouse Operator scans the pallet's barcode/RFID tag.
2. The system identifies the pallet and retrieves its inventory details.
3. The operator selects or enters the target rack, shelf, and 3D coordinates.
4. The system retrieves the maximum load capacity of the selected rack.
5. The system calculates the expected rack load after adding the pallet.
6. The system validates that the expected load does not exceed the rack's maximum structural limit.
7. The system confirms the pallet placement.
8. The system updates the pallet's 3D location in the inventory database.
9. The system records the stock movement details.
10. The system displays a successful pallet placement confirmation.

## Alternate Flow – Rack Maximum Weight Exceeded

1. During Step 6, the system determines that the proposed placement would exceed the rack's maximum load capacity.
2. The system rejects the placement request.
3. The system displays a message indicating that the selected rack cannot safely accommodate the pallet.
4. The Warehouse Operator selects another rack or valid shelf position.
5. The system validates the new placement against the rack's load capacity.
6. If the new location is valid, the system resumes the Main Success Scenario from Step 7.
7. If no valid location is selected, the placement operation is cancelled and no inventory location is changed.
