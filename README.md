
### install devbox

https://www.jetify.com/docs/devbox/installing-devbox#linux

```bash
devbox shell
# to go out
exit

# within path 03-installation-setup
devbox shell

task kind:01-generate-config

task kind:02-create-cluster

task civo:00-authenticate-cli

```

### Aliases
```bash
alias k=kubectl
alias t=task
alias tl="task --list-all"
```

### kubectl autocopmplete (within devbox shell)
```bash
 # Installing bash completion on Linux
  ## If bash-completion is not installed on Linux, install the 'bash-completion' package
  ## via your distribution's package manager.
  ## Load the kubectl completion code for bash into the current shell
  source <(kubectl completion bash)
  ## Write bash completion code to a file and source it from .bash_profile
  kubectl completion bash > ~/.kube/completion.bash.inc
  printf "
  # kubectl shell completion
  source '$HOME/.kube/completion.bash.inc'
  " >> $HOME/.bash_profile
  source $HOME/.bash_profile
```

### task autocomplete (within devbox shell)
```bash
# ~/.bashrc
# export TASK_EXE='go-task' if needed
eval "$(task --completion bash)"
``` 