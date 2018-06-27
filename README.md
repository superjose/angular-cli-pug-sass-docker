# Angular 6, Angular-CLI Pug, Sass, Docker
This is a blank app with Angular 6, Angular-CLI 6, Pug, Sass, and Docker support. 

There's a step by step tutorial on [medium](https://medium.com/@josjaviasilis/using-docker-docker-compose-angular-cli-6-sass-and-pug-jade-160896dfd208).

# How to use:
* Run `docker-compose up` 
* Navigate to `http://localhost:4200`
* Enjoy  😊
* Supports Webpack Hot Module Reloading via polling. 

# Files that you'd like to pay attention to
* [Dockerfile](./Dockerfile)
* [docker-compose.yml](./docker-compose.yml)
* [ng-add-pug-loader.js](./ng-add-pug-loader.js) (We changed async methods to sync! See [Medium post Step #4](https://medium.com/@josjaviasilis/using-docker-docker-compose-angular-cli-6-sass-and-pug-jade-160896dfd208#0a95))
* [package.json](./package.json)



# Some notes:
* There's a vulnerability in one of the packages. There's an outdated version of Hoek (as of this writing - June 27th, 2018) that seem to be causing issues. (The following GitHub issues are open)
  * https://github.com/angular/angular-cli/issues/10480
  * https://github.com/sass/node-sass/issues/2355
* Thanks [@danguilherme for his ng-add-pug-loader](https://github.com/danguilherme/ng-cli-pug-loader)!
* We use docker-compose version 3.6 just for the sake of using the newest version. There's no special syntax, so you can safely downgrade it (if you really need to).
* We had to modify [`ng-add-pug-loader.js`](./ng-add-pug-loader.js) to use synchronous methods. It was giving problems. 

