* Associations should have a foreign key restraint for data integrity.
  * These associations also tend to have an index because if you delete the association it will do a database lookup to see if there are any foreign key constraints.
  * You do not need an index if you probably will never delete the associated object.

