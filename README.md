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