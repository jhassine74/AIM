# AIM (Actor Interaction Metric)
**Description**: AIM (Actor Interaction Metric) Tool for measuring and classifying inter-actor dependencies in textual GRL goal models.

The AIM tool is a command line tool. It accepts as input: (1) a textual GRL specification file (.turn as extension), and (2) the initial satisfaction interval ranges (default [-100, 100], or [0, 100] or user defined intervals), and computes the global AIM of each GRL actor of the model (see Part A in the SampleOutput.txt), the impact and the classification of each dependency (see Part B in the SampleOutput.txt), and the most beneficial/harmful dependency if any (see Part C in the SampleOutput.txt).

The AIM tool is tested using java version "1.8.0_221"

How to run the tool:

c:\> java -jar AIMTool.jar filename.turn option

option = 1 for default intervals, i.e., [-100, 100]

option = 2 for [0, 100] intervals

option = 0 for user defined intervals (the user will be prompted to enter interval lower and upper bounds for each GRL intentional element leaf element)

For a sample execution of the tool using user defined intervals, on the "TURN Models/alumni.turn" example, please refer to SampleOutput.txt
