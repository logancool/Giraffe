# Giraffe




Giraffe

User Manual
K5



Written by: Alex Mair
With contributions from the rest of K5:
Logan Cool
Joey Eremondi
Joanne Traves
Ivan Vendrov




PREAMBLE
GIRAFFE is a learning tool designed to teach beginner programmers the basic
features of C or C++.

Please note that this is an early prototype version of GIRAFFE, and not all features of the C or C++ languages are supported; indeed, the programs you will write for GIRAFFE are not yet valid C or C++ programs and will not compile in a standards-compliant compiler.
INSTALLATION
JAVA PREREQUISITES
Please ensure that you have the latest Java Runtime Environment. Visit:

http://www.java.com/en/download/index.jsp

There you will be able to verify if you have Java installed. If you do not, you
must install it before you can use GIRAFFE.
GIRAFFE PREREQUISITES
Once Java is installed, simply place the giraffe_prototype.jar file where-ever
you like. Some recommended locations depending on your platform:

WINDOWS
	C:\Program Files\
	
OS X
	/Applications/
	
GNU/LINUX
	/usr/local/bin		if you have administrative privileges


USING GIRAFFE

To open GIRAFFE, navigate to where you placed giraffe_prototype.jar and double-click on it. Alternatively, if you prefer using a command line, you can start GIRAFFE using:

java -jar <folder>/giraffe_prototype.jar

where <folder> is the name of the folder that you placed giraffe_prototype.jar.
HELLO, WORLD
Let us showcase GIRAFFE's features with an example. Open up the text editor of your choice and enter in the following C++ code:

int main()
{
    cout << "hello, world\n";
}

	Note for more experienced C++ users: you might note the lack of three things:
#include <iostream>
Either using namespace std; or std::cout instead of cout
endl instead of \n

Note for all users: Please ensure that your text editor is using spaces instead of tabs for indentation.

	These are limitations of GIRAFFE that will be removed in a future release.

Save this file to your hard disc, then open the file using GIRAFFE. You will notice that GIRAFFE is displaying the contents of the file you saved. Awesome!

Notice that the four play controls are dark, like so:



This is because we have yet to tell GIRAFFE that we wish to compile our source
file and prepare the animations for it. To do so, simply press the button labelled Compile, near the top-left of the GIRAFFE window. GIRAFFE should then happily compile your program.

Note: If GIRAFFE fails to compile your source file, double-check that your source file is free of typos, does not have #include or tabs.

Notice now that the four play controls have lit up, like so:



Go ahead and press the Play button:



Wait, did nothing happen? The play controls only darkened! Well, something did happen, it's just that the source file we gave GIRAFFE is very simple and doesn't show off GIRAFFE's features very well. Do notice however that the text was displayed in the lower-left corner, like so:



That's pretty cool, but not nearly cool enough. Let's move on to another, more interesting example

Note: Output is done after the Compile step, not necessarily after Play. This is a limitation of GIRAFFE; we aim to fix this in a future release.
BABY STEPS...
Open up a new text file, and put the following C++ code in it:

int main()
{
	int a=42;
	int b;
	int c=100;
	a=c+c;
	b=a+c;
}

But wait, there's no cout! There’s no worry however, as GIRAFFE will still display the contents of the variables anyway - in fact, that's the major feature of GIRAFFE and one that we (the developers) hope that you will come to love.

Open the file in GIRAFFE and press Compile. Instead of pressing Play, this time, try pressing the button next to it:


This is the Step Forward button; it will advance the animations by one step. One step is a piece of code. Some examples include: declaring a variable, assigning a value to a variable, evaluating a single expression, and so on.

Note: We tried to make the buttons look like music player buttons so they can be recognisable. Hopefully you've caught on to our clever ploy!
	
A small box should slowly appear in the left side of the GIRAFFE window, with a small label: a. Hey, this is the first line of code in our program, and the name of the variable GIRAFFE encountered!

Press the Step Forward button again. The value 42 should appear in the box beside a. You can probably guess what happens when you click the Step Forward button again; it allows you to step through your code at your own pace.

If you get tired of clicking the Step Forward button, you can instead click on the Play button and GIRAFFE will automatically step forward for you.
ONE MORE ADVANCED EXAMPLE
Here's one final source example, to detail you with the full set of C or C++ language features that GIRAFFE supports:

int add_seven(int n)
{
    int result;
    result=n+7;
    return result;
}

int fact(int n)
{
    if (n==0)
        return 1;
    else
        return n*fact(n-1);
}

int main()
{
    cout << "Starting calculations...\n";
    int start_results[4];
    
    for (int i=0;i<4;i++) {
        start_results[i]=add_seven(i);
    }
    
    if (start_results[2]<10) {
        cout << "Yes!\n";
    }
    
    int five_factorial=fact(5);
    cout << five_factorial << "\n";
}

This example is long enough to show off GIRAFFE’s Pause and Stop functionality, detailed in these buttons, respectively:

		
If you press the Pause button whilst GIRAFFE is playing animations, it will stop automatically playing further animations until you press Play again. Stop resets the animations to the beginning.

Note: There is currently a bug involved with variables in function calls as GIRAFFE has no concept of scope... yet. We hope to fix this soon!

APPENDIX
LIST OF FEATURES THAT GIRAFFE CURRENTLY SUPPORTS
Variable declaration (including inline declaration) and assignment
if-, for-, and while-statements.
int and float literals
String literals (not C++ string objects)
Functions
Arrays
Boolean operations
Integer and floating point arithmetic (including comparison)
Integer postincrement (that is, i++)
	
PLAY CONTROLS IMAGE CREDIT
The images GIRAFFE uses for its Play controls are part of the Oxygen icon theme and are licensed under CC BY-SA 3.0. Their website is:

http://www.oxygen-icons.org/

You can view information regarding the CC BY-SA 3.0 license here:

http://creativecommons.org/licenses/by-sa/3.0/

