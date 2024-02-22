#  Here are the steps to create the angular microfrontend
1. ng new mono-workspace --create-application=false
2. cd mono-workspace
3. ng g application host-app --routing --style=scss
4. ng g application microfrontend-app --routing --style=scss
5. open new terminal on root mono-workspace and run this command to install webpack
   - npm i webpack webpack-cli --save-dev
   then run the next cmd with on the same path
   - ng add @angular-architects/module-federation --project host-app --port 4200
   - ng add @angular-architects/module-federation --project microfrontend-app --port 4300
   - at root create components and configure routing for host-app
     ng g c home --project=host-app
     ng g c todo --project=host-app