# StyleTransfer
Takes two images and slaps them together. 
The Folder Edit has the images of the Porn Clips at the point where God is mentioned

## Goal: 
Render an image where a porn participant is saying God is merged with an image caravaggio



## Influences
Code for Style Transfer - photo: https://github.com/luanfujun/deep-photo-styletransfer?utm_content=buffer39dd6&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer


### Nice Article Comparing various approaches
http://liipetti.net/erratic/2016/08/16/neural-style-transfer-after-the-first-year/

### FloydHub version
http://docs.floydhub.com/guides/style_transfer/ 

# StyleTransfer
Takes two images and slaps them together. E.g. 

## Our style image
http://www.artble.com/imgs/a/5/d/320796/simon_vouet.jpg


## How to use the Alone vs With Another model
This predicts whether the person in the video is Alone or WithAnother (person). 
Anything above 90% on WithAnother is usually With Another person, anything less than that is usually by herself. 

How to use the Prediction API
If you have an image URL:


https://southcentralus.api.cognitive.microsoft.com/customvision/v1.0/Prediction/3ddc339c-0e86-49a2-9352-ca24af24d0ef/url?iterationId=802c3a07-aa98-4f6e-bc74-d9474422ddb5
Set Prediction-Key Header to : 2b23286449c240658cf600fc05d30449
Set Content-Type Header to : application/json
Set Body to : {"Url": "<image url>"}
If you have an image file:


https://southcentralus.api.cognitive.microsoft.com/customvision/v1.0/Prediction/3ddc339c-0e86-49a2-9352-ca24af24d0ef/image?iterationId=802c3a07-aa98-4f6e-bc74-d9474422ddb5
Set Prediction-Key Header to : 2b23286449c240658cf600fc05d30449
Set Content-Type Header to : application/octet-stream
Set Body to : <image file>
Remember, you can mark an iteration as Default so you can send data to it without specifying an iteration id. You can then change which iteration your app is pointing to without having to update your app.
