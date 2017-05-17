# PythonOnXcode
Example Project that set up for python Programming
Using Xcode to execute python’s code.

Currently I’m working with a project that involve with Python Programming. So I need to start up to learn about python programming. However, I don’t like to use with Python REPL. And for now i decided to use Xcode instead then i’m trying to find the best solution for make my work easy more and more. More detail here: https://medium.com/@sourleangchhean/using-xcode-to-execute-pythons-code-98be65c1ea8a
Ok, These is some step i need to set up my project. 
## Step 1: Install Python 3.6
You can download and install with this url: https://www.python.org/downloads/sdfsdf
or install with Homebrew: or Python 3:

$ brew install python3

This will take a minute or two.
## Step 2: Locate python3
for me i use tcsh, so where python3 reports /usr/local/bin/python3. The location is surely the same for you, but I don’t know what the equivalent for where is in bash.
## Step 3: Create an Xcode project
File > New > Project > Cross-platform > External Build System > Next.

Enter a name (e.g. PythonOnXcode), and enter the path from Step 2 into the “Build Tool” line. Click Next.

Navigate to whatever location you like, and click Create.
## Step 4. Create a Python file
Choose File > New, select macOS > Other > Empty. Click Next.

You should already be in your project’s top level folder. If not, go there. Name your file Whatever.py, choosing whatever name you like. I went with Work.py. Make sure the “add to target Python” box is checked. Click Create.

## Step 5. Edit your Run Scheme
Click and hold on the PythonOnXcode target in the jump bar. Select Edit Scheme…
The Run scheme displays, with the Info tab selected.

## Step 6. Choose the Executable
I warn you now that this step is going to be delicate, fragile, and stupid. That’s because Xcode, for whatever reason, will not let you use the symbolic link at /usr/local/bin/python3. I don’t know why.
In the Info tab. Select “Other” from the Executable pop-up list. A file selection dialog appears.

When dialog pop, Go to Terminal then Type: cd /usr/local/bin

Type open /usr/local/bin

Right Click on Python3.6 then select Show Original

Get in to that location in terminal and Type ln python3.6 python36

Type open .

Drag python36 to Choose an executable to launch dialog box.

Select python36 then click choose button.

## Step 7. Add Launch Arguments
Now, click the Arguments tab. Click + under “Arguments Passed On Launch” and type $(SRCROOT)/ followed by the name of the Python file you created in Step 4.

## Step 8. Testing with python code

Finished

Thanks and i hope it can help you to getting start python with xcode. If you have any question, Feel free to ask and I will answer as can as possible. If you like it. please share it around. Happy Coding …… :)
## About Me
Medium: Sour LeangChhean
Github: https://github.com/sourleangchhean168
StackOverFlow: http://stackoverflow.com/users/4935811/sour-leangchhean
Facebook: https://www.facebook.com/sourleangchhean168
Twitter: https://twitter.com/leangchhean
