echidnaCSI README

This document describes the cross-platform mobile app developed for use in the Citizen Science project called Echidna Conservation Science Initiative. echidnaCSI gathers data about the iconic Australian monotreme the short-beaked echidna (tachyglossus aculeatus). See the project website at https://grutznerlab.weebly.com/echidna-csi.html for more info.

The app was developed with LiveCode (www.livecode.com, open source version at: www.livecode.org) and enables anyone to collect observations of short-beaked echidnas in Australia and submit them easily to the project site on the Atlas of Living Australia (ALA).

Observations can be recorded outside mobile network range and observations can be
submitted later when network access is available.

Note that there may be modifications to the code necessary to run on current versions of LiveCode and it will need to be modified to be of use in other Citizen Science projects.

This software is available under the CC-BY licence.

Note that uploading of data requires an available server and permissions with scripts to process the data. You can also write these scripts using LiveCode.


Requirements
To build the app for mobile, at least the Indy version of Livecode (www.livecode.com) is
required.


Building the App
Before building the app, you'll need to customise some parts.
Standalone Settings - the path to the "Script Libraries" folder will need modifying in the
"Copy Files" pane.
iOS/Android - you'll need to customise the Basic Application Settings for your 
app-specific name, ID, version, profile etc.


Stack Properties
Set the app version in the Custom properties of the Stack.


Admin screen
There shouldn't be any scripts needing modification here but you will need to modify some
fields in the Admin screen of the app before building, to enter your own server details,
website address, and other URLs.
Templates - you need to customise the upload templates for uploading data to the ALA (or
to whereever you decide to upload data to!). Currently we have 2 forms, one for normal 
echidna observations and another for "special" (i.e. signs of presence) observations. 
These are accessible by clicking on the buttons on the Admin screen, which will bring up
an editable field with the template values.


Script modifications
Most scripts are contained in the stack script with some also in card and object scripts.
Utility scripts of various sorts are in external script files located in the 
"Script Libraries" subfolder.

You will need to modify scripts to build your own version, particularly related to
uploading data to whereever you decide to store it. The function "smALAInitVars" must
be changed to reflect your own project details even if you continue to use the ALA
as the project repository. Note that all of this should be put into a text file or
added to the admin screen (left as an exercise for the reader, at this stage!).

User registration
If user registration data is to be collected, make sure you get ethics approval and store
this data securely. Then you'll need to provide a script on your server to receive this
data. We've used a script called "getUser.lc" but you can write it in whatever you want.
e.g. php or python. You'll want to modify the stack script function "smSubmitUser" to
reflect this.


Further work
I have been working on making a templated app development system but this is still very
much a work-in-progress. Contact the author if this may be of interest, and definitely
if you have funding available!


Recommendation
If you're looking at starting up a Citizen Science project for recording nature-related
data, then do look at setting up a project using iNaturalist (if in Australia check out
BioCollect at the ALA). Developing your own system is a lot of work and better to use
some of the existing systems (and make them even better).