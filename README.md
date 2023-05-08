# Sentiment_Analysis_SageMaker

In this repo, I introduce how to deploy a Sentiment Analysis model, using a pretrained Hugging face BERT model. I'll show how to deploy a endpoint in the SageMaker. To access that endpoint, I'll setup a AWS lambda function to inovoke that endpoint, and a API Gateway to allow you access the lambda function from public internet.

## Architecture
<img width="787" alt="image" src="https://user-images.githubusercontent.com/87917613/236928342-a4890aa4-01ba-44f5-a99b-7c2cce97bb5c.png">
