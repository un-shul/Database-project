# DBMS Assignment 3 - Club Management System Webapp

## Made with Flask and MySQL

### Setup (G1 and G2)

1. Install Python
2. Install MySQL
3. Install the required packages for python: 

    ```bash
    pip install flask
    pip install flask-mysql
    pip install flask-session
    pip install mysql-connector-python
    ```

4. Create the database `CLUB_MS`.
    In order to do login in to MYSQL Workbench using your root user and run the 'studentdb.sql' file in your SQL Workbench. This will create the database and populate it with the required tables and data.

5. Now update the mysql configurations in 'app.py' file.
    If you are using root user like us you can enter your root password for the password key below in the 'app.py' file, however, it should be best to rather use some other user and and passowrd, but for that you need to run the script 'studentdb.sql' with the same user.
    ```py
    mysql_config = {
    'host': 'localhost',
    'user': 'root',
    'password': 'DBMS_mysql@0204',    #Enter ur password for root
    'database': 'CLUB_MS'
    }
    ```
6. Login in to MYSQL Workbench using your root user.

   - Click on the 'Administration' tab.
   <img width="1440" alt="Screenshot 2024-04-04 at 4 31 17 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/ee5c9d35-38aa-4b1d-aa04-3507ab9d7377">
   
   - Click on the 'Users and Privileges' option.
   - Click on the 'Add Account' button.
   -Enter the following details keeping the rest of the fields as default:

       - Login Name: newuser
       - Password: mannudb
   - Click on the apply button.
      
<img width="1440" alt="Screenshot 2024-04-04 at 4 32 20 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/e1d45c6a-da12-41a3-aac6-3584d4a50cd6">

   - Click on 'Administrative Roles' and then click on 'Revoke All Privileges'.
   <img width="1440" alt="Screenshot 2024-04-04 at 4 33 23 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/65b4f338-152d-42a9-b252-2655136641cc">

   - Click on 'Schmema Privileges' and then click on 'Revoke All Privileges'.
    
   <img width="1440" alt="Screenshot 2024-04-04 at 4 33 43 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/183a31ce-71ba-408c-bd31-20c00185a12c">

   - Go to your home tab in Workbench and then add a new connection by clicking 
     on the '+' button:
     <img width="1440" alt="Screenshot 2024-04-04 at 4 34 03 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/f1cd9d7f-43d0-4263-846b-e3b27146defb">
     
   -  Here Enter the following:
            - Connection Name: student
            - Username: student

   - Click on 'Test Connection' and then enter the password mannudb when 
     prompted. Then click on 'OK'.


7. Repeat the entire above point for a new user 'employee' in your MYSQL 
     Workbench with the following details:
      - Login Name: employee
      - Connection Name: employee
      - Username: employee
      - Password: mannudb


8. Grant Permissions to the 'student' role.
     In order to do this, run the 'student_role_permissions' file in the 'Dump 
     Files' directory in your SQL Workbench. This will grant the required 
     permissions to the 'student' role.


9. Grant Permissions to the 'employee' role.
    In order to do this, run the 'employee_role_permissions' file in the 'Dump 
    Files' directory in your SQL Workbench. This will grant the required 
    permissions to the 'employee' role.



### Running the Webapp

After setting up the database and configuration, we can run our webapp. To do that:
1. Open your terminal window in the folder 'Database-Project/' and run the following:
    ```bash
    python app.py
    ```
2. Open your browser and go to the URL that is displayed in the terminal, like this:
    ```bash
    http://127.0.0.1:5000
    ```

Now your home page is opened which is a login page for our Club Management System where you can login as a student, employee or admin (person with all permissions).

### Login view

<img width="1440" alt="Screenshot 2024-04-05 at 5 44 03 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/fcb723c1-260b-49ba-8394-e4060fcce318">

<img width="1440" alt="Screenshot 2024-04-05 at 5 43 06 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/79a9e359-d3bc-4575-a5ad-3ad27723451d">

<img width="1440" alt="Screenshot 2024-04-05 at 5 44 20 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/29852eda-e02d-4e99-b081-ef34fde44956">

<img width="1440" alt="Screenshot 2024-04-05 at 5 44 31 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/1f3a9ec7-da8a-43c5-b776-1519066b7463">


