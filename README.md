# AWS Backup with tags and AWS Backup Vault Lock

AWS CloudFormation to provision automated backup with AWS Backup for all supported services using tags and vault lock feature. With AWS Backup Vault Lock, you can add an additional layer of defense that protects backups (recovery points) in your backup vaults from inadvertent or malicious.

## Use Agreement
We recommend that you use this template as a starting point for creating your own template, not for launching production-level environments. Before launching a template, always review the resources that it will create and the permissions it requires.
Using this code `I Agree` I'm solely responsible for any security issue caused due any misconfiguration and/or bugs.

## Instructions
The main template [cfn-demo-aws-backup.yaml](cfn-demo-aws-backup.yaml) is used to set up all resources using AWS SAM cli.

To build the stack, issue the following command. 
**Note**: You need to have docker installed and running to perform this.
```
sam build --use-container --container-env-var WRAPT_EXTENSIONS=false
```

Afterwards, you will need to deploy the generated stack. The following command will do it:
```
sam deploy --guided
```

<a href="https://console.aws.amazon.com/cloudformation/home?#/stacks/new">Launch the AWS CloudFormation stack</a> using the [cfn-demo-aws-backup.yaml](cfn-demo-aws-backup.yaml) template file as the source.
**Note**: Check AWS account and region before stack deploy.

To get the template, issue the following command.
```
git clone git@github.com:aws-samples/aws-backup-with-tags-and-vault-lock.git
```

## Additional Resources
In the *AWS CloudFormation User Guide*, you can view more information about the following topics:

- Learn how to use templates to create AWS CloudFormation stacks using the [AWS Management Console](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html) or [AWS Command Line Interface (AWS CLI)](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-cli-creating-stack.html).
- To view all the supported AWS resources and their properties, see the [Template Reference](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html).

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

