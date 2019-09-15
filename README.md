Project3:
 Explaination based wirter verififcation
==========================
Manish Reddy Challamala,
May 05, 2019 ,manishre@buffalo.edu

For detailed explaination, please visit the below link:
[link for report pdf](https://github.com/manish216/CSE-672-Project3/blob/master/proj3report.pdf)


## ❖ Abstract

We present ​http://betelgeuse.cse.buffalo.edu/and_dataset​ (XAI-AND) a dataset that
contains 13700 handwritten samples and 15 corresponding expert examined features for
each sample. Furthermore, we propose Deep Learning and explanation based systems
that can assist human examiners to detect authentic or forged handwritten samples. We
describe our approach based on the word “AND” extracted from full-page handwritten
samples in CEDAR Letter data. Our first approach is based on learning the mapping
between expert features and the input images using the soft probabilities learned by a
Features Learner Network (FLN). In the second, we use a Probabilistic Graphical Model
(PGM) in tandem with FLN to generate log-likelihood of samples coming from the same
or different source. We perform various experiments based on variations of our two
approaches and evaluate the results based on Type 1 Accuracy (T1), Type 2 Accuracy
(T2) and Likelihood Ratio (LR). The dataset is released for public use and the methods
can be extended to provide explanations on other verification tasks like face verification
and biomedical comparison. The code is available on
https://github.com/mshaikh2/HDL_Forensics​.
Another approach that we propose is the visual explanation of the decisions made by
Convolutional Neural Networks by using a visualization technique called
Gradient-weighted Class Activation Mapping (Grad-CAM). They provide a
high-resolution class-discriminative visualization. In the context our classication models,
these visualizations would (a) lend insights into failure modes of these models (what
factors led the model believe that the two image fragments came from the same/different
writer), (b) are more faithful to the underlying model, and (c) help achieve model
generalization by identifying dataset bias.
Finally, we propose to design and conduct human studies to measure if Grad-CAM
explanations help users establish appropriate trust in predictions from deep networks
and show that Grad-CAM helps untrained users successfully discern a ‘stronger’ deep
network from a ‘weaker’ one even when both make identical predictions.

## ❖ Introduction

The goal of Handwriting verification is to find a score of similarity between the two given
handwritten samples. Researchers have successfully approached the problem of
identifying inter-writer and intra-writer variations to solve the task of verification.
However, these approaches were based on conventional machine learning and purely


handcrafted features. The forensic community has used the Likelihood Ratio (LR) to denote the degree of similarity between a Known ​ k ​ and Questioned ​ q ​ sample. With the

advent of Deep Learning, where the features are automatically learned, the solutions of
this problem became a more black box. Siamese Networks and Triplet Loss have
attempted to solve the problem of isolating similar and dissimilar samples. However, the
predictions of such systems raise eyebrows in the expert community, as they do not
have a clue why those predictions were made. When a human examiner compares
forgery with real, he does it based on tangible features based on which a judge can
provide quality results. If the expert examiner merely states yes or no then his integrity
will be questioned. This instance applies to even an intelligent assistant of the human
examiner. Our proposed system provides such an intelligent assistant in the form of
Explainable Artificial Intelligence interface (XAI).
Many organizations like DARPA have invested heavily in providing explainable based
systems. Researches have been working on why a classifier's output should be trusted
and developed techniques like LIME to explain the predictions of any classifier in an
interpretable and faithful manner. There also have been attempts to trace the predictions
of the model back to the training data for understanding model behavior, debugging
models, detecting dataset errors, and even creating visually indistinguishable training-set
attacks. With these advances, the need for an interface that can provide trustworthy
predictions is imminent in the forensic community.
Many communities including Healthcare and Biomedical cannot completely rely on black
box predictions and require more explanation as to why a decision was made by the AI.
These communities need more understanding about the predictions of the black-box so
that they can assimilate their current surrounding context and carefully utilize the
intelligent explanations of the system and make an informed decision. The proposed
system learns from human observed annotations and takes one step towards helping
the forensic document examiner (FDE) make a rational examination.
Although the system exhibits extremely good performance, it fails to explain the
predictions of convolutional neural networks, as they lack the interpretability, that is, they
are unable to explain which features or which part of the image contributed in making the
final decision by the model. In order to build trust in intelligent systems and move
towards their meaningful integration into our everyday lives, it is clear that we must build
‘transparent’ models that explain why they predict what they predict. It would, therefore,
be helpful to be able to explain why a model made the prediction it made. For example,
when a model predict that the two images came from the same writer when, in reality,
the two images are written by different writers, it is hard to say why the wrong judgement
was made without visualizing the network’s decision. Visualizations can also build
confidence about the predictions of a model. For example, even if a model correctly
predicts that the two images were written by different writers, we would want to confirm
that the model bases its decision only on the distinguishing features of the “AND” image
and not some other object or background pixels.
Convolutional Neural Networks (CNNs) and other deep networks have enabled
unprecedented breakthroughs in a variety of computer vision tasks, from image
classification to object detection, semantic segmentation, image captioning, and more
recently, visual question answering. A visualization technique called Class Activation
Map(CAM) visualization can be deployed for this purpose. We intend to identify the pixel
locations in the image of handwritten word “and” that correspond to a certain feature (for
instance, for the feature “staff of a”, we need to identify the pixel locations that contain
staff of ‘a’ as seen by the model.
We also aspire to implement this technique for the writer verification task to visualize
which features in the image of handwritten word “and” were responsible for the decision
(whether the pair of images are written by same writer or not) made by the model.


We have summarized this content in the following blog:
[Blog Link](https://machinelearningfromub.home.blog/)

## ❖ FUTURE WORK

- We plan to provide a User Interface for explanation tool where users will
be able to get the textual as well as visual explanation for the task of
handwriting verification.

- We can extend the image fragment analysis to a document verification
 one.
