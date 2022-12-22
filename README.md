
# EMA ASMIS Prototype Solution for Queens Medical Centre 

## Overview

Queens Medical Centre needs an Appointment and Scheduling Management Information System (ASMIS). As part of the end-of-module assignment (EMA), this is a current working prototype solution requested by the clinic. The user is able to interact with the command-line user interface to access the prototype system of Queens Medical Centre.

Technologies here presented are selected considering the following items:
Development time and ease of use
User experience by users (i.e. patients, admins, doctors...)

The main concept is have a single application that performs all tasks being secure and
without requiring extensive work on many different subsystems and microservices (such
as backend, custom authentication systems, etc.) that can be hosted in any cloud
provider to guaranteed uptime, combined with an online database, this concept of
keeping all online and hosted on one or more cloud providers would prevent the
application of being held ransom by potential cyber attacks.

See risk assessments on the end of file.

## Setting up the environment for the project

###  Installation 

We create an environment for our project first of all. In order to create the environment,
we run the following commands :


  
 ### Follow steps in windows powershell for installation:
  
  The following are useful commands to install and check the prerequisites to run the program in the terminal (e.g. Windows PowerShell). Note that depending on the `python` versions pre-installed, the `python` commands may need to be `python3` instead.

To create a virtual environment called .venv:

`python -m venv .venv`

To activate the virtual environment in Windows PowerShell:

`.venv/Scripts/Activate.ps1`

To activate the virtual environment in Linux environment:

`source .venv/bin/activate`

To install all the required libraries and dependencies:

`python -m pip install -r requirements.txt`

Some library versions may not be compatible with the current running version of python. In that case, the version number(s) in requirements.txt may need to be changed.

To view and ensure all the required packages are installed:

`python -m pip list`

(Optional) To save all of the current dependencies to `requirements.txt`:

`python -m pip freeze > requirements.txt`

  
## Instructions to run the program
Once all the prerequisites are installed, we can start running the program. Note that
depending on the python versions pre-installed, the python commands may need to be
python3 instead.
  
1. Open the terminal and navigate to the project directory containing all the files,
including the Python file named main.py
2. Run the command: python main.py
## Technologies to be used for development
### Design
Figma
Design tool for prototypes and wireframes of screens
#### Frontend
NEXT.js or Vue.js (Javascript)
both are JavaScript frameworks NEXT.js runs on server side and Vue on client
side(browser), to create user interface using JavaScript, HTML and CSS/SCSS and
reusable components
NEXT.js is a Vercel framework, allows server-side-rendering (SSR), helping us
achieve better SEO, faster page loading and API features
💡 Vercel also provides hosting service
💡 As PWA (Progressive Web App): An development method that allows
users to install the web page as native application on device to benefit of
faster loading and offline capabilities
#### Database, API and Authentication
Firebase Firestore and/or Real time database: 
A highly scalable NoSQL Database, without requiring to code backend,
makes development easier and faster, hosted on Google Servers with high uptime
##### Firebase Authentication :
User login and management,
integrated to database for access control to information
Has with social login features
e.g. “login with Google”, “login with facebook”, etc.
##### Firebase Functions or Vercel Serverless functions:
Capability to run functions as API endpoints, to execute actions that for
example, manipulates database or send notifications
##  Notifications
Firebase Push Messaging
Send push notifications to web and/or apps:
Twilio (SMS messaging, if required): 
Platform that allows send SMS notifications with code, starting from
USD0,0079/sms (text) and USD0,0200 (with images) to send
##### Hosting
Any of client choice
Recommended:
Vercel (specially in case of NEXT.js)
Google Firebase hosting
Amazon AWS
## Risk assessment
The following table proposes how this tech stack would help prevent some common
cyber security risks: 
##### Risk scenario: Ransom - attacker
took over one
application and
edited code to
redirect users to
malicious website, Phishing targeting
staff members.
  
##### Detection
method : Number of users
using the
application
suddenly
changed, staff performed
suspicious
activity.
  
  ##### Mitigation method:
  Application hosted online and distributed trough
different cloud providers. In case of attack to one
site, it can be taken down automatically or by staff
while keeping the application alive.
  
  Users would be able to set a small security phrase,
saved and loaded from browser storage and
presented on application interface all the time to
indicate that is using a legitimate website. The
phrase cal also be saved to user account and visible
on every notification sent.
  
## Additional ways of tackling risks to the system
  
  
  Cyber security technologies that was implemented in the prototype solution include
multi-factor authentication (MFA) via the use of a time-based one-time pin (OTP),
and the encryption of user passwords using the combination of a randomly
generated salt value and hashing. These techniques are used to verify and validate
the user's identity and aim to prevent spoofing. The generating of OTP for MFA was
implemented with the help of the PyOTP library. The bcrypt library was used in the
process of password hashing. The sqlite3 library was used to store and read data
from a database.
  
  
## Instructions to run the program
Once all the prerequisites are installed, we can start running the program. Note that depending on the `python` versions pre-installed, the `python` commands may need to be `python3` instead.
1. Open the terminal and navigate to the project directory containing all the files, including the Python file named `main.py` 
2. Run the command: `python -m main` or `python main.py`
3. Follow the program instructions displayed to explore the working prototype features.

## Testing
Sample dummy data users have been prepopulated in the users table in the [Queens database](queens.db). Users are modelled as clinic patients or specialists. Login details:

#### Patients 

`joeking, Kidding!1`

`bendover, Stretch!1`

#### Specialists

`normalee, Usually!1`

`hollywood, Starring!1`

Example test outputs for patient and specialist users are in the [test-results](test-results/) directory.

## References
Arias, D. (2021) Adding Salt to Hashing: A Better Way to Store Passwords. [online] Auth0. Available from: https://auth0.com/blog/adding-salt-to-hashing-a-better-way-to-store-passwords/ [Accessed 1 September 2022].

GitHub. (2022) PyOTP - The Python One-Time Password Library. [online] Available from: https://github.com/pyauth/pyotp [Accessed 1 September 2022].

PyPI. (2022) bcrypt. [online] Available from: https://pypi.org/project/bcrypt/ [Accessed 31 August 2022].

Python 3.10.6 documentation. (2022) 9. Classes. [online] Available from: https://docs.python.org/3/tutorial/classes.html [Accessed 30 August 2022].

Python 3.10.6 documentation. (2022) datetime — Basic date and time type. [online] Available from: https://docs.python.org/3/library/datetime.html [Accessed 1 September 2022].

Python 3.10.6 documentation. (2022) enum — Support for enumerations. [online] Available from: https://docs.python.org/3/library/enum.html [Accessed 2 September 2022].

Python 3.10.6 documentation. (2022) sqlite3 — DB-API 2.0 interface for SQLite databases. [online] Available from: https://docs.python.org/3/library/sqlite3.html [Accessed 2 September 2022].

Stack Overflow. (2020) Python MySQLdb - Connection in a class. [online] Available from: https://stackoverflow.com/questions/38076220/python-mysqldb-connection-in-a-class [Accessed 2 September 2022].  
