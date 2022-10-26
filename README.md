# Token Embed Views

## Description

This module creates a site token called 'views-embed'. This token can be used to embed
your views into your content. 


## Prerequisites

You need the views module (which is part of Backdrop's core).
You also need the token_filter module to enable token replacing in your node 
fields if you wish to use these tokens in node fields like body, etc.

## Usage

The Backdrop version uses two different syntaxes for the token:

New syntax (Backdrop):
`[site:views-embed:view-name:display-id:arg1/arg2/arg3]`

Old syntax (Drupal 7 version):
`[views:embed:view-name:display-id:arg1/arg2/arg3]`

This will assure that ported sites from D7 that used the second syntax will still work.

## Problems with entity caching and tokens

Backdrop caches node pages. After the initial page visit, subsequent page requests are served directly from the Backdrop cache, and therefore any embedded tokens will not be dynamically fulfilled. This causes issues with views that change often, or with fields that are not supposed to be seen by non-admin users, like the Views' "Edit" link for nodes. Backdrop will serve the cached version of the node, meaning that you will end up with a stale version of the View, or a link that's not supposed to be shown.

To fix this situation, you need to download the [Entity Cache Administration](https://backdropcms.org/project/entity_cache_admin) module, which allows you to disable caching for specific entity types (for example for specific Content Types).

## Configuration

There is no specific configuration for this module.

If however, you wish to use this token in your node fields like body, then you 
need to have the token_filter module. Enable the token_filter module and you 
need to enable the "replace tokens" filter in your text formats in the 
text format options under admin/config/content/formats.

## Installation

- Install this module using the [official Backdrop CMS instructions](https://backdropcms.org/guide/modules)


## Current Maintainers

- [Alejandro Cremaschi](https://github.com/argiepiano)

## Credits

- Ported to Backdrop by [Alejandro Cremaschi](https://github.com/argiepiano)
- Original Drupal maintainer: [Tim Bozeman](https://www.drupal.org/tim-bozeman)

License
---------------

This project is GPL v2 software. See the LICENSE.txt file in this directory
for complete text.
