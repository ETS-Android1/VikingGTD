# VikingGTD

## Mission Statement

*To create the perfect "Getting Things Done" Software Suite*

## Background

I stumbled upon David Allens' brilliant book "Getting Things Done" 
a few years ago. Like hundreds of thousands of busy people before me,
I realized that this "GTD" methodology may actually work. I tried it
in my own "lite" version, and it did in fact work. Then I make a simple
Android App (VikingGTD in Google Play) - and it radically changed my 
productivity and almost removed stress from my life.

There are already several good GTD applications available, but none
that 100% filled my needs. So that is what I want to accomplish here:
The "GTD" application of my dreams. 

I sincerely hope that this will also become the GTD application of
*your* dreams, and I am therefore very open for your suggestions and 
thoughts.

## Current State
The project is currently in an early phase. Ideas are validated,
some technologies evaluated. Some code is written. But at this
time there are no release you can try out.

## Planned features in 2015
 * The full "GTD" work-flow in a nice, rich PC and Mac application.
 * A companion Android App that can do the basic operations when you are on the move.
 * A Cloud Server that handles synchronization between devices and backup.

## Architecture

### Abstract relationship between objects
The following diagram is a draft for the relationship between objects.
A *World* in this context is a single instance of a back-end (Cloud) server 
(with or without Fault Tolerance). As you can see, the architecture 
has the concept of *Organizations*, and *Users* (individuals). These
individuals organize their *Contexts*, *Lists* and *Projects* in *Folders*. 

![](doc/images/arcitecture_relations.png)

 - **Folder** - Just a place where you put other folders or Projects, Lists or Contexts.
 - **Project** - Any "Stuff" that require more than one Action to be completed. A project and it's actions can be shared among users.
 - **List** - Visualize a paper-sheet with some stand-alone scribbled *Actions* on it.
 - **Context** - A user-defined query (for example "In the Car", or "In the Office - when I have a good focus" where actions show up. It looks like a List, but one Action can appear in many Contexts.
 - **Attachment** - A Note, a Picture, a Scanned Document, an Email, a Word Document, a Web Page - an Url or pretty much anything (like your Email attachments or DropBox files).

### Location of Data

This diagram shows where the data is located. 

Each device have it's own database. There is no need for Internet access in order
to use any of the devices. Internet access is only required when you want to synchronize
the local data with the Server. Normally, this will happen in the background when
Internet is available - if you have linked the device with a server. If you only use
only one device (laptop, tablet or phone) - and you don't need or want a "Cloud Backup" - the 
application will work perfectly fine alone.

![](doc/images/arcitecture_devices.png)



