---
layout: post
title: "Thoughts about javac usage with package"
date: 2014-10-19 01:36:57 -0400
comments: true
categories: Java
---
I was long confused about the usage of javac and java with package. When I took java course in NYU, I encountered one homework problem about this knowledge. So I tried to learn from Google and stackoverflow, and finally, I figured it out.
<!--more-->
Say we have some java class files with package ```A.B.C``` and are located in ```~/Users/USER_NAME/documents/src/main/java/A/B/C``` folder. We can compile them with ```javac``` command 
```
javac ~/Users/USER_NAME/documents/src/main/java/A/B/C/*.java
``` 
if we are in the root or other directory. Then we can run these files with ```java``` command 
```
java -cp ~/Users/USER_NAME/documents/src/main/java A.B.C.YOUR_JAVA_CLASS
```

If we are in some specific directory like ```documents```, it’s simpler.
```
javac src/main/java/A/B/C/*.java
java -cp ./src/main/java A.B.C.YOUR_JAVA_CLASS
```

The reason for this is that we have to specifc the file location in ```java``` command with ```-cp PATH PACKAGE```