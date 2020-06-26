## The History interaction

The history interaction is used by the service to document events that have occured to a specific resource or the entire Master Person Index repository.

The history interaction retrieves the history of either a particular resource, all resources of a given type, or all resources supported by the system. These three variations of the history interaction are performed by HTTP GET command as shown:
~~~
  GET [base]/[type]/[id]/_history{?[parameters]&_format=[mime-type]}

  GET [base]/[type]/_history{?[parameters]&_format=[mime-type]}

  GET [base]/_history{?[parameters]&_format=[mime-type]}
~~~ 

The return content is a Bundle with type set to history containing the specified version history, sorted with oldest versions last, and including deleted resources. Each entry SHALL minimally contain at least one of: a resource which holds the resource as it is at the conclusion of the interaction, or a request with entry.request.method The request provides information about the result of the interaction that led to this new version, and allows, for instance, a subscriber system to differentiate between newly created resources and updates to existing resources. The principal reason a resource might be missing is that the resource was changed by some other channel rather than via the RESTful interface. If the entry.request.method is a PUT or a POST, the entry SHALL contain a resource.
