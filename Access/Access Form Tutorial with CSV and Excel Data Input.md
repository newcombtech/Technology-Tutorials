**Video Walk through of the process:
https://youtu.be/axRrun5OaEU**

Notes on forms - Delete the first line of the excel sheet if it's blank,
save the file as a new name to the Desktop and ".csv", have all the
answers be "Don't know" automatically (-99), have "Don't Know" and "n/a"
be programmed as the same thing (-99),

<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162013630-17ab1b80-048f-4652-97dc-ec5e47f1b2fa.png">

## Database 

1.  To create a new database based on updated forms download them by
     "export" after logging in, click on the section that you want and
     then click the "export", it should download as a CSV, which is
     what you want

<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162013743-23ee5ffc-53ed-4e34-9422-a9858f36eb44.png">

 2. to create a new database, click "blank database"

<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162013780-2ed8f2ab-6658-4e05-b3b7-8e79b79e749a.png">

 3. then click the red x on the right

<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162013814-2d5214c3-82cf-4526-b2d7-630d455a5ee8.png">

 4. which afterwards it should look like this

<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162013852-4d4bbb07-6b38-412a-ad93-ce86dd9ec8f1.png">

5.  Now you can officially import a new blank database, do this by
     choosing; "New Data Source", "From File", "Excel"

<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162013878-d5d5d6fc-23cf-410a-842c-010cf012528b.png">

6. This will then pop up, make sure "First Row contains column
 headings" is selected
<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162013919-599e38f4-74ae-4fa1-ba2a-b4ac0a215ddb.png">

 7. Make sure it then looks like this and click "Next"

<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162013945-17bd1002-9602-4893-98e5-adb0a96920fa.png">

 8. Choose "Choose my own primary key", and select "amnestyID"
<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162013969-9289e6c7-875c-4f5a-8b29-b6f02288ed3a.png">

9.  Then click "Finish", there might be a box that pops up that says
     there are IDs that don't work, and it will create a table like the
     one below, that's fine

<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162014009-8bb87363-64de-4681-9d93-ade30ae4b069.png">

<br><br>
## Forms 
On the selected Database, go to "Create" and choose Form, and it will create a form that is linked with the database

<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162014148-2d48c5a1-6754-40fb-a7d1-511b7d68769f.png">

1.  following the step above, a blank form will pop up, and then
     navigate to "Design View" after right clicking on the form name

<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162014164-daacc77a-aaef-4a37-b558-2ab264f94875.png">

2.  Design view will bring up this format so you can edit the form
     easily, and to create a header for each section, select the gray
     highlighted "Aa"
<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162014194-deaf25b7-36d7-4de7-a05a-1844167d4ddf.png">

 3. Using this you can create headers like this
<img width="189" alt="image" src="https://user-images.githubusercontent.com/89610126/162014221-1286622f-2aed-4a97-8d15-615ece056f99.png">

 4. You can change the background and letter colors through right
 clicking
<img width="246" alt="image" src="https://user-images.githubusercontent.com/89610126/162014247-13a4bd35-d983-4588-ad5b-f0088fc51a9f.png">

5.  In order to add form sections -- click "Add Existing Fields", and
     select the table that the form is connected to

<img width="162" alt="image" src="https://user-images.githubusercontent.com/89610126/162014276-77a744c2-e427-4176-b0da-1f1366d0d3cd.png">

 6. clicking on the "+" will have the drop down appear
<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162014306-20961c18-c67a-4987-a803-691df1c9e820.png">

7.  Once the new field has been added to the box, you want to create a
     new field, that you can apply to the field you just selected --
     scroll down on the design options, to get to the gray highlighted
     box
<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162014336-1f09b241-7d47-459e-a05e-32c173ca86d0.png">

8. Once you click on that option, choose "I will type in the values
 that I want"

<img width="467" alt="image" src="https://user-images.githubusercontent.com/89610126/162014360-dbdc7d95-1a1f-4e91-be0b-c86c03f3d4bf.png">

9.  Then add the values that resemble the ones from the TJ database,
     that correspond with the form options that the coders are shown on
     the left, and the right is the options that fill in the database
<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162014413-da14f3d2-d8df-4ea7-bd43-02b78ab8af8c.png">

10. After clicking next, select "Col2" so that the numbers and info are
     filled into the database, not the words
<img width="468" alt="image" src="https://user-images.githubusercontent.com/89610126/162014456-6ed9eab5-c9eb-4294-b77c-0a74cfc1d775.png">

11. Then choose the value that you want to store the information into,
     aka the field that you just added to the form

    a.  Try to make it so that the default answer or a blank response is
         "i don't know" aka --99

12. After this you can delete the original box that you added, before
     you create the new multiple selection box, and then move the
     selection box into place!
