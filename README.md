bwp-minify
==========

<p>Compatibilities => up to WP_3.6.X</p>

<div class="block-content"><p>Allows you to minify your CSS and JS files for faster page loading for visitors. This plugin uses the PHP library <a href="http://code.google.com/p/minify/" rel="nofollow">Minify</a> and relies on WordPress's enqueueing system rather than the output buffer (will not break your website in most cases). This plugin is very customizable and easy to use.</p>

<p><strong>Some Features</strong></p>

<ul>
<li><strong>Scripts to not deferred (not asynchrone) Beta</strong></li>
<li>Uses the enqueueing system of WordPress which improves compatibility with other plugins and themes</li>
<li>Allows you to customize all minify strings</li>
<li>Allows you to change various Minify configuration options by editing the config file directly</li>
<li>Offers various way to add a cache buster to your minify string</li>
<li>Gives you total control over how this plugin minifies your scripts</li>
<li>Supports script localization (<code>wp_localize_script()</code>)</li>
<li>Supports RTL stylesheets</li>
<li>Supports media-specific stylesheets (e.g. 'screen', 'print', etc.)</li>
<li>Supports conditional stylesheets (e.g. <code>&lt;!--[if lt IE 7]&gt;</code>)</li>
<li>Provides hooks for further customization</li>
<li>WordPress Multi-site compatible</li>
</ul>




<p><strong>Important Notes & Changelog</strong></p>

<p>If you want to make the most out of BWP Minify, it is highly recommended that you give this <a href="http://betterwp.net/wordpress-plugins/bwp-minify/#advanced_customization" rel="nofollow">BWP Minify Advanced Customizations</a> guide a read!</p>

<h4>1.3.6</h4>

<ul>
<li>Update Minify library to (2.1.7), there was a sérious <a href="https://groups.google.com/forum/#!msg/minify/cpN-ncKPFZE/kwYVpLMkfDwJ">vulnerability</a> on all the old version</li>
<li>Fix : jquery enqueued but wrong script written after. (WP_3.6)</li>
<li>Add deferred capacity for javascript files (beta)</li>
</ul>

<h4>1.2.2</h4>

<ul>
<li>Fixed a possible fatal error on certain installations.</li>
</ul>

<h4>1.2.1</h4>

<ul>
<li>Added support for inline styles (available since WordPress 3.3).</li>
<li>Cache directory is now hidden from normal admins when used on a Multi-site environment.</li>
<li>Added additional hooks allowing developers to control Minify Tags and Minify Src, more info:  <a href="http://betterwp.net/community/topic/226/additional-hooks-filters-to-getminifytag/" rel="nofollow">http://betterwp.net/community/topic/226/additional-hooks-filters-to-getminifytag/</a> (<code>bwp_get_minify_src</code>, <code>bwp_get_minify_tag</code>)</li>
<li>Added a new hook for buster allowing developers to dynamically work with this variable (<code>bwp_minify_get_buster</code>)</li>
<li>Fixed the pass-by-references fatal error when activating the plugin on a host using PHP 5.4 or higher.</li>
<li>Fixed a possible bug where dependencies are ignored, more info: <a href="http://betterwp.net/community/topic/153/dependencies-ignored/" rel="nofollow">http://betterwp.net/community/topic/153/dependencies-ignored/</a></li>
<li>Fixed a possible bug where scripts are echoed twice.</li>
<li>Updated Turkish (tr_TR) translation - Thanks to Hakan E!</li>
</ul>

<h4>1.2.0</h4>

<ul>
<li>New Features:

<ul>
<li>Added a Flush cache button</li>
<li>Split auto minify option into two options, auto minify js and auto minify css</li>
<li>Added a new buster: theme version - thanks to Jon for the patch!</li>
</ul></li>
<li>Bugs fixed:

<ul>
<li>Fixed a bug that broke minify strings if current port is not 80</li>
<li>Fixed two bugs that broke minify strings when <code>HTTPS</code> is enabled</li>
<li>Fixed <code>wp_localize_script</code> duplication issue</li>
<li>Fixed media style duplication issue</li>
<li>Fixed a deprecate notice caused by the use of <code>print_scripts_l10n</code></li>
<li>Fixed some script dependency issue when you choose to ignore certain scripts</li>
</ul></li>
<li>Enhancements:

<ul>
<li>Increased default cache time to something longer (2 hours)</li>
<li>Cache directory can now be edited in admin area. Please note that changing the cache directory is still a two-step process, which has been described in great details <a href="http://betterwp.net/wordpress-plugins/bwp-minify/#cache_directory" rel="nofollow">here</a>.</li>
</ul></li>
<li>Misc:

<ul>
<li>Added a Turkish translation - Thanks to Hakan E.</li>
<li>Added a French translation - Thanks to Sebastien</li>
<li>Added an Italian translation - Thanks to Gabriele</li>
</ul></li>
</ul>

<h4>1.0.10</h4>

