# Grad College Content Types

This is a custom migration module intended to define and generate custom content types for the UA Graduate College website, specifically the funding opportunity and the FAQ content types.


## Installation

This module can be installed as any other normal Drupal module.

## Maintenance

If something in this module needs to change, it helps to understand the underlying Drupal tech. Basically, there's three components that make this work:

- *Configuration Files* These are in the `config/install` directory. They're a series of YAML files that are consumed on module install to generate the content type. If these need to be chaanged, the easiest thing to do is edit the content types, use the `Configuration Sync` feature in the admin console to re-export the configuration and use that to re-generate the config file(s).

- *CSS Files* Custom, normal CSS for page elements setup in the content types. If new CSS files need to be added, they need to be specified in the grad_content_types.libraries.yml file.

- *Module File* Custom Drupal module code. All this does is attach the CSS files (see above) to whatever page(s) they need to be present for to work. Use the existing code to model any necessary changes. This is not the place for anything overly complicated or out of scope of attaching CSS files to pages.
