## application-insights-spo

This Application Customizer demonstrates how we can use Azure Application Insights client-side SDK to track pageviews and authenticated context in SharePoint Online modern pages.

### Building the code

```bash
git clone the repo
npm i
npm i -g gulp
gulp
```

This package produces the following:

* lib/* - intermediate-stage commonjs build artifacts
* dist/* - the bundled script, along with other resources
* deploy/* - all resources which should be uploaded to a CDN.

### Build options

gulp clean
gulp test
gulp serve
gulp bundle --ship
gulp package-solution --ship

#### PowerShell
Add-PnPCustomAction -ClientSideComponentId "df26cdf9-bffd-494f-92df-d9b1cc700d9d" -Name "AzureAnalytics" -Title "AzureAnalytics" -Location ClientSideExtension.ApplicationCustomizer -ClientSideComponentProperties: '{"testMessage":"Azure Insight"}' -Scope Site

