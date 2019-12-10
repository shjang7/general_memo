# Git memo
##### Set always commit for merge
```
$ git config --global --add merge.ff false
```

##### Remove all untracked files and folders
```
$ git clean -fd
```

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

##### Push heroku
```
$ heroku git:remote -a [name of heroku app]
$ heroku run rails db:migrate
$ heroku run rails db:seed
```

##### Rubocop code style check
```
$ rubocop --auto-correct   
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

# General memo
##### Get some dummy texts
```
https://hipsum.co
```

# CSS memo
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
