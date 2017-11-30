Welcome to the AWS CodeStar sample web application
==================================================

This sample code helps get you started with a simple Django web application
deployed by AWS Elastic Beanstalk.

What's Here
-----------

This sample includes:

* README.md - this file
* ebdjango/ - this directory contains your Django project files
* ebdjango/settings/env.example - sample environ .env file for local settings
* helloworld/ - this directory contains your Django application files
* manage.py - this Python script is used to start your Django web application
* static/ - this directory contains static web assets used by your application
* .ebextensions/ - this directory contains the Django configuration file that
  allows AWS Elastic Beanstalk to deploy your Django application

Getting Started
---------------

These directions assume you want to develop on your local computer, and not
from the Amazon EC2 instance itself. If you're on the Amazon EC2 instance, the
virtual environment is already set up for you, and you can start working on the
code.

To work on the sample code, you'll need to clone your project's repository to your
local computer. If you haven't, do that first. You can find instructions in the
AWS CodeStar user guide.


1. Clone this repository

        $ git clone https://github.com/abztrakt/mdot-codestar
        $ cd mdot-codestar

2. Create a Python virtual environment for your Django project. This virtual
   environment allows you to isolate this project and install any packages you
   need without affecting the system Python installation. At the terminal, type
   the following command:

        $ virtualenv .

3. Copy the env.example file into .env. This allows you set environment variables
   for running your application locally. After copying the sample, edit the
   necessary environment variables to suit your local development needs. You
   will also need to load the local environment files by running the source command:

        $ cp ebdjango/settings/env.local ebdjango/settings/.env

4. Activate the virtual environment:

        $ source bin/activate

5. Install Python dependencies for this project:

        $ pip install -r local-requirements.txt

6. Start the Django development server:

        $ python manage.py runserver 0:8000 --settings=ebdjango.settings.local

5. Open http://127.0.0.1:8000/ in a web browser to view your application.

What Do I Do Next?
------------------

Once you have a virtual environment running, you can start making changes to
the sample Django web application. We suggest making a small change to
/helloworld/templates/index.html first, so you can see how changes pushed to
your project's repository are automatically picked up and deployed to the Amazon EC2
instance by AWS Elastic Beanstalk. (You can watch the progress on your project dashboard.)
Once you've seen how that works, start developing your own code, and have fun!

Learn more about AWS CodeStar by reading the user guide.  Ask questions or make
suggestions on our forum.

User Guide: http://docs.aws.amazon.com/codestar/latest/userguide/welcome.html
Forum: https://forums.aws.amazon.com/forum.jspa?forumID=248
