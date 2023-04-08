## Overview

This part will go over how to use the debugger in PyCharm IDE. Debugging allows the user to be able to go through their code step by step. This allows users to understand how their code may work. The built-in debugger in PyCharm can also be used for fixing and catching errors. We will go step by step and help you debug your first code. There is some code to help you get started debugging.

``` py
def romannumeral(positive_int):
    roman = {1000: 'M', 500: 'D', 100: 'C', 50: "L", 10: "X", 5: "V", 1: "I"}
    roman_num = ''

    while positive_int >= 0:
        for key in roman:
            if positive_int == 0:
                return roman_num
            elif positive_int == key - 1:
                roman_num = roman_num + roman[1] + roman[key]
                positive_int -= key - 1
            elif positive_int - key >= 0:
                positive_int = positive_int - key
                roman_num = roman_num + roman[key]
                break



def main():
    print(romannumeral(39))


if __name__ == "__main__":
    main()
```

## Initiate Debug

To start debug process you have to setup the debugger first by placing a breakpoint.

1. Click in between the line numbers and the code divider.
![Breakpoint](/images/debug-photo/Breakpoint.png)

2. Click the debug icon located in the top right corner.
![Debug Icon](/images/debug-photo/debugIcon.png)Once you go through the steps you should have a debug console open in the bottom half of the screen. Now you can start to debug!

## Interacting With Debugger

Once the debug console opens up you will be able to start to debug your code. There will be different tasks you can perform with the debug console.

1. Click the step into icon which is the downward-facing arrow pointing to a line.
![Step Into Icon](/images/debug-photo/stepInto.png)
This allows you to go line by line in your debug console.

2. Click on the step into my code icon beside the step into icon.
![Step Into My Code Icon](/images/debug-photo/stepIntoMyCode.png)
The difference between step 1 and step 2 is that step 2 only steps into your code and not any library classes.

3. Click on the step over icon on the left side of the step into icon.
![Step Over](/images/debug-photo/stepOver.png)
Step over is used if you do not want to run the current line so you step over this line to the next.

4. Click the step out button in the debug console.
![Step Out](/images/debug-photo/stepOut.png)
You will step out of the current method to the caller function.

5. Click on the red stop button located on the left side of the debug console.
![Stop](/images/debug-photo/stop.png)
The stop button stops the execution and returns an error.
!!! info
        Alternatively, you can click on the stop icon located in the top right corner near the debug icon.

6. Repeat step 2 in Initiate Debug and repeat step 1 Interacting With Debugger till the debugger closes.
Once the debugging session ends the debugging will close and take you to the console. In the console the program will execute and display the finial information at the end.
!!! success
    Once the debug process has complete the code will execute in the console.

## Conclusion

Congratulations 🎉, now you should be able to go through and debug your code and understand what different debug icons do.!

Lessons learned:

- [x] How to initiate debug.
- [x] How to interact with the debugger.

You can now move on to the next step by clicking on the 'Next' button below me. :partying_face:
