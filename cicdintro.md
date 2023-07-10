#  CI/CD
- CI/CD is considered as the backbone of DevOps practices and automation.
- It plays a vital, challenging, and exciting role in DevOps culture.
- Growing numbers of companies are releasing software in minutes with the adoption of CI/CD practices.

- Approximately 2400 companies reportedly use CI/CD pipelines in their tech stack, including Facebook, Netflix, and Instacart.
- The primary reasons for adopting CI/CD include faster software builds, customer satisfaction through timely deployment, and simpler and quicker fault isolation with small code changes.

### Continuous Integration (CI):
- Developers merge/commit code to the master branch multiple times a day.
- Fully automated build and test process provides feedback within a few minutes.
- Avoids the integration hell that occurs when changes are merged into the release branch on release day.

### Continuous Delivery:
- An extension of continuous integration.
- Enables quick and sustainable release of new changes to customers.
- Automates the testing and release processes.
- Allows deployment of the application at any time by clicking a button.
- Deployment in continuous delivery is completed manually.

### Continuous Deployment:
- Goes beyond continuous delivery.
- Every change that passes all stages of the production pipeline is released to customers.
- No human intervention is required.
- Only a failed test will prevent a new change from being deployed to production.

### How CI/CD Practices Relate to Each Other:
- Continuous Integration (CI) is a part of both Continuous Delivery (CD) and Continuous Deployment (CD).
- The main difference lies in the deployment step:
    - In Continuous Delivery, deployment is done manually.
    - In Continuous Deployment, deployment happens automatically.

### What is a CI/CD Pipeline:
- The CI/CD pipeline is focused on automation.
- It involves initiating code builds, automated testing, and automated deployment to staging or production environments.
- It is a complex and exciting process that enables fast and efficient software delivery.
- If the output of any stage fails, the subsequent stages will also fail.


![Alt text](<images/MicrosoftTeams-image (4).png>)

### Why Jenkins?
- Jenkins is a popular and widely used open-source automation server.
- It offers extensive support for CI/CD pipelines and workflow automation.
- Jenkins provides a vast array of plugins and integrations with other tools, making it highly versatile.
- It has a large and active community that contributes to its continuous improvement and provides support.
- Jenkins allows for easy scalability and can be deployed on various platforms, including on-premises and cloud environments.
- It offers robust security features and supports authentication and authorization mechanisms.
- Jenkins supports a wide range of programming languages and technologies, making it suitable for diverse development environments.

#### Other tools that can be used for CI/CD:
- GitLab CI/CD: An integrated CI/CD platform that is part of the GitLab ecosystem.
- Travis CI: A cloud-based CI/CD platform that integrates well with GitHub.
- CircleCI: A cloud-based CI/CD platform that supports parallel builds and offers seamless integration with multiple version control systems.
- TeamCity: A powerful on-premises CI/CD server by JetBrains with support for multiple build agents and advanced build configurations.
- Azure DevOps: A comprehensive set of development tools by Microsoft, including CI/CD capabilities through Azure Pipelines.
- Bamboo: An on-premises CI/CD server by Atlassian that integrates well with other Atlassian products like Jira and Bitbucket.
- Jenkins X: A cloud-native CI/CD solution built on top of Kubernetes, designed specifically for modern cloud applications.
- GitHub Actions: Native CI/CD capabilities provided by GitHub, allowing developers to define workflows directly in their repositories.
- AWS CodePipeline: A fully managed CI/CD service by Amazon Web Services, designed to work seamlessly with other AWS services.

### Why build a pipeline? What is the business value?

- Automation and Efficiency:
  - Automated processes reduce manual effort.
  - Eliminates repetitive tasks and reduces human error.
  - Accelerates software delivery.

- Faster Time to Market:
  - Enables more frequent and reliable software updates and feature releases.
  - Allows businesses to stay ahead of the competition.
  - Enables quick response to market demands.

- Quality Assurance:
  - Automated testing ensures rigorous testing of code changes.
  - Catches bugs and issues early in the development cycle.
  - Results in higher-quality software and improved customer satisfaction.

- Continuous Feedback and Iteration:
  - Provides continuous feedback on software quality and stability.
  - Enables quick iteration and prompt issue resolution.
  - Incorporates user feedback for better products and user experiences.

- Risk Reduction:
  - Reduces the risk of errors and vulnerabilities in the production environment.
  - Enables fast rollbacks and easy recovery from issues.
  - Minimizes impact on users and the business.

- Scalability and Flexibility:
  - Handles large-scale development projects and growing teams.
  - Easily scales to accommodate complex software architectures.
  - Adapts to changing requirements and supports various environments and deployment strategies.

- Collaboration and Transparency:
  - Promotes collaboration among developers, testers, and operations teams.
  - Provides transparency into the software development and release processes.
  - Enhances communication, coordination, and alignment across teams and stakeholders.


# How to create a build on Jenkins

1. On dashboard click new item
2. Enter name
3. Select freestyle project
4. Select discard old builds
5. Input max builds to keep 3
6. Go to build and select execute shell
7. Input linux command
8. Add a post build action to make if this build is successful
9. Save and apply
10. Click build now 
11. Check command line output
