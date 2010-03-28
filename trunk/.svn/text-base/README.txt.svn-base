All roles, and permissions will be done via the interface. The only thing defined in the code will be the defaults, which can be overriden in the engine interface. It is imperitive that the code be introspected and permissions be granted on the top layer, being the application.

Access will be managed on a ARO level, that of which being a ActiveRecord model object. ARO's can be grouped into aro_groups, which allow for request objects, in this case the Model, User, can be grouped into "Admins", and Admins can have an ACL defined for them, which is a group of ACO (Access Control Objects). Each method within a ActiveRecord object, gets defined as a Access Control Object which can have a Allow or Deny permission on it.

Similarily found, the ActiveController methods would also follow this same principle to control each of the display views.

There will need to be a ActiveHelper that will be created which does simple checks on each field, such as for a form where the user only has access to modify the Body, but not the title. Each field will need a wrapper so the developer can do something like this <%= text_field ..... if rails_acl_grant :object, :field %> or something of the like. Exact syntax has not been defined yet.

When you install, the entire system will be empty, but the infrastructure will be there. The application using RailsACL will be introspected and all ActiveRecord and ActiveController objects will have a respective ACO for each of their methods.

In this fashion, you can extend the RailsACL to control pretty much anything, whether it’s a view, a helper etc. By default, the system will be configured on all Models (ActiveRecord), and Controllers (ActiveController), but the infrastructure can handle pretty much any type of request. Not just model permissions.
