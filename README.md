# Check-Point-Technical-Interview

In-Memory File System Simulator
This project implements a simple in-memory file system simulator in Python. It allows you to perform basic file system operations such as mkdir, cd, touch, and ls.

HOW TO RUN THE PROJECT

Copy the provided code into a Python file, Name it filesystem_interface.py.
Save the file.
Open powershell, terminal, or command prompt.
Navigate to the directory where you saved filesystem_interface.py using the cd command.
Run the program by typing python filesystem_interface.py and press Enter.


SAMPLE TEST
We start with an empty directory.
We create a directory named "documents" using the mkdir command.
We change into the "documents" directory using the cd command.
Inside the "documents" directory, we create two files named "file1.txt" and "file2.txt" using the touch command.
We list the contents of the current directory using the ls command, showing the two files we just created.
We move back to the parent directory using the cd command followed by "..".
We list the contents of the current directory again, showing the "documents" directory.
Finally, we exit the program using the exit command.
