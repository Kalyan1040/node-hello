Prerequisites:

1. Jenkins server installed in a machine
2. npm and node installed in the same machine
3. Both git and aws credentials are stored in jenkins credentials store.
4. jenkins should have aws sam plugin(for lambda deployment)


Solution Pipeline:

I have chosen Jenkins as an opensource tool and leveraged its Jenkisfile to build a pipline for deploying node.js app to lambda.

For this requirement, i have created a Jenkisfile whihc will have two stages. In stage 1, we will checkout the code and the second stage we will use aws sam plugin to deploy our lambda function.

I have created a sam template for lambda function with runtime as node.js.
Once the pipeline gets executed, we have to access the url and add that url in route53 A recordset.

I haven't done the route53 part.
