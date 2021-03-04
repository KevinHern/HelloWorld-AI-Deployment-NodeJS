# HelloWorld-AI-Deployment-NodeJS
Small demo to deploy an AI in a NodeJS App

## How to install the app
Clone the repo and run the following command inside the cloned directory:

npm install

## How to make the AI work
The AI is a simple linear regression predictor. It receives a float number and outputs a result of the form of  *_y = 2x+1_*.
The app listens on the port 16000 and by default, it runs locally on your machine (127.0.0.1).
Use an app like Postman and send a POST request to the said port and IP address:

http://127.0.0.1:16000/predict

In the body, send a json with the following format:

{
	"x": 100.0
}

*NOTE: You can replace the number to get a different output.*

The server returns a JSON containing the following format:

{
	"result": <number>
}

## Where is the AI model?
It is located in the *assets/ai/* directory. Make sure that there are 2 files inside the directory:
1. model.json
2. group1-shard1of1.bin

## Additional Notes
To check how to the code works, make sure to read the *index.js* file.