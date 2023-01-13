# Lab Report Week 1

Hello, future me or incoming 15L students, this lab report will illustrate the steps for logging into the course-specific account on *ibeng6*.

## Step 1: installing VScode. 
Since the computer in the lab has already installed with VScode, I just opened it from the PC directly, which showed the following interface. 

<img width="845" alt="Screen Shot 2023-01-12 at 10 28 59 PM" src="https://user-images.githubusercontent.com/101618208/212252576-6418d005-101e-4ce7-b94f-c76e37c7bcc2.png">

## Step 2: Remotely Connecting
This step makes sure that we are connected to the SSH remote server. We will start with looking for your [CSE15L account](https://sdacs.ucsd.edu/~icc/index.php). Please follow the tutorial on [how to reset the password](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit). You will need the password later to connect to the remote server.

After that, open the VScode's Terminal by either clicking it from the tool bar or use the short cut *Ctrl or Command +*. I am using the lab room's PC that has the *git* for windows already installed. Then, follow the step on [how to use Bash on Windows in VScode](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994). 
Next, I entered `$ ssh cs15lwi23zz@ieng6.ucsd.edu` (replace the 'zz' by the letters in your course-specific account). Following that, enter *yeYs*. Then enter your password that just created. (Your password will not be shown on the command line).

Upon success, your screen will be shown with this.

<img width="590" alt="Screen Shot 2023-01-12 at 10 47 46 PM" src="https://user-images.githubusercontent.com/101618208/212255402-a88ac753-d87a-4688-aae4-988c32ee701d.png">

## Step 3: Trying some commands
Now it's time to try out the commands just learned from the lecture. 

For example:
* cd ~ (change directory of sth)
* cd (change directory)
* ls -lat (list the content of)
* ls -a (list the content of)
ls <directory> (list the content under the specified directory)
  
These are pretty useful for you to navigate through and make changes to your file.
  
Here are what I tried:

<img width="722" alt="Screen Shot 2023-01-12 at 10 52 41 PM" src="https://user-images.githubusercontent.com/101618208/212256132-b538e4b4-2998-4b4d-b214-c36c9ced5707.png">
<img width="718" alt="Screen Shot 2023-01-12 at 10 52 53 PM" src="https://user-images.githubusercontent.com/101618208/212256160-4bbdc8fb-73c4-4b98-b9da-e99134a86a71.png">
