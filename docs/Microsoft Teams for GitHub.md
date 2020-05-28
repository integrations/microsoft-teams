The GitHub integration for Microsoft Teams gives you and your teams full visibility into your GitHub projects right in Teams channels, where you generate ideas, triage issues and collaborate with other teams to move projects forward. This integration isbuilt and maintained by GitHub.

You can subscribe to an Organization or Repository's activity using `@github subscribe <organization>/<repository>`. 
<p align="center"><img width="500" alt="Subscribe" src="images/Subscribe.PNG"></p>

After the app is installed, and once you've subscribed to your Organization or Repository, you will start receiving notificiations for the following activities as rich text in your channels.
- `issues` - Opened, closed and reopened issues
- `pulls` - New or merged pull requests

<p align="center"><img width="500" alt="Issue" src="images/Issue.PNG"></p>
<p align="center"><img width="500" alt="PR" src="images/PR.PNG"></p>

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
