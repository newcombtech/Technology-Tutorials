# Tableau Map Creation for MCH

Compiled by DRI Marisa Long

1.  Download these four files/folders from box and place somewhere
    convenient.<br>
    They can be found here: <https://app.box.com/folder/133174409935>

<img width="437" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159801239-bc7fe4dd-5b6d-41ea-8c0d-44d1f184a29b.png">


2.  Open Tableau Public on your desktop. You may need to login using the
    Tulane credentials, which are:<br>
    Username: ncitech@wave.tulane.edu<br>

    Password: Newcomb12!<br>

    Or if you are working on a personal project, create your own login with Tableau Public. <br>

    To start a new viz, you'll need to open either one of the geospatial
files or the excel sheets. Click on the appropriate one and then select
one of these files that you just downloaded. Click open.

<img width="114" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159801342-5c3162ef-3298-4a26-992e-fe425d73d04e.png">


3.  Tableau will take you to the data source page. Add all the other
    data sources you just downloaded by clicking on the "Add" button by
    "Connections." Once all four are added, click the "New Sheet"
    button.
    
<img width="439" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159801369-2e3f2844-a39d-4996-9eb5-3ae4041ddbb8.png">


4.  Go to your sheet. Select "Shapefile -- House" in the upper left hand
    corner and a list of tables should appear. Under the second heading
    labeled "House districts" you will see "Latitude (generated)" and
    "Longitude (generated)." Draw the longitude into the columns bar and
    the latitude into the rows bar.

<img width="468" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159801398-ef23e2ff-d933-4447-9515-63091e2bcdf7.png">

5.  Then, "Name" and "Geometry" under "Marks." You should now be able to
    scroll over the map and see the different districts.

<img width="468" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159801418-d45009cc-43c2-41d5-932a-b7197bbfe746.png">


6.  Next, go back to the tab at the bottom left labeled "data source."
    To be able to correctly query the data, we're going to need to join
    some of the data. Click on "birth outcomes" on the left and then
    drag "HOUSE DISTRICTS to the workspace. Right click on it and click
    open. Next, you going to want to drag over "Act 1 House 2011" across
    from it. At this point, Tableau will ask you how you want to join
    the data. For "HOUSE DISTRICTS", select "District Nums" from the
    dropdown and for "Act 1 House 2011" select "District I" from the
    drop down. Choose a full-outer join.

<img width="329" alt="Picture1" src="https://user-images.githubusercontent.com/89610126/159801479-7253a8fa-ad7f-4c47-802e-b6e54438b870.png">

<img width="346" alt="Pictur21" src="https://user-images.githubusercontent.com/89610126/159801483-9c1b99f2-6701-48fa-8b70-5baa93ccf162.png">


7.  Next, go back to the sheet you created with the map. Under the HOUSE
    DISTRICTS label on the left-hand side, begin dragging the data over
    to "Marks" as a detail. Here you can see that I've done it for
    Nbirths.

<img width="397" alt="3" src="https://user-images.githubusercontent.com/89610126/159801504-cd3c50d7-0436-49e5-899f-ae979f58e875.png">


Here is all of them dragged over. When you scroll over the map, the data
for the selected district should appear.

<img width="384" alt="1" src="https://user-images.githubusercontent.com/89610126/159801554-28a36cfa-b7b0-4129-bf01-b8fef1d3719d.png">


8.  Repeat steps 4-7 using the "United States Louisiana Administrative
    Boundaries Polygon" file for the latitude, longitude, geometry, and
    parish names, and "Louisiana Healthcare Providers by Parish" file in
    place of the HOUSE DISTRICTS file from "Birth outcomes by year".
    This new data will allow you to create the Parish map.

9.  Once you have created both maps on separate sheets, create a
    dashboard by clicking the grid-looking icon in the lower-right hand
    corner.

<img width="407" alt="2" src="https://user-images.githubusercontent.com/89610126/159801575-bc341ea5-8529-4b49-9d9d-746bd686f43d.png">

10. Drag "Horizontal" from under objects onto the blank dashboard where
    it says "drop sheets here." Then drag each of you sheets with your
    maps onto each side of the horizontal divide so that they lay
    side-by-side.

<img width="133" alt="3" src="https://user-images.githubusercontent.com/89610126/159801640-0dc686b1-cff9-4940-922a-fb7f797ef219.png">
<img width="428" alt="4" src="https://user-images.githubusercontent.com/89610126/159801648-0e3ef94e-26c7-46f9-a3bf-ba7cd32628fa.png">


11. Create a checkbox query by going back to the original sheets. I'm
    going to be demonstrating on the district map. From the left side
    bar, drag "race" and "year" into the filter box. For race, click all
    the checkboxes and for year leave as the default setting. Hit ok.

<img width="468" alt="1" src="https://user-images.githubusercontent.com/89610126/159801710-69cf6108-fac5-4876-b0bd-073b213038ee.png">
<img width="190" alt="2" src="https://user-images.githubusercontent.com/89610126/159801721-30ec38e5-f43a-4f9a-8e3e-e5b68f590965.png">
<img width="235" alt="3" src="https://user-images.githubusercontent.com/89610126/159801728-3f357f79-11a6-4e42-bc54-1170cde36a0c.png">


12. Right click on race and select "show filter." Do the same for year.
    Also right click each, go to "apply to worksheets" and select "all
    using this data source."
<img width="468" alt="1" src="https://user-images.githubusercontent.com/89610126/159801799-a8c410e9-4144-440e-ac14-ab071d451f78.png">


13. Repeat steps 11-12 for the parishes.

14. All done!

<img width="370" alt="2" src="https://user-images.githubusercontent.com/89610126/159801809-cc9cd866-faf5-487d-9438-ac7f01e1e9fa.png">

