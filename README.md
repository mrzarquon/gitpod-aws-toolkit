Use the `aws_init.sh` script to bootstrap your gitpod workspace for use with AWS SSO and ECR hosted registries

You can either add this to your gitpod.yml workspace tasks or dotfiles to ensure the configurations are in place

Note: you will have to have set these environment variables in your [gitpod](https://gitpod.io/variables) settings dashboard:
```
AWS_SSO_URL
AWS_SSO_REGION
AWS_ACCOUNT_ID
AWS_ROLE_NAME
AWS_REGION
```

Add this script to your repo and then update your .gitpod.yml file to run the aws_init.sh as a command when a workspace launches:
```yaml
tasks:
  - command: |
      # this will install all AWS tools and then open a browser window to authenticate your AWS session
      bash $GITPOD_REPO_ROOT/aws_init.sh
      # put things you want to do with AWS after this line
```

If you want to try this out, if you've set your variables to be shared with any repo (`*/*`), then you can just launch this repo in Gitpod:<br>
[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/mrzarquon/gitpod-aws-toolkit)
