# AIM (Actor Interaction Metric) Tool

**Description**: 
The AIM (Actor Interaction Metric) tool is a command line tool for measuring and classifying inter-actor dependencies in textual GRL goal models. 
It accepts as input: (1) a textual GRL specification file (.turn as extension), and (2) the initial satisfaction interval ranges ([-100, 100], [0, 100] or user defined intervals), and computes the global AIM of each GRL actor of the model (see Part A in the SampleOutput.txt), the impact and the classification of each dependency (see Part B in the SampleOutput.txt), and the most beneficial/harmful dependency if any (see Part C in the SampleOutput.txt).

The AIM tool is tested using java version "1.8.0_221"

**How to run the tool in Windows:**

c:\> java -jar AIMTool.jar filename.turn option

option = 0 for user defined intervals (the user will be prompted to enter interval lower and upper bounds for each GRL intentional element leaf element)

option = 1 for [-100, 100] satisfaction intervals

option = 2 for [0, 100] satisfaction intervals

**Example**: c:\> java -jar AIMTool.jar alumni.turn 0

For a sample output of the execution of AIM tool using user defined intervals, on the "TURN Models/alumni.turn" example, please refer to SampleOutput.txt
