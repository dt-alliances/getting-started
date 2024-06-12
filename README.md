# Dynatrace Accounts


1. Read [What is Dynatrace](https://docs.dynatrace.com/docs/get-started/what-is-dynatrace) overview docs. 

2. Signup for [Dynatrace Trial](https://www.dynatrace.com/trial) 
  * Let Dynatrace technical Allianace team know this tenant ID and we can extend the trial with a partner not-for-resale partner license per the terms of our Technical Partner Agreement (TAP)
  * Your unique environment ID is `https://{your-environment-id}.live.dynatrace.com`

3. Login and read the [navigate the Dynatrace UI](https://docs.dynatrace.com/docs/get-started/dynatrace-ui) docuemntation

4. Refer to these [guides](https://github.com/dynatrace-perfclinics/dynatrace-getting-started) for trying out your and the `Discover Dynatrace environment`
   
5. Invite users to your account
   * Open account management by opening [the My account URL](https://myaccount.dynatrace.com/accounts) or from the bottom left menu on the your Dynatrace account
   * Dynatrace has role based permissions.  You can made custom groups or easily clone the permissions of an existing users, but stick to `least privileges access` best practice.  Refer to the [Account Managment Docs](https://docs.dynatrace.com/docs/manage/account-management)

# Discover and Demo Environments 

You need a Dynatrace SSO to have access to these.  As a partner you can register on the [Dynatrace partner portal](https://partners.dynatrace.com) and then access these two environments.

1. [Discover Dynatrace environment](https://wkf10640.apps.dynatrace.com/) - a playground environment with demo data to which all customers and partners have access. 
2. [Partner Demo Environment](https://guu84124.apps.dynatrace.com/ui)- A playground environment for partners. Has much more data than the Discover Dynatrace and is used by Dynatrace solution engineers and partners

# Extend and Integrate with Dynatrace

Dynatrace is an open and [extensible platform](https://docs.dynatrace.com/docs/extend-dynatrace). Below are some resources for various interfaces.

## APIs

* [API overview](https://docs.dynatrace.com/docs/dynatrace-api/basics)
* [Create API Token](https://docs.dynatrace.com/docs/dynatrace-api/basics/dynatrace-api-authentication)
* Open `https://{your-environment-id}.apps.dynatrace.com/platform/swagger-ui/index.html` for the Swagger Interface for your environment.  Use the top right dropdown to choose the API definition work with. 

## OpenTelemetry 

* [OpenTelemetry and Dynatrace Overview](https://docs.dynatrace.com/docs/extend-dynatrace/opentelemetry)
* [Dynatrace Collector](https://docs.dynatrace.com/docs/extend-dynatrace/opentelemetry/collector)
* [Ingest API documentation](https://docs.dynatrace.com/docs/dynatrace-api/environment-api/opentelemetry)

## Custom Applications 

Here are the resources that should be useful for you:
* [Dynatrace Developer](https://developer.dynatrace.com/) - All the content you should need to create a Dynatrace app. If you have not seen it, check out our recently released new tutorial. After completing it, you should get a feeling for Dynatrace Apps.
* [Developer Q&A forum](https://community.dynatrace.com/t5/Developer-Q-A-Forum/bd-p/devs_qanda) - You can ask any question regarding creating a Dynatrace App in this forum. Together with my team, we are responsible for answering the questions there.
* [Developer newsletter](https://community.dynatrace.com/t5/Developer-Blog/bg-p/dev_blog) All the important changes for developers building Dynatrace Apps monthly.
* [Monthly office hours session about Dynatrace app development](https://community.dynatrace.com/t5/Events-and-webinars/eb-p/events?filter=includeUpcoming&depth=0&byPassHideMessagesFromListFilter=true&sort_by=occasionStartTime&include_upcoming=true)
* [AppEngine blogs](https://www.dynatrace.com/news/tag/appengine/)
  * [Building custom workflow actions](https://www.dynatrace.com/news/blog/build-custom-workflow-actions-dynatrace-app-toolkit/) 
  
