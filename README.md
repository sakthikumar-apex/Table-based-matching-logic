# Table-based-matching-logic
This repository has scripts to implement application called Table based matching logic

Oracle Application Express is a low code tool. But still few functionalities that are key for customers need more customization.
This tool helps to create an applicaton where users can create formula based on table columns from the frontend just like an excel.

Prerequisites
1 Apex Enviornment
2 Application and the scripts installed
3 Main table for which the formulae needs to be created (Eg. Table "Emp" all the formula columns like 5% commission, 10% commission can be created by users from frontend)

Initial changes for the application
Page 2 and Page 7 are the core for the application, No changes needed for Page 2, Below are the changes for page 7
1. Change the title for "Employee Table Edit" as necessary
2. Table name currently is VW_EMP should be changed to vw_"TABLE_NAME"

Working of the app. (User Perspective)
1. User should go to the page Create / Edit Formula, choose the table for which they want to create formula
2. List of columns in the table are available for reference
3. Users can use the Interactive Grid to add as many formula columns they want
4. This will be saved to formula_table
5. Go to the design view of the page 7 and right click on the Interactive grid, >> Synchronize columns
6. This will add all the new columns to the Interactive grid
7. User need to save the page to reflect the changes on the page
8. Process of synchronizing is not needed for existing columns

Implementation.
1. Table called Formula_Table stores all the formula created by the users.
2. Whenever a new formula column is added from the front end, Dynamic procedure is called from Apex to create or replace the view to add / remove necessary columns on the view
3. Braces are added automatically to the formula, so values are calculated with according to the user
4. All kinds of formula using case, Decode, Average, Sum can be used for formula
    VW_"TABLE_NAME" 
   
