# Meter Your Calories Platform
## MYC Database

### Database Instance creation

To create the database, the Azure Platform was used and an instance of a MySQL database 
that is available in the Azure environment was created.

### Relational Data Model

The data model was created following the idea that users can make N orders, orders can contain N foods.
As N orders contain N food, it is necessary to give preference to this relationship in a new table that was named order_food_item.
Thus 1 order contains N order food item and N order food item contains 1 Food.

![Data Model.png](Data%20Model.png)


### Scripts hierarchy

In the structure for creating and organizing the scripts, the pattern of the open-source tool Flyway was used.

The file name consists of the following parts: 
1. Prefix: 
   1. V for versioned (configurable)
   2. U for undo (configurable)
   3. R for repeatable migrations (configurable) 
2. Version: Version with dots or underscores separate as many parts as you like (Not for repeatable migrations)