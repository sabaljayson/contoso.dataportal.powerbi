# What is this?
This project is a sample to show how to implement Power BI embedded features within a web site with TypeScript. More specifically, this sample show:
- Azure AD App Authentication
- Embed of Tiles and Reports (on a specific tab)
- Dynamic filters
- Menu Command Extensions

This development is mainly based on [Microsoft/PowerBI-JavaScript](https://github.com/Microsoft/PowerBI-JavaScript/) and [HNeukermans/adal-ts](https://github.com/HNeukermans/adal-ts)

# What does it look like?
## Main view
![](https://github.com/aurelienprevotMVP/contoso.dataportal.powerbi/blob/master/wiki/screenshot1.png)
<br /><br />

## Filters
<img src='https://github.com/aurelienprevotMVP/contoso.dataportal.powerbi/blob/master/wiki/filters1.png' width=400 height=300 /><br /><br />

## Menu Command Extensions
<img src='https://github.com/aurelienprevotMVP/contoso.dataportal.powerbi/blob/master/wiki/command2.png' width=400 height=200 /><br />
Note that if you click on this, the code will populate a contact form at the bottom of the page.<br /><br />

<img src='https://github.com/aurelienprevotMVP/contoso.dataportal.powerbi/blob/master/wiki/command1.png' width=400 height=275 />

<br /><br />
# How to install it?

1. In the Power BI Portal (https://app.powerbi.com), create a Power BI workspace
1. Import `pbix-sample/Sales Management Demo.pbix` file within the Power BI workspace
1. Create an Azure AD Application and set `https://localhost:8008/dist/index.htm` as response URL
1. Download the code
1. Run `npm install`
1. Change `node-modules/powerbi-client/dist/powerbi-client.d.ts` line 1129 `detail:T` to `detail:any`. 
This is a bug fix I have shared with the owner of the Power BI Javascript library, but not fixed yet
1. Change values in src/constsMain.ts
1. Run `webpack -R` and/or `npm start` (that will run webpack-dev-server)

