# Dynatrace Overview

Read [What is Dynatrace](https://docs.dynatrace.com/docs/get-started/what-is-dynatrace) help docs. 

# Getting started

1. Signup for [Dynatrace Trial](https://www.dynatrace.com/trial) 
  * Your unique environment ID is `https://{your-environment-id}.live.dynatrace.com`
  * Let Dynatrace technical Allianace team know this environment ID and we can extend the trial with a partner not-for-resale partner license per the terms of our Technical Partner Agreement (TAP)

2. Login and read the [navigate the Dynatrace UI](https://docs.dynatrace.com/docs/get-started/dynatrace-ui) help documentation
   
3. Invite users to your account
   * Open account management by opening [the My account URL](https://myaccount.dynatrace.com/accounts) or from the bottom left menu, "Account Management" in the Dynatrace web UI.
   * Dynatrace has role based permissions.  You can made custom groups or easily clone the permissions of an existing users, but stick to `least privileges access` best practice.  Refer to the [Account Managment Docs](https://docs.dynatrace.com/docs/manage/account-management)
  
   * I suggest creating a `_Demo Users` and a `_Demo Admins` group.
     * Within Dynatrace [My account management](https://myaccount.dynatrace.com/accounts), under the `Identity and access management` menu, choose `Groups`
     * Click add group button
     * Name it such as: `_Demo Admin`.  The underscore as a prefix is useful later to sort it to the top of the groups list and to distinquish from the build in groups.
     * Add permissions for environment but not account.  You can, but with the best practice of least access only grant what is needed.  Non-Admins should just have view and limited permissions.
     * Pick all the policies under environment. Non-Admins should not have admin or policies like to ingest data.
     * Save it
   * Then under the `Identity and access management`, pick `People`
     * Click `Invite user` button
     * Enter the email and select a group such as `_Demo admins`
     * Click `Confirm` and the person will get an automated email to login

# Customer Discovery and Partner Demo Environments

The [Discover Dynatrace environment](https://wkf10640.apps.dynatrace.com/) is a playground environment with demo data to which all customers and partners have access.  Refer to these [guides](https://github.com/dynatrace-perfclinics/dynatrace-getting-started) for trying out your and the `Discover Dynatrace environment`

As a partner you can register on the [Dynatrace partner portal](https://partners.dynatrace.com) and then access the [Partner Demo Environment](https://guu84124.apps.dynatrace.com/ui). This is an environment that additonal demo applications than the Discover Dynatrace.  This environment is shared and used by Dynatrace solution engineers and Partners for giving demos.

# Extend and Integrate with Dynatrace

Dynatrace is an open and [extensible platform](https://docs.dynatrace.com/docs/extend-dynatrace). Below are some resources for various interfaces.

## Data Ingest

Logs, metrics and events can all be send into Dynatrace via [ingestion APIs](https://docs.dynatrace.com/docs/platform/openpipeline/reference/api-ingestion-reference).   Furthermore, data processing of this can be achieved via the Dynatrace OpenPipeline.

### OpenPipeline
* [Annoucement Blog](https://www.dynatrace.com/news/blog/dynatrace-openpipeline-converging-observability-security-and-business-data-at-massive-scale-for-unmatched-analytics-in-context/)
* [OpenPipeline Documentation](https://docs.dynatrace.com/docs/platform/openpipeline/concepts/data-flow)

### Logs
* To stream logs into Dynatrace, use the [log ingest API](https://docs.dynatrace.com/docs/dynatrace-api/environment-api/log-monitoring-v2/post-ingest-logs). For this follow the requirements for Content-Type and Authorization headers and required API Token scope as described in the guide.
* Validate logs coming is with the [log viewer](https://docs.dynatrace.com/docs/observe-and-explore/logs/lma-analysis/logs-and-events) or in a [notebook](https://docs.dynatrace.com/docs/observe-and-explore/dashboards-and-notebooks/notebooks).
* Guide to [create API Token](https://docs.dynatrace.com/docs/dynatrace-api/basics/dynatrace-api-authentication)

## APIs

Dyntrace has a rich set of API to query, load data, and update the Dynatrace configuration.
* [API overview](https://docs.dynatrace.com/docs/dynatrace-api/basics)

Broadly they fall into two categoies:

1) **Environment, Configuration, and Account Management**
   
* These are compatible with both Dynatrace SaaS and Managed.
* They are API Access Token Based and have the base endpoint of:
   * SaaS `https://{your-environment-id}.live.dynatrace.com`
   * Environment or Cluster ActiveGates	`https://{your-activegate-domain}:9999/e/{your-environment-id}`
* [Environment, Configuration, and Account Management APIs Docs](https://docs.dynatrace.com/docs/dynatrace-api)
* [Create API Token](https://docs.dynatrace.com/docs/dynatrace-api/basics/dynatrace-api-authentication)
* Open `https://{your-environment-id}.apps.dynatrace.com/platform/swagger-ui/index.html` for the Swagger Interface for your environment.  Use the top right dropdown to choose the API definition work with.

2) **Dynatrace SaaS Only**
   
* OAuth client based and have the base endpoint of `https://{your-environment-id}.apps.dynatrace.com`
* [Overview on OAuth](https://developer.dynatrace.com/develop/access-platform-apis-from-outside)
* [Two YouTube short demo videos of making OAuthClient and swagger](https://www.youtube.com/playlist?list=PLqt2rd0eew1YSULHGceQ-zsIU6Dww1nMw)
  
## OpenTelemetry

Dyntrace is both a significant contributor to the project as well as a provider to native platform support for Otel metrics, traces, and logs.
* [OpenTelemetry and Dynatrace Overview](https://docs.dynatrace.com/docs/extend-dynatrace/opentelemetry)
* [Dynatrace Collector](https://docs.dynatrace.com/docs/extend-dynatrace/opentelemetry/collector)
* [Ingest API documentation](https://docs.dynatrace.com/docs/dynatrace-api/environment-api/opentelemetry)

## Dynatrace Apps

Dynatrace provides the possibility to build custom functionality on top of all the observability data ingested into Dynatrace in the form of custom apps. The [Dynatrace Developer Portal](https://developer.dynatrace.com/) has all the content you should need to create a Dynatrace app. If you have not seen it, check out our recently released new tutorial. After completing it, you should get a feeling for Dynatrace Apps.
* [Getting Started](https://github.com/dt-alliances/getting-started?tab=readme-ov-file#custom-applications)

The Dynatrace SDK an abstraction to the Dynatrace Platform.  It’s not the same interface as the API, but you can review the DQL Query SDK here:
* [Building Dynatrace Apps that interfaces with Dynatrace data, platform services and config use the Dynatrace SDK](https://developer.dynatrace.com/develop/sdks)
* [DQL Query SDK](https://developer.dynatrace.com/develop/sdks/client-query)

Additonal resources:

* [YouTube Video series – Inside Dynatrace Apps](https://www.youtube.com/playlist?list=PLqt2rd0eew1bu5vGLUJ3pr2SgNpnpKb71)
* [Developer Q&A forum](https://community.dynatrace.com/t5/Developer-Q-A-Forum/bd-p/devs_qanda) - You can ask any question regarding creating a Dynatrace App in this forum. Together with my team, we are responsible for answering the questions there.
* [Developer newsletter](https://community.dynatrace.com/t5/Developer-Blog/bg-p/dev_blog) All the important changes for developers building Dynatrace Apps monthly.
* [Monthly office hours session about Dynatrace app development](https://community.dynatrace.com/t5/Events-and-webinars/eb-p/events?filter=includeUpcoming&depth=0&byPassHideMessagesFromListFilter=true&sort_by=occasionStartTime&include_upcoming=true)
* [webinar and blogs](https://www.dynatrace.com/news/tag/appengine/)
  * [Building custom workflow actions](https://www.dynatrace.com/news/blog/build-custom-workflow-actions-dynatrace-app-toolkit/)
  * [webinar - Creating custom solutions with ease: A journey through app development with Omnilogy](https://info.dynatrace.com/global-all-wc-partner-app-developer-journey-with-omnilogy-24634-registration.html)
  
