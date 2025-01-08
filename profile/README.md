# Eclipse Platform™

![splash](https://raw.githubusercontent.com/eclipse-platform/eclipse.platform/master/platform/org.eclipse.platform/splash.png)
<br>
[Pull requests](https://github.com/pulls?user=eclipse-platform) |
[Issues](https://github.com/issues?user=eclipse-platform)

Eclipse Platform is a comprehensive set of frameworks and common services that collectively provide a powerful software development infrastructure. It serves as the base framework for the [Eclipse integrated development environment IDE](https://www.eclipse.org/eclipseide/) and many other rich client applications.

The platform includes a wide range of frameworks and common services that are essential to supporting the use of Eclipse as a component model. These services include a standard workbench user interface model and a portable native widget toolkit, which ensure that the user interface of Eclipse is consistent across different platforms. The project model allows for the management of resources and enables automatic resource delta management for incremental compilers and builders.

Eclipse Platform also provides a language-independent debug infrastructure that enables developers to debug programs written in different languages. Additionally, the platform includes infrastructure for distributed multi-user versioned resource management, which allows for collaborative development and version control of resources.

Overall, Eclipse Platform is an essential set of tools and services for developers who need a robust and flexible platform for building complex software applications. Its comprehensive set of frameworks and common services ensure that developers can create high-quality software that meets the needs of their users. As the base framework for the Eclipse IDE and many other rich client applications, Eclipse Platform has a proven track record of providing a stable and reliable development platform that supports the creation of powerful software applications.

![workbench](https://raw.githubusercontent.com/eclipse-platform/eclipse.platform.releng.aggregator/master/eclipse.platform.common/bundles/org.eclipse.platform.doc.isv/guide/images/workbench.png)

See also https://projects.eclipse.org/projects/eclipse.platform and https://eclipseide.org/
## Community 

The Eclipse Platform is an Eclipse Community project so it obeys governance rules described in the [Eclipse Development Process](https://www.eclipse.org/projects/dev_process/) to guarantee meritocracry, diversity, vendor-neutrality and business-friendliness.

Please bear in mind that this project is almost entirely developed by volunteers and is not a product you contracted for. As a result, the contributors may not be able to look into some support requests. As per Eclipse Development Process, the committers are committed to review incoming code contributions though. If you do not provide the fix/implementation yourself (or pay someone to do it for you), the bug might never get fixed. If it is a serious bug, other people than you might care enough to provide a fix. As a consequence of all that, the only sure way to ensure some issue gets fixed or some feature gets implemented is that you contribute it yourself and convince some contributor that the change you submit is in the best interest of the project.

As you contribute more and more, you will eventually get nominated as a committer on the project.

### Reporting issues

Before reporting an issue, please consider whether the issue still exists or as already been reported:
* Find existing issues: https://github.com/issues?user=eclipse-platform
* Test the latest build of Eclipse Platform or SDK: [This page](https://download.eclipse.org/eclipse/downloads/) lists latest builds, and links to downloadable product archives and p2 repositories; and if you're using Maven artifacts, snapshots of Eclipse project are available at https://repo.eclipse.org/content/repositories/eclipse-snapshots/ .

The Eclipse Platform project codebase is split into multiple [repositories](https://github.com/orgs/eclipse-platform/repositories) owned by this organization. If you face an issue and have a sense of which particular GitHub repository is most related, you can open your issue against that particular repository, e.g.
* [New SWT issue](https://github.com/eclipse-platform/eclipse.platform.swt/issues/new)
* [New Platform issue](https://github.com/eclipse-platform/eclipse.platform/issues/new)
* [New Platform UI issue](https://github.com/eclipse-platform/eclipse.platform.ui/issues/new)

If you are unsure, you can open an [issue](https://github.com/eclipse-platform/.github/issues) against this current repository and the issue will then be moved as best by maintainers.

For errors please provide Stacktrace or [minimal reproducer](https://stackoverflow.com/help/minimal-reproducible-example).

For performance issues attach sampling snapshot (for example with [visualvm](https://visualvm.github.io/download.html)).

### Developing and Contributing

Contributions are always welcome!
See [CONTRIBUTING.md](https://github.com/eclipse-platform/.github/blob/main/CONTRIBUTING.md)

## Code of Conduct
🤝 This project is governed by the Eclipse Foundation [Code of Conduct](https://github.com/eclipse-platform/.github/blob/main/CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report any unacceptable behavior to [conduct@eclipse-foundation.org](mailto:conduct@eclipse-foundation.org).
