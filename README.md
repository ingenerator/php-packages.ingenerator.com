ingenerator-php-packages
========================

Manages the [composer](https://getcomposer.org) metadata repository for the custom
and internal packages used for inGenerator projects.

The project uses [satis](https://getcomposer.org/doc/articles/handling-private-packages-with-satis.md)
to update each package's metadata and build a static package archive site that can be used 
by end-users to track versions.

To update the package metadata:

```bash
composer install
bin/satis build satis.json build/web
```

Then upload/transfer the contents of build/web to your favourite static file hosting service.