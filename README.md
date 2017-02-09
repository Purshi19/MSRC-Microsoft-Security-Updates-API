# Welcome
This project serves to help developers quickly start processing data from the Microsoft Security Updates API (https://portal.msrc.microsoft.com/en-us/developer)

It is comprised of two main components, Documentation and example code.

**The documentation** (in the form of swagger documentation) can be used to help developers who wish to implement their own API requests / response handling to get the correct responses and fields. For more information check out http://swagger.io It is a great project and has great staff working on it. To view the API, you can open the [swagger-ui demo](http://petstore.swagger.io/) and put the link to the raw swagger.json in the top bar then click explore. swagger-ui can be downloaded locally and ran if you need to integrate this into how you interact with the api.

*as a note about the swagger, there are two response models defined for the CVRF endpoint. one for json and the other for xml. please swap out the return definition line as necessary* 

**The sample code** serves as an example on how to interact with the API. Currently, the sample code consists of one PowerShell project, however more languages may be provided in the future. In the PowerShell project, you will see three small functions that show how to interact with the API, as well as two larger functions that may facilitate automation and reporting on the most common data needed.

The function `getAffectedProducts` will build an array of PowerShell objects that contain the most commonly used fields, such as affected product name, ID, CVE name, description of the vulnerability, CVSS score information, links to knowledge base articles and downloads, and lastly a list of updates that supersedes the update links given. This function is not all encompassing of the data returned by the API, however other fields are easy to add if needed.

the function `generateReport` serves as an example of how you can build more traditional Microsoft security reports from the data surfaced by the API. This function will build a document, report.html, in the same directory as the PowerShell project. Most of the html elements used are put into html template variables, which are then filled in with string formatting. This is to allow easy modification of the report output. It is important to note that the example report generated by default simply formats the data given by the API into a html document. No data processing or pruning is being done, thus the reports will tend to be long and verbose. It is up to you to decide how to process the data. This is more of an example to show the possibilities of what can be done with the api, and how you may want to use it.


# Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

It is Microsoft’s mission to empower every person and every organization on the planet to achieve more. We thank you for helping shape that future by keeping the world a more secure place by tooling security into your organization’s practices. We would love to hear your feedback on features to add or bugs to fix.
