SpazAPI
=======

*Since this README.md uses symlinks developers will need to be on *nix/linux platforms -- FRAPI performs well on Windows, however joining the two repos together might prove to be a bitch -- unless you can magically make decent symlinks on windows :D*

First of all, install FRAPI (Follow the instructions on : http://wiki.github.com/frapi/frapi/getting-started )

Then in another directory (Let's call it SPAZ_API_PATH)  checkout the spaz-api repo (http://wiki.github.com/davidcoallier/spaz-api) in another directory -- hint: This is where you'll be doing the Spaz API PHP Development)

Once this is done, go to the FRAPI_PATH (Assuming you've followed the steps to installing FRAPI, you know what a FRAPI_PATH is) and "cd" into:

	cd FRAPI_PATH/src/frapi/custom

Then remove all that's there

	rm -rf *

And now symlink all your SPAZ_API_PATH custom files into this directory like such

	ln -s SPAZ_API_PATH/src/frapi/custom/* FRAPI_PATH/src/frapi/custom

Now go back to your FRAPI_PATH 

	cd FRAPI_PATH

And then go into:

	cd FRAPI_PATH/src/frapi/admin/application/config/app/

and remove what's there

	rm -rf *

And symlink the SPAZ_API_PATH config files into there like such

	ln -s SPAZ_API_PATH/src/frapi/admin/application/config/app/* FRAPI_PATH/src/frapi/admin/application/config/app


Restart apache and go to your "admin.frapi" page. You will see the actions and modules that the SpazAPI has to offer. 

You can now start hacking and testing  your actions (Which code is located into SPAZ_API_PATH/src/frapi/custom -- The actions (controllers) are in SPAZ_API_PATH/src/frapi/custom/Action)


CouchDB
======= 
The SpazAPI uses CouchDB and should you decide to develop features that use CouchDB, you can ask davidc_ to give you access to the developer's CouchDB database provided by Couchio|http://couch.io (This way you won't have to install erlang and setup your own couch :))
