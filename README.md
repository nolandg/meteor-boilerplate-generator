Load the big Meteor JavaScript files asynchronously.

This is intended as a partner package to [Crater Bunny](https://github.com/nolandg/meteor-crater-bunny)
to make Meteor landing pages super fast and score 100/100 on [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/).
Using this package eliminates the long wait on initial empty-cache page load and allows the browser
to completely render the app before the 1MB+ of script arrives.

This package can be used separately and simply overrides the core Meteor `boilerplate-generator` package and
adds `async` to the `<script>` tags where appropriate.

# Installation
1. Set an environment variable `METEOR_PACKAGE_DIRS` to any directory
1. Download and unzip this package to the directory above
1. When you build your project, Meteor should find this package and use it instead of the core package

# Usage
Run you app in production mode:
````
meteor --production
````
View page source and you should see `async` in the Meteor `<script>` tags.
