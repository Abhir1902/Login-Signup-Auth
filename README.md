# Login-Signup-Auth
This is an open source repository for login and signup authentication services.

This is a PHP API that will be used to manage the the sign-up and login feature.

# Steps to be used while using this repo

Fork from this repo, and create a clone for your local computer.
In the DataConfig.php file and change the details with respect to your database.

Include the below code in the DataConfig.php:

    $ require "DataBase.php";

In both the login and signup file add this object for the Database class

    $ db = new DataBase();
    
Call the above created function, with the below function:

    $ db->dbConnect();
    
Now, the below code will check if the conenction is successfull or not:
 
    $db = new DataBase();
    if ($db->dbConnect()) {
        // The connection have been successfully created
    }
    else{
        //There is an error in the connection.
    }

# Calling the Modules - Login and SignUp

Login Module - 

    $ db->logIn($tablename, $username, $password);
    
Sign-Up Module - 

    $ db->signUp($tablename, $fullname, $username, $password, $email);
