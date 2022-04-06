Important tutorials from Airtable:

[[https://support.airtable.com/hc/en-us/articles/360051028214]{.underline}](about:blank)
(automations),
[[https://support.airtable.com/hc/en-us/articles/206058268-Guide-to-forms]{.underline}](https://support.airtable.com/hc/en-us/articles/206058268-Guide-to-forms)
(general form tutorial)

**Before starting the tutorial open: airtable.com,**

**[[https://transitionaljusticedata.com/]{.underline}](https://transitionaljusticedata.com/),
[[https://tulane.box.com/s/wl2p4qjwbb9sl0ygkwa0nlqre5pongri]{.underline}](https://tulane.box.com/s/wl2p4qjwbb9sl0ygkwa0nlqre5pongri)**

**Tutorial:**

**Steps for downloading the data and seeing the form:**

1.  Go to
    > [[https://transitionaljusticedata.com/]{.underline}](https://transitionaljusticedata.com/)
    > and login

2.  Click on the name of the dataset that you're working on at the top
    > of the page, ex: Civil Trials

3.  Click "Export Civiltrials to CSV"

4.  Open up the file in excel

5.  Delete the first row of the excel file and save it

6.  Go back to the TJ website and click the "Add \_\_\_\_" for example
    > "Add Civil Trial" this will have the original form pop up that we
    > will be replicating, keep this open

**Steps for uploading the data to Airtable:**

1.  Login on
    > [[https://airtable.com/]{.underline}](https://airtable.com/)
    > (username:
    > [[gdancy@tulane.edu]{.underline}](mailto:gdancy@tulane.edu),
    > password: Transitionaljustice)

2.  Import from the file (the CSV) that you just saved and edited and
    > save it as the name of the form you are going to create

**Steps for converting the columns: (We need to convert each of the
columns because they are all currently single line)**

1.  Convert the first column -- ID, ex:civiltrialsID, to "Autonumber"

2.  For the number columns, other than the first ID column, convert them
    > to numbers by clicking on arrow and customize fields and changing
    > them to "Number"

3.  For date fields, except modified date and time, that all have the
    > same representation as dates, make those numbers as well

4.  Change modified date and time to a date field, local time filed, add
    > a time field, and make it 24 hours. **If the types of date aren't
    > the same, like 1-2-99 vs 1/4/1998, don't change it to a date**

5.  Change all other forms to "Long text"

**Steps for creating the form** (This step is a little complicated
because we will need to create automations for all the drop down options
and check boxes)**:**

1.  Click on the base and create a "Form View" - name it ex: "Civil
    > Trial Form"

2.  Once the form comes up it will have all of the columns with their
    > original names and not the corresponding ones on the original form
    > on
    > [[https://transitionaljusticedata.com/]{.underline}](https://transitionaljusticedata.com/)

3.  ~~Before we do anything we need to create our first automation that
    > will automatically fill in the form when it is created with 0.1.
    > 0.1 is the value that we will use when there is no information or
    > there is data missing. Scroll down to **Automation for when record
    > is created** for these instructions and then come back up to step
    > 4~~

4.  Start organizing the form by going down the original form, so for
    > the Civil Trial one on the TJ site it starts with Type, find the
    > column that it corresponds with, which in this case is type, then
    > find 'type' on the form, or whichever the first input is on the
    > form and move it up to the top, change the name so that it matches
    > (you can do this by just clicking on the box) the original TJ form
    > and move on to the next one

5.  If the original form option isn't a text box entry, ie. it is a drop
    > down list or a check box (**except for years -- we are now doing
    > years as text entry boxes DO NOT make them a drop down)** we need
    > to make a new automation, scroll down to **Automations for drop
    > down and check boxes**

6.  We'll have to make sure to include a date modified entry as well as
    > a coder name entry, both of which entry parts aren't on the
    > original form but are included in the columns

**~~Automation for when record is created:~~**

1.  ~~Click Automation at the top right and click "new automation"~~

2.  ~~Label it "Starting Automation"~~

3.  ~~Choose the "trigger" "when record is created"~~

4.  ~~Choose "imported table" as the table then click run test~~

5.  ~~Then click "Add action"~~

6.  ~~Choose "update record"~~

7.  ~~Choose "imported table" as the table~~

8.  ~~For "record ID" choose record from step 1 and click insert next to
    > "Record ID" in the drop down options~~

9.  ~~Then click "choose field" and for each of the columns put 0.1 as
    > the option, so you will need to add every single column under
    > "choose field" this is relatively simple because the column
    > disappears from the list of options after you've chosen it~~

10. ~~Once done click run test~~

11. ~~Go up to the top of the automation you just created and switch it
    > from off to on~~

12. ~~Go back to step 4 on **Steps for creating the form**~~

**Automations for drop down and check boxes(Note: Do the countries last,
these will take the longest time because there are so many that need to
be imputed)**:

1.  So you've gotten to an input that requires a drop down list or a
    > check box entry, the first thing that you need to do is create a
    > new column by scrolling to the end of the columns on the "Grid
    > View" on the database and clicking the plus button

2.  Name this column the title of the question on the original form, so
    > for example for civil trials there is a "Violations suffered"

3.  Choose "Single select" or "Check box" as the option for the input,
    > and if it's a check box choose the grey check mark

4.  If you're doing "Single select" choose "Add an option" and input all
    > the options for the drop down, so for "violations suffered" there
    > would be an option for kidnapping/disappearance, arbitrary
    > detention\.... etc

5.  **For the options in the drop downs that are "No data" or something
    > similar to that we will just put "Don't know". If there is a
    > "Don't know" and a "Missing Value" or something similar to that we
    > only need one -- For this value that eventually gets filled in we
    > will leave it blank, if the code book says 0 still leave it
    > blank**

6.  Then click "create field"

7.  Go back to the form and you should now see "Violations suffered" or
    > whatever you named the new column under Fields to the left of the
    > form, drag it onto the form in its correct spot on the form

8.  Now make a new automation, and name it "Name of the column -- drop
    > down option" for example "Violations suffered -
    > kidnapping/disappearance" which is the first option on the drop
    > down list

9.  Choose "When a record matches conditions"

10. Choose "imported table" as the table

11. If you're doing a drop down list make the condition "When Violations
    > suffered is kidnapping/disappearance", if you're doing a check
    > mark make it "When Violations suffered = check" or no check

12. Before testing the automation you will have to go to the last row in
    > the database, in "grid view", that has no data, and change the
    > value in the one column that you just made to be the option that
    > you named the automation, so in this example for the "violations
    > suffered" column you would click "kidnapping/disappearance" or you
    > will place a check there

13. Then run the test for the trigger

14. Make an action and choose "update record"

15. Choose "imported table" as the table

16. For "record ID" choose record from step 1 and click insert next to
    > "Record ID" in the drop down options

17. Choose field and select "violationsSuffered" - **this new column
    > that you're choosing is NOT the same on that you created, it is
    > the original column that will store the input in its number
    > format**

18. Under fields for "violationsSuffered" put the corresponding code
    > (found here:
    > [[https://tulane.box.com/s/wl2p4qjwbb9sl0ygkwa0nlqre5pongri]{.underline}](https://tulane.box.com/s/wl2p4qjwbb9sl0ygkwa0nlqre5pongri))
    > for the column **(for "Don't know" leave the box blank, don't add
    > anything, even if the code book says to add something, For the
    > options in the drop downs that are "No data" or something similar
    > to that we will just put "Don't know". If there is a "Don't know"
    > and a "Missing Value" or something similar to that we only need
    > one -- For this value that eventually gets filled in we will leave
    > it blank, if the code book says 0 still leave it blank)**

19. Then turn to automation "on" at the top

**Questions:**

Civil Trials: DateComplaintFiled, dateOutcome, both dates but all in
diff formats

Autonumber -- changes the first column

Trials: This trial fits the definition of transitional human rights
trial.

Amnesties - should there be a second action to have 1 or 2?
