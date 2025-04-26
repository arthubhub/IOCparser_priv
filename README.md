# IOCparser
This Threat hunting project aims to get information about recent security events in order to generate rules for detection and prevention. It uses one data source for now but will handle multiple ones later. It stores the datas in a database and allow automatic updating.

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![Threat Intel](https://img.shields.io/badge/Threat_Intel-blue)
[![Latest Release](https://img.shields.io/badge/Latest_Release-green)](https://github.com/arthubhub/IOCparser/releases/tag/v1.0.0)

## Components
This section contains different scripts and their usage.
* db.py : class to perform operation on the database, contains methods for managing database;
* event_class.py : class used to normalize data types, especially Event, Objects and Attributes formats;
* sigmaRule.py : contains functions and a class to store and generate Sigma detection rules;
* for more, see the scheme below
![projet_ioc](https://github.com/user-attachments/assets/64f20d23-8fe3-4729-83c2-0923f7303849)





## Usage 

### To simply use the program :
  1) Clone the repo and install the requirements
  2) edit the locations in main.py if needed
  3) run `python3.9 main.py` 

### To get the list of usefull IOCs, categories :
Put the programs categories_all_filler.sh, sort_usefull_content.sh, parser.sh in the same dir
  1) run categories_all_filler.sh
  2) run sort_usefull_content.sh
  3) run parser.sh
### To edit the whitelist
  1) Create a new branch named whitelist_update
  2) make your commits
  3) pull request and wait for an admin to review your suggestions   


## TO DO
### Events Downloading
  1) Make research about async functions
  2) Implement the async functions

###  Features
  1) Rule creation ✅
  2) Rule uploading ✅
  3) Rule editing ✅

### Rule uploading
Objectives : Automatise the exportation of new rules on the EDR ✅

### Rule editing
Objectives : Allow users to edit rules to make them more efficient
Comments : If the program generates the whole set of rules on each execution, we whould be able to implement modifications that will occur each time the program is launched.

### Other
Find a way to  make rules editing persistant. If a user edit a rule, we want it to keep as user defined and not reset when executing the script. ✅
