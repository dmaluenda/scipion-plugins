# scipion-plugins
A repo grouping all scipion plugins (except xmipp) as git-submodules

## Get started:

 ```
 cd whereever/you/want
 git clone https://github.com/dmaluenda/scipion-plugins [dirName]
 cd scipion-plugins    # or dirName if passed above
 git submodule update --init
 ```

## Utils:

 - Update all the submodules:
  ```
  ./git-update-submodules	[branch=devel]

  ```
  Use it to update all the submodules [in certain branch] of this repository and commit+push the changes (the commit will contain the today's date in the message)

 - Install all the plugins via symbolic link or setting the PYTHONPATH env.var.
  ```
  ./plugins-register [options]
  
         options: SCIPION_HOME = ~/scipion
	              PLUGINS_HOME = ~/scipion-em
	              XMIPP_HOME   = ~/xmipp-bundle
	              -env : to set the PYTHONPATH instead of making a symbolic link
  ```
  Use it to register all the plugins that are in PLUGINS_HOME and XMIPP_HOME inside SCIPION_HOME/. It's done via symbolic link (default) or via PYTHONPATH (-env)
  
 - To bypass the pypip repo, fill the `plugins.json` with a certain path for a certain package to make a local installation. In addition you need to set the `SCIPION_PLUGIN_REPO_URL` in `SCIPION_HOME/config/scipion.conf` in order to point to this `plugins.json` file.
