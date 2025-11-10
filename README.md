# akamai-cloudzero

This script pulls your Akamai billing data using the Akamai Billing APIs and packages the results into dataframes that are converted into [CBF](https://docs.cloudzero.com/docs/anycost-common-bill-format-cbf) and uploaded to CloudZero.

## Environment Variables
This requires five variables to be set in the environment. 

* APIVERSION - This is just the API version for the Akamai API and should be set to `v4` as of this release
* TOKEN - This is your Akamai personal access token. This needs read only access to your Akamai "Account" and nothing else.
* CZID - This is the CloudZero AnyCost custom integration Connection ID. Example: `b03586e3-fec9-654f-a02e-a47788f14f08`
* CZKEY - Your CZ API key
* DAYS - Number of days from today that you want to include in billing Example: `30`

## CloudZero Setup
Go to your CZ settings, select Cloud Integrations, Add Connections (upper right - red button) and then Custom
![Screenshot 2025-11-10 at 10 29 18 AM](https://github.com/user-attachments/assets/4dccb006-66c9-4438-8ca1-191882a7f281)

Select the REST API option
![Screenshot 2025-11-10 at 10 40 53 AM](https://github.com/user-attachments/assets/8b79eb35-b21b-421a-a882-f587bebed37f)

Provide names that are meaningful to you and your org
![Screenshot 2025-11-10 at 10 42 33 AM](https://github.com/user-attachments/assets/03a858d2-1736-4311-87d5-5228312af87c)

Click the connection you just created in the list. The "Connection ID" is used in the `CZID` environment variable mentioned above
![Screenshot 2025-11-10 at 10 43 28 AM](https://github.com/user-attachments/assets/16636f7e-ae61-4cd1-b9a6-b70cb76630d9)
