# GitHub + Microsoft Teams Integration

> **Heads Up!** The GitHub and Microsoft Teams app is in Alpha (private preview) 

## About

GitHub is worlds leading software developement platform. [Microsoft Teams](https://products.office.com/microsoft-teams/group-chat-software) is one of the best communication platforms where modern developers come together, collaborate trying to build world class products and services.

Today, developers spend considerable amount of time communicating with the team, monitoring the issues, pull requests and deployment statuses. This necessitates constant switching of context between GitHub and Microsoft Teams (collaborate). ChatOps is a team and collaboration centric way of working where in people, conversations, tools, and files are ensembled in one place i.e. workplace messaging apps.

The GitHub integration for Microsoft Teams gives you and your teams full visibility into your GitHub projects right in Teams channels, where you generate ideas, triage issues and collaborate with other teams to move projects forward. This integration is built and maintained by GitHub.

## Table of Contents
- [Installing the GitHub integration for Teams](#installing-the-github-integration-for-teams)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Connect to your GitHub account](#Signin)
  - [Subscribing and Unsubscribing](#subscribe)
  - [Command Reference](#commands)
  - [Authorization](#authorization)
- [Need help?](#questions-need-help)
- [License](#license)
--------
## Installing the GitHub integration for Teams
### Requirements
This app officially supports GitHub.com and Teams.microsoft.com.

### Installation
Download the [manifest]() and upload it as a custom app and install it in the team of your choice. 

 <p align="center"><img width="500" alt="Add as custom app" src="images/Uploadmanifest.png"></p>
 <p align="center"><img width="500" alt="welcome message" src="images/success.PNG"></p>

Upon installing, a welcome message is displayed as shown in the following image. Use the ``@GitHub`` handle to start interacting with the app.
 
 
### Connect to your GitHub account
 
At this point, your Teams and GitHub user accounts are not linked. To link the two accounts, authenticate to GitHub using a `@github signin` command.
<p align="center"><img width="500" alt="Signin" src="images/Signin.PNG"></p>
<p align="center"><img width="500" alt="Connect to GitHub" src="images/ConnectGitHub.PNG"></p>
<p align="center"><img width="500" alt="Authorize" src="images/Authorize.PNG"></p>
<p align="center"><img width="500" alt="Finish Signin" src="images/FinishSignin.PNG"></p>

### Subscribing and Unsubscribing
You can subscribe to an Organization or Repository's activity using `@github subscribe <organization>/<repository>`. 
<p align="center"><img width="500" alt="Install" src="images/Install.PNG"></p>

Before you subscribe, a Microsoft Teams app needs to be installed in GitHub. 
<p align="center"><img width="500" alt="Teams App for GitHub" src="images/TeamsAppForGitHub.PNG"></p>

If you originally gave the app access to "All repositories" and you've created a new private repository on GitHub after installing the GitHub integration for Teams, the `@github subscribe` command will work automatically on your new repository. If you installed the app on a subset of repositories, the app will prompt you to install it on the new repository.
<p align="center"><img width="500" alt="Subscribe" src="images/Subscribe.PNG"></p>

After the app is installed, and once you've subscribed to your Organization or Repository, you will start receiving notificiations for the following activities as rich text in your channels.
- `issues` - Opened, closed and reopened issues
- `pulls` - New or merged pull requests

<p align="center"><img width="500" alt="Issue" src="images/Issue.PNG"></p>
<p align="center"><img width="500" alt="PR" src="images/PR.PNG"></p>

In the future releases we will add support for commits, PR Checks, releases and also provide ability to customize the notifications at feature level for each repository.

The `@github` command also supports `unsubscribe`. To unsubscribe to notifications from a repository, use `@github unsubscribe <organization>/<repository>`
<p align="center"><img width="500" alt="UnSubscribe" src="images/UnSubscribe.PNG"></p>

You can view all the subscriptions available on the channel using `@github subscribe list`
<p align="center"><img width="500" alt="Subscribe list" src="images/subscribelist.PNG"></p>


### Command reference

The following table lists all the commands you can use in your Microsoft Teams channel.

|Command	| Functionality |
| -------------------- |----------------|
| @github signin	| Connect to your GitHub Account |
| @github signout	| Disconnect with your GitHub Account and remove all subscriptions |
| @github subscribe <organization>/<Repository>	| Subscribe to and Organization or Repository |
| @github subscribe list	| List the subscriptions in the channel |
| @github unsubscribe <Organization>/<Repository>	| Unsubscribe from Organization or Repository |

### Authorization
By granting the app access, you are providing the following authorizations to your GitHub and Microsoft Teams accounts:

#### Teams Permission Scopes

|Permission scope|Why we need it|
|---|---|
|Access private conversations between you and the App | To message you with instructions.  |
|Add link previews to GitHub.com to messages| To render rich links to `github.com`|
|Add github commands| To add the `@github` command to your Team channels |
|View the organization's name, email domain, and icon| To store subscriptions you set up|
|Post messages as the app| To notify you of activity that happens on GitHub|

#### GitHub Permission Scopes

|Permission scope|Why we need it|
|---|---|
|Read access to issues, metadata, pull requests, and repository projects | To render previews of links shared in Teams|


## Questions? Need help?
Please fill out GitHub's [Support form]('') and your request will be routed to the right team at GitHub.

## License
When using the GitHub logos, be sure to follow the [GitHub logo guidelines](https://github.com/logos).
