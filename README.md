📦 Daily ETL Pipeline — SSIS Data Warehouse Project
🧠 Overview

This project implements a Daily ETL pipeline using SQL Server Integration Services (SSIS).

The pipeline extracts transactional data from a source database, applies business transformations, and loads the processed data into a Data Warehouse (DW) destination database.

🏗 Architecture

Source Database → SSIS Transformation → Data Warehouse

Key Components

DailyETLMain.dtsx
Main SSIS package containing:

Control Flow tasks

Data Flow transformations

Error handling logic

Load sequencing

WWI_Source_DB.conmgr
Connection manager for source system

WWI_DW_Destination_DB.conmgr
Connection manager for data warehouse

Project.params
Centralized configuration parameters for environment flexibility

⚙ ETL Workflow
1️⃣ Extract

Pulls data from OLTP source tables

Supports incremental or full load (depending on implementation)

2️⃣ Transform

Data cleansing

Deduplication

Column mapping

Business rule transformations

Data type normalization

3️⃣ Load

Inserts data into DW fact and dimension tables

Maintains referential integrity

Handles load ordering

🔄 Control Flow & Data Flow

The package separates:

Control Flow

Orchestrates execution sequence

Manages task dependencies

Enables conditional logic

Data Flow

Performs extraction

Applies transformations

Loads into DW

🛠 Technologies Used

SQL Server Integration Services (SSIS)

SQL Server

Visual Studio SSDT

<img width="626" height="293" alt="image" src="https://github.com/user-attachments/assets/5b1c4b01-ecc1-4531-bf79-cb6881c8f34a" />
