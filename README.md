# Intelligent-System-Design-using-Cloud
A machine learning model to predict whether a message is spam or not. Also, created a system that upon receipt of an email message, will automatically flag it as spam or not, based on the prediction obtained from the machine learning model.This application has been developed as a part of the project component for the course- Cloud Computing (CS-GY 9223, New York University)

# Description
* Used Amazon SageMaker to implement a Machine Learning model for predicting whether an SMS message is spam or not. The model performs well on emails as well, and the model has been deployed to an endpoint.

* For the machine learning model we chose to build a neural network using Gluon.

* Implemented an automatic spam tagging system using SES service.

* For this, any new email that is received by the setup email address *(ammar@mydomain.codes)* will be stored in S3 and appropriately a Lambda function (L1) is triggered that extracts the body of the email and uses the prediction endpoint (E1) to predict if the email is spam or not.

* We also send a reply to the sender email address that we received the email along with the categorization of the email (spam or not) and the confidence score of the prediction made.

**Note**: The sender email has to be verified before sending the email to *ammar@mydomain.codes

* Finally, an AWS CloudFormation template is created for the automatic spam tagging system.

