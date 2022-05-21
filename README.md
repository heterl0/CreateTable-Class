# CreateTable-Class
NetBeans 8.2.

This class used used to create table, display it with your data set.

First of all, call constructor to create a new object CreateTable.
For example: you want to create a table with four columns: 
    ```
    
    ArrayList<String> attributes = new ArrayList<>();
    attributes.add("ID");
    attributes.add("Name");
    attributes.add("Total Area");
    attributes.add("Terrain");
    ArrayList<Boolean> isNumbers = new ArrayList<>();
    isNumbers.add(false);
    isNumbers.add(false);
    isNumbers.add(true);
    isNumbers.add(false);
    CrateTable ct = new CreateTable(attributes, isNumbers);
    
    ```