<ul>
<li>Fixed two possible PHP notices when using root-relative paths as Minify URL. Thanks to <a href="http://marcuspope.com/" rel="nofollow">Marcus</a>!</li>
<li>Fixed wrongly closed HTML <code>&lt;link&gt;</code> tags.</li>
<li>Fixed a bug that breaks the dynamic JS file enqueued by Mingle plugin.</li>
<li>Fixed an incompatibility issue with WP Download Monitor.</li>
<li>Fixed an incompatibility issue with Geo-Mashup, thanks to JeremyCherfas for reporting!</li>
<li>Added support for the new script localization function introduced in WordPress 3.3. Thanks to <strong>workshopshed</strong> for reporting!</li>
<li>Added Romanian translation, thanks to Luke Tyler!</li>
</ul>

<h4>1.0.9</h4>

<ul>
<li>Fixed a possible PHP warning about an argument not being an array.</li>
</ul>

<h4>1.0.8</h4>

<ul>
<li>Hot fix for 1.0.7, which resolves the broken CSS issues for the wp-login page when you install WordPress in a sub-directory.</li>
</ul>

<h4>1.0.7</h4>

<ul>
<li>Hot fix for 1.0.6, which resolves some compatibility issues with certain plugins.</li>
</ul>

<h4>1.0.6</h4>

<ul>
<li>Added four more hooks for theme developers to fully control how scripts and styles should be enqueued and minified.</li>
<li>Changed the Min URL hook a bit so themes can actually filter it.</li>
<li>Added support for plugins or themes that try to enqueue and print script using the <code>wp_footer</code> action instead of the <code>init</code> action. Plugins like 'Jetpack by WordPress.com' should be working correctly now.</li>
<li>Other improvements made to the positioning of styles and scripts.</li>
</ul>

<p><strong>Enjoy BWP Minify!</strong></p>

<h4>1.0.5</h4>

<ul>
<li>Added support for theme developers who would like to integreate BWP Minify into their themes 

<ul>
<li>Added a new hook added for <code>min</code> path.</li>
<li>Added new hooks to allow theme developers to only minify certain media files (see <a href="http://betterwp.net/wordpress-plugins/bwp-minify/#allowed-handles" rel="nofollow">this section</a> for more details).</li>
<li>Some bug fixes.</li>
</ul></li>
<li>A lot of improvements have been made to catch styles and scripts printed using <code>wp_print_scripts</code> and <code>wp_print_styles</code>.</li>
<li>The base (<code>b</code>) parameter has been removed from the minify string to add support for non-standard WordPress installation (<code>wp-content</code> has been moved or renamed.) Thanks to <a href="http://twitter.com/leepowell" rel="nofollow">Lee Powell</a> for bug reports and patches!</li>
<li>Fixed a bug that makes BWP Minify fail to determine the cache directory in a sub-folder installation of Multi-site.</li>
<li>Fixed a possible incompatibility issue with Easy Fancybox, thanks to Bob for reporting!</li>
<li>Minor bug fixes for login and signup pages.</li>
</ul>

<h4>1.0.4</h4>

<ul>
<li>Fixed an incompatibility issue with media files' uppercase letters.</li>
<li>Fixed a minor undefined offset notice, thanks to Torsten!</li>
</ul>

<h4>1.0.3</h4>

<ul>
<li>Fixed a compatibility issue with dynamically generated media files, thanks to naimer!</li>
<li>Not really a changelog, but <a href="http://betterwp.net/wordpress-plugins/bwp-minify/#positioning-your-scripts" rel="nofollow">a small snippet</a> for users who want to exclude CSS files has been posted.</li>
</ul>

<h4>1.0.2</h4>

<ul>
<li>Fixed a compatibility issue with other plugins loading styles and scripts on a separate .php page. Thanks to larry!</li>
<li>Also fixed a possible bug in 1.0.1</li>
</ul>

<h4>1.0.1</h4>

<ul>
<li>The plugin should now detect cache folder correctly for users who install WordPress in a sub-directory.</li>
</ul>

<h4>1.0.0</h4>

<ul>
<li>Initial Release.</li>
</ul>



<p><strong>Languages</strong></p>

<ul>
<li>English (default)</li>
<li>Romanian (ro_RO) - Thanks to <a href="www.enjoyprepaid.com" rel="nofollow">Luke Tyler, International Calling Cards</a>!</li>
<li>Turkish (tr_TR) - Thanks to Hakan E</li>
<li>French (fr_FR) - Thanks to Sebastien </li>
<li>Italian (it_IT) - Thanks to Gabriele - <a href="http://cookspot.it" rel="nofollow">http://cookspot.it</a></li>
</ul>

<p>Please <a href="http://betterwp.net/wordpress-tips/create-pot-file-using-poedit/" rel="nofollow">help translate</a> this plugin!</p>



Security fix for Minify library 
============

Please visit https://code.google.com/p/minify/


