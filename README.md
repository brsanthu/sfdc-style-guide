Salesforce Style Guide
======================

This document is colloborative (hopefully) effort from the community to define/document the coding styles that one could follow. 

This style is not necessarily the only way and so you may define your own that suits you/your company. While document takes a stand on some of the very **opinionated** standards like tab for indentataion, tab width as 4 spaces, Java style cursor placement etc., which you may not agree with and that is completely fine. So please feel free to take the bits you like and adopt your own.

# Apex Coding (Classes, Triggers, Controllers)
## Keywords
All keywords must use lower case, that means never write them in upper case or Upper Camel case etc.


# Classes
## Namespace
Salesforce could have done a better job to provide the namespace capability (may be similar to Java packages). I know there is packages but it is not that easy to use.

Generally most of the orgs develop all of their code in default namespace, aka unpackaged in Salesforce terms. When you do that, every class/vf page you create share the same namespace so you will have to be clever to minimize the conflicts. One convention that some orgs have adopted is to prefix your classes/vf pages with team or module name. I think may be prefix based on functional module is fine but prefixing based on the team name is bad idea in my opinion. This is because teams will get changed, renamed, replaced or moved but they leave their unsigtly legacy in code (visible to customers) all over the code.

If you prefer to use namespace prefix, define a set of very controlled acceptable namespaces for your org. For ex., 
```
Support => for anything related to Case management
Sales => For anything related to Lead, Opty, etc
Order
License
```

## Class Names
Must always be named in [UpperCamelCase](http://c2.com/cgi/wiki?UpperCamelCase) convention. So in the code when you look at a UpperCamelCase type, you know it is either Class Name or SObject Name.
