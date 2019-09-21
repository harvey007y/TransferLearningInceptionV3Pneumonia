# Transfer Learning with InceptionV3 for Pneumonia Detection
Detect pneumonia using transfer learning and Inception V3
## Transfer Learning
So we have all the different models floating around the web. WE have all heard about the Alexnet, VGG, Resnet, Inception and so on. they were all designed to find cats and dogs and toothbrushes, but how many times do we look for that in real life ?

In real life one needs to download a known neural network and use transfer learning to apply it to his/her problem. This generally means to cut of the last fully connected layers at the end and add others that are fit for the problem.

Below please how this transfer learning works:

![Transfer learning vs non-transfer](https://3qeqpr26caki16dnhd19sv6by6v-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/Three-ways-in-which-transfer-might-improve-learning.png)
## Pneumonia Deaths in Children are Primarily in Developing Countries

Source : Wikipedia

Pneumonia is an inflammatory condition of the lung affecting primarily the small air sacs known as alveoli. Typically symptoms include some combination of productive or dry cough, chest pain, fever, and trouble breathing. Severity is variable.

Vaccines to prevent certain types of pneumonia are available.Other methods of prevention include handwashing and not smoking.Treatment depends on the underlying cause. Pneumonia believed to be due to bacteria is treated with antibiotics. If the pneumonia is severe, the affected person is generally hospitalized. Oxygen therapy may be used if oxygen levels are low.

Pneumonia affects approximately 450 million people globally (7% of the population) and results in about 4 million deaths per year.

In 2008, pneumonia occurred in approximately 156 million children (151 million in the developing world and 5 million in the developed world).In 2010, it resulted in 1.3 million deaths, or 18% of all deaths in those under five years, of which 95% occurred in the developing world.

![Over half of child pneumonia deaths are in developing countries](https://pbs.twimg.com/media/CTiQG8XWUAA1czI.jpg)

## InceptionV3 Architecture for Transfer Learning.

![InceptionV3 Architecture](https://miro.medium.com/max/1200/1*gqKM5V-uo2sMFFPDS84yJw.png)

The project is about diagnosing pneumonia from XRay images of lungs of a person using self laid convolutional neural network and tranfer learning via inceptionV3. The images were of size greater than 1000 pixels per dimension and the total dataset was tagged large and had a space of 1.2 Gb . My work includes self laid neural network which was repeatedly tuned for one of the best hyperparameters and used variety of utility function of keras like callbacks for learning rate reduction and checkpointing. Could have augmented the image data for even better modelling but was short of RAM on kaggle kernel. Other metrics like precision , recall and f1 score using confusion matrix were taken off special care. The other part included a brief introduction of transfer learning via InceptionV3 and was tuned entirely rather than partially after loading the inceptionv3 weights for the maximum achieved accuracy on kaggle till date. This achieved even a higher precision than before.
