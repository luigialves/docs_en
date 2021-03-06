# Edge **Services**

[Edit on GitHub <svg width="14" height="14" xmlns="http://www.w3.org/2000/svg"><g fill="none" stroke="#F3652B"><path d="M4.81.71H.672v11.43H12.1V8.001" stroke-width=".8"/><path d="M6.87.786h5.155V5.94M6.31 6.5L12.026.786"/></g></svg>](https://github.com/aziontech/docs_en/edit/master/edge-orchestrator/edge-services/index.md)

Azion Edge Services is a module for the Edge Orchestrator product that allows orchestrated services to be managed within your own edge infrastructure, allowing resources and other configurations to be registered through Real-Time Manager and services to be created and customized so that they can be orchestrated at specified Edge Nodes.

You can configure the triggers for installing, uninstalling, reloading and defining the dependencies between the resources needed to run your service on your edge network.

> 1. [How does it works?](#how-it-works)
> 2. [Hands-on](#hands-on)
> 5. [Supporting documentation](#support-documentation)

---

## 1. How does it works? {#how-it-works}

By using Azion as your Edge platform, you can create and customize services to run on private and hybrid edge networks. Azion Edge Services operates using triggers to install, uninstall and reload, defines dependencies between resources and implements, natively, a set of Azion functions, such as Edge Applications, Edge Firewalls and Edge Functions, using the Azion Cells technology from Azion as its basis. This way, you can build Edge Applications for a wide variety of uses, ranging from high-quality, highly scalable CDNs, to hosting web applications, AI applications, VR and many others. To do so, you need to activate Azion Cells and define the Edge Nodes that should handle certain applications, and control everything from the control panel or APIs, using a centralized interface with variable access control.

### Resources

To be able to orchestrate services on your device, you need to configure the resources necessary to install, uninstall and reload.

A "Shell Script” type of resource indicates that the resource will be installed and run according to the selected *trigger*. The Edge Orchestrator agent uses the *sh-bang* placed in the content header to run the script and, if not available, it uses the POSIX-compatible shell in the device (*/bin/sh*).

A "Text” type of resource indicates that the content will be copied as plain text to the device. "Text” type resources are usually used for configuration files.

All resources are run using the path referred to in the registration. The "Path" field refers to the file's absolute path. Therefore, only directories starting and ending with "/" are accepted. Paths beginning with ".", ".." or "~" will not be accepted and are not supported.

When entering the content of your resource, it can contain a script, to be run as "Shell Script", or a “Text” type, when it is content for the resource’s configuration files. Both are compatible with using variables, as long as the tag "{{VARNAME}}" is included.

Variables in the resources’ content may be used if they use the tag "{% raw %}{{ VARNAME }}{% endraw %}". For example:<br />
{% raw %}`port = {{ PORT_HTTP }}`{% endraw %}

### Triggers

When configuring "Shell Script" type resources, you need to define which triggers will cause the resource to be executed.

The triggers are "Install", "Reload" and "Uninstall” and each has a function and order of execution:
1) Install: this is the first to be executed and must include the script needed to install the service.

2) Reload: when configured, this will be executed at the end of the installation of all the resources and also whenever there is any change to the links between the Edge Service and Edge Node, such as a change to the values of the variables.

3) Uninstall: this is executed every time the link between the Edge Services and Edge Node is broken, i.e. whenever the service is deleted from the Edge Nodes for which it was provisioned.

### Variables

Variables are dynamic values that affect the Edge Services that will be orchestrated and run on Edge Nodes. In other words, it is possible to orchestrate and run the same service, on different devices, with different values for the settings, such as configuring a service on port 3306 on one device and on port 3307 on another device.

### Link to the Edge Node

All registered services can be orchestrated and run on one or more Edge Nodes on your private network.

Only active services will be available for orchestration on the Edge Node and, after it has been linked, you can change the value of existing variables or delete or add new services to the device.

---

## 2. Hands-on. **Creating an Edge Service Step by Step** {#hands-on}

### Creating a Service

1- Go to [Real-Time Manager](https://manager.azion.com/);

2- From the top left menu, choose the *Edge Libraries* item and select the *Edge Services* page;

3- Click on the "Add Service” button. Note: your service will be created automatically. You can change the name of the service by clicking on "My New Service" in the name bar.

4- On the Resources list, click on "Add Resource";

5- Configure the resources you need for your service, using triggers "*Install*", "*Reload*" and "*Uninstall*";

6- Optional: where you have used variables in the content of one or more resources, you can set the default values for them in the "*Environment*" tab. Note: The variables must be in the format "Variable = Value", where "Variable" has been used in the content of resources that are already registered.

7- Activate the service. Done, now your service can use one or more edge nodes.

---

## 3. Supporting documentation {#support-documentation}

- [Edge Node](https://www.azion.com/en/documentation/products/edge-orchestrator/edge-node)
- [Edge Orchestrator](https://www.azion.com/en/documentation/products/edge-orchestrator)

---

Didn't find what you were looking for? [Open a support ticket.](https://tickets.azion.com/)
