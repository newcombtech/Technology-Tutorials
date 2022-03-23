# Form and Formula Creation

**Pages to open before beginning:**

[airtable.com](airtable.com)\
[https://transitionaljusticedata.com/](https://transitionaljusticedata.com/)\
[https://tulane.box.com/s/wl2p4qjwbb9sl0ygkwa0nlqre5pongri](https://tulane.box.com/s/wl2p4qjwbb9sl0ygkwa0nlqre5pongri)<br><br>

**Steps for downloading the data and seeing the form:**

1.  Go to
     [https://transitionaljusticedata.com/](https://transitionaljusticedata.com/)
     and login

2.  Click on the name of the dataset that you're working on at the top
     of the page, ex: Civil Trials

3.  Click "Export Civiltrials to CSV"

4.  Open up the file in excel

5.  Delete the first row of the excel file and save it

6.  Go back to the TJ website and click the "Add \_\_\_\_" for example
     "Add Civil Trial" this will have the original form pop up that we
     will be replicating, keep this open <br><br>

**Steps for uploading the data to Airtable:**

1.  Login on
     [https://airtable.com/](https://airtable.com/)
     (username:
     [gdancy@tulane.edu](mailto:gdancy@tulane.edu),
     password: Transitionaljustice)

2.  Import from the file (the CSV) that you just saved and edited and
     save it as the name of the form you are going to create <br><br>

**Steps for converting the columns: (We need to convert each of the
columns because they are all currently single line)**

1.  Convert the first column -- ID, ex:civiltrialsID, to "Autonumber"

2.  For the number columns, other than the first ID column, convert them
     to numbers by clicking on arrow and customize fields and changing
     them to "Number"

3.  For date fields, except modified date and time, that all have the
     same representation as dates, make those numbers as well

4.  Change modified date and time to a date field, local time filed, add
     a time field, and make it 24 hours. **If the types of date aren't
     the same, like 1-2-99 vs 1/4/1998, don't change it to a date**

5.  Change all other forms to "Long text"<br><br>

**Steps for creating the formulas and new columns needed for the
formulas** (formulas are only needed for checkboxes and dropdowns):

1.  See the section below for the formula code for the countryID column

2.  When you get to an input that requires a drop down list or a
     checkbox entry, the first thing that you need to do is create a
     new column by scrolling to the end of the columns on the "Grid
     View" on the database and clicking the plus button

3.  Name this column the title of the question on the original form, so
     for example for civil trials there is a "Violations suffered" and
     "This case is part of democratic transition sample."

4.  Choose "Single select" or "Checkbox" as the option for the input,
     and if it's a checkbox choose the grey check mark

5.  If you're doing "Single select" choose "Add an option" and input all
     the options for the drop down

    a.  For example, for "violations suffered" there would be an option
         for kidnapping/disappearance, arbitrary detention\.... etc

6.  For the options in the drop downs that are "No data" or something
     similar to that we will just put "Don't know". If there is a
     "Don't know" and a "Missing Value" or something similar to that we
     only need one --For this value that eventually gets filled in we
     will **leave it blank**, if the code book says 0 **still leave it
     blank**

7.  Then click "create field"

8.  Go back to the form and you should now see "Violations suffered" or
     whatever you named the new column under Fields to the left of the
     form

    a.  Note: you will make the form look like the original on the
         website in the next step, for now, just make sure your column
         was successfully created

9.  Find the original column in the database and rename it to it's
     original name + (old)

    a.  For example, if the origional name was policySource, I would
         rename it to policySource(old)

10. Right click and insert a new column to the right of this column and
     name it the original name and create it as a formula column

    a.  I would name this column policySource

<img width="216" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159797862-75cc1b12-01d6-486c-9c94-a491122c1ef5.png">


11. When you classify the column as a formula column, a text box will
     appear under the formula tab where you can enter in code for the
     formula. We are going to create a nested if loop that pulls from
     the drop down or check box options you created earlier.

12. The first if statement will take the following form:

    a.  IF({originalcolumn(old)} , {originalcolumn(old)}

    b.  This checks if there is data in the origional column and
         automatically updates that data so that it will not be erased.

13. The remaining IF statements: Create an IF statement for each of the
     options. Each if statement except the last one will have the
     following general form: IF({drop down column name} = "drop down
     option", \# corresponding to that option, ... (next IF statement).

14. If you are coding for a check box column:

    a.  For the "checked" option use the form IF({checkedboxcolumn}, \#
         corresponding to true}. This is a logical statement that
         checks if the box is true or false.

    b.  For the "unchecked" option use the form IF({checkedboxcolumn} =
         0, \# corresponding to false}. This is a logical statement
         checking if the box is unchecked and is therefore stored as a
         zero.

Refer to the following images with examples for drop down and checked
box columns:

[Drop Down] 

<img width="209" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159798025-7e90be96-932f-4b17-b611-b9ae40f2f9e6.png">


[Checked Box]

<img width="230" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159798073-7d651755-cce3-4f82-93e7-49fe47095363.png">


15. Key Notes for these if statements:

    a.  Separate each if statement with a comma so that they will be
         nested properly.

    b.  Do not close out your IF statements with parenthesis until the
         last statement.

16. Close out all of the parentheses then check to make sure that when
     you add a new dropdown option or checkbox, your column updates. It
     should update automatically. <br><br>

**Steps for creating the form** (Using the columns we created in the
previous step)**:**

1.  Click on the base and create a "Form View" - name it ex: "Civil
     Trial Form"

2.  Once the form comes up it will have all of the columns with their
     original names and not the corresponding ones on the original form
     on
     [https://transitionaljusticedata.com/](https://transitionaljusticedata.com/)

3.  Start organizing the form by going down the original form, so for
     the Civil Trial one on the TJ site it starts with Type, find the
     column that it corresponds with, which in this case is type, then
     find 'type' on the form, or whichever the first input is on the
     form and move it up to the top, change the name so that it matches
     (you can do this by just clicking on the box) the original TJ form
     and move on to the next one

    a.  The columns that you are putting on the forms are the ones that
         match with the language used on the original form
         [https://transitionaljusticedata.com/](https://transitionaljusticedata.com/)

    b.  These will be the columns with names that are more sentence-like
         (although some of them are just words) and less data-type like

    c.  For example, the column you are dragging into the form would be
         the column titled "This case is part of democratic transition
         sample." not civilSample or civilSample(old)

4.  We'll have to make sure to include a date modified entry as well as
     a coder name entry, both of which entry parts aren't on the
     original form but are included in the columns

**Steps for adding section dividers** (Airtable does not include this
feature, so this is a workaround)**:**

1.  In the form view, select add a field to this table (on the left
     side, under all of the column names in the field sidebar) and add
     a single select column.

2.  Name this column what you want the section divider to be called and
     press save. Do not add any options

3.  For example, you might want the divider to look something like this

    a.  \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

    b.  THE CIVIL TRIAL

    c.  \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

4.  Click on the column you just created and select List next to show
     field as

5.  Place the divider where needed to match the original form <br><br>

**Formula Code for Coding Countries** (Huge shoutout to Sarah for typing
all this up!)**:**

IF({countryID(old)},{countryID(old)},

IF({Country} = \"Afghanistan\", 1,

IF({Country} = \"Algeria\", 2,

IF({Country} = \"Andorra\", 3,

IF({Country} = \"Antigua & Barbuda\", 4,

IF({Country} = \"Argentina\", 5,

IF({Country} = \"Armenia\", 6,

IF({Country} = \"Australia\", 7,

IF({Country} = \"Austria\", 8,

IF({Country} = \"Azerbaijan\", 9,

IF({Country} = \"Bahamas\", 10,

IF({Country} = \"Bahrain\", 11,

IF({Country} = \"Bangladesh \", 12,

IF({Country} = \"Barbados\", 13,

IF({Country} = \"Belarus\", 14,

IF({Country} = \"Belgium\", 15,

IF({Country} = \"Belize\", 16,

IF({Country} = \"Benin\", 17,

IF({Country} = \"Bhutan\", 18,

IF({Country} = \"Bolivia\", 19,

IF({Country} = \"Bosnia and Herzegovina\", 20,

IF({Country} = \"Botswana\", 21,

IF({Country} = \"Brazil\", 22,

IF({Country} = \"Brunei \", 23,

IF({Country} = \"Bulgaria\", 24,

IF({Country} = \"Burkina Faso\", 25,

IF({Country} = \"Burundi\", 26,

IF({Country} = \"Cambodia\", 27,

IF({Country} = \"Cameroon \", 28,

IF({Country} = \"Canada\", 29,

IF({Country} = \"Cape Verde\", 30,

IF({Country} = \"Central African Republic\", 31,

IF({Country} = \"Chad\", 32,

IF({Country} = \"Chile\", 33,

IF({Country} = \"China\", 34,

IF({Country} = \"Colombia\", 35,

IF({Country} = \"Comoros\", 36,

IF({Country} = \"Congo, Democratic Republic of the\", 37,

IF({Country} = \"Congo Republic of the\", 38,

IF({Country} = \"Costa Rica\", 39,

IF({Country} = \"Cote d\'Ivoire\", 40,

IF({Country} = \"Croatia\", 41,

IF({Country} = \"Cuba\", 42,

IF({Country} = \"Cyprus\", 43,

IF({Country} = \"Czech Republic\", 44,

IF({Country} = \"Denmark\", 45,

IF({Country} = \"Djibouti\", 46,

IF({Country} = \"Dominica\", 47,

IF({Country} = \"Dominican Republic\", 48,

IF({Country} = \"East Germany\", 49,

IF({Country} = \"East Timor\", 50,

IF({Country} = \"Ecuador\", 51,

IF({Country} = \"Egypt\", 52,

IF({Country} = \"El Salvador\", 53,

IF({Country} = \"Equatorial Guinea\", 54,

IF({Country} = \"Eritrea\", 55,

IF({Country} = \"Estonia\", 56,

IF({Country} = \"Ethiopia\", 57,

IF({Country} = \"Federated States of Micronesia\", 58,

IF({Country} = \"Fiji\", 59,

IF({Country} = \"Finland\", 60,

IF({Country} = \"France\", 61,

IF({Country} = \"Gabon\", 62,

IF({Country} = \"Gambia\", 63,

IF({Country} = \"Georgia\", 64,

IF({Country} = \"Germany\", 65,

IF({Country} = \"Ghana\", 66,

IF({Country} = \"Greece\", 67,

IF({Country} = \"Grenada\", 68,

IF({Country} = \"Guatemala\", 69,

IF({Country} = \"Guinea\", 70,

IF({Country} = \"Guinea-Bissau\", 71,

IF({Country} = \"Guyana\", 72,

IF({Country} = \"Haiti\", 73,

IF({Country} = \"Honduras\", 74,

IF({Country} = \"Hungry\", 75,

IF({Country} = \"Iceland\", 76,

IF({Country} = \"India\", 77,

IF({Country} = \"Indonesia\", 78,

IF({Country} = \"Iran\", 79,

IF({Country} = \"Iraq\", 80,

IF({Country} = \"Ireland\", 81,

IF({Country} = \"Israel\", 82,

IF({Country} = \"Italy\", 83,

IF({Country} = \"Jamaica\", 84,

IF({Country} = \"Japan\", 85,

IF({Country} = \"Jordan\", 86,

IF({Country} = \"Kazakhstan\", 87,

IF({Country} = \"Kenya\", 88,

IF({Country} = \"Kiribati\", 89,

IF({Country} = \"Kosovo\", 90,

IF({Country} = \"Kuwait\", 91,

IF({Country} = \"Kyrgyzstan\", 92,

IF({Country} = \"Laos\", 93,

IF({Country} = \"Latvia\", 94,

IF({Country} = \"Lebanon\", 95,

IF({Country} = \"Lesotho\", 96,

IF({Country} = \"Liberia\", 97,

IF({Country} = \"Libya\", 98,

IF({Country} = \"Liechtenstein\", 99,

IF({Country} = \"Lithuania\", 100,

IF({Country} = \"Luxembourg\", 101,

IF({Country} = \"Macedonia\", 102,

IF({Country} = \"Madagascar\", 103,

IF({Country} = \"Malawi\", 104,

IF({Country} = \"Malaysia\", 105,

IF({Country} = \"Maldives\", 106,

IF({Country} = \"Mali\", 107,

IF({Country} = \"Malta\", 108,

IF({Country} = \"Marshall Islands\", 109,

IF({Country} = \"Mauritania\", 110,

IF({Country} = \"Mexico\", 111,

IF({Country} = \"Moldova\", 112,

IF({Country} = \"Monaco\", 113,

IF({Country} = \"Mongolia\", 114,

IF({Country} = \"Montenegro\", 115,

IF({Country} = \"Morocco\", 116,

IF({Country} = \"Mozambique\", 117,

IF({Country} = \"Myanmar\", 118,

IF({Country} = \"Namibia\", 119,

IF({Country} = \"Nauru\", 120,

IF({Country} = \"Nepal\", 121,

IF({Country} = \"Netherlands\", 122,

IF({Country} = \"New Zealand\", 123,

IF({Country} = \"Nicaragua\", 124,

IF({Country} = \"Niger\", 125,

IF({Country} = \"Nigeria\", 126,

IF({Country} = \"North Korea\", 127,

IF({Country} = \"Norway\", 128,

IF({Country} = \"Oman\", 129,

IF({Country} = \"Pakistan\", 130,

IF({Country} = \"Palestinian Territories\", 131,

IF({Country} = \"Panama\", 132,

IF({Country} = \"Papua New Guinea\", 133,

IF({Country} = \"Paraguay\", 134,

IF({Country} = \"Peru\", 135,

IF({Country} = \"Philippines\", 136,

IF({Country} = \"Poland\", 137,

IF({Country} = \"Portugal\", 138,

IF({Country} = \"Qatar\", 139,

IF({Country} = \"Republic of Palau\", 140,

IF({Country} = \"Romania\", 141,

IF({Country} = \"Russia\", 142,

IF({Country} = \"Rwanda\", 143,

IF({Country} = \"Samoa\", 144,

IF({Country} = \"San Marino\", 145,

IF({Country} = \"Sao Tome and Principe\", 146,

IF({Country} = \"Saudi Arabia\", 147,

IF({Country} = \"Senegal\", 148,

IF({Country} = \"Serbia\", 149,

IF({Country} = \"Seychelles\", 150,

IF({Country} = \"Sierra Leone\", 151,

IF({Country} = \"Singapore\", 152,

IF({Country} = \"Slovakia\", 153,

IF({Country} = \"Slovenia\", 154,

IF({Country} = \"Soloman Islands\", 155,

IF({Country} = \"Somalia\", 156,

IF({Country} = \"South Africa\", 157,

IF({Country} = \"South Korea\", 158,

IF({Country} = \"South Sudan\", 159,

IF({Country} = \"Spain\", 160,

IF({Country} = \"Sri Lanka\", 161,

IF({Country} = \"St. Kitts and Nevis\", 162,

IF({Country} = \"St. Lucia\", 163,

IF({Country} = \"St. Vincent and the Grenadines\", 164,

IF({Country} = \"Sudan\", 165,

IF({Country} = \"Suriname\", 166,

IF({Country} = \"Swaziland\", 167,

IF({Country} = \"Sweden\", 168,

IF({Country} = \"Switzerland\", 169,

IF({Country} = \"Taiwan\", 170,

IF({Country} = \"Tajikistan\", 171,

IF({Country} = \"Tanzania\", 172,

IF({Country} = \"Thailand\", 173,

IF({Country} = \"Togo\", 174,

IF({Country} = \"Tonga\", 175,

IF({Country} = \"Trinidad and Tobago\", 176,

IF({Country} = \"Tunisia\", 177,

IF({Country} = \"Turkey", 178,

IF({Country} = \"Turkmenistan\", 179,

IF({Country} = \"Uganda\", 180,

IF({Country} = \"Ukraine\", 181,

IF({Country} = \"United Arab Emirates\", 182,

IF({Country} = \"United Kingdom\", 183,

IF({Country} = \"United States\", 184,

IF({Country} = \"Uruguay\", 185,

IF({Country} = \"Uzbekistan\", 186,

IF({Country} = \"Venezuela", 187,

IF({Country} = \"Vietnam", 188,

IF({Country} = \"West Germany\", 189,

IF({Country} = \"Yemen\", 190,

IF({Country} = \"Yemen Arab Republic\", 191,

IF({Country} = \"Yemen People\'s Republic", 192,

IF({Country} = \"Yugoslavia", 193,

IF({Country} = \"Zambia\", 194,

IF({Country} = \"Zimbabwe\", 195

))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))))
