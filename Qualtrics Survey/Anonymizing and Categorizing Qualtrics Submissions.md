# Qualtrics Surveys

 **Goals**

-   Categorize submissions

-   Separate identifying information (name, email, etc.) from the
    content of the proposal for anonymous judging

-   Rejoin the identifying info with the proposal content <br><br>

**Resources and Ideas**

-  [**Good overview of
 qualtrics**](https://uregina.libguides.com/c.php?g=717078&p=5115910)

-   There might be an easier way to do this.
    [This](https://www.qualtrics.com/support/survey-platform/common-use-cases-rc/creating-an-anonymized-raffle/)
    could be helpful in keeping it anonymous while still having the
    ability to match entries back with the names, but I'm not sure if we
    could remove the random element

-   If we can make edits to the form itself, it might be useful to make
    title and abstract separate fields for convenience's sake.  <br><br>

**Workflow Idea**

1.  Get survey responses

2.  [Assign participant ID to each
    response](https://www.qualtrics.com/support/survey-platform/common-use-cases-rc/assigning-randomized-ids-to-respondents/)

3.  [Add an empty field for accepted to each
    response](https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/data/add-new-fields/manual-variables/)

    a.  Create a manual number field with 0 being not accepted and 1
         being accepted

4.  [If the proposal is a resubmission, mark it as
    accepted](https://www.qualtrics.com/support/survey-platform/survey-module/using-logic/)

5.  [Categorize responses by entry
    category](https://www.qualtrics.com/support/employee-experience/creating-ee-project/dashboards-tab/dashboard-management/dashboard-settings/categories-ee/)

6.  [Split the data into two
    tables](https://www.qualtrics.com/support/employee-experience/creating-360-project/reports-tab-360/edit-subject-report/tables-360/tables-overview-360/)

    a.  Table 1 with the participant ID, name, and email

    b.  Table 2 with the participant ID and the rest of the data

7.  Give table 2 to the judges to mark the accepted entries as accepted

    a.  You could also split the tables based on categories if there is
         going to be a different set of judges for each category and/or
         the judges prefer to judge one category at a time. This could
         also be helpful for basic organization and record keeping.

8.  Join the two tables (on the participant ID) together to add the name
    back

    a.  As of now, I think that this would require exporting each table
         to a CSV and using excel/a simple python script to join them
         back together, but I'll keep looking into it

9.  Filter based on accepted to find all the accepted participants  <br><br>

 **EXAMPLE OF TABLES**

**Entered Data**

					
![image](https://user-images.githubusercontent.com/89610126/159799958-7be93faa-05da-481a-85e5-cc31d3b0b2a6.png)

 **Add ID Column**
						
![image](https://user-images.githubusercontent.com/89610126/159800068-11c8af5a-8408-4e4c-a54f-91d2181cc9e8.png)

 **Add Accepted Column**

 
							
![image](https://user-images.githubusercontent.com/89610126/159800101-8c5bcd80-183e-45fe-8952-4dc03e387994.png)


 **Create a table for each category**

 Microtalk


						
![image](https://user-images.githubusercontent.com/89610126/159800145-c8e0304f-99ae-4094-9106-8c67b7f49769.png)


 Conference Paper


						
![image](https://user-images.githubusercontent.com/89610126/159800165-b2a0e194-d920-4a35-8de0-df419258de61.png)


 Pre-constituted panel

						
![image](https://user-images.githubusercontent.com/89610126/159800191-f0dc5a4e-1897-47d7-97c8-78807d8830e6.png)



 Screening/Workshop/Roundtable/Exhibition


						
![image](https://user-images.githubusercontent.com/89610126/159800215-57830ecc-bfc8-4517-a674-908e11def4e0.png)


 **Split each category table into two tables - a key and anonymous
 table**

 Microtalk_key


		
![image](https://user-images.githubusercontent.com/89610126/159800252-ca0983c3-6879-4647-b8ed-f6dea5a3555a.png)

 Microtalk_anonymous


					
![image](https://user-images.githubusercontent.com/89610126/159800285-648ef38f-9462-4e5f-91f7-879cc310f04b.png)

 \*repeat for all categories <br><br>

 **Give to the judges for evaluation**

 Microtalk_key



![image](https://user-images.githubusercontent.com/89610126/159800333-bde3725f-e391-4670-8bcc-f2e71d1ad689.png)


Microtalk_anonymous

![image](https://user-images.githubusercontent.com/89610126/159800364-6ac4d4d6-e647-4836-96ac-55654d7c3d4e.png)


 \*repeat for all categories  <br><br>

 **Join each category table on ID**

 Microtalk_judged

![image](https://user-images.githubusercontent.com/89610126/159800418-3ade2b59-dd8c-4fa2-af73-874e0e4ededf.png)


 \*repeat for all categories  <br><br>

 **Concatenate all the category tables together to get a master list**

 Microtalk_judged + ConferencePaper_judged
 +PreConstitutedPanel_judged + Exhibition_judged
	
![image](https://user-images.githubusercontent.com/89610126/159800460-8799ec4a-2a5d-434d-89fb-7f7eccc0f7bc.png)


