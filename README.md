## Deploying Lambda Function from VS Code using AWS SAM CLI

### Prerequisites

1. **AWS Account**: You need an AWS account with access key and secret key.
2. **Dependencies**: 
    - [awscli](https://aws.amazon.com/cli/): Install using `brew install awscli`.
    - [aws-sam-cli](https://aws.amazon.com/serverless/sam/): Install using `brew install aws-sam-cli`.
    - [Docker](https://www.docker.com/): Install Docker.
3. **Configure AWS Account**: Run `aws configure` to set up your AWS credentials locally.
4. **VS Code**: Install VS Code and the extension "AWS Toolkit" for easier Lambda function management.

### Steps

1. **Create a Lambda Function Project**:
    - Open VS Code and press `Cmd + Shift + P`.
    - Search for "AWS create lambda SAM Application".
    - Select the desired options (framework, machine configuration, etc.), and provide a name for your Lambda function.
    - Choose or create a folder for your project.

2. **Modify Function**:
    - Navigate to the `app.js` file in your Lambda project folder.
    - Modify the function according to your requirements.

3. **Build**:
    - Open the terminal in VS Code and navigate to the folder containing `template.yaml` (e.g., `cd sam-lambda-app`).
    - Run `sam build` to create a build folder with your project files.

4. **Run Locally**:
    - Run `sam local invoke` to test your Lambda function locally.
    - Optionally, you can modify the JSON in `events.json` for custom local testing.

5. **Deploy**:
    - Run `sam deploy --guided` to deploy your Lambda function to AWS.
    - Follow the prompts in the console to accept terms/details and configure deployment options.
    - Review and confirm the deployment settings.
  
### Additional Notes

- Ensure your AWS credentials are properly configured locally using `aws configure`.
- Make sure Docker is running before deploying or testing locally with `sam local invoke`.
- The AWS Toolkit extension for VS Code can simplify Lambda function management and deployment tasks.
- Always review the AWS documentation for any updates or changes to the deployment process.

### Conclusion

Following these steps, you can easily deploy Lambda functions from VS Code using AWS SAM CLI. Make sure to test your functions locally before deploying to AWS to ensure they work as expected.
