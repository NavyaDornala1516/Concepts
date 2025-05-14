## File Permissions in Linux

Linux uses Permissions to control who can read, change, or run a file or folder.

Every file or folder has 3 types of users:

    User Type	Who they are

    User   (u)	The owner of the file
    Group  (g)	Other users in the file's group
    Others (o)	Everyone else on the system

And 3 types of actions (called permissions):

    Permission	Symbol	What it allows

    Read	      r  	View the file or list folder contents
    Write	      w 	Modify or delete the file/folder
    Execute	      x    	Run the file (if it’s a program/script) or access folder


"ls -l" with this command we can view file and dirctories in long format and gives detailed information.

**Example**: -rw-r--r-- 1 navya navya  1234 May 14 12:00 harry.txt


    - means it’s a file (if it were a folder, we will see d)
    rwx → user has read, write, and execute permissions
    r-x → group can read and execute
    r-- → others can only read

## chmod(Change Mode)

It changes the permissions of file or directories.

    chmod u+x file.txt   # Add execute for user
    chmod g-w file.txt   # Remove write for group
    chmod o=r file.txt   # Others can only read

    rwx     binary  Decimal

    ---     000	    0
    --x 	001	    1
    -w-     010	    2
    -wx 	011	    3
    r-- 	100	    4
    r-x 	101	    5
    rw- 	110	    6
    rwx 	111     7        

**Example**:   chmod 754 file.txt
                  
            This gives:

                u  : 7 = rwx
                g  : 5 = r-x
                o  : 4 = r--

            So permission looks like:   -rwxr-xr--

We can also change the file permission recursively.

**Example**:  chmod -R [permissions] [directory_name]


## chown(Change Owner)

It changes the owner of the file and which group it belongs to.

**Example**  

            chown navya file.txt( for file )

            chown sony:navi file.txt(for file and group)                

for changing the ownership recursively for dirctories.

**Example**:  chown -R sony:navi dir/path

