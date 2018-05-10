INSTALL
===

```
$ composer create-project symfony/framework-standard-edition my_project_name "3.4.6"
$ composer require jms/i18n-routing-bundle
```

JMS i18 config:

```
jms_i18n_routing:
    default_locale: en
    locales: [en, fr]
    strategy: prefix
```

SF 3.4.6 behavior
===

Hits to "/" redirects to "/en/" => OK


REPRO
===
```
$ composer require "symfony/symfony" "3.4.7"
```

Now hits to "/" do not redirect to "/en/" => WRONG
