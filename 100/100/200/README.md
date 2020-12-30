# 200 Repository vs. Repository Manager: What's the Difference?

Next, let’s define the difference between a repository and a repository manager.

## Repository
A repository is a storage location where components such as packages, libraries, binaries, or containers are retrieved so they can be installed or used (you’ll learn more about components in lesson two). In order to ease consumption and usage of open source components, they are aggregated into collections on public repositories, and are typically available on the internet as a service. Examples of such repositories are:

- Central Repository, also known as Maven Central
- NuGet Gallery
- RubyGems.org
- npmjs.org

## Repository Manager
A repository manager is a dedicated server application used to manage all the repositories your development teams use throughout the course of development. At its core, a repository manager does the following:

- Proxies remote repositories and caches contents.
- Hosts internal repositories.
- Groups repositories into a single repository.

Using these core functions, a repository manager becomes the central and authoritative storage platform for all open source and proprietary items produced by your development team. With a repository manager, you can completely control access to, and deployment of, every component in your organization from a single location. It allows you to control what gets into your products from remote sources as well as examine, and keep track of, what’s produced by your build systems.  A repository manager also allows you to secure a connection to remote repositories, ensuring that your usage is not publicly exposed.
