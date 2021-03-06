# Rules Engine for Edge Application

[Edit on GitHub <svg width="14" height="14" xmlns="http://www.w3.org/2000/svg"><g fill="none" stroke="#F3652B"><path d="M4.81.71H.672v11.43H12.1V8.001" stroke-width=".8"/><path d="M6.87.786h5.155V5.94M6.31 6.5L12.026.786"/></g></svg>](https://github.com/aziontech/docs_en/edit/master/edge-application/rules-engine/index.md)

You can transfer part of the logic of your application's business rules to Azion's Intelligent Edge using the serverless computing features of the Application Acceleration product. That way, you build an architecture that delivers performance to your users while consuming less resources and processing at its origin.

The Rules Engine was designed to allow the coding of a logic of conditional execution of behaviors and actions directly in Azion's Intelligent Edge, closer to its users and, therefore, with better performance and throughput for your application.

> 1. [How does it work?](#how-does-it-work)
> 2. [Processing Phases](#processing-phases)
> 3. [Rules](#rules)
> 4. [Functions](#functions)

---

## 1. How does it work? {#how-does-it-work}

Each user request for your application is processed in two sequential phases:

1.  Request Phase
2.  Response Phase

At each processing phase, you can define a set of rules to handle the request according to the needs of your application or business. The rules are composed by criteria which represent the conditions for the execution of the rules, and by behaviors which represent the actions that need to be executed.

The processing of the phases is sequential and you can use as criteria a powerful set of variables and comparison operators. If the conditions are met, the behaviors of each rule are executed until all the rules are processed or a rule with a finalizing behavior is found in the path (Deny, Redirect To, Deliver).

---

## 2. Processing Phases {#processing-phases}

The processing phases represent the steps in which the requisition is. They are:

**Request Phase**

In the Request Phase your user is requesting a resource from your application. It is at this phase that you define the rules for accepting or not accepting your user's request. You must also use the Request Phase to handle your user's request according to your business rules, as well as to define which origins should handle the request in each situation, in case the requested content is not cached.

You can use as variables of the Request Phase rules any variable related to the data sent by your user in the request. As the response has not yet been processed by your application, at this phase you do not have access to variables related to the content that will be delivered to your user.

In this phase, you also define how Azion should manage your application's cache. If your application does not allow any type of cache, you can define the conditions to ignore the cache.

**Response Phase**

In the Response Phase you can build the rules for final handling of the response that will be delivered to your users. All handling processed in the Response Phase is dynamic and will be performed individually for each user.

---

## 3. Rules {#rules}

The rules are composed by Criteria, which determines the set of conditions that need to be met for the execution of Behaviors.

**Criteria**

In the Criteria you define the conditions for executing the rule. You can use a powerful set of variables, comparison operators on strings and logical operators to build your business rule.

**Variables**

| Variable | Description | **Phases in which it can be used** | Requirements |
|----------|-----------|---------------------------------|------------|
| ${arg_name} | The *name* argument sent by the user on the request line (query string). For example, for the GET/path?Search=test request, the variable ${arg_search} will assume the value test. | Request Phase <br>Response Phase | Application Acceleration |
| ${args} | All arguments sent by the user in the request string (query string). | Request Phase <br>Response Phase | Application Acceleration |
| ${cookie_name} | Value of the cookie name. For example, for cookie_icl_current_language = pt-br, the variable ${cookie__icl_current_language} will assume the value pt-br. | Request Phase<br> Response Phase | Adaptive Delivery |
| ${device_group} | User device group. Device groups are customized through the User Agent in the Device Groups tab of Real-Time Manager. | Request Phase <br>Response Phase | Adaptive Delivery |
| ${geoip_city_continent_code} | 2-letter continent code, using the geolocation base geoip_city. For example: EU for Europe, NA for North America, SA for South America etc. | Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_city_country_code} | 2-letter country code, using the geolocation base geoip_city. For example: RU for Russia, BR for Brazil, US for United States etc.	| Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_city} | Name of the city, using the geolocation base geoip_city. Sao Paulo, London, New York, Porto Alegre etc.	| Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_continent_code} | 2-letter continent code. For example: EU for Europe, NA for North America, SA for South America etc.	| Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_city_country_name} | Name of the country, using the geolocation base geoip_city. For example: United States, Brazil, Russian Federation etc. | Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_country_code} | 2-letter country code, using the geolocation base geoip_country. For example: RU for Russia, BR for Brazil, US for United States etc. | Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_country_name} | Name of the country, using the geolocation base geoip_country. For example: United States, Brazil, Russian Federation etc. | Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_region_name} | Name of the country, using the geolocalization base geoip_region. For sample: Ontario, Delaware, Sao Paulo etc. | Request Phase <br>Response Phase | Application Acceleration |
| ${geoip_region} | 2-letter region code. For exemple: RS for Rio Grande do Sul, DE for Delaware, ON for Toronto etc. | Request Phase <br/>Response Phase | Application Acceleration |
| ${host} | In order of precedence: the host name of the request line, or the value of the Host header field of the request, or the name of the server serving the request. | Request Phase <br>Response Phase | Application Acceleration |
| ${http_name} | The value of the request name header field. The name argument must be converted to lowercase and the hyphens must be converted to underscore. For example: ${http_accept} will take the value of the Accept footer of the HTTP request field. | Request Phase <br>Response Phase | Application Acceleration |
| ${remote_addr} | The IP address of the client performing the HTTP request. | Request Phase <br>Response Phase | Application Acceleration |
| ${remote_user} | The username provided by basic authentication, if any. | Request Phase <br>Response Phase | Application Acceleration |
| ${request} | Complete request query. | Request Phase <br>Response Phase | Application Acceleration |
| ${request_body} | POST arguments, sent in the body of the request. | Request Phase <br>Response Phase | Application Acceleration |
| ${request_method} | The HTTP method of the request. For example: GET, POST, PUT, etc. | Request Phase <br>Response Phase | Application Acceleration |
| ${request_uri} | The complete URI of the request, with arguments (query string). | Request Phase <br>Response Phase | Application Acceleration |
| ${scheme} | The scheme of the request: http or https. | Request Phase <br>Response Phase | Application Acceleration |
| ${sent_http_name} | The value of the response header field name. The name argument must be converted to lowercase and the hyphens must be converted to underscore. For example: ${sent_http_content_length} will take the value of the Content-Length header. | Response Phase | Application Acceleration |
| ${status} | Status code of the response. | Response Phase | Application Acceleration |
| ${upstream_addr} | The IP address and port of the queried origin for obtaining the response. If multiple origins are consulted during the processing of the request, the addresses will be separated by a comma. For example: 192.168.1.1:80, 192.168.1.2:80. If an internal redirect from one group of servers to another occurs, initiated by an “X-Accel-Redirect” or an error page, the addresses of the different groups will be separated by “:”. For example: “192.168.1.1:80, 192.168.1.2:80 : 192.168.10.1:80, 192.168.10.2:80”. | Response Phase | Application Acceleration |
| ${upstream_cookie_name} | Value of cookie name sent by the origin using the Set-Cookie header field. If multiple origins are consulted during the processing of the request, only cookies from the last origin are stored. | Response Phase | Application Acceleration |
| ${upstream_http_name} | Value of the name header field sent by the origin. The name argument must be converted to lowercase and the hyphens must be converted to underscore. If multiple origins are consulted during the processing of the request, only headers from the last origin are stored. For example: ${Upstream_http_server} will assume the value of the Server header field sent by the last queried origin. | Response Phase | Application Acceleration |
| ${upstream_status} | Status code of the origin response sent to Intelligent Edge. If multiple origins are consulted during the processing of the request, the status codes will be separated by a comma. If an internal redirect from one group of servers to another occurs, initiated by an “X-Accel-Redirect” or an error page, the status codes of the different groups will be separated by “:”. | Response Phase | Application Acceleration |
| ${uri} | The normalized URI of the request. The value of $ {uri} can change during the processing of a request, for example, when an internal redirect occurs or when index files are used. | Response Phase | - |


