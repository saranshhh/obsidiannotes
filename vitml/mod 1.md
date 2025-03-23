Introduction, Examples of Various Learning Paradigms, Perspectives and Issues, Version Spaces, Finite and Infinite Hypothesis Spaces, PAC Learning, VC Dimension

-> the field of study that gives computers the ability to learn without being explicitly programmed.
-> A computer program is said to learn from experience E with respect to some class of tasks T and
performance measure P, if its performance at tasks T, as measured by P, improves with experience
E.
-> Handwriting recognition learning problem
• Task T: Recognising and classifying handwritten words within images
• Performance P: Percent of words correctly classified
• Training experience E: A dataset of handwritten words with given classifications.

### The learning process, whether by a human or a machine, can be divided into four components,
namely, data storage, abstraction, generalization and evaluation. Figure 1.1 illustrates the various
components and the steps involved in the learning process.

![[Pasted image 20250323001710.png]]


1. Data storage
Facilities for storing and retrieving huge amounts of data are an important component of
the learning process. Humans and computers alike utilize data storage as a foundation for
advanced reasoning.
• In a human being, the data is stored in the brain and data is retrieved using electrochemical
signals.
• Computers use hard disk drives, flash memory, random access memory and similar devices
to store data and use cables and other technology to retrieve data.

2. Abstraction
The second component of the learning process is known as abstraction.
Abstraction is the process of extracting knowledge about stored data. This involves creating
general concepts about the data as a whole. The creation of knowledge involves application
of known models and creation of new models.
The process of fitting a model to a dataset is known as training. When the model has been
trained, the data is transformed into an abstract form that summarizes the original information.
3. Generalization
The third component of the learning process is known as generalisation.
The term generalization describes the process of turning the knowledge about stored data into
a form that can be utilized for future action. These actions are to be carried out on tasks that
are similar, but not identical, to those what have been seen before. In generalization, the goal
is to discover those properties of the data that will be most relevant to future tasks.
4. Evaluation
Evaluation is the last component of the learning process.
It is the process of giving feedback to the user to measure the utility of the learned knowledge.
This feedback is then utilised to effect improvements in the whole learning process.

### Different forms of data
1. Numeric data
If a feature represents a characteristic measured in numbers, it is called a numeric feature.
2. Categorical or nominal
A categorical feature is an attribute that can take on one of a limited, and usually fixed, number
of possible values on the basis of some qualitative property. A categorical feature is also called
a nominal feature.
3. Ordinal data
This denotes a nominal variable with categories falling in an ordered list. Examples include
clothing sizes such as small, medium, and large, or a measurement of customer satisfaction
on a scale from “not at all happy” to “very happy.”

### TYPES OF MACHINE LEARNING PAGE NO.26

### VERSION SPACES PAGE NO. 34

### PAC & VC DIMENSION CHAPTER 3

### Common issues in Machine Learning:

1. Inadequate Training Data The major issue that comes while using machine learning algorithms is the lack of quality as well as quantity of data. Although data plays a vital role in the processing of machine learning algorithms, many data scientists claim that inadequate data, noisy data, and unclean data are extremely exhausting the machine learning algorithms. For example, a simple task requires thousands of sample data, and an advanced task such as speech or image recognition needs millions of sample data examples. Further, data quality is also important for the algorithms to work ideally, but the absence of data quality is also found in Machine Learning applications. Data quality can be affected by some factors as follows: o Noisy Data- It is responsible for an inaccurate prediction that affects the decision as well as accuracy in classification tasks. o Incorrect data-It is responsible for faulty programming and results obtained in machine learning models. Hence, incorrect data may affect the accuracy of the results. o Generalizing of output data- Sometimes, it is also found that generalizing output data becomes complex, which results in comparatively poor future actions. 

2. Poor quality of data As we have discussed above, data plays a significant role in machine learning, and it must be of good quality as well. Noisy data, incomplete data, inaccurate data, and unclean data lead to less accuracy in classification and low-quality results. Hence, data quality can also be considered as a major common problem while processing machine learning algorithms. 

3. Non-representative training data To make sure our training model is generalized well or not, we have to ensure that sample training data must be representative of new cases that we need to generalize. The training data must cover all cases that are already occurred as well as occurring. Further, if we are using non-representative training data in the model, it results in less accurate predictions. A machine learning model is said to be ideal if it predicts well for generalized cases and provides accurate decisions. If there is less training data, then there will be a sampling noise in the model, called the non-representative training set. It won't be accurate in predictions. To overcome this, it will be biased against one class or a group. Hence, we should use representative data in training to protect against being biased and make accurate predictions without any drift. 

