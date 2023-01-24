# Contributing to Eclipse Platform

Thanks for your interest in this project.

## Project description

Eclipse Platform defines the set of frameworks and common services that
collectively make up infrastructure required to support the use of Eclipse as a
component model, as a Rich Client Platform (RCP) and as a comprehensive tool
integration platform. These services and frameworks include a standard workbench
user interface model and portable native widget toolkit, a project model for
managing resources, automatic resource delta management for incremental
compilers and builders, language-independent debug infrastructure, and
infrastructure for distributed multi-user versioned resource management.

* https://projects.eclipse.org/projects/eclipse.platform

## Developer resources

Information regarding source code management, builds, coding standards, and
more.

* https://projects.eclipse.org/projects/eclipse.platform/developer

The project issues and source code are maintained in [multiple GitHub repositories](https://github.com/orgs/eclipse-platform/repositories) like
* https://github.com/eclipse-platform/eclipse.platform
* https://github.com/eclipse-platform/eclipse.platform.common
* https://github.com/eclipse-platform/eclipse.platform.debug
* https://github.com/eclipse-platform/eclipse.platform.releng
* https://github.com/eclipse-platform/eclipse.platform.releng.aggregator
* https://github.com/eclipse-platform/eclipse.platform.swt
* https://github.com/eclipse-platform/eclipse.platform.swt.binaries
* https://github.com/eclipse-platform/eclipse.platform.text
* https://github.com/eclipse-platform/eclipse.platform.ua
* https://github.com/eclipse-platform/eclipse.platform.ui.tools


Be sure to search for existing issues before you create another one. Remember that
contributions are always welcome!

### Setting up your GitHub account

All contributors, who are not committers on this Eclipse project,
must electronically sign the [Eclipse Contributor Agreement (ECA)](https://www.eclipse.org/legal/ECA.php)
via their [Eclipse account](https://accounts.eclipse.org/).
For more information, please see the [Eclipse Committer Handbook](https://www.eclipse.org/projects/handbook/#contributing).

To verify the Eclipse Contributor Agreement, GitHub contributions must use the 
same email address like your [Eclipse account](https://accounts.eclipse.org/).
If your GitHub account was registered with a different address, you can [add your Eclipse
email address to the account](https://github.com/settings/emails) instead.

Also add your GitHub account name to your [Eclipse account](https://accounts.eclipse.org/) under social media links section
to enable automated management of access rights for Eclipse project members.
If you are a committer in any of the Eclipse projects, you should receive a email containing an invite to join 
that project's GitHub organisation within 2 hours. You should accept the invite 
to maintain committer status in the GitHub organisation.

It is also recommended to [add SSH public keys to your GitHub account](https://github.com/settings/keys).

### Create an Eclipse Development Environment

You can set up a pre-configured IDE for development of the Eclipse SDK using the following link.

[![Create Eclipse Development Environment for the Eclipse SDK](https://download.eclipse.org/oomph/www/setups/svg/Platform_SDK.svg)](https://www.eclipse.org/setups/installer/?url=https://raw.githubusercontent.com/eclipse-platform/eclipse.platform.releng.aggregator/master/oomph/PlatformSDKConfiguration.setup&show=true "Click to open Eclipse-Installer Auto Launch or drag onto your running installer's title area")

### Recommended workflow

The recommended way for contributions is to create a fork of the main project repository and to create changes only in that fork
(see [Fork and pull model](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models#fork-and-pull-model) in the GitHub documentation).

Here are the steps:

1. Use the _Fork_ button (top right) on the GitHub repository page to create a forked repository under your GitHub account.
2. Click _Fetch upstream_ to get the latest source code from the upstream repository.
3. Clone the forked repository to your Eclipse workspace. The repository URL can be found by clicking the _Code_ button on the top right of the _<> Code_ tab.
4. Create a local branch.
5. Change code as needed to fix the issue.
6. Commit code changes to the local branch. Make multiple commits if necessary as history can be retained.
7. Once the fix is ready, push the branch to your forked repository (not to the original upstream project repository).
8. Open the forked repository page in your browser, switch to the branch where the fix is developed. Click the _Contribute_ button to start the _Open Pull Request_ workflow.
9. On the new page verify the target branch is the correct one to merge your commits. Also verify the list of commits contains the changes you intend to merge. If every thing OK, please click on _Create pull request_ button at the bottom right.
10. You can add reviewers if you want certain people to review a change. If you leave this empty, anyone from the project team will review.
11. If you push more commits to the same branch in your fork, they automatically get added to the pull request (and trigger a new round of builds and reviews).
12. Reviewers can review the pull request on the GitHub website or fetch the PR using the menu _Fetch GitHub PR_ in egit.
13. Every PR is automatically verified to check that contributors have a valid Eclipse Contributor Agreement.
14. Once the PR is approved there are two options to merge. Select what fits best given these criteria:
  * Rebase and Merge (retains all commits separately; useful when developing a feature consisting of multiple independent commits)
  * Squash and Merge (all commits in the PR get squashed into a single commit; useful to avoid separate "fix comments" commits)
15. After the PR is merged the source branch used for the PR can be deleted. 

### Commit message recommendations

  \<issue title\> \#\<issue number\>
  
  Example: The eclipse-test-framework deliverable contains unsigned bundles \#32
  
  Again this is a recommendation on the issue title part. Instead of issue title, if needed provide a concise description of changes. 
  Please do not forget to add the issue number to the commit message. This is used to link with GitHub issue.

## Setting up development environment

See https://wiki.eclipse.org/Platform/How_to_Contribute

## Contact

Contact the project developers via the project's ["dev" mailing list](https://dev.eclipse.org/mailman/listinfo/platform-dev).

