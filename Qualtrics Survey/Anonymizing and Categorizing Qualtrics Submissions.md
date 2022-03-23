> **Qualtrics Surveys**
>
> **Goals**

-   Categorize submissions

-   Separate identifying information (name, email, etc.) from the
    content of the proposal for anonymous judging

-   Rejoin the identifying info with the proposal content

> **Resources and Ideas**
>
> [**[Good overview of
> qualtrics]{.underline}**](https://uregina.libguides.com/c.php?g=717078&p=5115910)

-   There might be an easier way to do this.
    [[This]{.underline}](https://www.qualtrics.com/support/survey-platform/common-use-cases-rc/creating-an-anonymized-raffle/)
    could be helpful in keeping it anonymous while still having the
    ability to match entries back with the names, but I'm not sure if we
    could remove the random element

-   If we can make edits to the form itself, it might be useful to make
    title and abstract separate fields for convenience's sake.

> **Workflow Idea**

1.  Get survey responses

2.  [[Assign participant ID to each
    response]{.underline}](https://www.qualtrics.com/support/survey-platform/common-use-cases-rc/assigning-randomized-ids-to-respondents/)

3.  [[Add an empty field for accepted to each
    response]{.underline}](https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/data/add-new-fields/manual-variables/)

    a.  Create a manual number field with 0 being not accepted and 1
        > being accepted

4.  [[If the proposal is a resubmission, mark it as
    accepted]{.underline}](https://www.qualtrics.com/support/survey-platform/survey-module/using-logic/)

5.  [[Categorize responses by entry
    category]{.underline}](https://www.qualtrics.com/support/employee-experience/creating-ee-project/dashboards-tab/dashboard-management/dashboard-settings/categories-ee/)

6.  [[Split the data into two
    tables]{.underline}](https://www.qualtrics.com/support/employee-experience/creating-360-project/reports-tab-360/edit-subject-report/tables-360/tables-overview-360/)

    a.  Table 1 with the participant ID, name, and email

    b.  Table 2 with the participant ID and the rest of the data

7.  Give table 2 to the judges to mark the accepted entries as accepted

    a.  You could also split the tables based on categories if there is
        > going to be a different set of judges for each category and/or
        > the judges prefer to judge one category at a time. This could
        > also be helpful for basic organization and record keeping.

8.  Join the two tables (on the participant ID) together to add the name
    back

    a.  As of now, I think that this would require exporting each table
        > to a CSV and using excel/a simple python script to join them
        > back together, but I'll keep looking into it

9.  Filter based on accepted to find all the accepted participants

> **EXAMPLE OF TABLES**
>
> **Entered Data**

  --------------------------------------------------------------------------
  Name        Email       Resubmission   Category    Title       Keyword
  ----------- ----------- -------------- ----------- ----------- -----------
                                                                 

  --------------------------------------------------------------------------

> **Add ID Column**

  ------------------------------------------------------------------------------
  **ID**     Name       Email      Resubmission   Category   Title    Keyword
  ---------- ---------- ---------- -------------- ---------- -------- ----------
                                                                      

  ------------------------------------------------------------------------------

> **Add Accepted Column**

  -----------------------------------------------------------------------------------
  ID     Name     Email    Resubmission   Category   Title   Keyword   **Accepted**
  ------ -------- -------- -------------- ---------- ------- --------- --------------
                                                                       

  -----------------------------------------------------------------------------------

> **Create a table for each category**
>
> Microtalk

+--------+---------+---------+------------+------+---------+---------+
| > ID   | > Email | > Name  | > Re       | > T  | >       | > A     |
|        |         |         | submission | itle | Keyword | ccepted |
+========+=========+=========+============+======+=========+=========+
|        |         |         |            |      |         |         |
+--------+---------+---------+------------+------+---------+---------+

> Conference Paper

+--------+---------+---------+------------+------+---------+---------+
| > ID   | > Email | > Name  | > Re       | > T  | >       | > A     |
|        |         |         | submission | itle | Keyword | ccepted |
+========+=========+=========+============+======+=========+=========+
|        |         |         |            |      |         |         |
+--------+---------+---------+------------+------+---------+---------+

> Pre-constituted panel

+--------+---------+---------+------------+------+---------+---------+
| > ID   | > Email | > Name  | > Re       | > T  | >       | > A     |
|        |         |         | submission | itle | Keyword | ccepted |
+========+=========+=========+============+======+=========+=========+
|        |         |         |            |      |         |         |
+--------+---------+---------+------------+------+---------+---------+

> Screening/Workshop/Roundtable/Exhibition

+--------+---------+---------+------------+------+---------+---------+
| > ID   | > Email | > Name  | > Re       | > T  | >       | > A     |
|        |         |         | submission | itle | Keyword | ccepted |
+========+=========+=========+============+======+=========+=========+
|        |         |         |            |      |         |         |
+--------+---------+---------+------------+------+---------+---------+

> **Split each category table into two tables - a key and anonymous
> table**
>
> Microtalk_key

  -----------------------------------------------------------------------
  ID                      Name                    Email
  ----------------------- ----------------------- -----------------------
                                                  

  -----------------------------------------------------------------------

> Microtalk_anonymous

+---------+----------+-----------+------+---------+------------------+
| > ID    | > M      | > Re      | > T  | >       | > Accepted       |
|         | icrotalk | submissio | itle | Keyword |                  |
|         |          | > n       |      |         |                  |
+=========+==========+===========+======+=========+==================+
|         |          |           |      |         |                  |
+---------+----------+-----------+------+---------+------------------+

> \*repeat for all categories
>
> **Give to the judges for evaluation**
>
> Microtalk_key

  -----------------------------------------------------------------------
  ID                      Name                    Email
  ----------------------- ----------------------- -----------------------
  12345                   Proposal 1              <test@email.com>

  67890                   Proposal 2              <another@email.com>
  -----------------------------------------------------------------------

> Microtalk_anonymous

+---------+----------+-----------+------+----------+-----------------+
| > ID    | >        | > Re      | > T  | >        | > Accepted      |
|         | Category | submissio | itle |  Keyword |                 |
|         |          | > n       |      |          |                 |
+=========+==========+===========+======+==========+=================+
| > 12345 | > M      | > 0       | > Ti | >        | > 1             |
|         | icrotalk |           | tle1 | Keywords |                 |
+---------+----------+-----------+------+----------+-----------------+
| > 67890 | > M      | > 0       | > Ti | >        | > 0             |
|         | icrotalk |           | tle2 | Keywords |                 |
+---------+----------+-----------+------+----------+-----------------+

> \*repeat for all categories
>
> **Join each category table on ID**
>
> Microtalk_judged

+-----+-------+------+-------------+----------+----+--------+-------+
| ID  | Cat   | Name | Email       | Res      | T  | Ke     | Ac    |
|     | egory |      |             | ubmissio | it | ywords | cepte |
|     |       |      |             | n        | le |        | d     |
+=====+=======+======+=============+==========+====+========+=======+
| 1   | Mic   | Pro  | <test       | 0        | T  | Ke     | 1     |
| 234 | rotal | posa | @email.com> |          | it | ywords |       |
|     | k     | l 1  |             |          | le | 1      |       |
| 5   |       |      |             |          | 1  |        |       |
+-----+-------+------+-------------+----------+----+--------+-------+
| 6   | Mic   | Pro  | <test       | 0        | T  | Ke     | 0     |
| 789 | rotal | posa | 2@email.co> |          | it | ywords |       |
|     | k     | l 2  | m           |          | le | 2      |       |
| 0   |       |      |             |          | 2  |        |       |
+-----+-------+------+-------------+----------+----+--------+-------+

> \*repeat for all categories
>
> **Concatenate all the category tables together to get a master list**
>
> Microtalk_judged + ConferencePaper_judged
> +PreConstitutedPanel_judged + Exhibition_judged

+----+--------+------+------------+----------+----+--------+-------+
| ID | Ca     | Name | Email      | Res      | T  | Ke     | Ac    |
|    | tegory |      |            | ubmissio | it | ywords | cepte |
|    |        |      |            | n        | le |        | d     |
+====+========+======+============+==========+====+========+=======+
| 12 | Mic    | Pro  | <test@     | 0        | T  | Ke     | 1     |
| 34 | rotalk | posa | email.com> |          | it | ywords |       |
|    |        |      |            |          | le |        |       |
+----+--------+------+------------+----------+----+--------+-------+
| 5  |        | l 1  |            |          | 1  | 1      |       |
+----+--------+------+------------+----------+----+--------+-------+
| 67 | Mic    | Pro  | <test2     | 0        | T  | Ke     | 0     |
| 89 | rotalk | posa | @email.co> |          | it | ywords |       |
|    |        |      |            |          | le |        |       |
+----+--------+------+------------+----------+----+--------+-------+
| 0  |        | l 2  | m          |          | 2  | 2      |       |
+----+--------+------+------------+----------+----+--------+-------+
| 23 | Con    | Pro  | <tes3t     | 1        | T  | Ke     | 1     |
| 45 | ferenc | posa | @email.co> |          | it | ywords |       |
|    |        |      |            |          | le |        |       |
+----+--------+------+------------+----------+----+--------+-------+
| 6  | e      | l 3  | m          |          | 3  | 3      |       |
|    | Paper  |      |            |          |    |        |       |
+----+--------+------+------------+----------+----+--------+-------+
| 34 | Pre-   | Pro  | <test4     | 0        | T  | Ke     | 0     |
| 56 | Consti | posa | @email.co> |          | it | ywords |       |
|    | tuted  | l 4  | m          |          | le | 4      |       |
| 7  |        |      |            |          | 4  |        |       |
+----+--------+------+------------+----------+----+--------+-------+
|    | Panel  |      |            |          |    |        |       |
+----+--------+------+------------+----------+----+--------+-------+
| 45 | Exhi   | Pro  | <test5     | 1        | T  | Title5 | 1     |
| 67 | bition | posa | @email.co> |          | it |        |       |
|    |        |      |            |          | le |        |       |
+----+--------+------+------------+----------+----+--------+-------+
| 8  |        | l 5  | m          |          | 5  |        |       |
+----+--------+------+------------+----------+----+--------+-------+
