# FarmBuild
The FarmBuild services are composed of an initial series of web service and open source code API’s developed by DEDJTR for consumption in third party systems.<br/>

##### Table of Contents
  - [Registration](#registration)<br/>
  - [Repositories Structure](#repositories-structure)<br/>
  - [Examples vs API](#api-vs-examples)<br/>
  - [FarmBuild Components](#farmBuild-components)
     - [FarmBuild Core](#farmBuild-core)
     - [Web Mapping](#web-mapping)
     - [Dairy Nutrient Calculator](#dairy-nutrient-calculator)
     - [Soil Sample Importer](#soil-sample-importer)
     - [Web service API’s and associated data sources](web-service)
  - [Technology stack](#technology-stack)


**<a name="registration">Registration</a>**<br/>
Except for the Web service API’s and associated data sources which registration is mandatory in order to get 'CLIENT ID' and a CLIENT SECRET', other APIs are open source and can be accessed through github.<br/>
At the same time DEDJTR strongly advises users to register their interest in using FarmBuild components in order for DEDJTR to provide better support and planning for future releases.<br/>
To register please visit FarmBuild main website at:<br/>
http://farmbuild.github.io/farmbuild/farmbuild_registration.html

**<a name="repositories-structure">Repositories Structure</a>**<br/>
Going through FarmBuild components, you will find out all components have a standard project structure which is inspired by JavaScript community conventions. To briefly describe the project structure, it includes:
 - "src" folder: containes all the source files. Distribution version of the apis are generated from the source via a build process.
 - "dist" folder: contains the production ready version of the libs that you can use in other applications.
 - "docs" folder: contains api documentaion of the component.
 - "lib" folder: contains external libraries used in the component.
 - "examples" folder: contains a series of example pages to demonstrate component's api usage. Examples are created using AngularJS JavaScript library, which is describe in the "technology stack" section of this document.
  
 
At the root level of the project you will find a bunch files. Some of them are concerned with the project's build proccess and project's development. The one that needs your attention is the LICENSE file which describes the condition under which you may use FarmBuild components. So please carefully read it before you start using FarmBuild.


**<a name="api-vs-examples"/>Examples vs API</a>**<br/>
We often use API and Example terms while describing different components.
To clarify further APIs are meant to be the main delivery on FarmBuild components. It is expected that you as a third party company/software developer will read through API docs and find the proper API to support your desired user story. APIs are not meant to be altered third parties.<br/>
If you believe there are issues in any part of APIs or you need specific type of functionality which is nice to addd to the APIs, please report that through github "issues" which you will find in each repository. FarmBuild team will respond to the issues and you will be able to track the proccess via the issues section.<br/>
Each FarmBuild component is accompanied by a series of examples which demonstrate ways to consume services and APIs. These examples are meant to be for demonstration purpose only. You can look at source codes to get an idea how to use FarmBuild components in your project.<br/>
Also you are welcome to use them as a base for your projects.


**<a name="farmBuild-components">FarmBuild components</a>** include:

- **<a name="farmBuild-core">FarmBuild Core</a>** <br/>
FarmBuild Core provides Common functionalities used in FarmBuild components.<br/>
These functionalities include google analytic, collection api and validation module. It is primarily used as an internal dependency in higher level components such as: Dairy Nutrient Calculator, Web Mapping and FarmData.<br/>
Some of its apis, like google analytics, are exposed as part higher level components' api.<br/>
 To understand more about FarmBuild Core please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-core" target="_blank"> https://github.com/FarmBuild/farmbuild-core</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-core/master/docs/farmbuild-core/1.0.41/index.html" target="_blank"> https://rawgit.com/FarmBuild/farmbuild-core/master/docs/farmbuild-core/1.0.41/index.html</a>

- **<a name="farmData">FarmData</a>** <br/>
 To facilitate the exchange of information between FarmBuild applications and other on-line environments a farm data block has been established which stores all data generated by the FarmBuild applications within a simple JSON structure.<br/>
 To understand more about FarmData please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-farmdata" target="_blank">https://github.com/FarmBuild/farmbuild-farmdata</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-farmdata/master/docs/farmbuild-farmdata/1.1.4" target="_blank">https://rawgit.com/FarmBuild/farmbuild-farmdata/master/docs/farmbuild-farmdata/1.1.4/index.html</a>

- **<a name="web-mapping">Web Mapping</a>** <br/>
Web Mapping is an open source farm mapping API javascript library. A demonstration page is provided as part of examples in web mapping repository that shows how users or developers can map and access spatial farm data for application both within FarmBuild API's and their own environment.<br/>
 To understand more about Web Mapping please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-web-mapping" target="_blank"> https://github.com/FarmBuild/farmbuild-web-mapping</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-web-mapping/master/docs/farmbuild-web-mapping/1.1.0/index.html" target="_blank">https://rawgit.com/FarmBuild/farmbuild-web-mapping/master/docs/farmbuild-web-mapping/1.1.0/index.html</a>

- **<a name="dairy-nutrient-calculator">Dairy Nutrient Calculator</a>** <br/>
This javaScript library can be used to model nutrient flow in and out of a dairy farms. Since Australian dairy farms generally import larger quantities of nutrients than they export, knowing the nutrient balance of a farm gives farmers the potential to save money.<br/>
 To understand more about Web Mapping please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-dairy-nutrient-calculator" target="_blank"> https://github.com/FarmBuild/farmbuild-dairy-nutrient-calculator</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-dairy-nutrient-calculator/master/docs/farmbuild-dairy-nutrient-calculator/1.0.0/index.html" target="_blank">https://rawgit.com/FarmBuild/farmbuild-dairy-nutrient-calculator/master/docs/farmbuild-dairy-nutrient-calculator/1.0.0/index.html</a>

- **<a name="soil-sample-importer">Soil Sample Importer</a>** <br/>
To further support nutrient management on-farm a soil import API javascript library and demonstration page has been developed to enable import, linking and nutrient status classification of soil test data to a farm paddock structure as generated by web mapping applications.<br/>
 To understand more about Web Mapping please visit following links:<br/>
 Git Repo: <a href="https://github.com/FarmBuild/farmbuild-soil-sample-importer" target="_blank"> https://github.com/FarmBuild/farmbuild-soil-sample-importer</a><br/>
 API doc: <a href="https://rawgit.com/FarmBuild/farmbuild-soil-sample-importer/master/docs/farmbuild-soil-sample-importer/1.0.0/index.html" target="_blank">https://rawgit.com/FarmBuild/farmbuild-soil-sample-importer/master/docs/farmbuild-soil-sample-importer/1.0.0/index.html</a>

- **<a name="web-service">Web service API’s and associated data sources</a>**<br/>
The web services and associated data sources will be served off DEDJTR infrastructure. The web services are available to access from the GitHub ‘FarmBuild’ account. They will be provided with an agreed service level, but the source code is not availabe.<br/>
You can find an example of how you can access these web services by going through examples found in the Web Services Demo github repository.<br/>
https://github.com/FarmBuild/farmbuild-web-services-demo

  Web services include:

    - Web Feature Services<br/>
      - Soils of the Goulburn Murray Irrigation Region
      - Victorian Rural Parcel Agricultural Land Use
  
    - Soil Information Services
      - Soils Area Calculation Services<br/>
        This service will return calculated areas of soil types in the Goulburn Murray Irrigation Region for a defined area (ie. Farm or paddock boundary)
  
      - Prototype soil data web service<br/>
      A prototype service is being offered for access to a snapshot of the Victorian Soil Information System data through the ANZSoilML standard.
      

**<a name="technology-stack">Technology Stack</a>**<br/>
FarmBuild components are using a range of diffrent client-side and server-side technologies to provide required functionalities.
On the client-side FarmBuild is using AngularJS framework to provide a modular architecture and have good separation between different modules. As result of this all JS APIs are available as AngularJS modules. Having said that you are not forced to use AngularJS framework in your application to use FarmBuild JS APIs. In other word all JS APIs are available through farmbuild global name space. (`farmbuild.webmapping`)<br/>
