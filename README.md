#### WELCOME TO NEIGHBORHOOD WATCH - A CRIME DATABASE APPLICATION ####

#### 1. PREREQUISITES ####

You're going to need a couple of prerequisites before you get started working on the app.
1) Download the latest version of Python - https://www.python.org/downloads/
2) Install pip - Most python environments will come preinstalled with pip but if yours is not you can run the following commands in your CLI
        - python3 -m ensurepip --upgrade
        - python3 get-pip.py
3) Install Django - After you've installed pip it should be easy to have django installed. Just run the following command
        - python3 -m pip install Django
4) Finally install the oracledb python module to access the CISE database - https://python-oracledb.readthedocs.io/en/latest/user_guide/installation.html

#### 2. GETTING STARTED ####

If you're unfamiliar with Django I definitely recommend going through the tutorial real quick for any answers you might need. If you follow it step by step 
you'll get the necessary essentials within an hour or two. 

####IMPORTANT NOTE####
The tutorial will cover using a database native with Django. However for the implementation, since i am working on apple silicon which runs
on ARM I cannot use the necessary cx_oracle module or the oracle instant client since they run on x86. But do not fret if you're in the same boat or 
thinking about manually integrating a database stresses you out its not too difficult.

Remember to fork your own repository before getting started and work on your own branch before making any merges.**

Once, you've forked and cloned your repository in the directory of your choice you have to manually connect to your data base since its currently hard 
coded to go to mine.

To do this navigate into the directory "/neighborhoodwatch/neighborhoodwatch/querydata/views.py" 
Once in this file look within the function oracle.connect() and change where is says user esteban.medero and change it to your user credentials.

Now its time to run the app. In your CLI navigate to the first directory neighborhood watch containing the manage.py file and type the following command:

        -python3 manage.py runserver
        
You will be prompted for a password. This is your autogenerated CISE DB password found here https://register.cise.ufl.edu/oracle/

The only page currently set up is the query page since Its going to take the most time to complete I decided to start there. You can now access the 
database at http://127.0.0.1:8000/querydata/ in your webbrowser.

#### NEXT ITEMS TO COMPLETE ####

1) input fields need to be added in the side bar for accepting user input i.e. what tables to select from. We can consider limiting the number of tables
that can be accessed at once as to not overwhelm and not have to account for any ambigous errors that might arise.

2) parsing the input field in views.py and feeding it into the query string also on views.py. This is how we will interact with the database.

3) Homepage, Aboutpage, Githun anchor (These should be pretty fast and I can work on them after querying is squared.







