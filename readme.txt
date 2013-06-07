................................
.......	OpenSkin Basic - Alpha1
.......................
.......	MyBB 1610
............

Warning, Read this!
--------------------
In order to implement all features we plan for OpenSkin, 
some core edits have to take place. If you rely on certain
plugins or other stuff that isn't "core", please check in the
plugin compability list if the plugin is compatible:
 >>>>>>>>link here <<<<<<<<<
 And please let us know if it isn't, OpenSkin always seeks to improve 
 MyBB in every aspect, we take your suggestions seriously

We (the creator of OpenSkin) take no responsibility 
for damages OpenSkin might cause to you. Having that
said there is a good chance you will get free support
on the forums: http//:voxelhost.net
and at: mybb.com/forumthread


Requirements
-------------
SCEditor (due to the default editor being broken, you'll love this editor :)
Download:  		https://github.com/samclarke/SCEditor-MyBB/tags


Core Edits
-----------
	bootstrap.js
	LINE	xxx
	--------------
	Reason: Tooltip conflict with Prototype 

	member.php
	-------------
	Reason: Dynamic profile avatar size, if you don't need this because your users upload big enough avatars to your board, you dont have to upload this. However this edit is recommend.
		LINE	1515
		$avatar = "<img src=\"{$memprofile['avatar']}\" alt=\"\" $avatar_width_height />";
		CHANGED TO:
		$avatar = "<img src=\"{$memprofile['avatar']}\" alt=\"\" class=\"profileAvatar\" />";

	Reason: Anoying hardcoded HTML, template please!
		LINE 2033
		$buddy_options = "<br /><a href=\"./usercp.php?action=do_editlists&amp;delete={$mybb->input['uid']}&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/remove_buddy.gif\" alt=\"{$lang->remove_from_buddy_list}\" /> {$lang->remove_from_buddy_list}</a>";
		CHANGED TO:
		$buddy_options = "<li><a href=\"./usercp.php?action=do_editlists&amp;delete={$mybb->input['uid']}&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/remove_buddy.gif\" alt=\"{$lang->remove_from_buddy_list}\" /> {$lang->remove_from_buddy_list}</a></li>";

		LINE 2037
		$buddy_options = "<br /><a href=\"./usercp.php?action=do_editlists&amp;add_username=".urlencode($memprofile['username'])."&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/add_buddy.gif\" alt=\"{$lang->add_to_buddy_list}\" /> {$lang->add_to_buddy_list}</a>";
		CHANGED TO
		$buddy_options = "<li><a href=\"./usercp.php?action=do_editlists&amp;add_username=".urlencode($memprofile['username'])."&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/add_buddy.gif\" alt=\"{$lang->add_to_buddy_list}\" /> {$lang->add_to_buddy_list}</a></li>";

		LINE 2043
		$buddy_options .= "<br /><a href=\"./usercp.php?action=do_editlists&amp;manage=ignored&amp;delete={$mybb->input['uid']}&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/remove_ignore.gif\" alt=\"{$lang->remove_from_ignore_list}\" /> {$lang->remove_from_ignore_list}</a>";
		CHANGED TO
		$buddy_options .= "<li><a href=\"./usercp.php?action=do_editlists&amp;manage=ignored&amp;delete={$mybb->input['uid']}&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/remove_ignore.gif\" alt=\"{$lang->remove_from_ignore_list}\" /> {$lang->remove_from_ignore_list}</a></li>";

		LINE 2047
		$buddy_options .= "<br /><a href=\"./usercp.php?action=do_editlists&amp;manage=ignored&amp;add_username=".urlencode($memprofile['username'])."&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/add_ignore.gif\" alt=\"{$lang->add_to_ignore_list}\" /> {$lang->add_to_ignore_list}</a>";
		CHANGED TO
		$buddy_options .= "<li><a href=\"./usercp.php?action=do_editlists&amp;manage=ignored&amp;add_username=".urlencode($memprofile['username'])."&amp;my_post_key={$mybb->post_code}\"><img src=\"{$theme['imgdir']}/add_ignore.gif\" alt=\"{$lang->add_to_ignore_list}\" /> {$lang->add_to_ignore_list}</a></li>";










Installation Instructions
--------------------------

1. Back up following files, OpenSkin replaces some of MyBB's core files (not many :P )
2. Upload the theme files
3. 


Recommendations




