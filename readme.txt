=== Plugin Name ===
Contributors: GaryJ
Donate link: http://code.garyjones.co.uk/donate/
Tags: genesis, js-no-js
Requires at least: 3.0
Tested up to: 3.1.2
Stable tag: 1.0

Make front-end styling based on whether JS is enabled or not easier for child themes on the Genesis theme framework.

== Description ==

Adds a `no-js` body class to the front-end, and a script on `genesis_before` which immediately changes the class to `js` if JavaScript is enabled. This is how WP does things on the back-end, to allow different styles for the same elements depending if JavaScript is active or not.

== Installation ==

1. Unzip and upload `genesis-js-no-js` folder to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

= What does this plugin actually do? =

If you look at the source of a WordPress back-end page, you'll see it has a body class of `no-js`. Immediately after the opening `body` tag is a small script which replaces `no-js` with `js` (you can see the amended class with Firebug / Inspector).

WordPress uses this to apply different styles to the same elements, depending on whether JavaScript is present or not.

This plugin recreates the same effect, but for the front-end of Genesis child themes.

= Shouldn't the script be at the end of the page? =

Usually, yes, but it's a fairly small script, so doesn't block rendering of other content for any noticeable length of time.

Doing it immediately also reduces a flash of incorrectly styled content, as the page loads with `no-js` styles, and then switches to `js` once everything has finished loading.

== Changelog ==

= 1.0 =
* First public version.

== Upgrade Notice ==

= 1.0 =
Update from nothingness. You will feel better for it.