# Accelerate API and Website performance using Azion Application Acceleration

[Edit on GitHub <svg width="14" height="14" xmlns="http://www.w3.org/2000/svg"><g fill="none" stroke="#F3652B"><path d="M4.81.71H.672v11.43H12.1V8.001" stroke-width=".8"/><path d="M6.87.786h5.155V5.94M6.31 6.5L12.026.786"/></g></svg>](https://github.com/aziontech/docs_en/edit/master/use-cases/apis-performance-sites-application-acceleration/index.md)

Application Acceleration is a service from Azion's Edge Computing platform developed to accelerate the performance of web applications and APIs, by optimizing protocols and managing the different requirements of dynamic content.

Application Acceleration allows advanced rules to be created for the request and response phases based on geolocation, type of device, HTTP headers, cookies, path, etc. This means that it is possible to set business rules that can be directly run on the Edge, closer to users, which significantly increases the performance of APIs and decreases the complexity required at the backend.

Some other advantages from using Application Acceleration:

* It improves the response time with unstable or overloaded network connections;
* Policies can be applied to divide or bypass the cache;
* Can create rewriting rules directly on the Edge, based directly on the user-agent;
* Support for the HTTP2 protocol;

Next, let's look at how to implement advanced rules using Application Acceleration.	

## How it works

Application Acceleration provides a set of advanced options for configuring the Rules Engine, which allows customers to create business logical conditions directly on the Edge. Therefore, every time a request arrives at one of Azion's Edge Nodes, the Edge Applications rules engine that is configured for that domain will be activated.

Application Acceleration enables the configuration of rules by path for:

* **Advanced Cache Key:** configure custom cache key rules based on Cookies or  Query String, with which you can define how the content in your application is divided and which enables dynamic content caching;
* **Bypass Cache:** define Bypass Cache rules for the paths for your website that cannot be cached on our infrastructure;
* **Forward Cookies:** if you wish, you can configure Azion so that the Set-Cookie is passed on to your users. By default, Azion filters the Response Header Set-Cookie sent by your origin;
* **Supports POST/PUT and other methods:** Application Acceleration extends the functionalities of Edge Application to support POST, PUT, PATCH, DELETE methods, as well as those that are already natively supported, GET, HEAD and OPTIONS.

## Creating rules in Edge with Application Acceleration

_**Path**_: Real-Time Manager > Edge Computing > Edge Application

To activate Application Acceleration, simply select it from the list of available services from the Main Settings tab, within the desired Edge Application, from the Real-Time Manager (RTM). Once it’s active, a series of options for configuring the rules will be available in the **Rules Engine** and **Cache Settings**.

## Creating advanced cache rules for dynamic content using query strings

As an example, let's use an API of a regional news site that lists the content of recent news, depending on the city, updated every five minutes. URL example: api.regionalnews.com/updated_news?city=_city_name_.


### Defining the cache configurations

The first step is to define an advanced cache rule to alter the content using the string "city". Using the RTM, choose the Edge Application for which the rule will be configured and, in the Cache Settings section, add a new cache setting, giving it an identifiable name (for example "CacheByCity").

**Define the cache setting (cache setting):** choose the cache settings for the Browser and the CDN and set the TTL to 300 (5 minutes).

**Define the Advanced Cache Key:** for the attribute "Cache by Query String", choose the option "Content varies by some Query String fields (Whitelist)". In the "Query String fields" field, enter the value "city". This will create a cache object with the string "city" for the path indicated in the Edge Application Rules Engine.

If you wish, you can still choose to manage the cache by cookies and by type of device, but these settings are not mandatory. Next, save your settings. 

### Define Validation criteria

Next, on the Rules Engine tab, add or edit a rule for the **Request Phase** to define the behavior for one or more paths. The rules (or Rules Engine) determine the set of conditions that need to be met for Behaviors to be executed.

**Defining validation criteria (criteria):** choose the variables, comparison operators and strings to create your business rule, as in the following example:


* **If**: _${uri}_ **starts with** ***/updated_news***
(next: logical operator, variable, comparison operator, string)

Here, the rule is executed if the URL accessed starts with the string  "_/updated_news_".

**Defining Behaviors:** add the behaviors you want to be carried out when the rule's conditions are met. Example:

* **Then**: ***Set Cache Policy*** **CacheByCity**
(next: logical operator, action, function)

In this example, if the conditions defined in the rules are satisfied, then the cache policy  **CacheByCity** will be run.

Finally, save your Edge Application and the new rule will be ready.

---

Didn’t find what you were looking for? [Open a support ticket.](https://tickets.azion.com/)
