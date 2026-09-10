

# Create a .vnudl file to connect to an Oracle database

If you are connecting to an Oracle server to retrieve the data, use a
.vnudl file. If you are connecting to a SQL server to retrieve the data,
use a [.udl
file](Create%20a%20udl%20file%20to%20connect%20to%20a%20SQL%20database.md).

Val Nav uses a (Value Navigator Universal Data Link) file to connect to
the data vendor’s Oracle hub.



If the text file is not recognized as a .vnudl file, you may need to
change your Windows Explorer view to display file extensions.



To create a .vnudl file

1.  Use Notepad or something similar to create an empty text file and
    save it as *\.vnudl*. Save this file on a network in a
    place all users can access.

2.  Enter the following connection string into *\.vnudl*,
    replacing the Password,
    User ID and
    Data Source with values provided by
    the data vendor:

    Provider=Devart.Data.Oracle;Password=\;User ID=\;Data
    Source=\;Persist Security Info=True

3.  Click Save.
