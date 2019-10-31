#The following are the key steps we’re going to follow:

- [ ]    Build the app and add tests
- [ ]    Define a new Docker image for this app via the Dockerfile
- [ ]    Setup Google Cloud Platform
- [ ]    Configure Kubernetes
- [ ]    Add some scripting
- [ ]    CircleCI setup




## Running the application locally
```
 npm install
```

```
npm start
```

In a browser, navigate to http://localhost:3000 (http://localhost:3000).


Build image
```
docker build -t ci-cd .
```

Run applicaion
```
docker run -p 3000:3000 ci-cd
```

Navigating to http://localhost:3000 (http://localhost:3000)


Tag images
docker tag <HOSTNAME>/<YOUR-PROJECT-ID>/<IMAGE-NAME>
```
docker tag ci-cd gcr.io/ci-cd-12347/ci-cd:0.1.0
```

Push image
gcloud docker -- push <HOSTNAME>/<YOUR-PROJECT-ID/<IMAGE-NAME>
```
gcloud docker -- push gcr.io/ci-cd-12347/ci-cd:0.1.0
```





## Google Cloud Platform setup

#### Linux

On your terminal, run:
```
curl https://sdk.cloud.google.com | bash
```
Restart the shell when the above step is done:
```
exec -l $SHELL
```
Initialize the gcloud environment:
```
gcloud init
```



###### About project
CI/CD for Node.js projects: using CircleCI, Kubernetes, and Docker with deployment to the Google Cloud Platform
Manual [Pages](https://circleci.com/blog/ci-cd-for-node-js-projects-using-circleci-kubernetes-and-docker-with-deployment-to-the-google-cloud-platform/?utm_content=buffer4813c&utm_medium=SCC&utm_source=Twitter&utm_campaign=Twitter-Buffer-Csy).