**Comparison Operators**

The condition for the execution of a rule must be the comparison of a variable with an argument. The comparison operators are:

| Operador | Descrição | Argumento |
|----------|-----------|-----------|
| is equal | The value of the variable is equal to the argument, compared character by character. | string |
| is not equal | The value of the variable is not exactly the same as the argument. | string |
| starts with | The value of the variable starts with the argument. | string |
| does not start with | The value of the variable does not start with the argument. | string |
| matches | The value of the variable matches the regular expression entered as an argument. | regular expression |
| does not match | The value of the variable does not match the regular expression entered as an argument. | regular expression |
| exists | The variable has a defined value. For example: *${arg_search}* exists if a search argument was sent in the request query string. | - |
| does not exist |The variable does not have a defined value. For example: *${arg_search}* does not exist if a search argument was not sent in the request query string. | - |

**Logic Operators**

Multiple conditions can be defined using the logical operators "and" and "or”. The operator “and” has implicit precedence over the operator “or”.

If explicit precedence is required, you can add multiple criteria groups under the and logic.

Behaviors

In Behavior you add the behaviors you want to perform, if the rule's conditions are met.

At each processing phase, different behaviors are available.

| Behavior | Description | **Phases in which it can be used** | Requirements |
|----------|-----------|-----------|------------|
| Add Request Header | Adds a header field to the request that will be sent to the origin. The header field must be informed as an argument in the format *Field:value* |  | Request Phase |
| Add Response Cookie | It adds a cookie in the response through the Set-Cookie header. The value of the cookie must be informed as an argument in the formats:<br><br> _&lt;cookie-name&gt;=&lt;cookie-value&gt;<br> &lt;cookie-name&gt;=&lt;cookie-value&gt;; Expires=&lt;date&gt;<br> &lt;cookie-name&gt;=&lt;cookie-value&gt;; Domain=&lt;domain-value&gt;<br> &lt;cookie-name&gt;=&lt;cookie-value&gt;; Path=&lt;path-value&gt;_<br>                         Multiple policies are also allowed, for example:<br> _&lt;cookie-name&gt;=&lt;cookie-value&gt;; Domain=&lt;domain-value&gt;;<br> Path=&lt;path-value&gt;; Expires=&lt;date&gt;_ | Response Phase | Application Acceleration |
| Add Response Header | Adds a header field to the response that will be sent to the user. The header field must be informed as an argument in the format Field: *value*. | Response Phase | - |
| Bypass Cache | Defines that Azion should not cache the response from its origin. The execution of this rule has no impact on the cache in the users' browser, which must be defined using the *Set Cache Policy* behavior. | Request Phase | Application Acceleration |
| Capture Match Groups | Support behavior for handling strings.<br><br>Stores in a temporary variable the result of capturing correspondence groups defined by a regex applied to one of the available HTTP request fields.<br><br>This temporary variable can be later referenced in the behavior Rewrite Request to assemble the rewrite string.<br><br>This behavior requires three arguments:<br><br>  *captured array name*: the name you want to give the temporary variable where the array of captured strings will be stored. <br> *subject*: the HTTP request field where you want to capture a string.<br> *regex*: the regular expression used to capture the strings. Each captured group must be represented in parentheses.<br><br> For example, to capture the path and name of a file in an HTTP request, you could use:<br><br> _captured array name:_ capture<br>_subject:_ ${uri}<br>_regex:_ ^(.*/)([^/]*)$<br><br> You may reference the capture variable as an array by using the notation %{*variable[index]*}. Because it is a local variable, you can only use it within the same rule you are setting up.<br><br>In this example, if the URI is /path/image.jpg, the capture variable will have the following values:<br><br> %{capture[0]} = “/path/image.jpg”<br>%{capture[1]} = “/path/”<br>%{capture[2]} = “image.jpg”<br><br>You can also name the indexes, to reference them using names instead of a numeric index. To do so, use the?*<name>* notation as in the example below.<br><br> _captured array name:_ capture<br> _subject:_ ${uri}<br> _regex:_ ^(?&lt;path&gt;.*/)(?&lt;filename&gt;[^/]*)$ | Request Phase | Application Acceleration |
| Deliver | It finishes processing the request and delivers the content to the user, without executing any of the following rules. By using the Deliver behavior, you are forcing the processing to end immediately. | Request Phase<br> Response Phase | - |
| Deny (403 Forbidden) | Delivers: *403 Forbidden* to the user. As it is a finalizing rule, this behavior ends the request processing. | Request Phase | - |
| Enable Gzip | Enables Gzip data compression, if supported by the user's browser. | Request Phase<br>Response Phase | - |
| Enable Sliced Files | Enables segmentation of large objects into 1MB slices, if their origin supports HTTP range requests.<br><br> Use this behavior if you deliver media larger than 1MB through the CDN so that Azion can start delivering content to its users even before it has received the entire object from its origin and, thus, optimizing the performance of your website or application.<br><br> When activating this functionality, Azion will request the objects for their origin via range requests and they will be cached in Azion with advanced cache key.<br><br> If your origin does not support range requests, Azion will only be able to start delivering your content to its users after your origin has completed the complete sending of the object. | Default Rule | - |
| Enforce HLS cache | This behavior is automatically included by Azion whenever you select a Live Ingest origin. Two actions are performed in this situation:<br><br> the bypass of all your Cache Phase rules.<br>the imposition of the cache policy defined by Azion for live transmissions in HLS.<br><br>Azion's cache policy for live HLS streams is:<br><br> 5 seconds of cache for playlists (.m3u8).<br>60 seconds of cache for chunks (.ts).<br> | Request Phase | Live Ingest |
| Filter Request Header | Removes a header field to the request that will be sent to the origin. The name of the header field must be entered as an argument. | Request Phase | - |
| Filter Response Header | Removes a header field to the response that will be sent to the user. The name of the header field must be entered as an argument. | Response Phase | - |
| Forward Cookies | By using the Forward Cookies behavior, you are determining that Azion forwards to the users the Set-Cookie header received from its origin, even in a cache content situation (cache hit). To prevent a user from receiving another user's Set-Cookie session, you must list all session cookies (private cookies) for your application in the Cache Settings tab of your Content Delivery configuration, in the Advanced Cache Key section, in Cache by Cookie. | Request Phase | Application Acceleration |
| Index Document | This behavior is automatically included by Azion whenever you select a Cloud Storage origin.<br><br>You must define the name of the index document you are using on Cloud Storage, typically index.html or index.htm.<br><br>For requests where the URI ends with / the content of the index document will be delivered.<br><br>If you use folders on Cloud Storage to organize your content, be sure to include / at the end of the URIs to ensure delivery of the index document. | Request Phase | Cloud Storage |
| Optimize Images | Enables image optimization. | Request Phase | Image Optimization |
| Redirect HTTP to HTTPS | Redirects the HTTP request to the respective HTTPS URL. If the request is already HTTPS, it does not perform any behavior. | Request Phase | - |
| Redirect To<br> (301 Moved Permanently) | Redirects the user to another URL entered as an argument, using the status code *301 Moved Permanently*. As it is a finalizing rule, this behavior ends the request processing. | Request Phase | - |
| Rewrite Request | Modifies the resource path that will be requested for the origin. You can rewrite the resource path using:<br><br> a string.<br> the requisition variables (the same ones that can be used in Criteria).<br>the local variables, in the format %*{name [index]*}, with the result of capturing strings, when using the auxiliary behavior *Capture Match Groups.*<br><br> For example, if you want a user's request for the /original/image.jpg resource to be sent to its origin as /new/image.jpg, you can:<br><br>>Use the *Capture Match Groups* auxiliary behavior with the arguments:<br>_captured array name:_ capture<br>_subject:_ ${uri}<br>_regex:_ /original/(.*)<br><br>Use the *Rewrite Request* behavior with the argument:<br>/new/%{capture[1]} | Request Phase | Application Acceleration |
| Set Cache Policy | Assigns the cache policy that should be used for the request. You must set up the cache policies previously in the Cache Settings tab. In the Cache Policies you can set up the time that an object will be stored in cache and the rules for the variation of objects in cache (advanced cache key). | Request Phase | - |
| Set Origin | Assigns an origin that must be consulted by the Intelligent Edge. You must set up the origins previously in the Origins tab. | Request Phase | - |

---

## 4. Functions {#functions}

For behaviors that request a mandatory argument, such as the Behavior Set Cookie, you can use the same variables that are available in each processing phase. That way you can, for example, compose cookies or http headers using data collected from the request, such as the user's device group or their geolocation.

Azion also provides some functions to simplify the handling of your arguments:

| **Function and Argument** | Description |
|--------------------|-----------|
| ${cookie_time_offset(number)} | Returns the current date plus an offset in seconds, entered as an argument, to be used to define the expiration time of a cookie. For example, if you want the cookie to expire in 1 hour, use the Add Response Cookie behavior with the argument:br> _&lt;cookie-name&gt;=&lt;cookie-value&gt;; Expires=${cookie_time_offset(3600)}_ |
| ${encode_base64(string)} | Returns the arguments coded in base64. For example,<br> _${encode_base64(www.domain.com)} will return the value d3d3LmRvbWFpbi5jb20K_ |

---

Didn't find what you were looking for? [Open a support ticket.](https://tickets.azion.com/)

