# LookingGlass
Context based Image Search Engine\n 
CS6675/CS4675: Advanced Internet Computing  Project

As the popular saying goes, a picture is worth a thousand words. A picture (or a series of them) has an amazing ability to convey emotion, mood, narrative, ideas and messages. Conveying the most elemental part of the stories to those that view them. In general, articles become more interesting when there are illustrations around them. The illustrations somehow make the stories more alive and they enhance your imagination. Imagine reading an article about Tourism Australia. An image or a few images showing the scenic beauty of Australia would have more impact on the mind of the reader than the article itself.
Today we have a lot of active recommender systems in different segments of the market and web search has mostly transformed into providing worthwhile recommendations to users based on personal preferences and browsing history. However, there are only a handful of those which deal with image recommendations. We intend to build an image recommendation system that automatically analyzes the content of an article/web page and suggests images (or one image) which best represent the context of the article. This feature will lend more visual appeal to the article and make it more impactful. The app will also provide an option to incorporate the image within the article depending on the article type. The user can then download/use the final product as required.

This project is a novel implementation of an image recommender system. It is different from typical image searches for reasons described above. Some of the most interesting contributions of this project are: 
It allows users to query the entire content of the document and not be limited to a couple of words of query length.
The application is offered as a web application and a chrome extension. The two expose similar functionality, but are geared to cater to specific use-cases. The web-app focuses on bloggers/writers who want to find relevant images to embed in their own posts. Chrome Extension, on the other hand, is oriented towards readers and casual internet users to find relevant images. 
The project uses reverse image search in order to find out relevant tags for an image and then recommends other similar images. This was done using Bing’s SearchByImage API and Selenium to parse through the result set. Extracted keyword was then used to find relevant images using Google’s custom search API.

To start the app, pip install django, django-haystack, django-jquery, elasticsearch
1. python manage.py makemigrations lookingglass_app
2. python manage.py migrate auth{, admin}
3. You can open the admin site : python manage.py createsuperuser
4. pip install google-api-python-client
5. pip install flickrapi
6. Start elasticsearch: brew install elasticsearch, start elasticsearch

To install the chrome extension,
1. Go to your browser(Google Chrome) and go to chrome://extensions/.
2. Click on developer mode and then click on load unpacked extensions.
3. Window explore would open and select the folder chrome_extension/.
4. Restart the browser and the extension should be ready to go.

Once all the extensions have been installed, start the server ./manage.py runserver
Go to localhost:8000 and Looking Glass should be ready to go.

----

Copyright (c) 2016 The persons identified as document authors. All rights reserved.


