David's Twitter Aggregator plugin (wp-tweet-aggregator)
===================

Wordpress Plugin, allows you to specify twitter accounts from which to aggregate and output tweets. It does some resource saving caching too (5 minute cache). I wanted to call it Alligator, but there's already a commercial plugin with that name. 

## Caveat

This is a first complete, working version. Extracted from a new client website and used as a learning experience for building plugins correctly. Provided under GPL2 which is 'as is' and 'without warranty.'

## Installation

Download [the ZIP tarball](https://github.com/davidlowry/wp-tweet-aggregator/archive/master.zip "latest ZIP file") and upload to your Wordpress installation as a new plugin.

You don't need to update any configuration files by hand.

## Twitter Application Setup

At the moment, you are required to set up or use an existing [Twitter App's authentication token + secret](https://dev.twitter.com/apps "Create a new twitter app for authentication"). The plugin's form will guide you as to the callback URL required for the app.

## Setup

Once uploaded and activated (through the Wordpress admin > plugins page), click on the new Admin Menu button and follow the instructions. The 20 character _Consumer Key_ and the 38 character _Access token_ are to be inserted, and then you can specify one or many twitter screen names to use.

## Usage

A widget 'Twitter Aggregator (Basic)' has been added to your Widgets configuration screen, drag it onto the sidebar of your choice. It should now appear on any page or post which has that sidebar. Note you'll need to clear any active cache for the widget to show on screen.

## Scripting

Assumes jQuery is installed. I'll endeavour to rewrite that to pure JS.

## Styling

Currently the plugin includes some basic styling to output white blocks with aligned . Assumes you already are using some form of *reset.css*.

Included in the plugin is a stylesheet DL_TA.sidebar.css - you can overwrite it or override the contents in your own stylesheet. 

## Notes

The plugin includes the [**twitteroauth**](https://github.com/abraham/twitteroauth [Abraham's Twitter OAuth Library]) and my own **dlfs** wrapper, which abstracts a few awkward WP_Filesystem operations. Both should be sufficiently isolated that they don't interfere with any other plugin, but I intend to further wrap them just incase. 

## Future plans

* Rewrite simple jQuery functions to JS (remove jQuery requirement)
* Alter CSS to provide basic structure and/or input form for custom styling
* See if there's any way to avoid having to start with token + keys.
