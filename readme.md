# Robotframework ARES

This repo consist of example for using TestAstra/ARES in robotframework

---

*What is ARES?*

  ARES is a web based portal, which provides automation results at one place. It can integrate with most popular automation tools like Selenium, Protractor etc.

*KEY FEATURES*

 - Live Execution status
 - Works with any automation tool (by using RESTAPI calls)
 - Supports Historical results
 - Visualization of execution status using charts
 - Centralized report (view reports from any part of globe by login)

  For more info on account, project creation refer - [ARES Introduction](https://github.com/testastra/ARES/blob/master/Tutorials/01_Introduction.md)

 - ARES Dashboard : https://testastra.com/ares
 - ARES Overview  : https://github.com/testastra/ARES

---

In order to use ARES Dashboard we need to do few Resutful API calls at designated places in script. They are

  1. Before Start Of Execution : To Create ARES session
  2. Before Start Of Suite     : To provide suite initiated info to ARES
  3. End Of Test Case          : To provide test result to ARES
  4. After End Of Suite        : To provide suite ended info to ARES
  5. After End of Execution    : To Close ARES session

---

HOW TO USE:

In this repo I have created AresListener.py (robotframework-listener) using python requests to make Respective REST API calls which are initiated at designated place.

Prerequisites
 - Basic knowledge on robotframework
 - Python requests library installed (`pip install requests`) to make REST API calls
 - Created project in ARES Dashboard ( creating project in ARES is explained in [01_Introduction.md](/Tutorials/01_Introduction.md) )


Steps to Use:

 - Step 1: Download this repo
 - Step 2: Copy AresListener.py, config.py to your project
 - Step 3: Modify config.py with USER_TOKEN, PROJECT NAME/TOKEN etc., fields
   > Create account in ARES, Create Project and copy details which are explained in *01_Introduction.md*
 - Step 4: Execute test case/suites using areslistener
   > robot --listener AresListener.py -V config.py suite.robot
 - Step 5: Go to ares dashboard
   > You can find live execution, detailed report and some charts

---

ARES Dashboard QUICK OVERVIEW

*LIVE EXECUTION*

  <a href="https://ibb.co/QkFJ8Xd"><img src="https://i.ibb.co/bFg6H7J/ARES-LIVE.jpg" alt="ARES-LIVE" border="0"></a>

*DASHBOARD*

   <a href="https://ibb.co/xD7YX41"><img src="https://i.ibb.co/f2x9qck/ARES-DASHBOARD.jpg" alt="ARES-DASHBOARD" border="0" /></a>

*HISTORIC DATA*

   <a href="https://ibb.co/q71TsM7"><img src="https://i.ibb.co/jb4nMvb/ARES-DETAILED.jpg" alt="ARES-DETAILED" border="0"></a>

---

ARES Dashboard is product of testastra. Powered by ZenQ

Licence: GPLv3
