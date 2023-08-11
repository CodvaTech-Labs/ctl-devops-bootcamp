+++
title = "Jenkins Slack Integration"
weight = 27
chapter = false
pre = "<b> 2.1 </b>"
+++

Jenkins Slack integration allows you to receive notifications, updates, and alerts from your Jenkins pipelines directly in your Slack workspace. This integration enhances communication and collaboration within your team by keeping everyone informed about build and deployment statuses. To set up Jenkins Slack integration, you typically follow these steps:

1. **Install and Configure the Jenkins Slack Plugin:**
   - Log in to your Jenkins instance.
   - Go to "Manage Jenkins" > "Manage Plugins."
   - In the "Available" tab, search for the "Slack Notification" plugin.
   - Install the plugin and restart Jenkins.

2. **Configure Slack Config in Jenkins:**
   - Click on Manage Jenkins -> Confiugre 
   - Search for Slack and enter below details 

```
Workspace Name- ctldevopssep22
Channel ID - C04E59FA6UR
Credentials(token id) - 5vxOE37X7oWRblfyqsFGBbf5

```


3. **Configure Jenkins Slack Connectivity locally:**

4. **Setup FreeStyle Job:**

5. **Setup Pipeline Job:**
- Refer below code snippet - https://github.com/codvatechlabs/devops-bootcamp/blob/main/Jenkins/jenkins_declarative_pipeline.yaml
```
stage('Slack Message') {
            steps {
                slackSend channel: '#devops-alerts',
                color: 'good',
                message: "*${currentBuild.currentResult}:* Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}\n More info at: ${env.BUILD_URL}"
                }
}

```

**Here are some benefits of Jenkins Slack integration:**

- **Real-time Updates:** Receive instant notifications about build successes, failures, and other pipeline events.
- **Team Collaboration:** Keep the entire team informed about pipeline statuses without leaving Slack.
- **Quick Insights:** Get a quick overview of build progress and results.
- **Centralized Communication:** Consolidate important build-related information in a single platform.
- **Customization:** Customize notification messages and formats to match your team's preferences.

Example Slack notification message:
```
[SUCCESS] Jenkins Build #123 (my-project) - Build was successful!
```

Remember that specific configurations might vary based on your Jenkins setup, Slack workspace settings, and requirements. Additionally, while the steps outlined above are generally accurate, it's advisable to refer to the latest documentation for the Jenkins Slack Notification plugin and Slack's official guides to ensure accuracy.