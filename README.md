# GiveMeLabeledIssues
Web platform to find new issues in a variety of open source project issues relevant to your selected project domains! 


# Deployment commands:

## Redeploying Flask project and hosting webpage 
When changing the server, you need to redeploy the Flask service to Firebase with an authorized account.

From server directory (where the needed Dockerfile is):
gcloud builds submit --tag gcr.io/flask-bert/flask-fire
gcloud beta run deploy --image gcr.io/flask-bert/flask-fire
  - Service name is flask-fire

Then you need to host the project with Firebase hosting with an authorized account. 

From the root directory (where node_modules is)
./node_modules/.bin/firebase deploy
After this finishes you will be given a link that is the public domain for the hosted webpage and Flask project. 

Currently the link to the deployed project is: https://flask-bert.web.app/


### Hosting locally
To host the project locally, modify the command slightly:
./node_modules/.bin/firebase serve

Open your browser to http://localhost:5000 after serving. 
