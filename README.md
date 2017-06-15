# Basic Yii2 API application
---
This repo is a purified empty application to build Restful APIs based on [Yii2 framework](https://github.com/yiisoft/yii2-app-basic). You can find a lot of documentation related to this framework, and the best place to start is maybe their [official documentation](http://www.yiiframework.com/doc-2.0/). This repo contains the minimal structure for an API application with the appropriate configuration already written and working. Without any database, you can still use the `HelloController` to get some dummy `Hello World message`.

## Installation
---
1. Download composer: `curl -s https://getcomposer.org/installer | php`
2. Create a new project based on this one `composer.phar create-project pingu1/yii2-minimal-api api`
3. Init the Git repository in your new project `git init`

## Setting up your web server
---
The default setup to server Yii2 projects are also valid for this application. Please read the documentation to setup your [Apache](https://github.com/yiisoft/yii2/blob/master/docs/guide/start-installation.md#recommended-apache-configuration-) or [Nginx](https://github.com/yiisoft/yii2/blob/master/docs/guide/start-installation.md#recommended-nginx-configuration-) server.

## Code structure
---

The code is structured as such:
```
api
-- commands
-- common
---- controllers
---- models
-- config
-- modules
---- v1
------ controllers
------ models
-- runtime
-- tests
-- web
vendor
```

- The `api` directory is basically the root of your application
- The `commands` folder contains all the console scripts
- The `common` directory contains all models and controllers that could be shared between different versions of your api
- The `modules` directory will contain the different versions of your api
- The `runtime` directory will stores cache and log files generated during runtime
- The `tests` directory will contain all your test files (Yii2 runs with [Codeception](http://codeception.com/))
- The `web` directory only contains the entry script of your api
- 

## Simple Hello World
---
Once your webserver up and ready, you should be able to access the following urls:
> http://127.0.0.1/v1/hello
> http://127.0.0.1/v1/hello/you


