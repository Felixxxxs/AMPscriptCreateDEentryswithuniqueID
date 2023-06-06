# AMPscriptCreateDEentryswithuniqueID
AMPscript - CreateDE entrys with uniqueID's as primary key

**Salesforce Marketing Cloud
If you try to write rows into a DE in the MC but you can't use the subscriber key as the primary key because some (or all) users should appear more than 1 times in the DE this is a solution you can use.

You need to create a DE with a column named 'Id' that is a number and set as the primary key. Create a different column to map to the subscriber key which is not the primary key. Furthermore you need to create a column in the DE with the name 'Dummy' and the default (text) value 'exists'.

The code will check for the entrys in the column of the primary key and add 1 to the largest entry in the primary key column to create a new unique primary key for each new row whenever an email is sent which includes this AMPscript.
