# CI-CD-Project-2-Demo

# This collection calls Google Analytics Reporting API to query the report and post to #Slack. 

# Notes: You do need an active Google Analytics Client Account to define User Type Internal or External. 

# Step 1
You need to set up a project with Google APIs console. Under Credentials, follow this workflow: click Create credentials ==> choose OAuth client ID ==> select Web application -> fill -> fill with https://www.getpostman.com/oauth2/callback ==> click Create ==> save the Client ID and Client secret in a safe place.

# Step 2
Go to this collection in Postman, under the Auth tag, follow this workflow: choose OAuth 2.0 from the Type dropdown list ==> click Get New Access Token ==> fill Auth URL with https://accounts.google.com/o/oauth2/v2/auth?access_type=offline -> fill Access Token URL with https://www.googleapis.com/oauth2/v4/token -> fill Client ID with the client ID you got above -> fill Client Secret with the client secret you got above -> fill Scope(Optional) with https://www.googleapis.com/auth/analytics.readonly -> select Authorization Code from the dropdown list -> check Request access token locally -> click Request Token
Save the refresh_token in a safe place (Important !)
Save the access_token and use it in the next couple minutes.

# Step 3
If you forgot to save the refresh_token for the first time you send the request, you won't be able to get the refresh_token again. Here's what you need to do: go to Google Sign-in & security ==> scroll down to Connected apps & sites and click MANAGE APPS ==> click on your project ==> click REMOVE ==> click Request Token in Postman again

# The concept works the same for Adobe Analytics. However, you do need a licensed account with an actual Adobe Access-Token. 
