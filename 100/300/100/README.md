# 100 Repository Types

## Objectives
By the end of this lesson, you will be able to:

- Explain the concept of a proxy repository.
- Explain the concept of a hosted repository.
- Explain the concept of a group repository.
- Identify the repository types needed in your organization.

## What are Repository Types?
In Nexus Repository Manager there are three repository types—proxy repositories, hosted repositories, and repository groups—all using a number of different repository formats. Understanding the available repository types helps define what is needed within your organization for a successful Repository Manager implementation.

For example, if your team needs to access public repositories, you’ll want to create proxy repositories. If your team has components that aren’t public, but are used by others in your development organization, then creating a hosted repository is the way to go. If you have multiple repositories that would be easier to access from a single URL, then creating a group repository fits that need.

With these examples in mind, you can see that creating and managing repositories is an essential part of your Nexus Repository Manager configuration because it allows you to expose more components to your users.

## Proxy Repositories
A proxy repository is a repository that is linked to a remote repository. Any request for a component is verified against the local content of the proxy repository. If no local component is found, the request is forwarded to the remote repository. The component is then retrieved and stored locally in the repository manager, which acts as a cache. Any future requests for the same component are fulfilled from the local storage, eliminating network bandwidth and time overhead when retrieving the component from the remote repository again. In addition, when components are downloaded to the Nexus Repository Manager proxy, a copy remains there indefinitely, unless removed by a Repository Manager administrator. This is extremely useful in the event a component becomes unavailable in the remote repository, and provides more control over the components needed to build your applications.

By default, the repository manager ships with the following configured proxy repositories:

- maven-central: This proxy repository accesses the Central Repository, formerly known as Maven Central. It is the default component repository built into Apache Maven and is well-supported by other build tools like Gradle, SBT or Ant/Ivy.
- nuget.org-proxy: This proxy repository accesses the NuGet Gallery. It is the default component repository used by the nuget package management tool used for .Net development.

As of this publication, the following proxy repositories are also available for user configuration:

- Bower
- Docker
- npm
- PyPI
- Raw
- RubyGems
- Yum

## Hosted Repositories
A hosted repository is a repository that stores components in the repository manager as the authoritative location for these components. For example, create a hosted repository when you have internal components that aren’t downloaded from a public repository, but are used by various development teams in your organization.

By default, the repository manager ships with the following configured hosted repositories:

- maven-releases: This hosted repository uses the maven2 repository format with a release version policy. It’s intended to be the repository where your organization publishes internal releases. You can also use this repository for third-party components that aren’t available in external repositories.
- maven-snapshots: This hosted repository uses the maven2 repository format with a snapshot version policy. It’s intended to be the repository where your organization publishes internal development versions, also known as snapshots.
- nuget-hosted: This hosted repository is where your organization can publish internal releases in repository using the NuGet repository format. You can also use this repository for third-party components that are not available in external repositories that could potentially be proxied to gain access to the components.

As of this publication, the following hosted repositories are also available for user configuration:

- Bower
- Docker
- Git LFS
- npm
- PyPI
- Raw
- RubyGems

## Snapshot and Release Subtypes
Within the hosted repository type, there is a subtype of release or snapshot for the maven2 format. Similar to the difference between a production environment and a staging environment, we recommend using a release repository for stable components in production and a snapshot repository for components still in the development phase. While there is a higher level of procedure and ceremony associated with deploying to a release repository, snapshot releases can be deployed and changed frequently without regard for stability concerns.


## Group Repositories
A repository group  is a collection of other repositories, where you can combine multiple repositories of the same format into a single item. This represents a powerful feature of Nexus Repository Manager that lets developers rely on a single URL for their configuration needs. For example, if your group has a Maven Central proxy repository and a hosted repository for 3rd party JARs, these can be combined into a group with one URL for builds.

The repository manager ships with the following groups:

- maven-public: This is a repository group of maven2 formatted repositories. It combines the external proxy for the Central Repository, along with the hosted repositories maven-releases and maven-snapshots. 
- nuget-group: This group combines the NuGet formatted repositories nuget-hosted and nuget.org-proxy into a single repository for your .NET development with NuGet.

As of this publication, the following group repositories are also available for user configuration:

- Bower
- Docker
- npm
- PyPI
- Raw
- RubyGems
