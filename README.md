# Sentiment_Analysis_SageMaker

In this repo, I introduce how to deploy a Sentiment Analysis model, using a pretrained Hugging face BERT model. I'll show how to deploy a endpoint in the SageMaker. To access that endpoint, I'll setup a AWS lambda function to inovoke that endpoint, and a API Gateway to allow you access the lambda function from public internet.

## Architecture
The following diagram shows how we call the deployed ML model. The client side calls the API Gateway. The API Gateway seals the backend, so that AWS lambda stays and runs in a protected private network. API Gateway passes parameters to the Lambda function. The Lambda parses the values and sends it to the model endpoint. The model performs the prediction and returns the predicted value to Lambda. The lambda parses the returned values and sends it back to API Gateway. API Gateway responds to the client with that value. To test the API, we will use postman from client side.
<img width="787" alt="image" src="https://user-images.githubusercontent.com/87917613/236928342-a4890aa4-01ba-44f5-a99b-7c2cce97bb5c.png">

## SageMaker Setup

I use the SageMaker Studio to launch the Sentiment_Analysis.ipynb notebook. I created this notebook by simplifying the hugging face distill notebook created by AWS. 
