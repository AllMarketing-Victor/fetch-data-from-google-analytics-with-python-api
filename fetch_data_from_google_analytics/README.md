
 # Consuming Google Analytics data from a Python application using a service account
 
 This idea is for create a simple report for my users. Since it isn't a critical report, my idea was to get the data once a day or once in a week whatever you want.
 
 So, as simple as it seems, it has been a tough trip for me and I want to share the whole process with the community. I hope anyone trying to achive something similar gets to this article and find it helpful.
 
 These are the main steps I had to take:
 
1. Run Below command one by one <br />
	    (i)   sudo apt-get update <br />
    	(ii)  sudo apt-get -y install python-pip <br />
     	(iii) pip install --upgrade google-api-python-client
	
2. Now go to the below link - <br />
	https://console.developers.google.com/apis/library/sheets.googleapis.com <br />
	
3.  If project already created select project else create new project
4.  Click on ENABLE API
5.  Now search for Google Analytics Reporting API, click on Google Analytics Reporting API.
6.  ### Create a service account
    Next we need to create the service account. In the left vertical menu you should click in the IAM & admin. You should see a big blue button saying create service account. Download the json and save in your local directory.
    
7. ### Register service account in Google Analytics
  * In this step you need to grant read access to the brand new service account in your Google analytics project.
  * Log in to Google Analytics and navigate to your project. Enter de Admin section and look for the Users tab.
  * Click in the New User button and type the email for the service account you previously created. Use the User role.
  * In the profile section, select your Analytics project profile and add it to Selected profiles panel.
  * Finally, push Create user button.
  
That's it. 

8. Fill the credential in ini file based on your requirments , And run below command.
   python fetchGAData.py fetchGAData.ini
