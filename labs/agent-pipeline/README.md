# Jenkins Agents in Pipeline
Agents can be configured to be used in the pipeline and is a more preferred way of doing the things.

We have a `products-api` project as a part of this learning repository. We will use a java agent to run the build on a docker container having `java` and `maven` installed.

Create a new pipeline job and use the [Jenkinsfile defined at /project/products-api/Jenkinsfile](/project/products-api/Jenkinsfile)

- Create a new job as _Pipeline_ and name it `products-api`
- select _Pipeline script from SCM_ in the dropdown
- set the SCM to _Git_
- set the _Repository URL_ to `http://gogs:3000/courselabs/jenkins-fundamentals.git`
- change the _Branch Specifier_ from `*/master` to `*/main`
- set the _Script Path_ to `project/products-api/Jenkinsfile`

Save and run the build. The build will be successful, you can check the build history and logs. Look for the agent