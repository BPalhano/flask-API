# REST API using Flask, Pydantic and TinyDB

## What's REST?
REST is an abbreviation for Representational State Transfer. It is a software architectural style that provides standards for computers on the web, dictating how the systems interact.

## 5 principles of REST:

+ Client-Server Mandate
> The REST protocol allows for independent implementation for the client and the server. This independence means that both parties can make changes without knowing or interacting with one another. Defining what a server and client are is the first step to understanding this principle.

+ Statelessness

> RESTful APIs do not cache anything about the HTTP request made on the client side. Not caching means the server treats every session as new and cannot take advantage of any previous information stored on the server. To be genuinely stateless, a server does not store any authentication details of any prior session by the same client. Because a REST API is stateless, a client must provide all the necessary information every session to enable a server to complete a task. 

+ Cacheable 

> Requests on a server go through different pathways or caches. These caches can either be a local cache, proxy cache, or reverse proxy, and a RESTful API’s server can mark information as either cacheable or non-cacheable. When a client requests their end, this request goes through a series of caches. If any caches along that path have a fresh copy of the representation, it uses that cache to generate a result. When none of the caches can fulfill the request, it goes back to the origin server. A RESTful API’s servers determine whether the information is cacheable or non-cacheable. 


+ Uniform Interface
> A system that utilizes the REST API has the client and the server interacting predictably. A resource in the system follows only one logical Uniform Resource Identifier (URI). What differentiates RESTful APIs from non-REST APIs is the uniformity of this interface regardless of the device or application used. Resources on a REST API use Hypermedia as the Engine of Application State (HATEOAS) to fetch related information whenever applicable. All resources on RESTful APIs follow specific guidelines with naming conventions and link formats.

+ Layered System 
> A RESTful API relies on a layered system to deliver results. This layered system provides a hierarchy that constrains a layer from seeing beyond the layer that it is assigned to. This layered system allows the developer to deploy various functions to different servers. Each layer works independently, and each layer does not know the functionality of other layers besides its own. On the user end, a layered system does not allow the user to ordinarily differentiate whether they are connected to a primary or intermediary server. The importance of intermediary servers is their ability to provide load-balancing cache sharing. 

## What's the main difference between REST and CRUD?

Because of the similarities between REST and CRUD, it’s easy to mistake them for having the same function. But that’s far from the truth. Delving a little bit deeper explores the differences between them. 

* REST is an architectural system centered around resources and Hypermedia using HTTP commands. CRUD is a cycle meant to maintain records in a database setting. In its base form, CRUD is a way of manipulating information, describing the function of an application. REST is controlling data through HTTP commands. It is a way of creating, modifying, and deleting information for the user. 
* CRUD functions can exist in a REST API, but REST APIs are not limited to CRUD functions. CRUD can operate within a REST architecture, but REST APIs can exist independent of CRUD. For example, a REST API can allow clients to reboot a server even if it doesn’t correspond to any CRUD functions. REST can do this as long as it uses the proper HTTP methods. 
* REST usually refers to using data through HTTP commands. It’s a dogma to facilitate how users manipulate data onscreen and the information that’s being saved on the server. Programmers can create a REST API that can handle the essential CRUD functions, but the same can’t be said the other way around. 
* The functions of REST and CRUD are similar (as discussed above), but they are not the same. PUT replaces a resource, even one that doesn’t exist yet. POST adds a new resource. Both of these commands create a new resource, but PUT is usually used to update resources that are already there. PATCH is mainly used to update a part of a resource, but PUT is used only to update an entire resource by replacing it. 
