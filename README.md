# Magento 2 Declarative Schema

1.	Create a etc/module.xml and registration.php to register your module
2.	Create a db_schema.xml under etc 
3.	Don’t forget to generate a 'db_schema_whitelist.json' file.</br>
    <i><b>bin/magento setup:db-declaration:generate-whitelist --module-name=LearningPath_DBSchema</b></i>
4.	Run setup upgrade command</br>
     <i><b>bin/magento setup:upgrade</b></i>























