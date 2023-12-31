#### 1.Share an example of using the command with no arguments.
  - command `cd` with no arguments.

![Image](451696610583_.pic.jpg)

  The working directory is /home. This will change the current directory to the user's home directory. It's not an error. 

  - command `ls` with no arguments.

![Image](461696610599_.pic.jpg)

  The working directory is /home. This will list the contents of the current directory. It's not an error. 

  - command `cat` with no arguments.

![Image](471696610651_.pic.jpg)
![Image](481696610660_.pic.jpg)

  The working directory is /home. It waits for input from standard input. It is an error because using command `cat` with no arguments will crash the terminal as shown in the picture.

#### 2.Share an exmaple of using the command with a path to a directory as an argument.
  - command `cd` with a path to a directory as an argument.

![Image](491696610966_.pic.jpg)
  The working directory is /home/lecture1. command `cd` is used to change the currect dicrectory to the specified directory-lecture1. It's not an error.
  
  - command `ls` with a path to a directory as an argument.

![Image](501696611053_.pic.jpg)

  The working directory is /home/lecture1. command `ls` is used to list the folders and files in the given path-lecture1. It's not an error.
  
  - command `cat` with a path to a directory as an argument.

![Image](511696611296_.pic.jpg)

  The working directory is /home/lecture1. command `cat`is used to give the path of the file and print the content of it. It is an error because commnad `cat` can't be applied to directory, and lecture1 is a directory. 

#### 3.Share an example of using the command with a path to a file as an argument.
  - command `cd` with a path to a file as an argument.

![Image](521696611444_.pic.jpg)
  The working directory is /home/lecture1/messages. command `cd` is used to change the currect dicrectory to given path, and here we try to access to the file-en-us.txt, which does not work. Therefore, it is an error.
  
  - command `ls` with a path to a file as an argument.

![Image](531696611503_.pic.jpg)

  The working directory is /home/lecture1/messages. command `ls` is used to list the folders and files in the given path, and here we try to list the content in the file:en-us.txt. It's not an error.
  
  - command `cat` with a path to a file as an argument.

![Image](541696611581_.pic.jpg)

  The working directory is /home/lecture1/messages. command `cat` is used to print the content in the given path, trying to print the content in the file-en-us.txt. Inside en-us.txt, we have content "Hello World!". It's not an error.


