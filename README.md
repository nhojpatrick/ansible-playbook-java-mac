# Install JDK EA (Early Access) on MacOS

## Install default jdk

```bash
$ ansible-playbook --ask-become-pass playbook.yaml
```

Will install the default playbook version. Check playbook for jdk_major and jdk_build to understand what version will be installed.

## Install specific jdk

```bash
$ ansible-playbook --ask-become-pass --extra-vars "jdk_build=18" playbook.yaml
```
Will install a specified version. Check playbook for jdk_major and jdk_build to understand what version will be installed, but jdk_build will be taken from the command line.

Even a different major version
```bash
$ ansible-playbook --ask-become-pass --extra-vars "jdk_major=16 jdk_build=5" playbook.yaml
```

## Troubleshoot

 - Install homebrew https://brew.sh/
 - Using `brew install ansible`
 - Using `brew install gnu-tar` will get around opening archive issue.
