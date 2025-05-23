<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- First Download the osticket files and unzip them
- Enable ISS
- Install A Database
- Link osTicket to Database

<h2>Installation Steps</h2>


First, we download the osticket files from here https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD
and we must unzip the files so we can use and access them
-Now we are going to enable ISS on the remote windows desktop
<p>
<img width="1137" alt="Screenshot 2025-04-22 at 1 30 44 PM" src="https://github.com/user-attachments/assets/d0c22b7f-3dff-477f-b483-8b9c0ea2c1dd" />

</p>
<p>
To reach this window you must go to the window button on the bottom left corner and search for control panel. Once you are on the control panel screen you will see a section called programs and under programs there is a sub-section called uninstall programs (we aren't uninstalling anything it's just to get us to the window above faster) and now you are here and we are going to select the Internet Information Services and click ok. Next we are going to install PHP Manager for IIS
</p>
<br />

<p>
<img width="1137" alt="Screenshot 2025-04-22 at 1 44 59 PM" src="https://github.com/user-attachments/assets/4ce9f92f-a3e0-4f4d-ae57-e908313b16b2" />
</p>
<p>
Now we are going back and using the same files we downloaded and unzipped earlier to install the php manageer which will allow use to use the osTicket Software. So once you open the files you will see the php file and you will double click and open and accept and agree to the license and then it will download it. Also we will then install the Rewrite Module
  
  <img width="1138" alt="Screenshot 2025-04-22 at 1 48 53 PM" src="https://github.com/user-attachments/assets/8744cfcd-0a0c-452c-8050-509cb906f7a8" />

After that is installed we are going to go back to create the directory on Windows(C.) and create a new file and name it PHP

<img width="1187" alt="Screenshot 2025-04-22 at 2 29 39 PM 1" src="https://github.com/user-attachments/assets/f4401ad5-0446-4ead-8d7f-e06f2c2f06f4" />
Next we are now going to go back to the first files we downloaded from the drive that had all the files needed to run and install osTicket and we are going to extract the php 7.3.8 and unzip it and select it to be extracted to the file we just created on the windows C. file called PHP you can see how it will look in the image below 
<img width="1319" alt="Screenshot 2025-04-22 at 2 38 17 PM" src="https://github.com/user-attachments/assets/ed1cd6d7-396d-453b-93ed-cfeb127cd95b" />
Still staying on the same file we are now going to download another file called vc_redist.x86.exe which is also called C++ its another arbitray requirement needed before we can start to run osTicket 

