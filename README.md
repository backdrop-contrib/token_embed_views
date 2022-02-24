# Token Embed Views

## Description

This module create a token type called 'views'. This token can be used to embed
your views into your content. 


## Prerequisites

You need the token module and the views module (which are part of Backdrop's core).
You also need the token_filter module to enable toking replacing in your node 
fields if you wish to use these tokens in node fields like body f.ex.

## Usage

Example: `[views:embed:view-name:display-id:arg1/arg2/arg3]`

## Installation

To install, copy the token_embed_views directory and all its contents to your 
modules directory.

To enable this module, visit Administration -> Modules, and enable 
token_embed_views.


## Configuration

There is no specific configuration for this module.

If however, you wish to use this token in your node fields like body, then you 
need to have the token_filter module. Enable the token_filter module and you 
need to enable the "replace tokens" filter in your text formats in the 
text format options under admin/config/content/formats.

## Current Maintainers

- [Alejandro Cremaschi](https://github.com/argiepiano)

## Credits

- Ported to Backdrop by [Alejandro Cremaschi](https://github.com/argiepiano)
- Original Drupal maintainer: [Tim Bozeman](https://www.drupal.org/tim-bozeman)

License
---------------

This project is GPL v2 software. See the LICENSE.txt file in this directory
for complete text.
