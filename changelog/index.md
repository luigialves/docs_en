# **Changelog**

[Edit on GitHub <svg width="14" height="14" xmlns="http://www.w3.org/2000/svg"><g fill="none" stroke="#F3652B"><path d="M4.81.71H.672v11.43H12.1V8.001" stroke-width=".8"/><path d="M6.87.786h5.155V5.94M6.31 6.5L12.026.786"/></g></svg>](https://github.com/aziontech/docs_en/edit/master/changelog/index.md)

This page lists the latest changes to Azion products and services. Here you will find a summary of information about the release of new features or changes in the behavior of the products.

---

**Oct/2020**

* Added support for Query String when using HMAC authentication in Edge Application.
* Improvements in Network Layer Protection, Web Application Firewall, and Edge Functions to support a larger number of Domains per Edge Firewall.
* Launch of the Early Access Program for [Edge Functions using JavaScript](https://www.azion.com/en/blog/javascript-azion-edge-functions/)

---

**Sep/2020**

* Added a new menu and footer at Real-Time Manager.
* Added a new feature to evaluate password strength at User Preferences.
* Bugfix at the reseller's user list.
* Bugfix in the feature of duplicate an Edge Application with Error Responses.
* Added consumption information of the metric **Invocations of the Edge Functions product** in the billing interface.
* Added consumption information of the metric **Standard Queries of the Intelligent DNS product** in the billing interface.
* Bugfix in the Data Streaming product interface;

---

**Aug/2020**

* Domain availability ** ns3.aziondns.org ** in the Intelligent DNS product extending our * Anycast * network.
* Added graph of the metric  **Invocations** of the Edge Functions product, in interface Real-Time Metrics.  
* Added graph of the metric  **Standard Queries** of the Intelligent DNS product, in interface Real-Time Metrics. 
* Bugfix timezone in the Real-Time Metrics.
* Bugfix in SameSite Cookie with value "None".

---

**jul/2020**

* Bugfix in the Intelligent DNS product.
* Launch of the new version of Origin Shield, with support for querying through Network List via Real-Time Manager and API.
* Added functionality for sending email notification when the Origin Shield product Network List changes.
* Added functionality to view the changes that occurred in the Origin Shield product's Network List through the RTM History.
* Bugfix in the Digital Certificate product.
* Launch of the Single Sign-On.

---

**jun/2020**

* Support for adding a response starting with "_" for CNAME type records in the Intelligent DNS product.
* Bugfix of synchronization of the serial number of the SOA record in the Intelligent DNS product.
* Azion Online Sales Channel released.
* Additional feature Sampling in the Data Streaming product (in Early Access).
* Option to activate / deactivate the Edge Functions product through account subscriptions.
* Bug fix Network Lists UI adjustment to prevent saving empty Network Lists.
* Bug fix adjustment in Edge Functions to allow creating and instantiating using special characters.

---

**may/2020**

* Additional qtype support for CAA (Certification Authority Authorization) in the Intelligent DNS product.
* Now you can view the content of Network Lists provided by Azion through Real-Time Manager user interface or Network Lists API.
* Real-Time Analytics renamed to Real-Time Metrics
* Added graphics referring to "L2 Caching" metrics, in the Real-Time Metrics interface
* Bug fix performance Data Streaming
* Bug fix Real-Time Metrics supporting larger number of domains Edge Application

---

**apr/2020**

*  Azion Edge Firewall's General Availability.
*  Bug fix in the Intelligent DNS product interface.
*  Bug fix in the Real-Time Metrics product interface.
*  Bug Fix in the Edge Application product at Cache error pages.
*  Integration with Radware Bot Manager.

---

**mar/2020**

* Making  [API]({% tl documentation_products_intelligent_dns %}) available for managing Zones and Records for the Intelligent DNS product.
* Added the graph referring to the "Data Streaming Requests" metric of the Data Streaming product, in the Real-Time Metrics interface.
* Added support for ECC - _Elliptic Curve Cryptography_ in [Digital Certificates]({% tl documentation_products_edge_applications_digital_certificates %}).
* Improvements in the propagation of Json args from Edge Function Instances.
* Bug fix when editing _Origins_ through the Real-Time Manager interface.
* Bug fix on the _subdomain_ purge when using [Wildcard Purge]({% tl documentation_products_edge_applications_real_time_purge %}).

---

**fev/2020**

* Added "host" variable to Real-Time Events for Data Source "Edge Application".
* Bug fix in the Real-Time Events interface.
* Added the graph referring to the "Data Streamed" metric of the Data Streaming product, in the Real-Time Metrics interface.
* New Bot Management solution integrated to the Azion platform, using [Edge Functions]({% tl edge_services_compute_modules_edge_functions %}) in [Edge Firewall]({% tl documentation_products_edge_firewall %}).
* Added [TLS Minimum Version]({% tl documentation_products_edge_applications %}#minimum-tls-version) selection component to the Edge Application interface.
* Bug fix in [Api V3]({% tl api_v3 %}) page when listing [Edge Applications]({% tl api_v3_edge_applications %}).

---

**jan/2020**

* End-Of-Life of the Raw Logs product, with the Data Streaming product as an alternative to its use.
* Bug fix in the Real-Time Analytics product interface.
* Improvements to the Intelligent DNS product interface.
* End-Of-Life of the Cloud Storage product, with the L2 Caching product as an alternative to its use.
* Updates to the geolocation service.
* Improvements in Edge Caching to support a larger number of Domains per Edge Application.

---

**dec/2019**

* Included HMAC Authentication for authentication from private sources in Edge Caching.
* Direct connector added with support for the S3 (Simple Storage Service) protocol for the Data Streaming product.
* Bug fix in the Real-Time Analytics product interface.
* Improvements in the propagation of updates to the Network Lists of the Network Layer Protection module.
* Added Cache Settings option for L2 Caching add-on in early access for Customers with Cloud Storage.

---

**nov/2019**

* Added the value domain_name to the results of the V3 API for Domains.
* Added the possibility to link an already used Domain, to more than one Data Streaming.
* Support for TLS 1.3 Protocol in Edge Application.
* Added the Behavior Drop to the Rules Engine of the New Edge Firewall.
* Set-Cookie and Cache Key improvements for Edge Functions A / B Testing and Cookie Targeting.

---

**oct/2019**

* Launch of the New Edge Firewall with Rules Engine and support for the Network Layer Protection and Web Application Firewall modules.
* Launch of the API for managing Network Lists of the Network Layer Protection module.
* New Real-Time Purge and Purge User Interface in the L2 Caching layer.
* Additional Section support for NS/MX responses in the Intelligent DNS product.
* Added change history for the Intelligent DNS product in Real-Time Manager.
* Bug fix in the DNS entry in the Intelligent DNS product.

---

**sept/2019**

* Release of the variable ${remote_port} for use in the Rules Engine in Edge Application.
* Added Azion Edge Function for Cookie Targeting.
* Improvements in the TTL response for ANAME resolutions in the Intelligent DNS product.

---

**aug/2019**

* Launch of Edge Functions Instances to run in Edge Application.
* Added the Azion Edge Function Instance for Massive Redirect.
* Improvements to the Image Optimization module.
* Added option to include HTTP/HTTPS Headers for the Data Streaming product.
* Edge Caching add-on L2 Caching available in early access for Customers with Cloud Storage.
* Improvements in the Server Fail response in the Intelligent DNS product, for when the server is unable to respond.
* Support to the Wildcard in the registration of Records in the Intelligent DNS product.

---

**jul/2019**

* Added direct connector with Apache Kafka for the Data Streaming product.
* Filter option made available for a period of up to 3 days in the Real-Time Events product.
* Support for PTR type Records in the Intelligent DNS product.
* Added Pulse Events Data Source to Real-Time Events.

---

**jun/2019**

* Launch of API [Versão 3]({% tl api_v3 %}) with API endpoints for managing Digital Certificates, Domains and Edge Application.
* Improvements in viewing the change history in Real-Time Manager.

---

**may/2019**

* Improved the interface of the Real-Time Events product to highlight the searched terms.
* Added option to edit records in the Data Streaming product.
* Data Streaming product interface improvements.
* Data Streaming Data Source added to Real-Time Events.
* Added the option to choose to honor TTL from origin or Default configuration in Cache Settings of an Edge Application.

---

**apr/2019**

* Added advanced filters option (KEY: VALUE, AND and OR) in the Real-Time Events product interface.
* Added security permissions for the Data Streaming product.
* Bug fix in the Real-Time Analytics product interface when a time interval is informed.
* Added interface with the option of viewing, deleting and creating records in the Data Streaming product.
* Bug fix in the Real-Time Analytics product API.
* Data Streaming product interface improvements.

---

**mar/2019**

* Option to activate / deactivate the Real-Time Events product through account subscriptions.
* Release of the variables ${geoip_region} and ${geoip_region_name} for use on the Rules Engine.

---

**feb/2019**

* Added exclusive Team Permission for Wildcard Purge privileges in Real-Time Purge.
* Cache key bugfix for HLS content.

---

**jan/2019**

* Filter option made available for a period of up to 1 days in the Real-Time Events product.
* Improvements to the Real-Time Events product interface.
* Security Fixes in the Real-Time Events product.
* Added functionality that allows the use of Wildcard in Cache Settings Whitelist/Blacklist.
* Improvements to the RTM interface for WAF Rule Sets.
* Team Permissions improvements for Edge Applications and Domains.

---

**dec/2018**

* Beta version of the Big Data product made available. From now on it is possible to view the Edge Applications and WAF Events logs, within a period of 24 hours, as well as to filter by specific terms.
* Added Bypass functionality on the WAF screen, allowing it to be possible to include one or more IPs that will not pass through the Firewall.
* Fixed an issue that caused an error when trying to create a cache rule.
* Fixed an issue in the Rules Engine that caused an error when trying to add criteria with a very high number of characters.
* Fixed the field label for Purge URLs that were incorrect when a validation error occurred.

---

**nov/2018**

* Created the functionality that allows it to be possible to customize Error Pages, regarding the definition of the Origin that will deliver the error pages.
* New behavior made available, called Filter Request Cookie, where from this behavior it is possible to configure the removal of a Cookie sent by the user.
* It is now possible to activate Azion modules directly via the Edge Applications menu, on the Main Settings tab.
* Added ASN Blocking functionality, responsible for limiting access to a resource, in Edge Firewall.
* Created the functionality responsible for allowing to configure a value less than 60 seconds for the Maximum TTL field of the CDN Cache Settings when the Application Acceleration product is provisioned.
* Fixed an issue that caused the GEO_IP field not to be displayed in Raw Logs.
* Fixed an issue that made it impossible to add Rules Engine in the Request phase.
* Fixed an issue that prevented a configuration from being saved in the Main Settings tab after it was cloned.
* Fixed the problem that occurred when trying to activate HTTPS in an Edge Application.
* Fixed an issue that caused Adaptive Delivery to be unable to be turned off in Edge Applications.
* Fixed an error that occurred when creating Edge Application single origin with Media Packager.
* Fixed the issue in the search engine of the Edge Applications Rules Engine.

---

**oct/2018**

* Created an option to list the Error Responses presets in an Edge Application configuration.
* Added the Behavior Add Request Cookie to the Request Phase as well.
* Created functionality that allows all Functions parameterized in an Edge Application to be available for selection when selecting the Behavior Run Function.
* Option to enable/disable the use of the Edge Functions Product for a given Edge Application configuration.
* Created an option to delete a parameterized function instance in an Edge Application configuration.
* Option created to add a parameterized function to an Edge Application configuration.
* Created a new Behavior in the Response Phase, responsible for removing a Set-Cookie sent by the origin.
* Rate Limit functionality is available on the Edge Firewall.
* Created the option to edit an Edge Function already parameterized linked to an Edge Application configuration.
* Created option to add/edit Error Responses presets.
* Increased the limit of the inputs of the arguments of Add Response Header, both in Criteria and in Behaviors.
* Improvement to the functionality responsible for auto-saving the Rules Engine rules.
* Improved the Name field of the Rules Engine rules.
* Improvement made that is responsible for making the Cache Settings list, when the CDN Cache is in override, the configured TTL is displayed.
* Fixed an issue that caused an error to be generated when adding a new Edge Application with a Cloud Storage origin.
* Fixed an issue that caused the link to be sent to the tab listing when selecting the option to return to the list of Edge Applications.
* Adjustment made that is responsible for making RawLogs work as expected with Edge Applications.

---

**set/2018**

* Contrast adjustments made to the new Edge Applications and Domains layout for easy viewing.
* Adjustments made in Analytics to support the new Edge Applications configurations.
* Implementation of the download functionality for Managed Configurations in Edge Applications.
* Implementation of the functionality of multiple Domains to be associated with the same Edge Application.
* Bugfix in saving the Default Rule in the Rules Engine.
* Bugfix in saving the Default Rule in the Rules Engine.
* Security fixes.

---

**aug/2018**

* Added Manage Keys button on the Cloud Storage home screen to retrieve access credentials via s3cmd.
* Cloud Storage subscription included in the Sign Up process for new customers.
* New Edge Applications interface launched.
* New Domains interface launched.
* New menu structure launched in Real-Time Manager.
* New layout launched in some Real-Time Manager applications.
* Bug fixes.
* Infrastructure expansion.

---

**jul/2018**

* Bugfix for Image Optimization integration with Cloud Storage.

---

**jun/2018**

* Added the Others field in the Error Responses tab to configure cache time for other error codes, not listed.
* Release of $ {geoip_country_ *} variables for use on the Rules Engine.
* Update of the Add Configuration form to allow creation with origin type Cloud Storage and Media Packager.
* Correction of behavior binding to Cloud Storage origin.
* Interface development for Subscription management.
* Correction for cleaning Sliced Files headers, when the functionality is turned off.
* Adjustment of the Live Ingest switching mechanism to force reconnection of encoders in case of failure.
* Added live stream fallback support for the hls.js player.
* Infrastructure expansion.

---

**may/2018**

* Launch of the [Cloud Storage]({% tl documentation_products_cloud_storage %}) product web interface.
* Integration of origin type Media Packager to Real-Time Manager.
* Development of the [videojs-azion-multisrc](https://github.com/aziontech/videojs-azion-multisrc/) plugin for the video.js player.
* Configuration of POST Cache activation via Real-Time Manager.
* Development of the Capture Match Groups behavior in the Rules Engine.
* Development of the Rewrite Request behavior in the Rules Engine.
* Development of the behavior Enable Sliced Files.
* Development of the behavior Index Document.

---

**apr/2018**

* Integration of origin type Live Ingest to Real-Time Manager.
* Integration of origin type Cloud Storage to Real-Time Manager.

---

**mar/2018**

* Correction of pre-selected dates from the Analytics API that were not taking into account the user's time zone.
* Fixed listing of duplicate settings in the API.
* Launch of API endpoints for managing Digital Certificates.
* Launch of API endpoints for managing Device Groups.
* Launch of API endpoints for managing Error Responses.

---

**feb/2018**

* Launch of the new UI for configuring Conditional Rules Engine Rules for a portion of customers.
* Bypass Cache configuration leaves Cache Settings and starts to be done in the Rules Engine.
* Configuration of content variation by Device Group (Adaptive Delivery) leaves the Rules Engine and starts to be done in Cache Settings.
* Custom Headers tab no longer exists and the functionality is incorporated by the Rules Engine.
* Application Acceleration is activated in the Main Settings tab of the Configuration.
* Host Header is now required in the Real-Time Manager user interface. In the API, the field remains optional.
* Admin restriction to generate API tokens removed. Permissions are based on the user who generated the token.

---

**jan/2018**

* Development of the UI for configuring conditional rules for the Rules Engine.

---

**dec/2017**

* Improved flow integration with the support tool Freshdesk.
* New SDN Router with support for network maps in Beta mode.
* Expansion of network infrastructure in Argentina.
* Live Streaming (Beta) charts for content delivery.
* Bug fixes.
* Sensitive fields (certificate and private key) are now hidden when editing a digital certificate.

---

**nov/2017**

* New [types of purge]({% tl documentation_products_edge_applications_real_time_purge %}#tipos-de-purge): purges can now be done via URL, CacheKey or Wildcard.
* The purge history will now show the type, method and form in which the system received the purge request.
* Bug fix for purge in the case of URLs with Unicode.

Note: Just as the interface has been updated to require the purge type, the [Purge API]({% tl api_v1_real_time_purge %}#tipos-de-purge) has also changed.

---

**sept/2017**

* Release of the use of the $host (request host header) variable when configuring the Host Header of an origin.
* Implementation of [Multi-Factor Authentication]({% tl documentation_accounts_multi_factor %}).

---

**aug/2017**

* Launch of the new version of the [Purge API]({% tl api_v1_real_time_purge %}).
* Bug fix in the Live Streaming endpoint of the Analytics API.
* Implementation of Sign Up online.
* Stability improvements in the Analytics platform.
* Evolution of the SDN Router routing algorithms.
* Bug fix in login error messages.
* Bug fix in the flow of activation of new accounts.
* Security fixes.

---

**jul/2017**

* [Edge Firewall's]({% tl documentation_products_edge_firewall %}#ip-blocking) IP Blocking functionality is integrated into Real-Time Manager.
* [Edge Firewall]({% tl documentation_products_edge_firewall %}) IP Blocking integrated in to the API.
* Integration of the functionality that allows the download of the advanced settings file (_locked_) with Real-Time Manager, when required by the customer.

---

**jun/2017**

* Implementation of Origin Path support in to Real-Time Manager.
* Integration with Real-Time Manager the functionality for editing automatic rules in the WAF whitelist.
* Implementation of Rate Limit in the API.
* Implementation of the functionality to allow creation and removal of custom rules in the WAF whitelist.

---

**may/2017**

* Launch of new API endpoints for [for creating, changing and removing cache settings]({% tl api_v1_content_delivery_cache_settings %}).
* Implementation of the Elastic Search endpoint in the [Data Streaming]({% tl documentation_products_data_streaming %}) product.
* Implementation of new features in Lua in Content Delivery for advanced conditional rules.
* Implementation of new Device Detection functionalities for configuring conditional rules based on the device.
* Evolution of the Learning Tool of the [Web Application Firewall]({% tl documentation_products_web_application_firewall %}) product.

---

**apr/2017**

* Implementation of breadcrumbs in Real-Time Manager.
* Improvements in the creation flow of the first configuration.
* Launch of new API endpoints for [creating, changing and removing origins]({% tl api_v1_content_delivery_origins %}).
* Launch of new API endpoints for [creating, changing and removing rules from the rules engine]({% tl api_v1_content_delivery_rules_engine %}).
* Launch of new API endpoints for [querying, creating, changing and removing rule sets from the edge firewall]({% tl api_v1_cloud-security_edge_firewall %}).
* Launch of new API endpoints for [query WAF rule sets]({% tl api_v1_cloud-security_web_app_firewall %}).
* Launch of a new graph in Analytics to evaluate bandwidth savings using Image Optimization.

---

**mar/2017**

* Launch of new API endpoints for [querying origins]({% tl api_v1_content_delivery_origins %}).
* Launch of new API endpoints for [query cache settings]({% tl api_v1_content_delivery_cache_settings %}).
* Launch of new API endpoints for [querying the rules engine]({% tl api_v1_content_delivery_rules_engine %}).
* Launch of the Billing screen for consulting consolidated accounting data per product.
* Implementation of the interface for managing WAF whitelist rules.
* Fixed the Cache Settings tie with behaviors in the Rules Engine.

---

**feb/2017**

* Launch of endpoints to configure the [Content Delivery API]({% tl api_v1_content_delivery %}).
* Launch of the new [Data Streaming]({% tl documentation_products_data_streaming %}) product.
* Improvements to the texts of the [Advanced Cache Key]({% tl documentation_products_application_acceleration %}#AdvancedCacheKey) options.
* Improvements in the behavior of the Rules Engine, to simplify the flow of creating Redirect and Access Denied rules.
* Implementation of the customizable “Add Request Header” functionality in the [Adaptive Delivery]({% tl documentation_products_adaptative_delivery %}) product.

---

**jan/2017**

* Renewal of the Azion [Shared Certificate]({% tl documentation_products_edge_applications_digital_certificates %}) with CA, for all customers of the product.
* Fix for the creation/editing of the Rule Engine in Real-Time Manager to make the selection of an Edge Firewall rule set optional.
* Fix for viewing graphs in Analytics that account for the occupation of the RawLogs bucket in Cloud Storage.
* Fix for using Image Optimization in conjunction with Cloud Storage without the need to create a segregated Configuration.
* Performance optimization when loading Real-Time Manager.
* Launch of authentication framework in the [Azion API]({% tl api_v1 %}).
* Launch of analytics data query endpoints in the Azion API.
* Integration of the Advanced Cache Key functionalities (cache key by cookie and cache key by query string) of the [Application Acceleration]({% tl documentation_products_application_acceleration %}) product with Real-Time Manager.
* Launching of a new Cache Settings tab and changing the behavior of the Rules Engine tab, in Real-Time Manager, to enable the reuse of cache settings by path.

---

**sept/2016**

* Launch of new Image Optimization graphics in [Analytics]({% tl documentation_products_real_time_analytics %}).
* Launch of new Live Ingest charts in Analytics.
* Launch of new Media Packager graphics in Analytics.
* The convergence of the Web Performance and Media Delivery products as the [Content Delivery]({% tl documentation_products_content_delivery %}) product, used for HTTP/HTTPS delivery of small files, large files, live streaming, VOD or any other content and web application that has been completed.

---

**ago/2016**

* HTTP/2 support.
* Update of the Origins tab in Real-Time Manager to integrate the [Load Balancer]({% tl documentation_products_load_balancer %}) product functionalities.
* Update of Real-Time Manager to include the new interface for creating [Web Application Firewall]({% tl documentation_products_web_application_firewall %}) rule sets.

---

**jun/2016**

* Update in the Permissions by Time interface, in Real-Time Manager.
* Real-time Wildcard Purge support.
* Update of the [Image Optimization]({% tl documentation_products_image_optimization %}) platform, with good gains in image optimization.

---

**may/2016**

* Launch of the new interface for uploading [Digital Certificates]({% tl documentation_products_edge_applications_digital_certificates %}) to Real-Time Manager.
* New point of presence (POP) in Rio de Janeiro.

---

**apr/2016**

* Update of the [Edge Firewall]({% tl documentation_products_edge_firewall %}) interface to support the reuse of rule sets.
* Update of the Custom Headers interface to support configuration reuse.
* Launching of the tab for configuring Device Groups and updating the Rules Engine tab for integrating the [Adaptive Delivery]({% tl documentation_products_adaptative_delivery %}) product.

---

Didn't find what you were looking for? [Open a support ticket.](https://tickets.azion.com/)
