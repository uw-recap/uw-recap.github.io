---
layout: post
title:  "Code Reorganization"
date:   2019-03-05 12:00:00 -0500
tags: RECAP code organization refactoring
---
After our first session of in-car testing our main Arduino sketch file had grown to almost 700 lines of code. Up to this point, no consideration had been given to the organization of code and files had been kept small, but after integrating code for all of the major subsystems into one file it was becoming harder to manage. Furthermore, the monolithic file structure made it difficult for multiple developers to work in parallel to address problems in different subsystems without creating merge conflicts.

We decided that refactoring the code would help keep things organized and make it easier to branch and merge code. Common macros, constants and type declarations were pulled into a common header file. For each subsystem a header file was created to declare the publically accessible functions that could be used in the main sketch. Each subsystem also has a source file that defines all of these public functions and any additional private functions used locally within that file.

```
.
├── main.ino
├── recap_common.cpp
├── recap_common.h
├── recap_DataProc.cpp
├── recap_DataProc.h
├── recap_GPS.cpp
├── recap_GPS.h
├── recap.h
├── recap_LCD.cpp
├── recap_LCD.h
├── recap_LoRa.cpp
├── recap_LoRa.h
├── recap_OBD.cpp
└── recap_OBD.h
```

This new paradigm makes it easier to find and fix issues with the code and will save us time while conducting further testing.