<img width="1277" alt="Screenshot 2025-04-22 at 2 45 42 PM" src="https://github.com/user-attachments/assets/1b2bdefa-a5ff-4b94-9875-eaa9b46717ec" />
Then we are going to still be looking at the same file where we just installed the last file and now we are going to install mySQL_5.5.62 which is important because this is the database where it will store all the data from the osTicket and this refers to users, and the ticket information as being the data in this scenario. Once you install there will be a step where it will the option to pick detailed configuration or standard and we will pick standard then you will get to this window  
<img width="1326" alt="Screenshot 2025-04-22 at 2 59 16 PM" src="https://github.com/user-attachments/assets/45b660a5-0080-4301-9935-915eef5bb054" />
Now for this practice example: the password will be easy and simple just the word "ROOT" in the workspace its never smart to use a super simple password. After that we are going to go back and open the ISS software but (open as an admin)
<img width="1440" alt="Screenshot 2025-04-22 at 3 09 04 PM" src="https://github.com/user-attachments/assets/087468ae-0d38-4b73-a48d-5ebc31b837be" />
After that we are going to register the PHP from within the ISS and we will do by clicking on the PHP Manger and it will take us to here
<img width="1440" alt="Screenshot 2025-04-22 at 3 09 04 PM" src="https://github.com/user-attachments/assets/1110da81-d479-4b2b-b5fb-181d855a7521" />
Here we are selecting the file needed which is under Window C. ->PHP -> PHP-cgi we select this one and click open after. We after have to reload ISS so that it now can read the PHP file and we does this if you look to the right of the screen there is a stop and start button we are clicking the stop button and waiting a couple minuetes and then click start.
Now we are installing the actual osTicket and we will have to unzip and extract it again
<img width="1376" alt="Screenshot 2025-04-22 at 3 20 27 PM" src="https://github.com/user-attachments/assets/c540648c-5e77-4860-a2b9-cbe2d714d6b6" />
Next you will go back to File explorer you can find it on the bottom left again then click the Window C. drive then we will open inetpub.
<img width="1440" alt="Screenshot 2025-04-22 at 3 27 48 PM" src="https://github.com/user-attachments/assets/0d17a36b-fc7c-4b5a-b1be-626b0468b56b" />
Next open the wwwroot
<img width="1440" alt="Screenshot 2025-04-22 at 3 30 51 PM" src="https://github.com/user-attachments/assets/06bc224d-fb1a-4d4f-a3d0-09320d4facb3" />
Now once we have opened the wwwroot we will see we have two files already the actual microsoft edge and a file and here we will upload the "upload" file name it should look like this after just drag it from the left to right 
<img width="1440" alt="Screenshot 2025-04-22 at 3 34 11 PM" src="https://github.com/user-attachments/assets/0a4316a6-59c3-4bae-82c3-d7c6e07a6d09" />
and name the file to "osTicket" cap senstive and no space betweeen os and Ticket. after go back to ISS look at previous images in case you forgot how to get to ISS and we are going to stop and start the server again.Now we are going to open the osTicket
<img width="1440" alt="Screenshot 2025-04-22 at 3 38 52 PM" src="https://github.com/user-attachments/assets/496dfe7a-24e0-41ff-843f-3c122f4b44eb" />
</p>
<br />
Now that we should be at this window right here however you will notice some extensions are not yet enabled so we will activate them right now which are the following: PHP Imap, Intl Extension, 
<p>
<img width="1440" alt="Screenshot 2025-04-23 at 3 11 11 PM" src="https://github.com/user-attachments/assets/932be5c7-e24e-4591-900f-77b7d4ada1db" />
We are going back to the PHP manager which is on the ISS we click on osticket then sites, then Default Web Services, and under osTicket we will open the PHP Manger and double left click and get to this window.
  <img width="1440" alt="Screenshot 2025-04-23 at 3 18 55 PM" src="https://github.com/user-attachments/assets/c29981e2-0ca7-4815-9459-7eeac0d70784" />
  Now we will click on the enable or disable extensions and enable the extensions mentioned earlier. Once you enable and fresh the other tab with the osTicket yours should look like this 
<img width="1440" alt="Screenshot 2025-04-23 at 3 24 06 PM" src="https://github.com/user-attachments/assets/cdf4f647-1b30-4cb3-a1c8-2068cf5e6d9f" />
We will look into rename a file called ost-sampleconfig.php to ost-config.php  
<img width="1440" alt="Screenshot 2025-04-23 at 3 27 29 PM" src="https://github.com/user-attachments/assets/42bc51e0-1075-411e-94a5-2bc6b147153d" />
Now we are going back to the browser to finish configuring the osTicket, click continue on the browser and then here you will create a name for the helpdesk and signup with email and names and passwords that best can be remembered and that correspond to you.Now once you get to the last portion it will say MySQL and this is basically use setting up the database where it will store all the data and tickets history from our ticketing system to do this we will need to setup and install HeidiSQL we will find this on the first files we downloaded.
<img width="1440" alt="Screenshot 2025-04-23 at 3 48 27 PM" src="https://github.com/user-attachments/assets/156a9317-29cf-4dcc-8c51-06c1a87252bb" />
After you were able to install the SQL we now will need to connect our database we created earlier and use login with the password we made which was really easy and should not be used in real life called "root" 
  <img width="1440" alt="Screenshot 2025-04-23 at 3 52 25 PM" src="https://github.com/user-attachments/assets/36a13b8b-4663-461c-bab4-72cbadd44a16" />
So at this point we have our database tied to our ticketing system and now we are going to open a a new data table to which all the files will be sent and organized to and if you right click where it says unamed and it will give you the option to open the new table and there is where you will name it osTicket make sure its type like this exaclty.
<img width="1440" alt="Screenshot 2025-04-23 at 3 59 35 PM" src="https://github.com/user-attachments/assets/c1519cc1-7584-4746-a84b-9b0599baf6c5" />
Continue setting up my osTicket on the browser by putting in your name of database, username, and password and then click install now
<img width="1440" alt="Screenshot 2025-04-23 at 4 22 57 PM" src="https://github.com/user-attachments/assets/ad137214-a83d-4779-a8e6-e61bd74af161" />

</p>
<p>  
Congratulations at this point you have setup your own osTicket System. You can save the URL given on the browser so that you can login as a admin.
</p>
<br />
