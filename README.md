# Magento 2 Declarative Schema

1.	Create a etc/module.xml and registration.php to register your module

# Create a table

1.	Create a db_schema.xml under etc 
2.	Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
3.	Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>


# Drop a table

1. Remove all lines of code related to your table in db_schema.xml file
2.	Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
3.	Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>


# Rename a table 

1. New table will create and old table will delete while renaming the table using declarative schema
2. Use 'onCreate' attribute on table declarative 
    <i><b>onCreate="migrateDataFromAnotherTable(old_table_name)</b></i>
    <i><table name="new_table_name" onCreate="migrateDataFromAnotherTable(old_table_name)"></i>
3. Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
4. Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>


# Add a column to table

1. For adding new column in a existing table, define new column in db_schema.xml
2. Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
3. Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>


# Drop a column from a table

1. For removing existing column in a table, remove entire column inside db_schema.xml or else add disabled=true attribute in the column.
2. Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
3. Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>


# Change the column type

1. Change the column type in db_schema.xml
2. Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
3. Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>


# Rename a column

1. Delete the original column declaration and create a new one while doing renaming a column
    onCreate="migrateDataFrom(column_name)"
2. Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
3. Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>
   



















