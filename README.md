# FarmBuild Developer Guide
The FarmBuild services are composed of a set of web service and open source code APIs developed by DEDJTR for use in third party agricultural software systems.<br/>

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [FarmBuild Developer Guide](#farmbuild-developer-guide)
  - [Registration](#registration)
  - [GitHub Repository Structure](#github-repository-structure)
  - [Examples vs API](#examples-vs-api)
  - [FarmBuild components include:](#farmbuild-components-include)
    - [FarmBuild Core](#farmbuild-core)
    - [FarmData](#farmdata)
    - [Web Mapping](#web-mapping)
    - [Dairy Nutrient Calculator](#dairy-nutrient-calculator)
    - [Soil Sample Importer](#soil-sample-importer)
    - [Web Service APIs and associated data sources](#web-service-apis-and-associated-data-sources)
  - [Technology Stack](#technology-stack)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## Registration
The FarmBuild APIs are open source and can be accessed through GitHub.  The Web services and associated data sources are published from a DEDJTR server and registration is required to use these.<br/>
DEDJTR requests that all users to register their interest in using FarmBuild components to enable DEDJTR to provide better support and planning for future releases.<br/>
To register please visit FarmBuild main website at:<br/>
http://farmbuild.github.io/farmbuild/farmbuild_registration.html

## GitHub Repository Structure
Going through the FarmBuild components, you will see that all components have a standard project structure, inspired by JavaScript community conventions. To briefly describe the project structure, it includes:
 - "src" folder: contains all source files. The distribution (ie compiled) version of the APIs are generated from the source via a build process.
 - "dist" folder: contains the production ready version of the API libraries that you can use in your applications.
 - "docs" folder: contains API documentation of the component.
 - "lib" folder: contains external libraries used in the component.
 - "examples" folder: contains a series of example pages to demonstrate how to use the component's API. Examples have mainly been created using AngularJS JavaScript library, which is described in the "Technology Stack" section of this document, althugh a JQuery example is also provided for the Nutrient Calculator component.
  
 
At the root level of the project you will find a bunch of files. Some of them are concerned with the project's build proccess and the project's development. One that requires your careful attention is the LICENSE file which describes the conditions under which you may use FarmBuild components. Please read it carefully before you start using FarmBuild.


## Examples vs API
We often use the terms API and Example when describing different components.
To clarify further, APIs are the main delivery of the FarmBuild components. It is expected that you as a third party software developer will read through API docs and find the proper API to support your desired use. APIs are not meant to be altered by third parties unless in the future you wish to work with DEDJTR to extend the API.<br/>
If you believe there are issues with any part of the APIs or you need a specific type of functionality which is nice to addd to the APIs, please report that through the GitHub "Issues" page which you will find in each repository. The FarmBuild team will respond to the issues.<br/>
Each FarmBuild component is accompanied by a series of examples which demonstrate how you can to consume web services and call the APIs. These examples are meant to be for demonstration purposes only ie they do not deliver working applications, although you may choose to use the example code as a "kick starter". You can look at example source code to get an idea of how to use FarmBuild components in your project.<br/>

## FarmBuild components include:

### FarmBuild Core
FarmBuild Core provides Common functions used in other FarmBuild components.<br/>
These functions include Google Analytics integration and the collection API and validation module. It is primarily an internal dependency in higher level components such as Dairy Nutrient Calculator, Web Mapping and FarmData.<br/>
Some of its APIs, such as Google Analytics, are exposed as part of the higher level components' API.<br/>
 To understand more about the FarmBuild Core please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-core" target="_blank"> https://github.com/FarmBuild/farmbuild-core</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-core/master/docs/farmbuild-core/1.0.41/index.html" target="_blank"> https://rawgit.com/FarmBuild/farmbuild-core/master/docs/farmbuild-core/1.0.41/index.html</a>

### FarmData
 To facilitate the exchange of information between FarmBuild applications and other on-line environments a standard farm data block has been established which stores all data used and generated by the FarmBuild applications within a simple JSON structure.<br/>
 To understand more about FarmData please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-farmdata" target="_blank">https://github.com/FarmBuild/farmbuild-farmdata</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-farmdata/master/docs/farmbuild-farmdata/1.1.4" target="_blank">https://rawgit.com/FarmBuild/farmbuild-farmdata/master/docs/farmbuild-farmdata/1.1.4/index.html</a>

### Web Mapping
Web Mapping is an open source farm mapping API javascript library. A demonstration page is provided as part of the examples in the web mapping repository which shows how users or developers can map and access spatial farm data for applications both within FarmBuild API's and their own environment.<br/>
 To understand more about Web Mapping please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-web-mapping" target="_blank"> https://github.com/FarmBuild/farmbuild-web-mapping</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-web-mapping/master/docs/farmbuild-web-mapping/1.1.0/index.html" target="_blank">https://rawgit.com/FarmBuild/farmbuild-web-mapping/master/docs/farmbuild-web-mapping/1.1.0/index.html</a>

### Dairy Nutrient Calculator
This JavaScript library can be used to model nutrient flow in and out of a dairy farm. Since Australian dairy farms generally import larger quantities of nutrients than they export, knowing the nutrient balance of a farm gives farmers the potential to improve the efficiency of their operations and potentially save money.<br/>
 To understand more about Web Mapping please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-dairy-nutrient-calculator" target="_blank"> https://github.com/FarmBuild/farmbuild-dairy-nutrient-calculator</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-dairy-nutrient-calculator/master/docs/farmbuild-dairy-nutrient-calculator/1.0.0/index.html" target="_blank">https://rawgit.com/FarmBuild/farmbuild-dairy-nutrient-calculator/master/docs/farmbuild-dairy-nutrient-calculator/1.0.0/index.html</a>

### Soil Sample Importer
To further support nutrient management on-farm, a soil import API Javascript library and demonstration page has been developed to enable the import, linking and nutrient status classification of soil test data to the farm paddock structure, such as is generated by the web mapping component.<br/>
 To understand more about Soil Sample Importer please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-soil-sample-importer" target="_blank"> https://github.com/FarmBuild/farmbuild-soil-sample-importer</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-soil-sample-importer/master/docs/farmbuild-soil-sample-importer/1.0.0/index.html" target="_blank">https://rawgit.com/FarmBuild/farmbuild-soil-sample-importer/master/docs/farmbuild-soil-sample-importer/1.0.0/index.html</a>

### Web Service APIs and associated data sources
The web services and associated data sources are published from a DEDJTR server. The web services are available to access from the GitHub ‘FarmBuild’ account. They are provided with an agreed service level, but the source code is not published.<br/>
You can find an example of how to access these web services by going through examples found in the Web Services Demo GitHub repository.<br/>
https://github.com/FarmBuild/farmbuild-web-services-demo

  Web services include:

    - Web Feature Services<br/>
      - Soils of the Goulburn Murray Irrigation Region
      - Victorian Rural Parcel Agricultural Land Use
  
    - Soil Information Services
      - Soils Area Calculation Services<br/>
        This service will return calculated areas of soil types in the Goulburn Murray Irrigation Region for a defined area (ie. Farm or paddock boundary)
  
## Technology Stack
The FarmBuild components use a range of client-side and server-side technologies.<br/>
On the client-side, the FarmBuild APIs use the AngularJS framework to provide a modular architecture and to enable good separation between different modules. <br/>

AngularJS is a structural framework for dynamic web apps. It lets you use HTML as your template language and lets you extend HTML's syntax to express your application's components clearly and succinctly. Angular's data binding and dependency injection eliminate much of the code you would otherwise have to write.<br/>
To read more about AngularJS please visit the following links:<br/>
- <a href="https://docs.angularjs.org">https://docs.angularjs.org</a>

All of the Farmbuild Javascript APIs are available as AngularJS modules.<br/>
You are however <b>not</b> forced to use the AngularJS framework in your application in order to use the FarmBuild APIs. 
The Farmbuild Javascript APIs are also available via the farmbuild global name space. (eg `farmbuild.webmapping`) and in the case of Diary Nutrient Calculator in addition to AngularJS examples there are a full series are examples available which use JQuery to demonstrate API usage.<br/>

Apart from AngularJS, FarmBuild also uses the OpenLayers3 and Turf.js Javascript libraries in the Web Mapping component to provide map display and vector editing tools. For developers to be able to effectively make use of the Web Mapping component in their applications, they will need to have a good understanding of OpenLayers3.<br/>
To read more on these libraries please visit to following links:<br/>
- <a href="http://openlayers.org/">OpenLayers: http://openlayers.org/</a><br/>
- <a href="http://turfjs.org/">TURF: http://turfjs.org/</a>
