# FORK

We(Spoke) are forking [gunpowderlabs/buildpack-ruby-rake-deploy-tasks](https://github.com/gunpowderlabs/buildpack-ruby-rake-deploy-tasks) to avoid buildpack updating without noticing it.

# Heroku buildpack for running arbitrary rake tasks on deploy

This buildpack is intended for use after the regular [ruby-buildpack].

# Usage

If you are using the default buildpack, manually set your buildpack to Heroku's default Ruby buidlpack

```
heroku buildpacks:set https://github.com/heroku/heroku-buildpack-ruby
```

Append the buildpack-ruby-rake-deploy-tasks to your buildpack list:

```
heroku buildpacks:add https://github.com/spokelaw/buildpack-ruby-rake-deploy-tasks
```

Configure DEPLOY_TASKS environment variable with the tasks you want to run:

```
heroku config:set DEPLOY_TASKS='db:migrate cache:clear'
```

# License

MIT, see the LICENSE file.

[ruby-buildpack]:https://github.com/heroku/heroku-buildpack-ruby
