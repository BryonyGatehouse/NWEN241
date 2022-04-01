# Assignment 3 : Database Management System

This Assignment is to implement a simple database management system (DBMS). Fundamental concept in DBMS is the table which consists of zero or more records or entries, and each record can have one or more fields or columns. In this database, each record has 4 fields: id, title, year, and artist.

  -   C Structure to hold one table record
  -   C++ class for holding information about the table (DbTable) including
  rowsUsed and rowsTotal
  -   Default constructor for DbTable which has space for 5 records (created 
  using malloc() or calloc()
  -   Destructor for DbTable which frees allocated memory
  -   Show() method in DbTable which displays the information stored in a 
  row to the screen. Returns true or false based on record existance.
  -   Add() method for adding a record to the table. Takes a reference to
  a record as input parameter. If no space in table (rowsUsed == rowsTotal)
  additional memory for 5 records is allocated. Returns true unless allocation
  of extra memory fails
  -   Remove() method that removes a record from DbTable. Row number to be 
  removed as the input, moves all the records after it up one so there are
  no gaps. Returns true if successful
