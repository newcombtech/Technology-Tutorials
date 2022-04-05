# UPLOADING CSV TO WORDPRESS #

1.  Ensure you have the Custom Post Type UI, Custom Fields, and All
     import Free plugins installed and running on the WordPress site.

2.  Add a void column into the Database. This should be a blank column
     with a header that can be used to fill the title of the posts
     later.

3.  Ensure that the title of each column on the CSV database is
     lowercase and either one word or connected using underscores.

4.  Open CPT UT to create a new post type to contain the imported data.

    a.  Under ​**Add New Post Type**​ fill in the ​**Post Type Slug**
         ​ (this is the name of the new post type), ​**Plural Label,**
         ​ and ​**Singular Label.** ​For example, if I wanted to upload
         data about movies, I would fill in the fields as follows:

<img width="173" alt="image" src="https://user-images.githubusercontent.com/89610126/161863501-f2b0daa9-0be3-49d0-bfbc-c921683fa337.png">

b.  Click the ​**Add Post Type** ​button at the bottom of the page. The
     new post type should now appear in the main menu on the left-hand
     side of the screen with a thumbtack icon next to it.

<img width="63" alt="image" src="https://user-images.githubusercontent.com/89610126/161863583-0d4d0194-7948-45b1-8231-f044946e3c50.png">

5.  Open Custom Fields to create fields to upload data into.

    a.  In the ​**Add Title** ​bar, choose a general name for the group
         of custom fields you are creating.

    b.  In the box that says ​**Location**​ it should say "show this
         field group if Post Type is equal to Post". Change the Post
         setting to the custom post type you created in the previous
         step.

<img width="321" alt="image" src="https://user-images.githubusercontent.com/89610126/161863610-b0fd46f9-913f-4374-9929-a94050058b97.png">

c.  Click the ​+ Add Field ​button and choose a ​**Field label,
     Field Name, and Field Type.** ​The field type is specific to the
     type of data that will be uploaded into that field. The two most
     common field types are ​**Text** ​or ​**Number** ​but there are
     many options for specific kinds of data like URLs, images, etc.

d.  Make sure the names of your custom fields are the exact names of the
     fields in the CSV file (the first row of your data set in the CSV
     file).

e.  There are options to set a default value in the field, prepend and
     append, set character limits and other customizations that can be
     altered based on the data being uploaded but are usually
     unnecessary.

f.  Click ​**Publish** ​to create the Custom Field group. A published
     custom field group will look like this:

<img width="387" alt="image" src="https://user-images.githubusercontent.com/89610126/161863635-e040ed6f-9041-40ff-8b3b-55fbcc579021.png">

6.  Open the post type you created in Step 1 and click the ​**Add
     New**​ button to create a "dummy" post. This will allow WordPress
     to recognize the custom fields you have created when it uploads
     the data from you CSV file.

    a.  Enter in the title and fill in custom fields for a post. This
         does not have to be anything in your data set, it just
         functions as a placeholder before you upload your data.

  
    b.  Publish the dummy post


7.  Select new import in All Import and upload the CSV file

8.  Select the type of post you your import to be (page, post, custom
     type, etc.)

9.  All of your data will be imported. Check to see if it looks correct

10. Drag and drop one of the blue elements on the right into the title
     section

11. Format the post using the visual or html editor (I thought it was
     easier to use the html).

12. Drag and drop the blue elements anywhere you want to include the
     data from that column in the CSV. For example, wherever you drag
     and drop the element corresponding to the ID number, the ID number
    for that entry will be placed. The element that will be imported
     from the CSV will appear in {curly braces}

13. Add a unique identifier that is unique for each element you are
     importing

14. Press confirm and run import

15. Check to make sure your posts imported correctly
