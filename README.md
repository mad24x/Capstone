### Project Title

Optimizing Travel Planning: Predicting Meeting Attendance Mode

Author: Andrew Nordstrom

#### Executive summary

This project aims to improve travel planning for professionals by predicting whether a meeting will be attended in-person or online based on calendar invite data. By leveraging features extracted from meeting titles and locations, we developed a predictive model that can accurately distinguish between in-person and virtual meetings. The model's output enables better scheduling and travel time calculations, ultimately saving time and reducing operational costs. This could be used with traffic data to determine the best time to leave for an offsite meeting and also consider some users preferences such as arriving early.  The final piece would to create an invite for the users calendar to block off the time when user should leave for offsite meeting.  This would would be helpful for people trying to schedule other meetings that the user would be unvaialable due to traveling.


#### Rationale
In today’s fast-paced professional environment, many employees are required to travel frequently for in-person meetings, while others can join meetings virtually. Misclassifying a meeting can lead to wasted time, increased travel costs, and reduced productivity. Accurately predicting the attendance mode is crucial for optimizing travel schedules and ensuring that employees allocate their time and resources efficiently. This project addresses a real-world problem that affects a broad range of industries, from sales and finance to legal services.

#### Research Question
Can this model accurately predict whether a meeting will be attended in-person or online using features derived from meeting invites (specifically, the title and location), in order to optimize travel planning and resource allocation?


#### Data Sources
Synthetic Data Generation: For project purposes, a synthetic dataset was generated of meeting invites that include fields such as title, location, start time, end time, and attendance choice.
Calendar APIs: Data extracted from platforms such as Google Calendar or Microsoft Outlook, including meeting titles, locations, and timestamps.

#### Methodology
Data Preparation:
Synthetic dataset generation that simulates meeting invites for multiple users.
Feature engineering to combine text features (title and location) into a single field.
Model Building:
Initial experiments with numerical features alone, followed by the inclusion of text-based features.
Implementation of a text-based pipeline using TF-IDF vectorization and a Random Forest classifier.
Hyperparameter tuning (e.g., grid search) and threshold adjustment to favor predictions that flag in-person meetings for travel planning.
Evaluation:
Model performance was assessed using accuracy, classification reports, and confusion matrices.
Visualizations such as ROC and precision-recall curves were used to further analyze performance.


#### Results
The best-performing model using title and location achieved an accuracy of 93%.
High precision and recall for both classes indicate that the model effectively differentiates between in-person and online meetings.
Focusing on text-based features (title and location) significantly improved model performance compared to using numerical features alone.
Adjustments such as threshold tuning allowed the model to favor in-person meeting predictions—critical for planning travel time.

#### Next steps
Model Refinement:
Experiment with other models (e.g., ensemble methods, neural networks) and further optimize hyperparameters.
Consider cost-sensitive learning to further penalize misclassification of in-person meetings.
Real-World Validation:
Test and validate the model using real calendar data and user feedback.
Integrate the model into a travel planning system to dynamically adjust departure times and travel plans.
Deployment:
Build a prototype application that integrates with calendar APIs to provide real-time travel planning recommendations based on model predictions.

#### Outline of project


Prediction model link

https://github.com/mad24x/Capstone/blob/main/meeting_prediction_attendance.ipynb

data generator - include for future data colection.  (no need to run as data is include in the repository) 
https://github.com/mad24x/Capstone/blob/main/data%20generator.ipynb

Data file 
https://github.com/mad24x/Capstone/blob/main/meeting_invites.csv



##### Contact and Further Information
mad24x@gmail.com




