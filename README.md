
AMIS

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
-------------------------------------------

We create an environment for our project first of all. In order to create the environment,
we run the following commands :

To create a virtual environment in the lunux environment, we need to install the library that helps in installation :
pip install virtualenv
To use venv in your project, in your terminal, create a new project folder, cd to the
project folder in your terminal, and run the following command:
python<version> -m venv <virtual-environment-name>
Now that we have created our virtual environment, we need to activate our virtual
environment using the following command:
AMIS2source env/bin/activate # we navigate using command prompt to the env folder and
then bin folder and run the command : “activate”
Now we can start installing the relevant libraries and start working.
After installing your required libraries, you can view all installed libraries by using pip list,
or you can generate a text file listing all your project dependencies by running the code
below:
pip freeze > requirements.txt
To recreate your development environment, your friend will just need to follow the above
steps to activate a new virtual environment.
Instead of having to install each dependency one by one, they could just run the code
below to install all your dependencies within their own copy of the project:
pip install -r requirements.txt
To deactivate your virtual environment, simply run the following code in the terminal:
deactivate
Instructions to run the program
Once all the prerequisites are installed, we can start running the program. Note that
depending on the python versions pre-installed, the python commands may need to be
python3 instead.
1. Open the terminal and navigate to the project directory containing all the files,
including the Python file named main.py
2. Run the command: python main.py
Technologies to be used for development
AMIS3Design
Figma
Design tool for prototypes and wireframes of screens
Frontend
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
Database, API and Authentication
Firebase Firestore and/or Real time database
An highly scalable NoSQL Database, without requiring to code backend,
makes development easier and faster
Hosted on Google Servers with high uptime
Firebase Authentication
AMIS4User login and management
integrated to database for access control to information
Has with social login features
e.g. “login with Google”, “login with facebook”, etc.
Firebase Functions or Vercel Serverless functions
Capability to run functions as API endpoints, to execute actions that for
example, manipulates database or send notifications
Notifications
Firebase Push Messaging
Send push notifications to web and/or apps
Twilio (SMS messaging, if required)
Platform that allows send SMS notifications with code, starting from
USD0,0079/sms (text) and USD0,0200 (with images) to send
Hosting
Any of client choice
Recommended:
Vercel (specially in case of NEXT.js)
Google Firebase hosting
Amazon AWS
AMIS5Risk assessment
The following table proposes how this tech stack would help prevent some common
cyber security risks
Risk scenario Detection
method Mitigation method
Ransom - attacker
took over one
application and
edited code to
redirect users to
malicious website
Number of users
using the
application
suddenly
changed
Application hosted online and distributed trough
different cloud providers. In case of attack to one
site, it can be taken down automatically or by staff
while keeping the application alive
Phishing targeting
staff members
staff performed
suspicious
activity
Users would be able to set a small security phrase,
saved and loaded from browser storage and
presented on application interface all the time to
indicate that is using a legitimate website. The
phrase cal also be saved to user account and visible
on every notification sent
Additional ways of tackling risks to the
system.
Cyber security technologies that was implemented in the prototype solution include
multi-factor authentication (MFA) via the use of a time-based one-time pin (OTP),
and the encryption of user passwords using the combination of a randomly
generated salt value and hashing. These techniques are used to verify and validate
the user's identity and aim to prevent spoofing. The generating of OTP for MFA was
implemented with the help of the PyOTP library. The bcrypt library was used in the
process of password hashing. The sqlite3 library was used to store and read data
from a database.
