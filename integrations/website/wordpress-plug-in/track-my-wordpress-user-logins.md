# track my WordPress user logins?

How to track user logins on my WordPress website

In order to track user logins form your website, you need to add the data to the user profile:

There are multiple ways to achieve this but we recommend to use a plugin called [Code Snippets](https://wordpress.org/plugins/code-snippets/). Code Snippets allows you to add code to your site without the need to mess around with templates, etc

Once you have installed the plugin, simply create a new snippet and add this code:

```
function hook_javascript() {

?>
<script type="text/javascript" src="//script.leadboxer.com/?dataset=YOUR DATASETID HERE"></script>		
    <?php
		};

function hook_identification() {

	$user_info  = wp_get_current_user();
	$user_email = $user_info->user_email; 
	$user_firstname = $user_info->user_firstname; 
	$user_lastname = $user_info->user_lastname; 
?>
		
<script type="text/javascript">

	// define an empty variable called 'map' 
	var map = new OTMap();

	//define one or multiple properties to be added to the visitor profile 
	map.put("firstName", "<?php echo $user_firstname; ?>"); 
	map.put("lastName", "<?php echo $user_lastname; ?>"); 
	map.put("email", "<?php echo $user_email; ?>"); 


	//send (submit) the data to LeadBoxer 
	OTLogService.sendEvent("Login added", map, false);

</script>
    <?php
		}
	
function lb_function()
{
    if ( is_user_logged_in() ) 
    {
        add_action('wp_head', 'hook_identification');
    }
}

add_action('wp_head', 'hook_javascript');
add_action('init', 'lb_function');<br>
```

Paste the above inside the snippet to to send us a signal when a user logs in to your system. This will add that first and lastname and email address to the visitor profiles. You can use any data available like usernames, LoginID, etc.

#### Notes:

* Replace the datasetID with your own
* Enable the snippet to run everywhere.
* And don't forget to disable the regular LeadBoxer Wordpress plugin, or remove the tracking pixel from your templates, etc. as it is included in the above script.

Still need help? [Contact Us](broken-reference)

Last updated on July 30, 2019
