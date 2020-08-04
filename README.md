# Git memo
##### Set always commit for merge
```
$ git config --global --add merge.ff false
```

##### Remove all untracked files and folders
```
$ git clean -fd
```

##### Change previous commit history
```
$ git rebase -i --root
$ git commit --amend
$ git rebase --continue
```

##### Check git log graph
```
$ git log --graph --oneline
```

# AWS
### RDS - PostgreSQL
- create database with free tier option
- #connectivity: create new VPC (or set proper VPC setting for rds)
- #connectivity - additional connectivity configuration - Publicly accessible: yes
- create button

# linux commands
##### find program location
```
$ locate -b '\atom'
```

# Node memo
##### update method
- consider to use lodash npm _.merge

# API memo
##### json placeholder website
http://jsonplaceholder.typicode.com/

##### axios
Promise based HTTP client for the browser and node.js

##### async-await
async means a function returns a resolved Promise. await means wait until the Promise settles and return its result.

# Typescript
##### Type
easy way to refer to the different properties + functions that a value has

# Rails memo
##### Rails new default option set
- postgresql default database / not using minitest / skip coffee auto generating
```
# ~/.railsrc
--database=postgresql
-T
--skip-coffee
```

##### After rails new with postgresql
```
$ rails db:create
$ rails db:migrate
```

##### After setting back-end environment, check working
$ curl -H "Content-Type: application/json" -X POST -d '{"username":"1st_user","password":"foobar"}' http://localhost:3001/login

$ curl -H "Content-Type: application/json" -X POST -d '{"username":"2nd_user","password":"foobar"}' http://localhost:3001/login

##### Push heroku
```
$ heroku git:remote -a [name of heroku app]
$ heroku run rails db:migrate
$ heroku run rails db:seed
```

##### Rubocop code style check
- Choose the option one of this below
```
$ rubocop -x
$ rubocop --auto-correct
```

- Make exception
```
$ rubocop --auto-gen-config  
```

##### Postgresql restart
```
$ sudo service postgresql restart
```

##### Server restart
```
$ ps -aef | grep rails    
$ kill -9 [pID]   
```

##### Rails console save error
```
> p.errors.messages
```

##### Heroku rails app image not showing
- config > environments > production.rb
```
config.assets.compile = true
config.assets.digest = true
```

##### heroku server reset
```
$ heroku pg:reset DATABASE
```

##### Haml
- [tutorial](http://haml.info/tutorial.html)

##### Nested form
- with stimulus

##### Active Storage
- [tutorial](shorturl.at/ehOX2)

##### Rails 6 connect bootstrap
- [tutorial](https://www.youtube.com/watch?v=bn9arlhfaXc)

# General memo
##### E-R diagram tool
https://app.lucidchart.com/

##### Get some dummy texts
```
https://hipsum.co
```

# CSS memo
##### sass watch
- basic
```
sass --watch scss/style.ss:dist/css/style.css
```
- compressed
```
sass --watch scss/style.ss:dist/css/style.min.css --style compressed
```

##### gradient picker
- https://uigradients.com

##### css 3 generator
- https://css3generator.com/

##### float with clearfix
```
<div class="clearfix">
  <div class="float-left">
  </div>
</div>

.clearfix:after {
   content: ".";
   visibility: hidden;
   display: block;
   height: 0;
   clear: both;
}
```
