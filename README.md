# Dragoman - A Pocket Translator App


Dragoman is an android app which can recognise and translate language from text, speech and even photos. It has four options speech, text, photo and conversation.


# Screenshots


HOME PAGE   |  TEXT TRANSLATION |  VOICE TRANSLATION |
:---------:|:----------:|:---------:
![](https://github.com/sumitkhamar22/drago/blob/master/art/HomePage.jpeg?raw=true)  |  ![](https://github.com/sumitkhamar22/drago/blob/master/art/texttransaltion.jpeg?raw=true) |  ![](https://github.com/sumitkhamar22/drago/blob/master/art/voicetranslation.jpeg?raw=true) 


IMAGE TRANSLATION   |  CONVERSATION SIGNUP |  LOGIN |
:---------:|:----------:|:---------:
![](https://github.com/sumitkhamar22/drago/blob/master/art/image.JPG?raw=true)  |  ![](https://github.com/sumitkhamar22/drago/blob/master/art/signup.jpeg?raw=true) |  ![](https://github.com/sumitkhamar22/drago/blob/master/art/lagin.JPG?raw=true) 


CONNECTING WITH FRIENDS   |  CONVERSATION -1  |  CONVERSATION -2 |
:---------:|:----------:|:---------:
![](https://github.com/sumitkhamar22/drago/blob/master/art/friendrequest.jpeg?raw=true)  |  ![](https://github.com/sumitkhamar22/drago/blob/master/art/Chat.jpeg?raw=true) |  ![](https://github.com/sumitkhamar22/drago/blob/master/art/chat2.jpeg?raw=true) 
    


# What does this app do?
It is an open source Android application that allows people to download children's story books. The books are available
in different languages such as English, Sepedi, Zulu, Afrikaans etc. The books are free to distribute and translate.

Read more about Book Dash here:
http://bookdash.org/


# Libraries this app uses:

1. MaterialHelpTutorial - https://github.com/spongebobrf/MaterialIntroTutorial
2. FabButton - https://github.com/ckurtm/FabButton
3. Firebase - https://firebase.google.com/ 
4. Fabric - https://fabric.io/dashboard
5. Glide Image Loading - https://github.com/bumptech/glide

# Setup

1. Clone or download this repo.
2. This app runs off a Firebase backend. You will need to generate your firebase backend. To do this, navigate to https://firebase.google.com/ and sign up. Create a project called 
"Book Dash" (or what ever you want to call it). 
3. Navigate to "Database", select the three dots and then select "Import JSON". Select the file [server/book-dash-a93c3-export.json](server/book-dash-a93c3-export.json). 
Allow Firebase to import the data. You will also then need to place books in the storage container on firebase. You can find an example book located here: 
[server/simaandsiza-en.zip](server/simaandsiza-en.zip). Navigate to your Firebase console, and click storage, create a folder for the books and place them in there. 
You can then set the download URL of one of the books to use the book you have just uploaded to firebase storage in the STORAGE_PREFIX object.
 Within each zip file for a book, there is a file called bookdetails.json, this file is used to describe the images used and the number of pages in a book. 
In FirebaseConfig class you will need to change the base url of your book storage in the variable named - 
4. The database rules and storage rules can also be imported into Firebase, those files are also located in the server folder. 
(For more info on getting your own server up and running, check out https://github.com/bookdash/bookdash-backend-admin-portal
5. You will need to generate your own google-services.json file to use with the app. Navigate to the Firebase project settings dashboard. You should see an option to download the 
google-services.json file. This must then be placed into the app folder of this project. 


# [OPTIONAL setup] 
1. If you wish to build a release version you will need to create your own keystore file and edit the password values in the following file - (create a version of the file without the .sample extension): release-keystore.properties.sample
2. Setup a Fabric Account. https://fabric.io/dashboard
3. Get your Fabric API Key and Client key, change it in the file: /app/fabric-sample.properties and rename the file to fabric.properties

# Contributions
Contributions are welcome. Please read the [contributions guide](CONTRIBUTING.md) for more information. 

# License
Copyright 2016 Book Dash.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements. See the NOTICE file distributed with this work for
additional information regarding copyright ownership. The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License. You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations under
the License.
