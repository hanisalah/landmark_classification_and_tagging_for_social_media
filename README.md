# landmark_classification_and_tagging_for_social_media
This is Udacity - Deep Learning course project 2 where a Convolutional Neural Network (CNN) is built and trained to classify image set into 50 classes depending on different landmarks in each image.

Photo sharing and photo storage services like to have location data for each photo that is uploaded. With the location data, these services can build advanced features, such as automatic suggestion of relevant tags or automatic photo organization, which help provide a compelling user experience. Although a photo's location can often be obtained by looking at the photo's metadata, many photos uploaded to these services will not have location metadata available. This can happen when, for example, the camera capturing the picture does not have GPS or if a photo's metadata is scrubbed due to privacy concerns.

If no location metadata for an image is available, one way to infer the location is to detect and classify a discernable landmark in the image. Given the large number of landmarks across the world and the immense volume of images that are uploaded to photo sharing services, using human judgement to classify these landmarks would not be feasible.

In this notebook, you will take the first steps towards addressing this problem by building models to automatically predict the location of the image based on any landmarks depicted in the image. At the end of this project, your code will accept any user-supplied image as input and suggest the top k most relevant landmarks from 50 possible landmarks from across the world. The image below displays a potential sample output of your finished project.

In this project, I experienced some interesting things to play with:
1. I documented several trials to build my scratch CNN, explaining my thinking process for those who are interested.
2. I used transfer learning utilizing vgg19 model. However, instead of freezing the featurizer and retraining the classifier, I froze the whole model and added just one linear layer at the end. The results were spectacular!
