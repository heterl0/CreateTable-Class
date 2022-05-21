# CreateTable-Class
###NetBeans 8.2.

This class is used to create table, display it with your data set.

First of all, download file CreateTable.java and copy it to your project, refactor package!

First, call constructor to create a new object CreateTable.

For example: you want to create a table with four columns: 
    
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
   
After constructing new object, you can create a table with your dataSet. Example if you have a list of country, each country contains four attributes, id, name, totalArea, terrain. And all of them saved into:

    List<Country> list;

You have to turn this `list` into a dataSet that has a structure ArrayList<ArrayList<String>>.
The inside ArrayList contain each column, all value must casting to String. The outside ArrayList contain four ArrayList columns. After that call method create `drawTable(dataSet);` to draw table. 

    ArrayList<ArrayList<String>> dataSet = new ArrayList<ArrayList<String>>();
    ArrayList<String> id = new ArrayList<>();
    ArrayList<String> name = new ArrayList<>();
    ArrayList<String> totalArea = new ArrayList<>();
    ArrayList<String> terrain = new ArrayList<>();
    for (EastAsiaCountry country : list) {
        id.add(String.valueOf(country.getCountryCode()));
        name.add(country.getCountryName());
        totalArea.add((new DecimalFormat("0.0")).format(country.getTotalArea()));
        terrain.add(country.getCountryTerrain());
    }
    dataSet.add(id);
    dataSet.add(name);
    dataSet.add(totalArea);
    dataSet.add(terrain);
    ct.drawTable(dataSet);
    
    
