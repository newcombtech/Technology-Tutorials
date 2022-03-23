Tableau Map Creation for MCH

Compiled by DRI Marisa Long

1.  Download these four files/folders from box and place somewhere
    convenient.

They can be found here: <https://app.box.com/folder/133174409935>

![Graphical user interface, text Description automatically
generated](media/image1.png){width="6.069444444444445in"
height="1.375in"}

2.  Open Tableau Public on your desktop. You may need to login using the
    Tulane credentials, which are:

Username: ncitech@wave.tulane.edu

Password: Newcomb12!

Or if you are working on a personal project, create your own login with
Tableau Public.

To start a new viz, you'll need to open either one of the geospatial
files or the excel sheets. Click on the appropriate one and then select
one of these files that you just downloaded. Click open.

![Graphical user interface, application Description automatically
generated](media/image2.png){width="1.593176946631671in"
height="3.354055118110236in"}

3.  Tableau will take you to the data source page. Add all the other
    data sources you just downloaded by clicking on the "Add" button by
    "Connections." Once all four are added, click the "New Sheet"
    button.

![Graphical user interface, application Description automatically
generated](media/image5.png){width="6.116750874890639in"
height="3.4942596237970256in"}

4.  Go to your sheet. Select "Shapefile -- House" in the upper left hand
    corner and a list of tables should appear. Under the second heading
    labeled "House districts" you will see "Latitude (generated)" and
    "Longitude (generated)." Draw the longitude into the columns bar and
    the latitude into the rows bar.

![Graphical user interface Description automatically
generated](media/image6.png){width="6.5in"
height="3.6708333333333334in"}

5.  Then, "Name" and "Geometry" under "Marks." You should now be able to
    scroll over the map and see the different districts.

![Graphical user interface Description automatically
generated](media/image7.png){width="6.5in"
height="3.6034722222222224in"}

6.  Next, go back to the tab at the bottom left labeled "data source."
    To be able to correctly query the data, we're going to need to join
    some of the data. Click on "birth outcomes" on the left and then
    drag "HOUSE DISTRICTS to the workspace. Right click on it and click
    open. Next, you going to want to drag over "Act 1 House 2011" across
    from it. At this point, Tableau will ask you how you want to join
    the data. For "HOUSE DISTRICTS", select "District Nums" from the
    dropdown and for "Act 1 House 2011" select "District I" from the
    drop down. Choose a full-outer join.

![Graphical user interface, application Description automatically
generated](media/image8.png){width="4.591911636045494in"
height="2.9871948818897636in"}

![Graphical user interface, application Description automatically
generated](media/image9.png){width="4.846515748031496in"
height="2.9902373140857392in"}

7.  Next, go back to the sheet you created with the map. Under the HOUSE
    DISTRICTS label on the left-hand side, begin dragging the data over
    to "Marks" as a detail. Here you can see that I've done it for
    Nbirths.

![Graphical user interface, text, application Description automatically
generated](media/image10.png){width="5.516188757655293in"
height="3.5195166229221346in"}

Here is all of them dragged over. When you scroll over the map, the data
for the selected district should appear.

![Graphical user interface, application, map Description automatically
generated](media/image11.png){width="5.336212817147857in"
height="3.3471062992125984in"}

8.  Repeat steps 4-7 using the "United States Louisiana Administrative
    Boundaries Polygon" file for the latitude, longitude, geometry, and
    parish names, and "Louisiana Healthcare Providers by Parish" file in
    place of the HOUSE DISTRICTS file from "Birth outcomes by year".
    This new data will allow you to create the Parish map.

9.  Once you have created both maps on separate sheets, create a
    dashboard by clicking the grid-looking icon in the lower-right hand
    corner.

![Graphical user interface, application, Word Description automatically
generated](media/image12.png){width="5.646765091863517in"
height="3.552755905511811in"}

10. Drag "Horizontal" from under objects onto the blank dashboard where
    it says "drop sheets here." Then drag each of you sheets with your
    maps onto each side of the horizontal divide so that they lay
    side-by-side.

![Graphical user interface, application Description automatically
generated](media/image13.png){width="1.8504483814523185in"
height="1.7904800962379703in"}

![Graphical user interface, map Description automatically
generated](media/image14.png){width="5.943127734033246in"
height="4.372896981627297in"}

11. Create a checkbox query by going back to the original sheets. I'm
    going to be demonstrating on the district map. From the left side
    bar, drag "race" and "year" into the filter box. For race, click all
    the checkboxes and for year leave as the default setting. Hit ok.

![Graphical user interface, map Description automatically
generated](media/image15.png){width="6.5in" height="4.09375in"}

![Graphical user interface, text, application Description automatically
generated](media/image16.png){width="2.641541994750656in"
height="1.8989884076990375in"} ![Graphical user interface, text,
application Description automatically
generated](media/image17.png){width="3.2787784339457566in"
height="2.4254549431321086in"}

12. Right click on race and select "show filter." Do the same for year.
    Also right click each, go to "apply to worksheets" and select "all
    using this data source."

![Map Description automatically
generated](media/image18.png){width="6.5in" height="3.89375in"}

13. Repeat steps 11-12 for the parishes.

14. All done!

![Map Description automatically
generated](media/image19.png){width="5.1370417760279965in"
height="4.3807556867891515in"}
