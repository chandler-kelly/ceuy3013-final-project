# ceuy3013-final-project
Chandler Kelly
12/13/2020

*  Please take a look at the readme file and make sure you have necessary imports.
*  Code written with Google Colab, link provided in source.py for ease of use
*  When using the program, please use only real, positive numbers for inputs. Numbers with decimals are okay. There are recommended values for user most user inputs. Extremely large values may cause model to fail. Only use 0 as an input when stated it is okay to do so, 0's for most variables will cause divide by zero error.

# User Input
This tool models the fate and transport of a contaminant in a river system.
*  The user must first chose the *contamination type*.
*  The tool can model pollution a one-time *spill* or a constant *continuous source*
*  The user then chooses the *contaminant*.
*  The tool has presets for *lead*, *nutrients*, and *PCBs*, as well as the option to use a generic contaminant.
*  The user must then imput the *river properties*.
*  The user selects the *size*, *flow speed*, and *mixing* of the river.
*  Depending on the *contamination type*, different river properties are required.
*  The user will be given typical or suggest values for river properties if actual properties are not known.
*  Depending on the *contaminant*, the user will be suggested or given a first-order decay constant and EPA drinking water standard.

# Output - Spill
*  For the *Spill*, the tool will show a plot of the concentration as a function of time as well as the horizontal limit line.
*  The tool will tell the user whether operations will have to stop, based on whether or not the maximum concentration is exceeded.
*  If the limit is *not exceeded*, the tool will tell the user that the maximum concentration at the site did not violate the limit.
*  If the limit *is exceeded*, the tool will tell the user that operations will have to stop. The tool will tell the user the time operations must stop, the time operations can resume, and the total time the operation will be down. The tool will mark the curve at the time operations must stop and at the time operations can resume.
*  Here is an example of a PCB spill that violates the limit:
![PCB Spill](https://github.com/chandler-kelly/ceuy3013-final-project/blob/main/PCB%20Spill%20Output.PNG)

# Output - Continuous Source
*  For the *Continuous Source*, the tool will show a plot of the concentration as a function of distance, due to the steady state nature of continuous sources, time has no bearing on concentration. The horizontal limit line will also be plotted.
*  The tool will tell the user whether they can operate or not.
*  If the limit is *not exceeded*, the tool will tell the user that the concentration at the site does not violate the limit. The tool will plot a green dot on the curve at the site location.
*  Here is an example of a Nitrate (Nutrient) Continuous Source that does not violate the limit:
![Nutrient Cont Source](https://github.com/chandler-kelly/ceuy3013-final-project/blob/main/Nutrient%20Cont%20Source%20Output.PNG)
*  If the limit *is exceeded*, the tool will tell the user that operations will have to stop. The tool will tell the user that operations must stop, and the value of mass loading must be reduced to so that operations can occur. The tool will plot a red dot on the curve at the site location.
*  Here is an example of a Lead Continuous Source that violates the limit:
![Lead Cont Source](https://github.com/chandler-kelly/ceuy3013-final-project/blob/main/Lead%20Cont%20Source%20Output.PNG)

