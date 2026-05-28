Utilises SQL code to create a relational database after planning database design. 

This repository contains all deliverables for the Monash Functions (MF) data modelling and database design assessment. It includes:

* **mf_normalisation.pdf** — Full normalisation (UNF → 3NF).
* **mf_logical.pdf** — Final logical model exported from Oracle Data Modeler.
* **mf_oraclemodel.zip** — Complete Oracle Data Modeler project (logical + relational models).
* **mf_schema.sql** — Generated database schema (CREATE TABLE statements).
* **mf_schema_output.txt** — Oracle spool output confirming successful table creation.
* **mf_assumptions.pdf** — Documented modelling assumptions.
* **mf_G18_diaryAss1B.pdf** — Team diary.
* **Database_Design_Project_Instructions.docx** — The instructions given by the university (i.e., the Monash Functions brief and all specific conditions that must be met by the database design).

The repository supports a full data-modelling workflow for the Monash Functions booking system, covering customer registration, function bookings, chefs, cuisine specialisations, function rooms, room availability, evaluations, costing components, and decoration themes.

## Tasks

### Task 1: Normalisation to 3NF
Perform normalisation to 3NF for the data depicted in the sample Monash Functions reports. Note that only one normalisation is required for each of the provided form types. You have been provided with two samples of the room evaluation form so you can appreciate some of the variety that occurs.

The approach you are required to use is the same approach as shown in the normalisation tutorial solution from the Normalisation activity on Ed. The normalisation must be carried out form by form, beginning by representing the document you are working on as a single UNF relation and then moving through 1NF, 2NF and 3NF. 

During normalisation, you must:
* **Not add surrogate keys.** * **Include all attributes** (you must not remove any attribute as derivable).
* **Clearly show** UNF, 1NF, 2NF and 3NF.
* **Clearly show all candidate keys** for each relation in 1NF.
* **Clearly identify the Primary Key** in all relations by underlining the PK attribute/s.
* **Clearly identify all dependencies** at the various normalisation stages (Partial at 1NF, Transitive at 2NF and Full at 3NF). You should use the same notation as depicted in the normalisation sample solutions, for example: `attr1 -> attr2, attr3`
  * *If none exist, you must note this by stating:* `No partial dependencies present` and/or `No transitive dependencies present`
* **Carry out attribute synthesis.**
* **Maintain consistency:** The relation and attribute names used throughout your normalisation and those on your subsequent logical model must be the same.

### Task 2: Logical Level Design
Based on your group’s Assignment 1 Conceptual model, your marker's feedback, your reading of this case study, and the normalisations you carried out in step 1 above, prepare a logical level design for the Monash Functions database.

* **Tooling & Notation:** The logical model must be drawn using the Oracle Data Modeler. The information engineering or Crow’s foot notation must be used. 
* **Data Types:** Your logical model must **not** show datatypes.
* **Normal Form:** All relations depicted must be in 3NF.
* **Surrogate Keys:** You are required to add at least one surrogate key to your design (you are free to select the most appropriate relation to make this change in).
* **Database Comments:** All attributes must be commented in the database (i.e., the comments must be part of the table structure, not simply comments in the schema file). 
* **Constraints:** Check clauses/look up tables must be applied to attributes where appropriate. 
* **Legend:** You **MUST** include the legend as part of your model. Please edit the legend panel to show your group name.

### Task 3: Generate the Schema for the Database
Generate the schema for the database in Oracle Data Modeler and use the schema to create the database in your Oracle account (this should be tested in your individual Oracle accounts if a group Oracle account is not available).

The only edit you are permitted to carry out to the generated schema file is to add header comment/s containing your details (group/members names) and the commands to spool/echo your run of the script. Ensure that:
* You capture the output of the run of your schema statements using the `spool` command.
* Your script includes `drop table` statements at the start of the script.
* You name the schema file as `mf_schema.sql` (or `fdas_schema.sql` as per alternate brief specifications).

### Task 4: Group Diary
Maintain a Group Diary which records when the group met to discuss/work on the task, including:
* The date.
* Who was present.
* A brief statement of what occurred.

> **Note:** This Group Diary must be maintained in Microsoft Teams as a shared document in your private group channel.
