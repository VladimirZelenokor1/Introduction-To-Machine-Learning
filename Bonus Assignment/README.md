## Bonus Assignment
Innopolis University, 
Introduction to Machine Learning, Fall 2022 - Bachelors

In this assignment, particularly the Incremental Learning section, I discovered that traditional machine learning methods, 
also known as offline machine learning, function effectively when we possess all the data upfront. 
We typically divide this data into training and testing sets, conduct feature engineering, build our model, 
and then deploy it to make predictions based on the training data. 
However, when dealing with data that arrives sequentially, such as data in motion, 
this traditional approach falls short as it doesn't address the continual arrival of data points. 
This is where the concept of online machine learning comes into play.

To construct an Incremental Learning model, 
I first developed a network comprising a shared feature extractor (shared layers) section and a distinct classifier head (fully connected layers). 
For the feature extractor (Backbone), a CNN model was utilized without fully connected layers. 
Additionally, a simple ANN model was employed for the head (classifier) section to generate linear outputs. 
During training on a new task, both the shared layers and the head of the current task were updated. 
Following training on each task (Task 1 & 2), the performance of the current and previous tasks was evaluated on Te. 
It was observed that the model's accuracy increased, indicating incremental learning.

Upon completion of training on the final task, the model was tested on Te, and its performance was compared with that of the CNN trained in II. 
The results revealed that classical learning outperformed incremental learning. 
In conclusion, classical learning demonstrates superior performance; 
however, incremental learning offers the advantage of being able to predict upcoming (unknown) data or objects in the future, 
which aligns with the primary purpose of incremental learning.
