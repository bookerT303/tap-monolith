# tap-monolith

TAP for a single monolith application

## Setup

Install the following:

- kubectl

    - try `kubectl version`
    - if command is not found then you need to install from https://kubernetes.io/docs/tasks/tools/#kubectl
    - try `kubectl version` and if not correct might need to also
      ```
      brew list kubectl  # copy the first line from the output
      ln -s -F /opt/homebrew/Cellar/kubernetes-cli/1.29.0/bin/kubectl /usr/local/bin/kubectl
      ```
- tanzu-cli

  - try `tanzu version`
  - if command is not found then you need to install from https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/1.7/tap/install-tanzu-cli.html#install-or-update-the-tanzu-cli-and-plugins-3
  - try `tanzu version`
  

- TAP workspace (good only for 8 hours)
    
    - get a TAP workspace using https://tanzu.academy/guides/developer-sandbox
    - follow the directions for **Kubernetes Configuration** and copy the file into the 'kube' directory
    - follow the directions for **Cleanup** and copy the file into the 'kube' directory

   - follow the directions for **IDE Configuration** and copy the file into the 'kube' directory
   - Intellij plugins `Settings -> Plugins`
       - search for 'tanzu' and install 'Tanzu Developer Tools'
       - Follow the steps listed at https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/1.7/tap/application-accelerator-intellij.html to install the Application Accelerator plugin

# End of Setup

Now that we are setup we can start with creating a basic web app.
`git checkout basic-web-app` to continue