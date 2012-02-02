Rack Maint 
==========
This plugin allows you to track physical racks and associate devices stored in ONA with a location in a physical rack.  This is an initial release of this plugin and it still has a long way to go and probably a bunch of bugs.  I hope it is useful to someone.

Install
=======

  * Unzip the archive and place it in your $ONABASE/www/local/plugins directory
        tar -C /opt/ona/www/local/plugins -zxvf pluginname.tar.gz
  * Click _Plugins->Manage Plugins_ while logged in as an admin user
  * Click the install icon for the plugin which should be listed by the plugin name 
  * Follow any instructions it prompts you with.  They may or may not include the following (some user/group names may differ on various platforms):
    * chown -R www-data /opt/ona/www/local/plugins
    * if you have not already, run the following command _echo '/opt/ona' > /etc/onabase_.  This assumes you installed ONA into /opt/ona 
  * Ensure you have prerequisites installed:
    * Currently there are none for this plugin

Usage
===== 

  * Click _Plugins->Rack Maintenance_
  * Add a new rack.  You must give it a name and a height/size.. this would be something like 42 U.
  * You will now be taken to the rack display page.  you can hover your mouse over the appropriate rack unit line on the grid. To the right of that line will be two buttons.  The left button will allow you to add a device as inserted from the front of the rack.  The add icon on the right will add a device as inserted from the back of the rack.
  * When adding a device to the rack you must give it a hight in 'U' and a depth (in quarters).
  * You must either select an FQDN of an existing ONA device or type in a general name in one of the two bottom boxes.  Obviously not all things in a rack have IP addresses and/or entries in ONA so it all depends on what you are adding.  
  * The add icons will turn to delete icons when a device is defined in the rack.
  * There are now new dcm.pl modules to use from the CLI as well:
    * rack_assignment_add
    * rack_assignment_modify
    * rack_assignment_del
    * rack_add
    * rack_modify
    * rack_del

Future
======

  * allow definition of racks that start from the bottom and go up in number
  * allow easier moves from rack positions, includes inserts, dragging etc
  * define rack adjacency.  then you can navigate from rack to rack as you view them.


