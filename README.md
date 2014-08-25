Dockyard Ember Rails Tutorial
=======================

The tutorial backing this repository can be found here:

http://reefpoints.dockyard.com/2014/05/07/building-an-ember-app-with-rails-part-1.html

http://reefpoints.dockyard.com/2014/05/08/building-an-ember-app-with-rails-part-2.html

http://reefpoints.dockyard.com/2014/05/09/building-an-ember-app-with-rails-part-3.html

http://reefpoints.dockyard.com/2014/05/31/building-an-ember-app-with-rails-part-4.html

There never was a Part 5 regarding deployment to Heroku as [Dockyard had a parting of the ways with Heroku](http://reefpoints.dockyard.com/2014/06/23/goodbye-heroku.html).

### Notes

After adding `landing-page-test.js` we should only be seeing one error but I get a second one, `tests/integration/landing-page-test.js: line 10, col 5, 'Ember' is not defined.`.

Fixes [here](http://stackoverflow.com/questions/24312362/ember-cli-fix-for-ember-is-not-defined)

I added `import Ember from "ember";` to my `landing-page-test.js` file. Adding `Ember: true` to `.jshintrc` didn't work.

### Run

Without rails

```bash
$ cd ember
$ ember server
```
with rails

```bash
$ cd ember
$ ember server --proxy http://localhost:3000
$ cd rails // in another terminal window
$ rails server -p 3000
$ postgres -D /usr/local/var/postgres // in another terminal window
```

Tests are here

<http://localhost:4200/tests>

### ToDo

1. Add grunt ES6 transpiler task so that we can see what our code looks like in ES5 as well.

see <https://www.npmjs.org/package/grunt-es6-transpiler>

2. Change app name from `dockyardemberrails` to `adelaideember`.



