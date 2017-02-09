# Starting A New Rails Project

Yes, it can be as simple as `rails new project_name`; however, I keep
getting burned because I want to use `postgresql` for my DB (`sqlite`
can't deploy to Heroku) and `rspec` for my tests. 

## Already Started A Project With Sqlite?
If you've already started a project with `sqlite` and want to change it,
you need to add 

```
gem 'pg'
```

to your Gemfile. Then, you'll need to update the database adapter and
name in the `database.yml` file.

```
default: &default
  adapter: postgresql
  encoding: unicode
  pool: 5

development:
  <<: *default
  database: some_project_development

# Warning: The database defined as "test" will be erased and
# re-generated from your development database when you run "rake".
# Do not set this db to the same as development or production.

test:
  <<: *default
  database: some_project_test

production:
  <<: *default
  database: some_project_production
  username: some_project
  password:
```

Then you'll need to do a standard `rake db:create` and `rake db:migrate`
to get this new database created and up to date.

## Already Started a Project With Minitest?

If you've already started a project with Rails' default test suite and
want to change it to Rspec, you need to add

```
group :development, :test do
  gem 'rspec-rails'
end
```

to your Gemfile. 

Then you'll need to run 

```
bundle install
```

to update the installed gems.

Then you'll need to have rails generate the Rspec installation:

```
rails generate rspec:install
```

Finally, you'll need to clean up the old testing directories by removing
the `/test` directory from the application.

## Or Just Improve Your Rails New

You can save yourself some configuration headaches by declaring most of
this in the `rails new`:

```
rails new yourapp -T --database=postgresql
```

The `-T` drops the test unit, and the `--database=` specifies the database
you want to use.
