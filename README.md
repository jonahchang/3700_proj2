My code used argparse and socket for network communication and URL parsing. I
started off by making an argparse function in order to take in the command line
arguments. Initially, I tried to pass in around 5 different arguments (operation,
username, password, param1, and param2). Then I modeled my code around this in
order to parse the arguments and then call the respective functions. After setting up
the socket, I made functions to set up the transfer settings and connect and login to
the server. I used a if-elif
statement to decide the operation that was being called, and then called the respective
function that would send the command to the FTP server. I implemented the list function
by setting up a data socket in order to receive the information to be printed, and then
iterated through the files in chunks and then printed the files so that I wouldn't be
trying to print too much information at once and slow down the program. I then implemented
the easiest functions (remove file, remove directory, and make directory) by just sending
the command to the server and then receiving and printing the response from the server.
Afterwards, I implemented the copy function by first detecting if it was an upload or a
download by checking if the first parameter started with a "ftp" or not. If it started
with "ftp", then I would upload from the source path to the server path, otherwise I would
download a file from the server path to the destination/local machine path.


After implementing all the functions required, I tested them on the command line, and
this is where I ran into all my problems. I had implemented and error tested properly
for all my functions, but I couldn't figure out why the hostname, username, and password
weren't being parsed correctly. For this problem, I went to TA office hours and puzzled
over it for a while, with the TA telling me that I just needed to hard code in the username
and password because I would be the only one using this code. That turned out to be the
opposite of what I needed to do, and I didn't manage to turn in the project on time. Stumped,
I asked a friend what was wrong, and they said that when they had login issues, they made
sure that there were default values for the username and password so that the code could 
login accordingly. After implementing this fix, my code passed with flying colors, and I
was able to get 100%.

All my testing was done by sending commands to the FTP server through the command line
on my machine, and for each method, I tested adding and removing for everything.