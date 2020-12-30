# 300 Repository Planning Checklist

## Plan Your Organization’s Repo
Before installation, it’s a good idea to lay out the various ways a repository manager could be used and configured in your organization. Determining the answers to these questions will help plan a successful implementation of Nexus Repository Manager. 

- Determine the number of employees using Nexus Repository Manager. (This will affect permission models)
- Determine how user accounts are managed in your organization. (For example LDAP, Crowd, etc.)
- Decide the number of Repository Manager installations needed by your organization. (For example, globally dispersed teams will need more than one installation – even if the teams are small)
- Decide where repositories will be located. (Location is determined by placement of teams and resources)
- Determine which source control management tools are used in your organization. (For example, GIT, Subversion, etc.)
- Determine which build tools are used in your organization. (For example, Jenkins, Bamboo, etc.)
- Determine the languages used in your organization. (For example Java, Python, JavaScript, etc.)
- Determine which package formats are used in your organization. (For example Maven Central, NuGet, npm, etc.)
- Determine language and package formats anticipated for future use. (Will you need access to additional languages or formats for future development?)
- Determine which public repositories are accessed by your team. (For example Maven Central, NuGet, npm, etc.)
- Determine if your team plans to host components. (For example internal components accessed on non-public repositories)
- Determine if multiple hosted repositories are needed.  (This is useful when you have multiple teams that don’t share all components)
- Determine the number of applications managed in your organization. (The amount of applications used or produced by your development team)
- Determine the gateway used for external OSS and commercial components. (The approach your team uses for open source and proprietary components)
- Determine the amount and location of storage needed for internal components. (For more information, see Nexus Repository Manager System Requirements) 
- Determine the amount and location of storage needed for build output. (For more information, see Nexus Repository Manager System Requirements)

## Download the Repository Planning Worksheet
In addition to the checklist, we’ve provided [a repository planning worksheet](http://learn.sonatype.com/wp-content/uploads/2020/04/Repository_Manager_Planning_Worksheet.pdf) available for PDF download.
