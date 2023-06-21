# wwwroot
Static files can be stored in any folder under the wwwroot and can be accessed with a relative path to that root
files: css, js, lib, favicon.ico

In order to serve the static files, you need to include the app.UseStaticFiles() middleware

# Can we rename the wwwroot Folder?
Yes, need to call .UseWebRoot("MyWebRoot") to config webroot folder

