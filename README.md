# AIM
AIM Tool for measuring and classifying inter-actor dependencies in textual GRL goal models.
===========================
Java version: 
==============================
Tested using java version "1.8.0_221"
=========================================
How to run the tool
=========================================
c:\> java -jar AIMTool.jar filename.turn option
option = 1 for default intervals, i.e., [-100, 100]
option = 2 for [0, 100] intervals
option = 0 for user defined intervals (the user will be prompted to enter interval lower and upper bounds for each GRL intentional element leaf element)
=================================================
Sample execution of the tool using the alumni.turn case study
==================================================
c:\>java -jar AIMTool.jar alumni.turn 0
Please enter the interval lower bound for:organizenetworkingevents:
10
Please enter the interval upper bound for:organizenetworkingevents:
50
Please enter the interval lower bound for:usesocialmedia:
10
Please enter the interval upper bound for:usesocialmedia:
50
Please enter the interval lower bound for:supportindustryprojects:
20
Please enter the interval upper bound for:supportindustryprojects:
60
Please enter the interval lower bound for:provideaccessfacilities:
30
Please enter the interval upper bound for:provideaccessfacilities:
70
Please enter the interval lower bound for:donatetouniverity:
10
Please enter the interval upper bound for:donatetouniverity:
100
Please enter the interval lower bound for:identifycollaborationareas:
30
Please enter the interval upper bound for:identifycollaborationareas:
50
Please enter the interval lower bound for:advertisejobopenings:
10
Please enter the interval upper bound for:advertisejobopenings:
100
Please enter the interval lower bound for:shareexpwithstudents:
10
Please enter the interval upper bound for:shareexpwithstudents:
100
Please enter the interval lower bound for:mentorcurrentstudents:
10
Please enter the interval upper bound for:mentorcurrentstudents:
100
==================================================
===== PART A:(All Dependencies vs Isolation) =====
==================================================

===============Leaf Element(s)' Satisfaction Values intervals:=================
organizenetworkingevents Intervals:
All Dependencies:       [10, 50]
Isolation:              [10, 50]

usesocialmedia Intervals:
All Dependencies:       [10, 50]
Isolation:              [10, 50]

supportindustryprojects Intervals:
All Dependencies:       [20, 60]
Isolation:              [20, 60]

provideaccessfacilities Intervals:
All Dependencies:       [30, 70]
Isolation:              [30, 70]

donatetouniverity Intervals:
All Dependencies:       [10, 100]
Isolation:              [10, 100]

identifycollaborationareas Intervals:
All Dependencies:       [30, 50]
Isolation:              [30, 50]

advertisejobopenings Intervals:
All Dependencies:       [10, 100]
Isolation:              [10, 100]

shareexpwithstudents Intervals:
All Dependencies:       [10, 100]
Isolation:              [10, 100]

mentorcurrentstudents Intervals:
All Dependencies:       [10, 100]
Isolation:              [10, 100]

Important Elements satisfaction intervals:
fosteringunivalumnirel Intervals:
All Dependencies:       [7, 12]
Isolation:              [10, 50]

givebackuniversity Intervals:
All Dependencies:       [15, 100]
Isolation:              [15, 100]

Actors' satisfaction intervals:
Actor alumnirelations Intervals:
All Dependencies:       [7.0, 12.0]
Isolation:      [10.0, 50.0]
AIM (AIM(A) = Mp(A_AllDeps) - Mp(A_isol)): -20.5
Interaction Type: Negative

Actor alumnus Intervals:
All Dependencies:       [15.0, 100.0]
Isolation:      [15.0, 100.0]
AIM (AIM(A) = Mp(A_AllDeps) - Mp(A_isol)): 0.0
Interaction Type: Neutral/No External Interaction

======================================================
PART B:(All Dependencies Except D vs All Dependencies)
======================================================
1) Remove dependency link between enhancedcollindustry--->establishresearchcollaboration(D1)


Important Elements satisfaction intervals
fosteringunivalumnirel intervals:
All Dependencies:       [10, 50]
Isolation:              [10, 50]

givebackuniversity intervals:
All Dependencies:       [15, 100]
Isolation:              [15, 100]

Actors' satisfaction intervals:
Actor alumnirelations Intervals:
All Dependencies Except D1:     [10.0, 50.0]
All Dependencies:               [7.0, 12.0]
AIM (AIM(A,D) = Mp(A_AllDepsExceptD) - Mp(A_AllDeps)) : 20.5
Dependency Impact: Harmful

Actor alumnus Intervals:
All Dependencies Except D1:     [15.0, 100.0]
All Dependencies:               [15.0, 100.0]
AIM (AIM(A,D) = Mp(A_AllDepsExceptD) - Mp(A_AllDeps)) : 0.0
Dependency Impact: Neutral

2) Remove dependency link between helpingcurrentstudents--->provideaccessfacilities(D2)

Important Elements satisfaction intervals
fosteringunivalumnirel intervals:
All Dependencies:       [7, 12]
Isolation:              [10, 50]

givebackuniversity intervals:
All Dependencies:       [15, 100]
Isolation:              [15, 100]

Actors' satisfaction intervals:
Actor alumnirelations Intervals:
All Dependencies Except D2:     [7.0, 12.0]
All Dependencies:               [7.0, 12.0]
AIM (AIM(A,D) = Mp(A_AllDepsExceptD) - Mp(A_AllDeps)) : 0.0
Dependency Impact: Neutral

Actor alumnus Intervals:
All Dependencies Except D2:     [15.0, 100.0]
All Dependencies:               [15.0, 100.0]
AIM (AIM(A,D) = Mp(A_AllDepsExceptD) - Mp(A_AllDeps)) : 0.0
Dependency Impact: Neutral

======================================================
PART C: I- Most harmful dependency for each actor(if any)
======================================================
The most harmful interaction for actor 'alumnirelations' is D1 which is between: enhancedcollindustry--->establishresearchcollaboration

The actor 'alumnus' has no harmful/external dependency(ies)

=============================================================
PART C: II- Most beneficial dependency for each actor(if any)
=============================================================
The actor 'alumnirelations' has no beneficial/external dependency(ies)

The actor 'alumnus' has no beneficial/external dependency(ies)

*****************************************End*****************************************
 
