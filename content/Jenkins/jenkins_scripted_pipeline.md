+++
title = "Jenkins Scripted Pipeline Job "
weight = 23
chapter = false
pre = "<b> 1.8 </b>"
+++

Jenkins Scripted Pipeline is a more flexible and powerful way to define complex continuous delivery pipelines using Groovy scripting. Unlike the Declarative Pipeline, which focuses on a structured and simpler syntax, the Scripted Pipeline allows you to write custom Groovy code to define every aspect of your pipeline's behavior. This makes it suitable for highly customized or intricate build and deployment processes.

Here are the key characteristics and features of Jenkins Scripted Pipeline:

**1. Groovy Scripting:**
   Scripted Pipeline uses the Groovy programming language to define pipeline logic. You have full access to Groovy's capabilities, including conditional statements, loops, and functions.

**2. Nodes and Stages:**
   Pipelines in Scripted Pipeline start with defining nodes (agents) and stages. Nodes specify where the pipeline runs, and stages define the different phases of your build process.

**3. Steps and Custom Logic:**
   You use Groovy script steps to define build steps, custom logic, and integrations with various tools. This allows for more advanced customization than the Declarative Pipeline.

**4. Environment and Variables:**
   You can define and manipulate environment variables using Groovy scripting. Variables can be used across different stages and steps.

**5. Post-Build Actions:**
   Like in Declarative Pipeline, you can define post-build actions that execute after the pipeline completes.

**6. Extensibility:**
   Scripted Pipeline allows you to create and use custom functions and libraries, increasing code reusability.

**7. Conditional Execution:**
   You can use Groovy's conditional statements (`if`, `else`, `switch`) to control the flow of your pipeline based on conditions.

**8. Error Handling:**
   Scripted Pipeline allows you to implement error handling using try-catch blocks to gracefully manage exceptions.

**9. Advanced Integrations:**
   For more complex integrations or custom logic, Scripted Pipeline offers greater flexibility compared to the Declarative Pipeline.

Here's a simple example of a Jenkins Scripted Pipeline:

```groovy
node {
    def gitURL = 'https://github.com/example/repo.git'
    
    stage('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: gitURL]]])
    }
    
    stage('Build and Test') {
        sh 'make clean'
        sh 'make test'
    }
    
    stage('Deploy') {
        sh 'make deploy'
    }
    
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed :('
        }
    }
}
```

In this example, the Scripted Pipeline defines three stages: `Checkout`, `Build and Test`, and `Deploy`. Each stage contains custom Groovy code to execute specific tasks.

Jenkins Scripted Pipeline is ideal for teams with advanced requirements or who want fine-grained control over their pipeline logic. It provides the flexibility to integrate complex build, test, deployment, and notification processes using custom Groovy scripting.