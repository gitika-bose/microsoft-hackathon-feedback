# microsoft-hackathon-feedback
Analyzing social media feedback (from Reddit) about PowerPoint

### get_raw_data.ipynb
This notebook has been divided into two parts 
<br/><br/>
(A) Training Data <br/>
The model to classify reddit posts as user feedback was trained using positive examples from User Voice and negative examples labelled manually from a set of Reddit posts. The data has been stored in txt files *positive_training_data.txt* and *negative_training_data.txt* respectively. Running these code cells will allow you to update these files. This is only needed once in a while if you to add fresh data. Recommended: Add newly classified to improve the training as well.
<br/><br/>
(A) Social Media Raw Feedback <br/>
Reddit contains a vast amount of user data, some of which is extremely valuable user feedback including requests for new features and improvements on existing ones. Hence, the model creates is applied on the bulk of reddit data to extract the relevant information. These cells extract unfiltered data from reddit given a query. I included two queries that can be used. This should also be done every couple of days to allow a constant influx of a data. In this case, the data is added to a new file instead of appending to the old data so as to not classify the same data multiple times.

### extract_feedback.ipynb
This notebook 
1. Creates the classifier trained on User Voice and some manually labelled reddit data
2. Applies that classifier to unfilitered reddit data 
3. Stores the useful feedback in a file called *reddit_powerpoint_feedback.txt*