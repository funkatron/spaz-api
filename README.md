SpazAPI
=======

**Since this README.md uses symlinks developers will need to be on *nix/linux platforms** -- **FRAPI performs well on Windows, however joining the two repos together might prove to be a bitch -- unless you can magically make decent symlinks on windows :D**

First of all, install FRAPI (Follow the instructions on : http://wiki.github.com/frapi/frapi/getting-started )

Then in another directory (Let's call it SPAZ\_API\_PATH)  checkout the spaz-api repo (http://wiki.github.com/davidcoallier/spaz-api) in another directory -- hint: This is where you'll be doing the Spaz API PHP Development)

Once this is done, go to the FRAPI\_PATH (Assuming you've followed the steps to installing FRAPI, you know what a FRAPI\_PATH is) and "cd" into:

	cd FRAPI_PATH/src/frapi/custom

Then remove all that's there

	rm -rf *

And now symlink all your SPAZ\_API\_PATH custom files into this directory like such

	ln -s SPAZ_API_PATH/custom/* FRAPI_PATH/src/frapi/custom

Restart apache and go to your "admin.frapi" page. You will see the actions and modules that the SpazAPI has to offer. 

You can now start hacking and testing  your actions (Which code is located into SPAZ\_API\_PATH/custom -- The actions (controllers) are in SPAZ\_API\_PATH/custom/Action)

*If you are seeing some file-access errors on the administration panel, just make sure your SPAZ\_API\_PATH/custom is writeable by the web user*

CouchDB
======= 
The SpazAPI uses CouchDB and should you decide to develop features that use CouchDB, you can ask davidc_ to give you access to the developer's CouchDB database provided by [Couchio](http://couch.io) (This way you won't have to install erlang and setup your own couch :))

Memcache
========
For rate limiting, FRAPI uses memcache on localhost. You may want to setup memcache and redis (As future versions will be using Redis
