# Secert Server Postman Collections

[![Professional Services](https://img.shields.io/badge/Professional%20Services-supported-informational?style=for-the-badge)]()

This repository holds the collection and the environment variable JSON files to import into Postman.

The collection allows you to test the Secret Server APIs from within Postman. This collection will work against both Secret Server (on-premises) and Secret Server Cloud.

Support covers using the OAuth2 authentication and tries to simplify your ability to get started fast with testing and discovery of the Secret Server API.

# Setup

To setup the Postman collections follow these steps:

1. Download/register for [Postman](https://www.getpostman.com/).
2. Click **File | Import ...**
3. Select **Import From Link**.
4. Past the following two URLs and click Import after each.

```
To be populated once we publish to GitHub, these will be the raw GitHub URL for both json files
```

You should now see the `Secret Server` collection on the left hand side Collections pane.

5. Click on the **No environment** drop down in the top right hand corner of Postman.
6. Select **Secret Server environment**
7. Click the **eye** icon to the right and then click **Edit**.
8. Enter in the **current** values (_do not alter the initial values_) for each variable specific to your environment: **SecretServerUrl**, **UserName**, **UserPassword**
9. Select **Update**. CLose the **Manage Environments** dialog.
10. Expand the folder **Start Here**, click on the **Get Access Token using OAuth2**. Click the **Send** button on right hand side.
11. Expand the folder **active-directory | domains**, click on **Get Domain**. Click the **Send** button.

## Troubleshooting Postman

If you are using this collection against your internal or local Secret Server lab you may see an initial error like this when you try to retrieve an access token:

![postman initial error](/images/postman-initial-error.png)

If you show the Postman console (`ATL + CTRL + C` or _View | Show Postman Console_) you will see this message to indicate the SSL certificate for your web service cannot be validated:

![postman error](/images/postman-settings-ssl-cert-verification-log-entry.png)

To fix this you need to go into your settings for Postman (`CTRL + comma` or _File | Settings_) and toggle off the setting **SSL certificate verification**.

![postman cert verification error](/images/postman-settings-ssl-cert-verification.png)