**This Local host tutorial is for creating a local host with XAMPP and
with preexisting wordpress files!!**

**Link to video walk through:
[https://youtu.be/GRTnvzjfpHU]{.underline}**

Local host basics *(would recommend doing research if you do not know
anything about hosting)*:
[https://whatismyipaddress.com/localhost]{.underline}

TUTORIAL USED:
[https://theme4press.com/installing-wordpress-localhost-xampp/]{.underline}

-   [https://www.wpbeginner.com/wp-tutorials/how-to-move-live-wordpress-site-to-local-server/]{.underline}

-   VIDEO: https://www.youtube.com/watch?v=U13263EuLAw

NOTE: you should make sure to "eject" XAMPP every time (not delete).
this will stop it from running on your computer - if you leave the
server running it will waste battery and slow your computer

1.  Aquire wp files

    a.  Put on desktop NOT in folder. see below

    b.  files in the link above already have the wordpress files from
        > CVML included. DO NOT DUPLICATE

2.  Download XMAPP from
    > [https://www.apachefriends.org/download.html]{.underline}

    a.  DON'T DOWNLOAD "BIGGER" VERSION. This is the VM version and
        > doesn't work (source:

> [https://community.apachefriends.org/f/viewtopic.php?f=29&t=79877]{.underline})

3.  You should get a pop up from [http://127.0.0.1/]{.underline} or
    > localhost

4.  Start server. navigate to services and make sure "mySQL" and
    > "Apache" are running. *This is the important part that XMAPP is
    > helping us with.*

5.  "Open applications folder" in XMAPP \> htdocs. insert the group of
    > files into htdocs

![](media/image1.png){width="6.403472222222222in"
height="5.513194444444444in"}

a.  Check [http://127.0.0.1/site/]{.underline} to make sure folder is
    > there i. here, "site" is cmvl

![](media/image2.jpeg){width="3.6319444444444446in"
height="2.420138888888889in"}

2.  THE WORDPRESS FILES ARE INCLUDED IN THE GOOGLE DRIVE LINK GIVEN.

    1.  download wordpress off
        > [https://wordpress.org/download/]{.underline}

    2.  put into our site folder

![](media/image3.png){width="6.317361111111111in"
height="4.726388888888889in"}

> a\.

![](media/image4.png){width="3.2868055555555555in"
height="0.18680555555555556in"}

3.  should refresh [http://127.0.0.1/site/]{.underline} tab and see this

4.  open **[http://localhost/phpmyadmin]{.underline}**

    a.  **go to our db \> privileges**

    b.  **can add a new user and grant all privleges**

![](media/image5.jpeg){width="4.019444444444445in"
height="2.3381944444444445in"}

> **c.**
>
> 5\. go to; http://127.0.0.1/cmvl/wp-admin/setup-config.php

![](media/image6.jpeg){width="5.352777777777778in"
height="3.234027777777778in"}

> 1\.
>
> 2\. if needed: go to php admin site and create a new user to edit user
> privileges.

![](media/image8.jpeg){width="3.421527777777778in"
height="3.8118055555555554in"}

> a\.

![](media/image9.jpeg){width="4.301388888888889in"
height="3.495138888888889in"}

i.  make sure to chose all credentials.

```{=html}
<!-- -->
```
3.  check MySQL credentials in 'wp-config.php'

![](media/image10.jpeg){width="2.504166666666667in"
height="1.9006944444444445in"}

> a\.

4.  Adding DB into our WP instance

![](media/image11.jpeg){width="4.420138888888889in"
height="2.329861111111111in"}

> 5\.

a.  navigate to the xampp \> htdocs \> site folder, create a file names
    > "wp-configure.php" and copy and paste this

> i\. NOTE you need a text editor that will save files as a php. Atom
> works well

![](media/image12.jpeg){width="4.061111111111111in"
height="2.1993055555555556in"}

> b\.

![](media/image13.jpeg){width="5.2375in" height="3.1305555555555555in"}

> 6\.
>
> 7\. ready to install. should get to the site after this!

![](media/image14.jpeg){width="3.7493055555555554in"
height="2.265277777777778in"}

> a\.

b.  [http://127.0.0.1/cmvl/wp-admin/]{.underline}

TROUBLESHOOTING

**DB errors**

-   "Error establishing a database connection"

    i.  This means that you probably need to go into XAMPP \> manage
        > servers. Make sure MySQL and Apache are running. Double check
        > the info from wp-config.php

-   "Can't select a database"

![](media/image15.jpeg){width="3.698611111111111in"
height="2.115972222222222in"}

> \-

-   likely have wrong log in info, or need to grant privileges in php
    > myadmin

```{=html}
<!-- -->
```
-   **ISSUE:** if someone already tried to add the files needed, and
    > there are dupes you'll have an issue. Needs to be perfect set up.
    > Also, must have ONE database running, which will be in your
    > wp-config file (php admin is pretty easy to use thankfully)

> o Was already installed:

-   After installation I got "was already installed" because kila put it
    > on another db. So went into the one she used and found her log in
    > on php admin.

    -   Must have used a randomly generated one.

    -   Make sure to use cvmldb, and change log ins in wp-config

![](media/image16.jpeg){width="4.290277777777778in"
height="2.5305555555555554in"}

> ●

-   Note: The files on the drive link already include the wordpress
    > download. So don't need to worry about that step.

![](media/image17.jpeg){width="5.0in" height="2.8854166666666665in"}

o.  Update WP-sample-config to wp-config. No need to make a new file
