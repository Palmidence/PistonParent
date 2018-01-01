How to contribute
=================

The Piston project aims to become community driven, here are the guidelines we've set out to achieve that.

## The Basics
1. [Create or find an issue](#creating-an-issue) to contribute to on our [Issue tracker](https://github.com/Laxio/Issues/issues).
2. Does your proposed change fit [Piston's goals](#piston's-goals)?
3. Fork the repositories you intend on making changes to.
4. Create a new branch in each of the repositories, we suggest you use the same branch name across all affected repositories.
5. Where applicable create test cases for any of your code.
6. Ensure your code is well documented and readable.
7. Test your changes, we highly suggest that you test changes on both single and multi-server instances.
8. Push to your fork and [submit a pull request](#submitting-a-pull-request).

## Creating an Issue
When creating an issue you should ensure that it does not already exist. If an issue exists which is similar to the one you are creating, make sure to address _why_ you have created a new issue instead of building upon the existing one. Refrain from creating broad sweeping issues which encompass a variety of problems. If you have found multiple issues, create a unique issue for each one.

Security violations should be directed to one of the team directly, via [Discord](https://discord.gg/RND5Kz7) or email {not currently available}.

**Note:** Don't create issues referring to Minecraft version updates, these will be planned ahead of time within the core Piston team. If you would like to help in this process head over to our [Discord](https://discord.gg/RND5Kz7)

## Submitting a Pull Request
You've finished up your changes, tested them thoroughly, and are pleased that your code is ready to be submitted for review. Here's some tips to help ensure that your pull request gets accepted without a hitch.
* Ensure that no merges are present within the commits included in your PR.
* Make sure your code follows our code conventions.
* Make sure your code compiles under Java 8.
* Provide proper, detailed JavaDocs where appropriate.
  * Your JavaDocs should try to detail the limitations of the code you are adding.
* Test your code and it's testing material.
  * Additional testing material may include plugins.
  * Ensure that these test-plugins are linked to in your request, and that they are documented in detail so we can test your code too.
* Follow the Pull Request guidelines which are relevant for the repository your are contributing to.

## Piston's Goals
The aim of the Piston project is to create a lightweight Minecraft server with an API to go alongside it; allowing developers to make large changes to major systems via plugins. This includes the ability to modify the base server structure that the plugin is running on. Attempts should be made by all contributors to avoid requiring the use of specific implementation classes outside of the Protocol. An example of a poor practice is shown below:

```java
StickyPistonServer server = (StickyPistonServer) ServerManager.getServer("MyServer");
server.myNewMethod();
```

Unless absolutely necessary, references to specific implementations is to be avoided. If the implemented method you are trying to access can be put into the API, then it is best to do so. By doing this, custom server implementations are not forced out of implementing certain features.