#####################
Community Health Work
#####################

Access to a health provider is something that is commonly taken for granted.
From a kenyan perspective, the doctor to patient ratio is approximately 2:10000, implying that there are chances you may not get to see one in your lifetime!.

Community Health workers come in to change that.

A community health worker is trained to provide the most essential life saving interventions such as emergency care. They also equip families with knowledge and skills to prevent diseases. They Promote sanitation, hygiene, and good nutrition. 


*****************
Community module
*****************

The community module is primarily meant for recording household visits/episodes that are done by Community Health Workers.  To achieve this, the following distinct activities are defined:


Household registration:
-----------------------
A household refers to a house and its occupants.
Unique households are defined during a household mapping activity. These details are captured into the com_household table and implemented through HouseholdController in StoneHMIS
com_household table.


Household Residents Registration:
---------------------------------
These are the occupants of the house.
A house must have residents for community health work to be done. 
To avoid running parallel systems, I.e community module running parallel to stoneHMIS, household residents are registered during the normal registration in stone,(in the registry module). However, the household residents details go into a different table called com_household_residence, which is linked to the reg_person table through reg_person_id. 
 
.. note::

   The residents are registered starting with the head of the household, so that the subsequent occupants are assigned that head. 


The com_household_residence table contains : 
