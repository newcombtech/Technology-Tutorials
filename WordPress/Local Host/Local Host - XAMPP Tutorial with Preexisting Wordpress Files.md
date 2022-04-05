**This Local host tutorial is for creating a local host with XAMPP and
with preexisting wordpress files!!**

**Link to video walk through:
https://youtu.be/GRTnvzjfpHU**

Local host basics *(would recommend doing research if you do not know
anything about hosting)*:
https://whatismyipaddress.com/localhost

TUTORIAL USED:
https://theme4press.com/installing-wordpress-localhost-xampp/

-   https://www.wpbeginner.com/wp-tutorials/how-to-move-live-wordpress-site-to-local-server/

-   VIDEO: https://www.youtube.com/watch?v=U13263EuLAw <br><br>

NOTE: you should make sure to "eject" XAMPP every time (not delete).
this will stop it from running on your computer - if you leave the
server running it will waste battery and slow your computer <br><br>

1.  Aquire wp files

    a.  Put on desktop NOT in folder. see below

    b.  files in the link above already have the wordpress files from
        > CVML included. DO NOT DUPLICATE

2.  Download XMAPP from
     https://www.apachefriends.org/download.html

    a.  DON'T DOWNLOAD "BIGGER" VERSION. This is the VM version and
         doesn't work (source: https://community.apachefriends.org/f/viewtopic.php?f=29&t=79877

3.  You should get a pop up from http://127.0.0.1/ or
     localhost

4.  Start server. navigate to services and make sure "mySQL" and
     "Apache" are running. *This is the important part that XMAPP is
     helping us with.*

5.  "Open applications folder" in XMAPP \> htdocs. insert the group of
     files into htdocs

<img width="461" alt="image" src="https://user-images.githubusercontent.com/89610126/161860959-c83cc179-0d2a-431e-b7bc-3fcbd8d81c1e.png">

a.  Check http://127.0.0.1/site/ to make sure folder is
     there i. here, "site" is cmvl

<img width="262" alt="image" src="https://user-images.githubusercontent.com/89610126/161860993-0b5c9ae7-aa31-4eec-89cb-b7875b4c5808.png">

2.  THE WORDPRESS FILES ARE INCLUDED IN THE GOOGLE DRIVE LINK GIVEN.

    1.  download wordpress off
         https://wordpress.org/download/

    2.  put into our site folder

<img width="455" alt="image" src="https://user-images.githubusercontent.com/89610126/161861031-064bdca0-6066-4f61-8d33-6a81ee9256fa.png">





3.  should refresh http://127.0.0.1/site/ tab and see this

4.  open **http://localhost/phpmyadmin**

    a.  **go to our db \> privileges**

    b.  **can add a new user and grant all privleges**



 5. go to; http://127.0.0.1/cmvl/wp-admin/setup-config.php

<img width="386" alt="image" src="https://user-images.githubusercontent.com/89610126/161861194-5816a61e-c453-4ca8-81c5-3fa38643dccc.png">

<br><br>

 1. <img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/161861250-b5274ed4-83bd-4ef2-84a7-c5c5970fce5d.png">

 

 2. if needed: go to php admin site and create a new user to edit user
 privileges.

<img width="247" alt="image" src="https://user-images.githubusercontent.com/89610126/161861304-3b39bd86-c8fc-4996-93f7-ad3bf84566fa.png">

<img width="310" alt="image" src="https://user-images.githubusercontent.com/89610126/161861316-76cf77ae-835b-43d5-a5fb-6de6c7fe521e.png">


make sure to chose all credentials.


3.  check MySQL credentials in 'wp-config.php'

<img width="181" alt="image" src="https://user-images.githubusercontent.com/89610126/161861336-603b8893-d3d1-4fc0-a11e-920a265a92ac.png">

4.  Adding DB into our WP instance

<img width="319" alt="image" src="https://user-images.githubusercontent.com/89610126/161861344-28128860-715d-44da-9dca-6f8513a5dd4c.png">
5.

a.  navigate to the xampp \> htdocs \> site folder, create a file names
     "wp-configure.php" and copy and paste this

  i. NOTE you need a text editor that will save files as a php. Atom
 works well

<img width="293" alt="image" src="https://user-images.githubusercontent.com/89610126/161861390-b4bee95d-d37e-4d7c-a246-eb734d91c828.png">
6.
<img width="377" alt="image" src="https://user-images.githubusercontent.com/89610126/161861403-80f166a6-6638-4660-944a-d3154cbc22a2.png">



 7. ready to install. should get to the site after this!

a. <img width="270" alt="image" src="https://user-images.githubusercontent.com/89610126/161861440-25888cf0-2361-46da-9079-35ef19ab36cd.png">


b.  http://127.0.0.1/cmvl/wp-admin/

<br><br>

TROUBLESHOOTING

**DB errors**

-   "Error establishing a database connection"

    i.  This means that you probably need to go into XAMPP \> manage
         servers. Make sure MySQL and Apache are running. Double check
         the info from wp-config.php

-   "Can't select a database"

<img width="267" alt="image" src="https://user-images.githubusercontent.com/89610126/161862107-7f0ef541-99e7-4252-8b51-a8e1f16f2b69.png">



likely have wrong log in info, or need to grant privileges in php
     myadmin <br><br>


-   **ISSUE:** if someone already tried to add the files needed, and
     there are dupes you'll have an issue. Needs to be perfect set up.
     Also, must have ONE database running, which will be in your
     wp-config file (php admin is pretty easy to use thankfully)

      -  Was already installed:

            -   After installation I got "was already installed" because kila put it on another db. So went into the one she used and found her log in on php admin.

                 -   Must have used a randomly generated one.

                  -   Make sure to use cvmldb, and change log ins in wp-config

<img width="309" alt="image" src="https://user-images.githubusercontent.com/89610126/161862209-e284eb72-7bf6-412a-8bda-18b209f49fe8.png">
-   Note: The files on the drive link already include the wordpress
     download. So don't need to worry about that step.
<img width="360" alt="image" src="https://user-images.githubusercontent.com/89610126/161862239-8f176c05-0c11-4617-b6c1-32aa1900ec26.png">

Update WP-sample-config to wp-config. No need to make a new file
