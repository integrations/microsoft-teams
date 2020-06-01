# GitHub + Microsoft Teams Integration (Private Preview)

## About

GitHub is worlds leading software developement platform. [Microsoft Teams](https://products.office.com/microsoft-teams/group-chat-software) is one of the best communication platforms where modern developers come together, collaborate trying to build world class products and services.

Today, developers spend considerable amount of time communicating with the team, monitoring the issues, pull requests and deployment statuses. This necessitates constant switching of context between GitHub and Microsoft Teams (collaborate). ChatOps is a team and collaboration centric way of working where in people, conversations, tools, and files are ensembled in one place i.e. workplace messaging apps.

The GitHub integration for Microsoft Teams gives you and your teams full visibility into your GitHub projects right in Teams channels, where you generate ideas, triage issues and collaborate with other teams to move projects forward. 

This integration is built and maintained by GitHub.

## Table of Contents
- [Installing the GitHub integration for Teams](#installing-the-github-integration-for-teams)
  - [Requirements](#requirements)
  - [Installation](#installation)
 - [Get Started](#get-started) 
   - [Connect your GitHub account](#Connect-your-github-account)
   - [Subscribing and Unsubscribing](#Subscribing-and-Unsubscribing)
   - [Notifications](#Notifications)
   - [Command Reference](#commands)
   - [Authorization](#authorization)
- [Limitations](#limitations)
- [Future work](#future-work)
- [Feedback](#Feedback-and-queries)
- [License](#license)
--------
## Installing the GitHub integration for Teams
### Requirements
This app officially supports GitHub.com and Teams.microsoft.com.

### Installation
Download the [manifest](raw/master/blob/manifest.zip) and upload it as a custom app and install it in the team of your choice. 

 <p align="left"><img width="500" alt="Add as custom app" src="images/Uploadmanifest.png"></p>
 <p align="left"><img width="500" alt="welcome message" src="images/success.PNG"></p>

Upon installing, a welcome message is displayed as shown in the following image. Use the ``@GitHub`` handle to start interacting with the app.
 
## Get Started 
### Connect your GitHub account
 
At this point, your Teams and GitHub user accounts are not linked. To link the two accounts, authenticate to GitHub using a `@github signin` command or clicking on the 'Connect GitHub account' button and authorize the app. 
<p align="left"><img width="500" alt="Signin" src="images/Signin.PNG"></p>
<p align="left"><img width="500" alt="Connect to GitHub" src="images/ConnectGitHub.PNG"></p>
<p align="left"><img width="500" alt="Authorize" src="images/Authorize.PNG"></p>
<p align="left"><img width="500" alt="Finish Signin" src="images/FinishSignin.PNG"></p>

### Subscribing and Unsubscribing
You can subscribe to get notifications for pull requests and issues for an Organization or Repository's activity using `@github subscribe <organization>/<repository>` command. 
<p align="left"><img width="500" alt="Install" src="images/Install.PNG"></p>

Before you subscribe, a Microsoft Teams app needs to be installed in GitHub. 
<p align="left"><img width="500" alt="Teams App for GitHub" src="images/TeamsAppForGitHub.PNG"></p>

If you originally gave the app access to "All repositories" and you've created a new private repository on GitHub after installing the GitHub integration for Teams, the `@github subscribe` command will work automatically on your new repository. If you installed the app on a subset of repositories, the app will prompt you to install it on the new repository. Note: You need to be an organization / account owner to install the app.  

<p align="left"><img width="500" alt="Subscribe" src="images/Subscribe.PNG"></p>

The `@github` command also supports `unsubscribe`. To unsubscribe to notifications from a repository, use `@github unsubscribe <organization>/<repository>`
<p align="left"><img width="500" alt="UnSubscribe" src="images/UnSubscribe.PNG"></p>

You can view all the subscriptions available on the channel using `@github subscribe list`
<p align="left"><img width="500" alt="Subscribe list" src="images/subscribelist.PNG"></p>

## Notifications
After the app is installed, and once you've subscribed to your Organization or Repository, you will start receiving notificiations for the following activities as rich text in your channels.
- `issues` - Opened, closed and reopened issues
- `pulls` - New, merged and closed pull requests

<p align="left"><img width="500" alt="Issue" src="images/Issue.PNG"></p>
<p align="left"><img width="500" alt="PR" src="images/PR.PNG"></p>

In the future releases we will add support for commits, PR Checks, releases and also provide ability to customize the notifications at feature level for each repository or organization.

### Command reference

The following table lists all the commands you can use in your Microsoft Teams channel.

|Command	| Functionality |
| -------------------- |----------------|
| @github signin	| Connect to your GitHub Account |
| @github subscribe <organization>/<Repository>	| Subscribe to and Organization or Repository |
| @github subscribe list	| List the subscriptions in the channel |
| @github unsubscribe <Organization>/<Repository>	| Unsubscribe from Organization or Repository |
| @github signout	| Disconnect with your GitHub Account and remove all subscriptions |

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

## Limitations
Being a private preview, the app has certain limitations as detailed below. We will continue to invest in the app to remove some of these constraints.

* The app needs to be sideloaded and is not avaialble in Teams app store as we are in private preview.
* Markdown is not extensively supported in Teams currently so some styles like checkboxes, blockquotes might not be rendered properly. Request you to share issues found so that we can improve the experience.  

## Future work
We’re constantly at work to improve the app, and soon you’ll see new features stated below. If you would like to see additional capabilities please [request a feature](https://github.com/integrations/microsoft-teams/issues/new).  

* Actions for Issues and PR
* Additional notification and ability to filter 
* @mention support
* URL unfurling

## Feedback and queries
Please [file an issue](https://github.com/integrations/microsoft-teams/issues/new) and we will get back to you. 

## License
When using the GitHub logos, be sure to follow the [GitHub logo guidelines](https://github.com/logos).