4. Overfitting and Underfitting Overfitting: Overfitting is one of the most common issues faced by Machine Learning engineers and data scientists. Whenever a machine learning model is trained with a huge amount of data, it starts capturing noise and inaccurate data into the training data set. It negatively affects the performance of the model. Let's understand with a simple example where we have a few training data sets such as 1000 mangoes, 1000 apples, 1000 bananas, and 5000 papayas. Then there is a considerable probability of identification of an apple as papaya because we have a massive amount of biased data in the training data set; hence prediction got negatively affected. The main reason behind overfitting is using non-linear methods used in machine learning algorithms as they build non-realistic data models. We can overcome overfitting by using linear and parametric algorithms in the machine learning models. Methods to reduce overfitting: o Increase training data in a dataset. o Reduce model complexity by simplifying the model by selecting one with fewer parameters o Ridge Regularization and Lasso Regularization o Early stopping during the training phase o Reduce the noise o Reduce the number of attributes in training data. o Constraining the model. Underfitting: Underfitting is just the opposite of overfitting. Whenever a machine learning model is trained with fewer amounts of data, and as a result, it provides incomplete and inaccurate data and destroys the accuracy of the machine learning model. Underfitting occurs when our model is too simple to understand the base structure of the data, just like an undersized pant. This generally happens when we have limited data into the data set, and we try to build a linear model with non-linear data. In such scenarios, the complexity of the model destroys, and rules of the machine learning model become too easy to be applied on this data set, and the model starts doing wrong predictions as well. Methods to reduce Underfitting: o Increase model complexity o Remove noise from the data o Trained on increased and better features o Reduce the constraints o Increase the number of epochs to get better results. 

5. Monitoring and maintenance As we know that generalized output data is mandatory for any machine learning model; hence, regular monitoring and maintenance become compulsory for the same. Different results for different actions require data change; hence editing of codes as well as resources for monitoring them also become necessary. 

6. Getting bad recommendations A machine learning model operates under a specific context which results in bad recommendations and concept drift in the model. Let's understand with an example where at a specific time customer is looking for some gadgets, but now customer requirement changed over time but still machine learning model showing same recommendations to the customer while customer expectation has been changed. This incident is called a Data Drift. It generally occurs when new data is introduced or interpretation of data changes. However, we can overcome this by regularly updating and monitoring data according to the expectations. 

7. Lack of skilled resources Although Machine Learning and Artificial Intelligence are continuously growing in the market, still these industries are fresher in comparison to others. The absence of skilled resources in the form of manpower is also an issue. Hence, we need manpower having in-depth knowledge of mathematics, science, and technologies for developing and managing scientific substances for machine learning. 

8. Customer Segmentation Customer segmentation is also an important issue while developing a machine learning algorithm. To identify the customers who paid for the recommendations shown by the model and who don't even check them. Hence, an algorithm is necessary to recognize the customer behavior and trigger a relevant recommendation for the user based on past experience. 

9. Process Complexity of Machine Learning The machine learning process is very complex, which is also another major issue faced by machine learning engineers and data scientists. However, Machine Learning and Artificial Intelligence are very new technologies but are still in an experimental phase and continuously being changing over time. There is the majority of hits and trial experiments; hence the probability of error is higher than expected. Further, it also includes analyzing the data, removing data bias, training data, applying complex mathematical calculations, etc., making the procedure more complicated and quite tedious. 

10. Data Bias Data Biasing is also found a big challenge in Machine Learning. These errors exist when certain elements of the dataset are heavily weighted or need more importance than others. Biased data leads to inaccurate results, skewed outcomes, and other analytical errors. However, we can resolve this error by determining where data is actually biased in the dataset. Further, take necessary steps to reduce it. Methods to remove Data Bias: o Research more for customer segmentation. o Be aware of your general use cases and potential outliers. o Combine inputs from multiple sources to ensure data diversity. o Include bias testing in the development process. o Analyze data regularly and keep tracking errors to resolve them easily. o Review the collected and annotated data. o Use multi-pass annotation such as sentiment analysis, content moderation, and intent recognition. 

11. Lack of Explainability This basically means the outputs cannot be easily comprehended as it is programmed in specific ways to deliver for certain conditions. Hence, a lack of explainability is also found in machine learning algorithms which reduce the credibility of the algorithms. 

12. Slow implementations and results This issue is also very commonly seen in machine learning models. However, machine learning models are highly efficient in producing accurate results but are time-consuming. Slow programming, excessive requirements' and overloaded data take more time to provide accurate results than expected. This needs continuous maintenance and monitoring of the model for delivering accurate results. 13. Irrelevant features Although machine learning models are intended to give the best possible outcome, if we feed garbage data as input, then the result will also be garbage. Hence, we should use relevant features in our training sample. A machine learning model is said to be good if training data has a good set of features or less to no irrelevant features.