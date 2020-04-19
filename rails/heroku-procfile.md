# Create a Heroku Procfile

When you're running apps on Heroku, you can specify commands to run for
different processes on your app. A common error I ran into when I was first
developing Rails applications and deploying them to heroku was watching them
break because I included a migration but hadn't yet logged in to run the
migration. 

This basic Rails Procfile, included in the application root, will always run
migration during the release phase in the app. For large-scale professional
applications this might not be the desired setup, as you might need to hold off
on running a migration until a specified time due to table-locks, but this
removes a step for almost all the small-scale side work I do.

```
web: bundle exec rails s
release: bin/rake db:migrate
```

The Procfile's a lot more powerful than this, allowing you to specify dynos and
commands for running workers and things, but I wanted to catch this one while
I thought of it.

For more information, [here's
Heroku](https://devcenter.heroku.com/articles/procfile).
