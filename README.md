# WebPlatform Docs

This repository should be the replication of WebPlatform.org content and user contribution as of 2015-09-04

## Goals

1. Migrate all content and contribution history from MediaWiki reading from recommended backup strategy into a Git repository
1. Change to Git to store future contributions and history, with minimal metadata loss
1. Use a static site generator to manage the contents instead of a full CMS system and infrastructure
1. Allow us to save on computing resources by serving static files
1. Use tools web developer already uses, ease contribution


## Purpose, how to setup and use

This repository contains raw documentation files in Markdown format that is used on [**WebPlatform Docs**](http://www.webplatform.org/docs/).

Content is separated in multiple repositories, this one has main docs pages.

Planning, and discussions ("other content") are migrated into separate repositories:

* [**Meta/**][docs-meta]; What was originally published in **docs.webplatform.org/wiki/Meta:...**
* [**WPD/**][docs-wpd]; What was originally published in **docs.webplatform.org/wiki/WPD:...**

To publish the site, we use a *static site generator*, see [**webplatform/generator-docs** repository][generator-docs]


## Expected steps

See [webplatform/generator-docs](https://github.com/webplatform/generator-docs#expected-steps)


## How was it done?

To learn how the conversion was done, take a look at the [mediawiki-conversion] utility and
the [**webplatform/mediawiki-conversion** library][mediawiki-conversion] library.

  [mediawiki-conversion]: https://github.com/webplatform/mediawiki-conversion "Migration workbench to extract contents out of MediaWiki"
  [content-converter]: https://github.com/webplatform/content-converter "Abstract conversion utility library used in MediaWiki migration workbench"
  [docs-wpd]: https://github.com/webplatform/docs-wpd "WebPlatform Docs exported WPD section"
  [docs-meta]: https://github.com/webplatform/docs-meta "WebPlatform Docs exported Meta section"
  [generator-docs]: https://github.com/webplatform/generator-docs "WebPlatform Static site generator"
