# akamai-cloudzero

This script pulls your Akamai billing data using the Akamai Billing APIs and packages the results into dataframes that are converted into [CBF](https://docs.cloudzero.com/docs/anycost-common-bill-format-cbf) and uploaded to CloudZero.

## Environment Variables
This requires five variables to be set in the environment. 

* APIVERSION - This is just the API version for the Akamai API and should be set to `v4` as of this release
* TOKEN - This is your Akamai personal access token. This needs read access to your Akamai billing and nothing else.
* CZID - This is the CloudZero AnyCost custom integration Connection ID. Example: `b03586e3-fec9-654f-a02e-a47788f14f08`
* CZKEY - Your CZ API key
* DAYS - Number of days from today that you want to include in billing Example: `30`

