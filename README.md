# Ontoseer
This document provides documentation for the first version of OntoSeer.OntoSeer is a tool that monitors the ontology development process andprovides suggestions in real time to improve the quality of the ontology under development.


# Table of Contents
1. [ Introduction. ](#intro)

2. [ Pre-Requisites. ](#prerequisites)

3. [ Installation Guide. ](#InstallationGuide)

	3.1 [Using Source Code](#code)
	
	3.2 [Downloading .jar files](#exe)

4. [ User Manual. ](#UserManual)

   4.1 [ ODP Recommendation ](#ODP)
   
   4.2 [ Vocab and Alternate Name Recommendation ](#Vocab)
   
   4.3 [ Naming Convention Recommendation ](#Naming)
   
   4.4 [ Axiom Recommendation ](#Axiom)
   
   4.5 [Class Hierarchy Validation](#class)
   
5. [ Future Work. ](#future)
6. [Sustainibility](#sustain)
7. [Brief Demo ](#Demo)
8. [Google Form for User Study ](#google)
9. [Index Creation](#index)

<a name="intro"></a>

## 1. Introduction

While building an ontology, there are several things to consider such as reusing concepts/properties from the existing ontologies, using ontology design patterns (ODPs), following the naming conventions for concepts/properties and designing a good class hierarchy. These are issues that beginner ontology engineers find hard and can be tricky for experienced ones as well. OntoSeer (https://github.com/kracr/ontoseer) is a Protege plugin that overlooks the ontology that is being built in Protege and offers different types of recommendations.
                            
<a name="prerequisites"></a>

## 2.Prerequisites

1. User should have Protege installed in the machine. Version should be >5.0.0.

 	If one is not having protege or protege5.0.0 or higher installed they can download latest version of protege from https://protege.stanford.edu/products.php based on machine’s operating system:
	

2. JRE should be installed in user machine and version should be  >1.8.
   To check for java version one can type java -version in terminal.The following will be the output. 
   
   ![java-versioncheck](https://github.com/kracr/ontoseer/blob/master/Images/Onto1.png)

<a name="InstallationGuide"></a>

## 3.Installation Guide

In this section we will discuss how one can download OntoSeer.

<a name="code"></a>

## 3.1 Using Source Code

This repository contains  code for OntoSeer (*versions 5.0.0 and higher*).  The Maven POM file in the top-level directory demonstrates all the dependencies to run the tool

#### Prerequisites

To build and run Ontoseer through code compilation , one must have the following items installed:

+ Apache's [Maven](http://maven.apache.org/index.html).
+ A tool for checking out a [Git](http://git-scm.com/) repository.
+ A Protege distribution (5.0.0 or higher).  The Protege 5.2.0 release is [available](http://protege.stanford.edu/products.php#desktop-protege) from the main Protege website. 

#### Installation Steps:

1. Get a copy of the example code:

     git clone https://github.com/kracr/ontoseer
    
2. Change into the OntoSeer directory.

3. Type mvn clean package.  On build completion, the "target" directory will contain a OntoSeer-${version}.jar file.

4. Copy the JAR file from the target directory to the "plugins" subdirectory of your Protege distribution.
 
 a. Click on the plugins folder.

![OntoSeer_jar_plugin](https://github.com/kracr/ontoseer/blob/master/Images/Onto4.png)	

b.Copy OntoSeer.jar in the plugin folder.

![OntoSeer_jar_plugin_folder](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/OntoSeer_plugin.png)

5. Restart Protege.

6. Go to about Section of Protege and check whether the plugin has been correctly installed or not .It will be shown in the window.

![OntoSeer_jar_plugin_About](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/OntoSeer2.png)

7. Click on Windows. Click on Tabs .Click on OntoSeer Tab.This window will appear.

![OntoSeer_jar_plugin_Actual_Tab](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Opening%20shot.png)

<a name="exe"></a>

## 3.2 Downloading .jar files

1.One can download Ontoseer.jar file from the  following link:
	
	https://github.com/kracr/ontoseer/releases
	
![OntoSeer jar](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/OntoSEER67.png)	

The link to download the code repository and instruction manual is :

	https://github.com/kracr/ontoseer

2. Click on Assets->Ontoseer.jar

![OntoSeer jar](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Assets.png)	

The jar file will get downloaded.

3. Copy the jar file to the plugins folder of Protege.

a. Click on the plugins folder.

![OntoSeer_jar_plugin](https://github.com/kracr/ontoseer/blob/master/Images/Onto4.png)	

b.Copy OntoSeer.jar in the plugin folder.

![OntoSeer_jar_plugin_folder](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/OntoSeer_plugin.png)





4. Restart Protege.

5. Go to about Section of Protege and check whether the plugin has been correctly installed or not .It will be shown in the window.

![OntoSeer_jar_plugin_About](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/OntoSeer2.png)

6. Click on Windows. Click on Tabs .Click on OntoSeer Tab.This window will appear.

![OntoSeer_jar_plugin_Actual_Tab](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Opening%20shot.png)

Now Start Building your Ontology.

For tutorial on ontology building one can refer to the Protege tutorial. This can be found in the following link:

https://cgi.csc.liv.ac.uk/~frank/teaching/comp08/protege_tutorial.pdf .

For more information for using OntoSeer please go through **OntoSeer_Manual.pdf** file present in master branch of OntoSeer. 


<a name="UserManual"></a>

## 4.User Manual
 
 This section discusses how OntoSeer can be used  along with Protege to get various recommendations.
  1. Click On OntoSeer tab button.
 This window will be shown.
 
 ![Plugin Window](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Opening%20shot.png)
 

 
 ## 4.1 ODP Recommendation
 1. Click On ODP recommendation  button. Two classes must be present for getting ODP recommendation.
 This window will be shown.
 

 
 ![OntoSeer ODP](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/ODP12.png)
 
2. Enter description of the ontology that one is trying to make .Alternatively domain
name,name of class and properties one want to make or can additively provide with the competency
questions.One can provide additional comments also. But one have to make sure that they are actually
making at least two classes to get recommendation. But the
recommendation will get better if one provide answer to as many questions as one can.


 
3. Get Recommendation. The recommendation is based on the data that we have scraped from 223
ODPs that we collected from http://ontologydesignpatterns.org/wiki/Community:ListPatterns

 ![OntoSeer_jar_ODP_reco_show](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/ODP11.png)
 
  <a name="Vocab"></a>
 
 ## 4.2 Vocab and Alternate Name Recommendation
 
 1. One should start buliding classes and properties in Protege .For example:-
  ![OntoSeer_jar_Vocab](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Vocab11.png)
 2. Click on VocabRecommendation button.
 3. Select the class or property for which you want the recommendations.Recommendations will be provided based on query results from LOV,Bioportal and our indexed files.
 4.Get the recommendations.
 ![OntoSeer_jar_Vocab_reco_show](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Vocab12.png)

 
  <a name="Naming"></a>
  
 ## 4.3 Naming Convention Recommendation 
 
 1. One should start buliding classes and properties in Protege .For example:-
 
   
 2. Click on the NamingRecommendation button.

![OntoSeer_jar_Name](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/ClassNami11.png)

 3. Select the class or property for which you want the recommendations.
 
 4.Get the class recommendations.
 
 ![OntoSeer_jar_Name_reco_show](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/ClassNami12.png)
 
 
 5.Get the property recommendations.
 
 ![OntoSeer_jar_Name_reco_show](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/PropertyNami12.png)

 <a name="Axiom"></a>
 
 ## 4.4 Axiom Recommendation 
1. Start building the ontologies .

  
2. Click on Axiom Recommendation button .


  ![OntoSeer_jar_Name](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Axiom11.png)
  
3. Select the class or property for which you want the recommendations.

4.Get the recommendations.

![Axiom Recommendation](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Axiom12.png)


<a name="class"></a>
 ## 4.5 Class Hierarchy Validation
 
 Class hierarch validation actually validates the correctness of a subclass hierarchy based on properties like rigidity, identitiy and unity of the classes.
1. Click on Class Hierarchy Validation button .
  ![OntoSeer_jar_Name](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Classhierarchy.png)

2. Answer the questions in (Y/N) format. Answer to all the questions are mandatory to velidate the hierarchy.
3. Validate the Hierarchy
![Class Hierarchy](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/ClassHierarchy2.png)

<a name="future"></a>
## 5.Future Work

As part of future work, we plan to engage in a dialogue with the ontology developer to resolve confusing issues such as having some term as a class vs.property vs. instance. This confusion will be resolved by asking the ontology developer a series of questions such as does the term interact with other concepts, are the terms very specific or general, if a term is made into a class, what will be its instances? 

<a name="sustain"></a>
## 6.Sustainability Plan

In the process of building OntoSeer, we have been able to collect only a few owl corpora and index them. The end-user can add other corpora according to their suitability by downloading them; OntoSeer will index them.

<a name="Demo"></a>
## 7.Demo Video of OntoSeer
1.A brief demo of OntoSeer can be found in the link:https://youtu.be/LGXHGXmVanI .
2.A brief presentation of OntoSeer is available at: https://www.youtube.com/watch?v=8WrgaHixkww&t=0s

<a name="google"></a>
## 8.Google Form for User Study 

Please find the link of Google form for user study here. Please give inputs so that we can make the tool better.
https://docs.google.com/forms/d/1TlYaGaQYB2ewwAJbcIZDxXz2APyngvsvSbMRmizbf94/edit?usp=sharing

<a name="index"></a>
## 9.Index Creation
For creating a new index for OntoSeer please follow the following steps.
1. Clone the entire OntoSeer project from "https://github.com/kracr/ontoseer.git"
2. Import the project as a Maven project in eclipse.
3. Go to ![indices.java](https://github.com/kracr/ontoseer/blob/master/OntoSeer/src/main/java/edu/stanford/bmir/protege/examples/view/indices.java) file under "OntoSeer/src/main/java/edu/stanford/bmir/protege/examples/view/indices.java" folder.
4. Run the file as a java application.
5. The system will ask for the name of the folder which you want to index. Please provide it with it.
6. It will take some time based on number and size of files. On completion it will print a message "Done indexing".
7. After this click on Maven install for the entire project.
8. Now use OntoSeer.jar following the procedure mentioned in above steps.

Alternatively,
	1.Clone the entire OntoSeer project from "https://github.com/kracr/ontoseer.git"
	2.Go to the folder where OntoSeer is dowloaded through command prompt.
	![OntoSeer Folder](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/ImageCommandLine1.png)
	3. Go to the OntoSeer/src/main/java/edu/stanford/bmir/protege/examples/view/ folder.
	![View Folder](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Image%20commadprompt2.png)
	4. Run the index.sh file.
	![index.sh](https://github.com/kracr/ontoseer/blob/master/ImagesOntoSeer/Commandprompt3.png)
	5. On completion "Done Indexing" will be shown.
Use the generated OntoSeer.jar for recommendation.






