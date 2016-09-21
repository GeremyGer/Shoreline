Aqua Monitor shows how the Earth's surface water has changed during the last 30 years.

http://aqua-monitor.appspot.com

See also the following Nature Climate Change paper: http://nature.com/nclimate/journal/v6/n9/full/nclimate3111.html

# How to build?

Install Node.js, which is used by build scripts to compile sources and prepare everything for deployment.

Then run the following commands:

* npm install - downloads and installs all packages required to build the app (see packages.json)
* bower install - downloads and installs all client-side packages (see bower.json)

After that, run:

* gulp build - compiles everything (minifies code, generates styles, etc.) and places results in dist/

The resulting dist/ directory can be used to deploy everything as a Google App Engine app.

Use "gulp watch" to monitor sources continuously during development - they will be automatically compiled into dist/ on every change. 
See gulpfile.babel.js for the rules used to do this.

# How to run and deploy?

To deploy the Aqua Monitor under Google App Engine. The following files need to be added / modified:

* app/privatekey.pem - add your service account key, this is used by Python backend.
* app/config_web.py - add your client id, secret and refresh token, used at runtime to generate access to GEE for the JavaScript code. 




