# AIM
AIM Tool for measuring and classifying inter-actor dependencies in textual GRL goal models.

The AIM tool is tested using java version "1.8.0_221"

How to run the tool:

c:\> java -jar AIMTool.jar filename.turn option

option = 1 for default intervals, i.e., [-100, 100]

option = 2 for [0, 100] intervals

option = 0 for user defined intervals (the user will be prompted to enter interval lower and upper bounds for each GRL intentional element leaf element)

For a sample execution of the tool using the alumni.turn case study, please refer to SampleOutput.txt
