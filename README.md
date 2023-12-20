# TAP Monolith Instructions

TAP for a single application

If you did not start from the command line.... close Intellij Idea and
change to the project directory and use the command launcher `Idea .`

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
  - if command is not found then
    
    - install the cli and plugins from https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/1.7/tap/install-tanzu-cli.html#install-or-update-the-tanzu-cli-and-plugins-3
    - For tanzu cli plugins:
 
      `tanzu plugin group search --show-details`

      Look for 'Plugins for TAP' and get the latest version

      For example the version number is `v1.7.2` then the command is:

      `tanzu plugin install --group vmware-tap/default:v1.7.2`

      That will get all the tanzu plugins that are needed.
  - try `tanzu version`
  
- Tilt
  - try `tilt version`
  - if command is not found then

    - install tilt from https://docs.tilt.dev/install.html
  - try `tilt version`

- TAP workspace (good only for 8 hours)
    
  - get a TAP workspace using https://tanzu.academy/guides/developer-sandbox
  - follow the directions for **Kubernetes Configuration** and copy the files into the '~/.kube' directory
  - follow the directions for **Cleanup** and copy the file into the '~/.kube' directory
  - `chmod +x ~/.kube/*.sh`
  - `~/.kube/set-context.sh`

  - Install the tanzu cli plugins from https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/1.5/tap/cli-plugins-apps-tutorials.html

  - follow the directions for **IDE Configuration** and copy the file into the 'kube' directory
  - Intellij plugins `Settings -> Plugins`
    - search for 'tanzu' and install 'Tanzu Developer Tools'
    - Follow the steps listed at https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/1.7/tap/application-accelerator-intellij.html to install the Application Accelerator plugin~~
      - might not be obvious that you select the file and have to click apply to see the plugin in the list of installed plugins.
      - Even less obvious is that you need copy the link to the 'Tanzu Developer Portal' from either page 1 or 2 of the Tap Sanbox left hand instructions.
      - Configuration `Settings -> Tanzu Application Accelerator` and paste in that URL.

# End of Setup

TODO - Create the src code using the accelerator plugin
TODO - start the workload
TODO - debug
TODO - add Actuators