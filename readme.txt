1. Use ubuntu ec2
2. Configure ssh agent
3. Add to ~/.zshrc 👇
alias kamal='docker run -it --rm -v "${PWD}:/workdir" -v "/run/host-services/ssh-auth.sock:/run/host-services/ssh-auth.sock" -e SSH_AUTH_SOCK="/run/host-services/ssh-auth.sock" -v /var/run/docker.sock:/var/run/docker.sock -v ~/.ssh:/root/.ssh -e AWS_ECR_PASSWORD=$(aws ecr get-login-password)  ghcr.io/basecamp/kamal:latest'
