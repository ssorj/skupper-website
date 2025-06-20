---
title: Installation
---

# Installing Skupper

## Installing Skupper on Kubernetes

To install the Skupper controller and CRDs on Kubernetes, use `kubectl
apply` with the [installation YAML](https://skupper.io/install.yaml):

~~~ shell
kubectl apply -f https://skupper.io/install.yaml
~~~

Additional Kubernetes installation methods are available in the
[release
artifacts](https://github.com/skupperproject/skupper/releases/tag/2.0.0).

## Installing Skupper on Linux

Docker and Podman!  Bare metal and VMs!

First install the CLI.

~~~ shell
skupper system install
~~~

## Installing the Skupper CLI

The Skupper CLI provides

With Skupper v2, you can install and configure Skupper on Kubernetes without the Skupper CLI.
You don't need the CLI to use Skupper.
You can use custom resources directly.

On Linux or the Mac, you can use the [install script][install-script]
to download and extract the command:

<div class="code-label">Linux or Mac</div>

~~~ shell
curl https://skupper.io/install.sh | sh
~~~

The script installs the command under your home directory.  It prompts
you to add the command to your path if necessary.

[install-script]: https://github.com/skupperproject/skupper-website/blob/main/input/install.sh

## More resources

* [Skupper releases at GitHub](https://github.com/skupperproject/skupper/releases)
* [Skupper images at Quay.io](https://quay.io/organization/skupper)

<!-- ## Installing manually -->

<!-- ### Download the latest release -->

<!-- Select the latest release for your platform: -->

<!-- <nav class="button-group"> -->
<!--   <a class="button" href="https://github.com/skupperproject/skupper/releases/download/{{latest_release_version}}/skupper-cli-{{latest_release_version}}-linux-amd64.tgz"><span class="material-icons">get_app</span> Linux</a> -->
<!--   <a class="button" href="https://github.com/skupperproject/skupper/releases/download/{{latest_release_version}}/skupper-cli-{{latest_release_version}}-mac-amd64.tgz"><span class="material-icons">get_app</span> Mac</a> -->
<!--   <a class="button" href="https://github.com/skupperproject/skupper/releases/download/{{latest_release_version}}/skupper-cli-{{latest_release_version}}-windows-amd64.zip"><span class="material-icons">get_app</span> Windows</a> -->
<!-- </nav> -->

<!-- To get artifacts for other operating systems and architectures, see -->
<!-- the [GitHub release page][release-page]. -->

<!-- [release-page]: https://github.com/skupperproject/skupper/releases/tag/{{latest_release_version}} -->

<!-- ### Extract the Skupper command -->

<!-- Use `tar` or `unzip` to extract the command from the release archive: -->

<!-- <div class="code-label">Linux or Mac</div> -->

<!-- ~~~ shell -->
<!-- tar -xf skupper-cli-{{latest_release_version}}-linux-amd64.tgz -->
<!-- ~~~ -->

<!-- <div class="code-label">Windows</div> -->

<!-- ~~~ shell -->
<!-- unzip skupper-cli-{{latest_release_version}}-windows-amd64.zip -->
<!-- ~~~ -->

<!-- This produces an executable file named `skupper` in your current -->
<!-- directory. -->

<!-- ### Place the command on your path -->

<!-- Move the executable file to your preferred location and make it -->
<!-- available on your path.  For example, this is how you might install it -->
<!-- in your home directory: -->

<!-- <div class="code-label">Linux or Mac</div> -->

<!-- ~~~ console -->
<!-- mkdir $HOME/bin -->
<!-- mv skupper $HOME/bin -->
<!-- export PATH=$PATH:$HOME/bin -->
<!-- ~~~ -->

<!-- <div class="code-label">Windows</div> -->

<!-- ~~~ console -->
<!-- mkdir %UserProfile%\bin -->
<!-- move skupper.exe %UserProfile%\bin -->
<!-- set PATH=%PATH%;%UserProfile%\bin -->
<!-- ~~~ -->

<!-- ### Check the command -->

<!-- To test your installation, run the `skupper version` command.  You -->
<!-- should see output like this: -->

<!-- ~~~ console -->
<!-- $ skupper version -->
<!-- client version                 {{latest_release_version}} -->
<!-- transport version              not-found (no configuration has been provided) -->
<!-- controller version             not-found (no configuration has been provided) -->
<!-- ~~~ -->

<!-- ### Upgrade sites -->

<!-- When you install a new version of the CLI, you can upgrade each site -->
<!-- using the `skupper update` command.  While we try to make Skupper -->
<!-- compatible between sites with different versions, we recommend -->
<!-- updating all sites at the same time. -->
<!-- Updating can take some time. Wait a minute before running the -->
<!-- `skupper version` command to validate your upgrade. -->

<!-- Do not use `skupper update` on sites created using the Skupper Operator. See [Using the Skupper Operator on Kubernetes](/docs/operator/index.html) for more information about using the Operator. -->

<!-- You can only use `skupper update` on Podman sites from version 1.5 and later. If -->
<!-- you have an older version Podman site, delete the site and recreate it with the -->
<!-- latest CLI version. -->
