# Call for Code 2020 - Quiz App Starter Kit

This is a very simple example quiz application that uses a Loopback generated express app with a react frontend.

As more and more learning and collaboration moves online, developers will start to build microservices for distance learning. In this case a simple quiz app. The starter kit could easily be remixed into a short essay app, a grading app, or other education tool. Loopback is an open source tool for quickly building a data api for your applications. Whatever your specific application does, using loopback gets you quickly writing application logic and not writing data handling code.

## Getting started

The core of this example is *generated code* from the Loopback utility. For clarity, we're using the now-deprecated version 3.0 of the library. This just makes it even easier to start, consider upgrading to Loopback v4 to get the latest features and security updates.

To get the most out of this starterkit, you should create your own Loopback app. (It's super fast!) [https://www.youtube.com/watch?v=iOMD27DjuO4]. However, to start this one, here are the steps:

```bash
npm install
npm serve
```

Once the API is up, you can navigate to the swagger api explorer at <https://localhost:3000/explorer>. Once there you can start to put data into your API right away. See screenshots:

TODO: <screenshots of swagger api>

Try creating a question with this json blob:

```json
{
  "question_text": "Which immobile ground unit has the longest range?",
  "answers": [
    "Siege Tank",
    "Spore Colony",
    "Photon Cannon",
    "Bunker (Marines"
  ],
  "correct_answer_index": 0,
  "quizId": 1
}
```

### Frontend

The frontend is coded in (React)[https://reactjs.org/], a library for user interfaces. If you don't have experience with React or want something simpler, you could get something similar with simpler tools like (bootstrap)[https://getbootstrap.com/] and (jQuery)[https://jquery.com/]. The frontend code is compiled once, then served by the express app generated by Loopback.

```bash
TODO: instructions for building react frontend code
```


## Deployment

As this is a standard express application, you can use either Cloud Foundry or Kubernetes to host your application.  A Dockerfile is included.

To deploy using cloud foundry, follow (these steps)[https://github.com/IBM/nodejs-express-app#ibm-cloud-developer-tools].

To deploy using Kubernetes, use the included manifest in `deployment/deploy.yaml`. Note: If using ingress, you must populate the ingress hostname with the Ingress Subdomain of your cluster. Example:

```
$ ibmcloud ks cluster get --cluster nibz-falco-test-2 | grep Ingress
Ingress Subdomain:              nibz-falco-test-2-5290c8c8e5797924dc1ad5d1b85b37c0-0000.us-east.containers.appdomain.cloud
```
