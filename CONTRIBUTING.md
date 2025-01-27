# Contributing to Eclipse Platform

Thanks for your interest in this project.

## Project Description

Eclipse Platform defines the set of frameworks and common services that supports the usage of Eclipse as a component model, 
as a Rich Client Platform (RCP) and as a comprehensive tool integration platform. 
These services and frameworks include a standard workbench
user interface model and portable native widget toolkit, a project model for
managing resources, automatic resource delta management for incremental
compilers and builders, language-independent debug infrastructure, and
infrastructure for distributed multi-user versioned resource management.

* https://projects.eclipse.org/projects/eclipse.platform

## Developer Resources

Information regarding source code management, builds, coding standards, and
more.

* https://projects.eclipse.org/projects/eclipse.platform/developer

The project issues and source code are maintained in [multiple GitHub repositories](https://github.com/orgs/eclipse-platform/repositories) like
* https://github.com/eclipse-platform/eclipse.platform
* https://github.com/eclipse-platform/eclipse.platform.releng.aggregator
* https://github.com/eclipse-platform/eclipse.platform.swt
* https://github.com/eclipse-platform/eclipse.platform.ui


Be sure to search for existing issues before you create another one. 
Remember that contributions are always welcome!

## Setting up Your Eclipse and GitHub Account

Create an [Eclipse account](https://accounts.eclipse.org/) if you don't already have one. 
See the ["Eclipse Foundation Account" section](https://www.eclipse.org/projects/handbook/#contributing-account) in the Eclipse Committer Handbook.

All contributors, who are not committers on this Eclipse project,
must electronically sign the [Eclipse Contributor Agreement (ECA)](https://www.eclipse.org/legal/ECA.php)
via their [Eclipse account](https://accounts.eclipse.org/).
For more information, please see the [Eclipse Committer Handbook](https://www.eclipse.org/projects/handbook/#contributing).

To verify the Eclipse Contributor Agreement, GitHub contributions must use the 
same email address like your [Eclipse account](https://accounts.eclipse.org/).
If your GitHub account was registered with a different address, you can [add your Eclipse
email address to the account](https://github.com/settings/emails) instead.

Also add your GitHub account name to your [Eclipse account](https://accounts.eclipse.org/) to enable automated management of access rights for Eclipse project members. 
You can do this by logging into your Eclipse account, choosing ["Edit Profile"](https://accounts.eclipse.org/user/edit) and add your GitHub account name in the social media links section.

If you are a committer in any of the Eclipse projects, you should receive an email containing an invite to join  that project's GitHub organisation within 2 hours. 
You should accept the invite to maintain committer status in the GitHub organisation.

It is also recommended to [add SSH public keys to your GitHub account](https://github.com/settings/keys).

## Creating an Eclipse Development Environment

You can set up a pre-configured IDE for development of the Eclipse SDK using the following link.

[![Create Eclipse Development Environment for the Eclipse SDK](https://download.eclipse.org/oomph/www/setups/svg/Platform_SDK.svg)](https://www.eclipse.org/setups/installer/?url=https://raw.githubusercontent.com/eclipse-platform/eclipse.platform.releng.aggregator/master/oomph/PlatformSDKConfiguration.setup&show=true "Click to open Eclipse-Installer Auto Launch or drag onto your running installer's title area")

## Recommended Workflow

The recommended way for contributions is to create a fork of the main project repository and to create changes only in that fork
(see [fork and pull model](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models#fork-and-pull-model) as well as [working with fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks) in the GitHub documentation).
Then you can create a pull request (PR) to have your changes merged from the fork into the main project repository.

The workflow can be separated into two parts:
1. [Creating and managing a fork](#creating-and-managing-a-fork)
2. [Creating a PR](#creating-a-pull-request) from the fork and specifics of that process in the `eclipse-platform` organization

If you are familiar with how to create and manage a fork, you can [skip that part](#creating-a-pull-request).

### Creating and Managing a Fork

Use the _Fork_ button (top right) on the GitHub repository page and choose _Create a new fork_ to create a forked repository under your GitHub account.
Whenever changes are pushed to the main project repository, you can click _Sync fork_ in the forked repository to get the latest source code from the main project repository.

Then you have two options:

1. Clone the main project repository and add the forked repository as an additional remote
   
   _With this option, you can easily retrieve the most recent changes from the main project repository by simply pulling the `master` branch, as your default remote repository will be the main project repository._

   Clone the main repository to your Eclipse workspace or, if you use the Eclipse installer as explained in [Creating an Eclipse Development Environment](#creating-an-eclipse-development-environment), the repository is already cloned that way. The repository URL can be found by clicking the _<> Code_ button on the top right of the _<> Code_ tab within the GitHub page for the main project repository. When you clone the repository, it will automatically be the added as the "origin" remote to your local clone.

   You then have to add your fork as an additional remote to push your changes to a branch of that fork.
   To this end, add the forked repository as an additional remote called "fork" (or whatever you like):
   * Go to your fork on GitHub.
   * Click the _<> Code_ button on the top right of the _<> Code_ tab copy the URL .
   * Add the URL as the "fork" remote to your local clone.

   Whenever the `master` branch of the main project repository changes, pulling the `master` branch of your local clone will give you the current state. In case you have created a branch and committed changes to it, you can rebase it onto the updated `master` branch.

2. Clone the forked repository and add the main repository as an additional remote

   _With this option, you can easily create new branches for committed changes in your fork, as the default remote repository will be your forked repository._

   Clone the forked repository to your Eclipse workspace or, if you use the Eclipse installer as explained in [Creating an Eclipse Development Environment](#creating-an-eclipse-development-environment), you have to change the URL for the repository during the setup. The repository URL can be found by clicking the _<> Code_ button on the top right of the _<> Code_ tab within the GitHub page for the forked repository. When you clone the forked repository, it will automatically be added as the "origin" remote to your local clone.

   You then have to add the main project repository as an additional remote.
   To this end, add the main project repository as an additional remote called "upstream":
   * Go to the main project repository on GitHub.
   * Click the _<> Code_ button on the top right of the _<> Code_ tab copy the URL.
   * Add the URL as the "upstream" remote to your local clone.

   Whenever the `master` branch of the main project repository changes, you have to synchronize the `master` branch of your fork. Go to the GitHub page of your forked repository and click _Sync fork_. You can then pull the `master` branch of your local clone to retrieve the current state. In case you have created a branch and committed changes to it, you can rebase it onto the updated `master` branch.


### Creating a Pull Request

When you have set up your fork of a repository that you want to contribute to and prepared a local clone for it, you can perform changes, commit them, and propose them via a pull request according to the standard ["pull requests from a fork" workflow](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork). In the following, the workflow is sketched with some specific information for the Eclipse platform projects.

1. **Preparing the PR:** Create a branch in your fork and apply the desired changes to it. Push the branch with the changes to your forked repository (not to the original upstream project repository).
   - Make multiple commits if necessary as history can be retained, but note that you will usually be asked to combine your changes to a single commit per pull request. So keep changes as small as possible and try to split them up.

2. **Creating the PR:** Open the page of the forked repository in your browser, switch to the branch where the fix is developed. Click the _Contribute_ button to start the _Open Pull Request_ workflow.
   - On the new page verify the target branch is the `master` branch of the main project repository.
   - Verify that the list of commits contains the changes you intend to merge.
   - If you are a committer, you can add reviewers if you want certain people to review a change. If you leave this empty, anyone from the project team will review.

3. **Updating the PR:** To update your pull request, you can push more commits to the same branch in your fork. They automatically get added to the pull request (and trigger a new round of builds and reviews). You can also amend your previous commits and force push them to your branch.
    - You will usually be asked to squash your commits to a single one before a PR will be merged.
    - Exception: when you bump versions in the Manifest/POM files, you could provide 2 separate commits in the same PR: one with the functional changes (_i.e._ in the code) and one with the version bump (_i.e._ in the Manifest/POM files). This is not a rule but, if necessary, it would help cherry-picking commits when merging your PR.

4. **Validating and verifying the PR:** 
   - Reviewers can review the pull request on the GitHub website or fetch the PR using the _Fetch GitHub PR_ menu entry in the _Git Repositories_ view inside the Eclipse IDE.
   - Every PR is automatically verified to check that contributors have a [valid Eclipse Contributor Agreement (ECA)](#setting-up-your-eclipse-and-github-account).
   ### What does a valid PR look like? (Checklist)
   These are the basic criteria that need to be fulfilled for a PR to be considered valid. 
   
   **If you are a contributor, consider these points as prerequisites before your PR can be reviewed. Please ask for help if needed, either by making a comment on the PR or via a _GitHub discussion_.**

   - All checks need to pass.
     - If tests are broken then they should either be fixed or documented (create a new issue or mention an existing one).
     - The code must compile.
     - The versions of the affected plugins should be properly bumped.
     - There should be no new API warnings. If a warning can’t be fixed then suppress it and write a comment explaining why.
     - If there are other (obscure) errors in the checks, please find them (read the logs) and actively ask what is happening and how to fix them.
   - The commit text should be well-written (see [Commit Message Recommendations](#commit_message_recommendations)).
   - If tests were added, they should meet the following criteria:
      - They should **run**: check the logs and make sure they are being executed.
      - They should **pass**: do not add broken tests.
   - If the PR has been reviewed and the reviewer left some comments, address them and clearly document what you did. Either write a proper response like "addressed in commit _XYZ_" or explain why you did what you did. A mere "thumbs up" is not enough.

5. **Merging the PR:** Once the PR is approved, it can be merged by a committer
   - One of two options to merge can be selected, based on what fits best given these criteria:
      - _Rebase and Merge_: retains all commits separately; useful when developing a feature consisting of multiple independent commits
      - _Squash and Merge_: all commits in the PR get squashed into a single commit; useful to avoid separate "fix comments" commits
   - After the PR is merged, the source branch used for the PR (in the fork) can be deleted. 
   - Your fork is now _out-of-date_ with the main (upstream) project repository. In case the "origin" remote of your local clone is the forked repository, you should get it back up to date. You can either use the _Sync Fork_ function on GitHub to update the fork and pull the `master` branch to your local clone, or pull the latest changes from "upstream" (the main project repository) into your local repository.

## Commit Message Recommendations

```
<issue title> #<issue number>

Short description/summary as to why this change is being made
  
Fixes https://github.com/<Full URL to issues/issue #>
```
 
  Example: 

```
Make memory view cell editor visible on Linux GTK3 #132

Since SWT change from GTK2 to GTK3 as its backend the cell
editing in the memory view has not worked properly
with the cell editor not visible. This change uses explicit
setVisible rather than adjusting Z-order of the controls.

Fixes https://github.com/eclipse-platform/eclipse.platform.debug/issues/132 
```

  Again this is a recommendation on the issue title part. Instead of issue title, if needed provide a concise description of changes. 
  Please do not forget to add the issue URL to the commit message. This is used to link with GitHub issue.

## Building the project on commandline

Even though most of the time you can work in the IDE it is sometime beneficial to build on the commandline as this is how we also execute the verification builds, also some test might not run at all in the IDE if they require a veri specific setup,
also if you want to produce an update site from changes or want to have a local build artifact of your changes you will currently need to do this on the commandline.

### Required tools

We are using [Apache Maven](https://maven.apache.org/index.html) for building the sources, usually it it fine to just use the [latest release](https://maven.apache.org/download.cgi) you can use whatever [install method](https://maven.apache.org/install.html) that is sufficent for your system.

### Running the build

Most project repositories are already setup so that you can run `mvn clean verify` directly, one exception is the [aggregator build](https://github.com/eclipse-platform/eclipse.platform.releng.aggregator/) that builds all projects together and requires [special attention](https://github.com/eclipse-platform/eclipse.platform.releng.aggregator/?tab=readme-ov-file#how-to-build-the-eclipse-sdk).

### Tips and Tricks

- If your **changes seem to be not applied** this is usually a sign that you forget to increment the version of the bundle, or don't have commited (you don't need to push) your changes in wich case the baseline replace might come into effect, you will see a warning in the log like this `[WARNING] <project name>: baseline and build artifacts have same version but different contents`
- If you just want to **build one specific module**, this is usually possible without special consideration just keep in mind that if the tests are seperated from the module you have changed you need to build both of them or the whole reactor,
for example you can run the tests and the bundle under test with the command `mvn clean verify -pl :<name of the bundle under test>,:<name of the test bundle>`, one specific test can be run by adding `-Dtest=<full qualified class name of test>`
- You can perform a **quick run** to check everything compiles with `-DskipTests` in comibination with `-T1C` this can really speed up things, just keep in mind that the tests are not executed.
- If you want to **make sure you didn't broke the API** you can specify `-Papi-check'
- If you want to **check the javadoc** (JDT currently [not find all issues](https://github.com/eclipse-jdt/eclipse.jdt.core/issues/1858) in the IDE) you can specify `-Pjavadoc` additionally `-DfailOnJavadocErrors=true` will even fail the build, you can even [try to fix them](https://maven.apache.org/plugins/maven-javadoc-plugin/fix-mojo.html) automatically by adding 'javadoc:fix' to your command


## Contact

- For official announcements, use the project's ["dev" mailing list](https://dev.eclipse.org/mailman/listinfo/platform-dev).
- To ask for help, either use the current issue/PR or start a **GitHub Discussion**