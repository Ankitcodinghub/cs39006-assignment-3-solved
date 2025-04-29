# cs39006-assignment-3-solved
**TO GET THIS SOLUTION VISIT:** [CS39006 Assignment 3 Solved](https://www.ankitcodinghub.com/product/cs-39006-assignment-3-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113942&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS39006 Assignment 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
In this assignment, we will implement a simplified file transfer protocol. The actual working of ftp is more complex, this is a simplified version of it.

You will write two C files – the ftp server ftpS.c, and the ftp client ftpC.c. The ftp server will be a concurrent TCP server.

You will need to setup a few things first. In the directory from which you will run the server program, create a file called user.txt. Each line of the file contains a one word user login name and a one word password, separated by one or more spaces, in that order. There should be nothing else in the file. Create the file to contain 2 users, U1 and U2. Give arbitrary passwords.

Your ftpC.c should give a prompt “myFTP&gt;” and wait for user commands. The user will type the commands (shown below), and the commands below will be sent to the server (except for the command open to open a connection (for which no command is sent to the server as there is no connection opened before that), lcd and quit).

1. open IP_address port – This causes the client to open a TCP connection to the server with the designated IP address and port. This should be the first command entered on the client side (the client should check for it and not accept any other command before this). The IP address is to be given in dotted decimal form (like 10.15.60.3). Port should be any number between 20000 and 65535 for this assignment. The client prints a text message if the connection is opened successfully, else prints an error message.

2. user username – This must be the first command sent by the client to the server, the server should check for this. If any other command is sent as the first command, the server should send an error code of 600. If the username exists in the user.txt file of the server, a reply code of 200 is sent. If no such user exists, reply code of 500 is sent.

3. pass password – This must be the second command sent to the server. If any other command is sent as the second command, the server sends an error code 600. If the password matches the user’s password specified in the user.txt file, the server sends a reply code 200. If the password does not match, the server sends an error code 500.

The commands from 4 to 10 below should only be executed if the username and password have already matched. Both the client and the server should check that before executing any of these commands. If the username matches but the password does not, the user must enter both in that order again (not just the password).

4. cd dir_name – It changes the server side directory to dir_name. If the directory change is successful, the server sends a reply code 200; otherwise the server sends an error code 500.

5. lcd dir_name – It changes the local (client side) directory to dir_name. Nothing is sent to the server.

6. dir – It shows the contents of the current directory of the server. The client sends the command to the server and the server sends the directory content to the client. The server needs to send (and hence the client needs to print) only the names of the files and directories, no other information (such as file or directory, size etc.) need to be printed. The server should send the directory entries as null-terminated strings, with a final empty string (just a ‘’) to indicate the end of entries. If the directory is empty, only an empty string is to be sent.

7. get remote_file local_file – It gets the file named remote_file from the server and stores it under the name local_file on the client. File names can be just a file name, in which case it must exist on the current directory in the server. Or there can be an absolute path name to a file (ex. /usr/home/agupta/myfile.txt). The file name cannot be relative to the current directory or parent directory (i.e., cannot start with . or ..). If any file with the name local_file already exists in the client, it is overwritten. The client first checks if it can open the local file for writing. If not, a message is printed and no command is sent to the server. Otherwise, the command is sent. If the remote file does not exist in the server, it sends an error code 500 to the client, and transfers nothing. Otherwise the server first sends the code 200, followed by the contents of the file in the format specified later.

8. put local_file remote_file – It puts the file named local_file from the local directory of the client to the file remote_file in the server. The file names are similar to that in the get command. If any file with the name remote_file already exists in the server, it is overwritten. The client first checks if it can open the local file for reading. If not, a message is printed and no command is sent to the server. Otherwise, the command is sent. If the server is able to open the remote file, it sends a code 200. The client then transfers the file in the format specified later. If the server is unable to open the remote file for some reason, it sends the error code 500 and the client sends nothing.

10. mput file1, file2,… – same behavior as mget, just puts files from the client on to the current directory of the server. This command is to be executed by sending the put command multiple times with the proper arguments.

11. quit – closes the connection (if open) and exits.

The file transfer does not happen in one step when the file is arbitrarily long. The file is sent in binary mode as a sequence of bytes, block by block. Each block is prefixed with a header containing two fields, a character (‘L’ indicates it is the last block of the file, and a character ‘M” indicates it is not the last block of the file and more blocks will follow), and a 16-bit integer (short) indicating the length in bytes of the data sent in this block (not including the header bytes). So a file transfer is over after a block with ‘L’ in the character field is received. Note that this check is sufficient for detecting the end of the file, as TCP ensures that data bytes are received in order. Thus, the sender of the file will read the file block by block (with red call), prefix it with the header, and send it (with send call). Some points to remember:

• This being a TCP connection, there is no guarantee that the entire block will reach together to the other side, you should take care of that.

• The files can contain anything, do not assume txt files

The commands are to be sent exactly as shown as null-terminated strings from the client to the server, except for open (connection open, no command to send), lcd (local operation at client), quit (connection close only), and mget/mput (sends get and put commands).
