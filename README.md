# Bambu Mail

A shortcut function for sending template-based emails in HTML and plain-text format, and subscribing
users to newsletters

## About Bambu Mail

This package allows for the quick and simple sending of emails in both plain-text and HTML format, without
needing to specify both. A base HTML template is supplied which can be overridden. Markdown is the expected
format for the email body, which means it gets transformed into HTML but left alone for the text-only
version.

In addition, Bambu Mail has a simple provider system for newsletter subscriptions, allowing new signups to
be automatically added to a mailing list (should they choose to). The only current provider in this package
is for Mailchimp, but the base type is easily extensible.

Finally, Bambu Mail provides a Postmark email backend, based on the
[django-postmark](https://github.com/dstufft/django-postmark) but with a slight bug fix.

## About Bambu Tools 2.0

This is part of a toolset called Bambu Tools. It's being moved from a namespace of `bambu` to its own
'root-level' package, along with all the other tools in the set. If you're upgrading from a version prior
to 2.0, please make sure to update your code to use `bambu_mail` rather than `bambu.mail`.

## Installation

Install the package via Pip:

```
pip install bambu-mail
```

Add it to your `INSTALLED_APPS` list along with Bambu Markup:

```python
INSTALLED_APPS = (
    ...
    'bambu_mail',
    'bambu_markup'
)
```

Add `bambu_mail.urls` to your URLconf:

```python
urlpatterns = patterns('',
    ...
    url(r'^mail/', include('bambu_mail.urls')),
)
```

## Todo

* Prepare for internationalisation
* Write more tests

## Documentation

Full documentation can be found at [ReadTheDocs](http://bambu-mail.readthedocs.org/).

## Questions or suggestions?

Find me on Twitter (@[iamsteadman](https://twitter.com/iamsteadman))
or [visit my blog](http://steadman.io/).
