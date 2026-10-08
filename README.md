# Airline-Management-System-SQL
Relational SQL database system for airline management, featuring automated operational triggers, stored procedures for fleet control, and complex business logic.

# Airline Management System – Relational SQL Database

## Executive Summary
**Airline Management System** is an enterprise-grade relational database solution developed in SQL Server (T-SQL) designed to model, manage, and optimize end-to-end commercial airline operations. The system handles fleet management, flight scheduling, destination logistics, passenger bookings, ticketing, crew assignment, and salary structures while enforcing complex business logic and strict transactional data integrity.

---

## System Architecture & Data Model

+------------------------------------------------------+
|             Relational Database Engine               |
|                    (SQL Server)                      |
+--------------------------+---------------------------+
                           |
  +------------------------+------------------------+
  |                        |                        |
  v                        v                        v
+------------------+  +------------------+  +------------------+
| Fleet & Aircraft |  | Flights & Routes |  | Passengers &     |
| Management       |  | Scheduling       |  | Ticketing        |
| - Airplanes      |  | - Flight Numbers |  | - Passenger Info |
| - Models         |  | - Destinations   |  | - Seat Allocation|
| - Capacity       |  | - Departure/Arr. |  | - Pricing        |
+--------+---------+  +--------+---------+  +--------+---------+
         |                     |                     |
         +---------------------+---------------------+
                               |
                               v
+------------------------------------------------------+
| Business Logic Layer (Transact-SQL)                  |
|   ├── Stored Procedures (Fleet maintenance, bookings)|
|   ├── Automated Triggers (Destination/aircraft sync) |
|   ├── User-Defined Functions (Seat occupancy, age)   |
|   └── Views & Indexes (Query optimization & reports) |
+--------------------------+---------------------------+
                           |
                           v
+------------------------------------------------------+
| Operations & HR Management                           |
|   ├── Crew & Ground Staff Allocation                 |
|   └── Salary & Payroll Auditing                      |
+------------------------------------------------------+

### Key Execution & Logic Features
1. **Relational Schema Design:** Normalized database structure (3NF) ensuring minimal data redundancy across aircraft, routes, staff, passengers, and financial transactions.
2. **Automated Triggers:** Event-driven database triggers for automatic fleet assignment, flight-destination status synchronization, and operational record auditing.
3. **Stored Procedures:** Encapsulated operational workflows including ticket issuance, maintenance-driven aircraft substitution, and flight cancellation handling.
4. **User-Defined Functions (UDFs):** Real-time calculation of seat capacity utilization, flight durations, passenger age validation, and dynamic pricing metrics.
5. **Data Integrity & Security:** Enforced Primary/Foreign key constraints, Unique indexes, Check constraints, and transactional ACID guarantees to prevent invalid state mutations.

---

## Documentation & Deliverables Breakdown

The repository includes complete technical documentation and architectural diagrams:

### 1. Database Engineering & Project Book (`Airline-Management-System-SQL.pdf`)
* **Entity-Relationship Diagram (ERD):** Complete conceptual and logical data models showing all entities, attributes, primary keys, foreign keys, and cardinalities.
* **Schema Definition & Constraints:** In-depth explanation of normalized table structures, index strategies, and data domain constraints.
* **Business Logic & T-SQL Scripts:** Detailed breakdown of procedural T-SQL implementation including triggers, stored procedures, cursor usage, and custom functions.
* **Analytical Queries & Reports:** Sample query suite covering fleet utilization rates, revenue analysis, crew scheduling, and high-density route reporting.

---

## Repository File & Directory Structure

docs/
└── Airline-Management-System-SQL.pdf  # Comprehensive database project book and technical documentation
images/
├── erd_diagram.png                     # Entity-Relationship Diagram (ERD)
├── schema_relational_model.png         # Relational schema structure screenshot
└── sample_query_results.png            # Query execution outputs and analytical reports
sql/
├── 01_schema_tables_constraints.sql   # DDL script: Table creation, PK/FK constraints, and indexes
├── 02_stored_procedures.sql            # DML/Procedural script: Business workflow procedures
├── 03_triggers.sql                    # Event triggers for automated operational logic
├── 04_functions_views.sql              # Scalar/table-valued functions and reporting views
└── 05_sample_data_and_tests.sql        # Mock data insertion and test validation suite
README.md                               # Repository overview, ERD preview, and setup guide