### Equipment view

<img width="1440" alt="Screenshot 2024-04-05 at 5 48 08 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/d354de73-b912-40fa-831d-ffeb26f41924">

<img width="1440" alt="Screenshot 2024-04-05 at 5 48 14 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/58c975e3-eb5d-4c1b-80b1-19ecbd5f08c6">

<img width="1440" alt="Screenshot 2024-04-05 at 5 48 27 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/5530957e-508d-48c9-8054-5a5d8b503e7d">

<img width="1440" alt="Screenshot 2024-04-05 at 5 48 48 PM" src="https://github.com/msrathore-69781/Database-project/assets/103460353/ed012e03-d971-4fd8-91ec-71c50cc26f1d">


### Operations on ADMIN view
 Admin can perform INSERT, DELETE and RENAME queries on the tables of the database.
 BEFORE : </br>
 ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/f9cd98f7-48ce-4889-b64d-24a143fcd1b7) </br>
 ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/6e0391af-5ff9-477f-955a-b787fe864437) </br>

1. Performing INSERT </br>
    We INSERT a club "Club_dummy" to our clubs table. Fill in all the fields and press INSERT button. Changes will reflect both on the webapp and database. </br>
   ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/e84ec765-ff34-4b2a-8f4c-7737fffa94c4) </br>
   ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/8dfbb7a9-21bf-4b52-8200-3646299043b3) </br>
2. Performing  DELETE </br>
    We DELETE the club "Club_dummy" which we earlier added. Just fill in the corresponding fields and press DELETE. </br>
    ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/e496a804-7a74-44b0-94cb-3e176b3a6c7a) </br>
    ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/7425238f-1b80-4d57-ac3f-998d83729a59) </br>
3. Performing RENAME </br>
    Admin can rename a table and it will reflect over the database and the webapp. </br>
    On pressing the RENAME button the following fields appears asking fora new name. Fill in the field and press enter.</br>
    ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/ff82ea9c-a551-4784-9573-d541b7ea030d) </br>

   Renaming clubs to clubs_of_iitgn.</br>
   ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/e7c00069-bf10-4bf8-baad-de0f8c2eb5ee)</br>
    Also reflected on the sql where now club_ms.clubs table doesn’t exist, instead club_ms.clubs_of_iitgn exists. Same can be tried out for other tables from the admin Page whose access only lies with admin (if you login as admin).</br>
   ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/f765f449-dbdc-457e-9546-f766a90ed031) </br>
   Also the main admin page has now changed </br>
   ![image](https://github.com/msrathore-69781/Database-project/assets/102381105/2c05286d-8ab7-49c8-a8e5-e425ed326222)









## Work Distribution

### G1

1. #### Anshul Choudhary
   - Worked on ideating the initial design of the website.
   - Made sketches and illustrated the flow of the website and different requirements
   - Made front-end for couple of website including css styling
   

2. #### Shrijan Sahu
   - Made front-end for many pages and beautified their looks
   - Ideated on various possible design themes for the website.
   - Added javascript and accomplished dynamic changes obtained from running backend

3. #### Amey Rangari
   - Participated in initial design ideation for the website to discuss flow and execution.
   - Made beautification and visual changes to various components of project.
   - Assisted in debugging of various issues arrived during linking.

### G2

1. #### Shubh Singhal
   - Ideated and wrote various backend queries required for smooth functioning of webapp.
   - Added and tested various views and dynamic operations. 
   - Led in debugging various inconsistences and bugs accumulated in running the webapp.

   

2. #### Yashraj Deshmukh
   - Led in writing back-end code for various pages and setting routing protocols.
   - Ideated on what routing protocols to follow and work-flow of app.
   - Worked on combining various elements of database system.
   

3. #### Pratham Sagar
   - Ideated on what permissions to be alloted to different users and implemented that.
   - Documented the screenshots of the execution in the ReadMe.MD file.
   - Collaborated with Front-end team and contributed to html structure of pages.
   

4. #### Manvendra Singh
   - Setup the inital required connections for flask and mysql integration with the webapp.
   - Documented the testing output with snapshots in the ReadMe.MD file.
   - Made backend-routing protocols for many pages and fit them in the front-end.
   




   




   
