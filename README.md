# Fix wp-cli not working if $WP_CORE is provided
This repository serves as a Proof-of-Concept for the bug trying to be fixed in [Pull Request !1810](https://github.com/drud/ddev/pull/1810).

The WordPress project is based on [Bedrock](https://roots.io/bedrock/).

## Reproduce
1. Clone the repository
2. Start ddev: `ddev start`
3. Run wp-cli. E.g: `ddev exec wp core version`
   
   Instead of showing the core version, wp-cli fails with the following error:
   ```
   Error: This does not seem to be a WordPress install.
   Pass --path=`path/to/wordpress` or run `wp core download`.
   Failed to execute command wp core version: exit status 1 
   ```

## Setup
This project has been setup by running the following commands:
```sh
composer create-project roots/bedrock ddev-pull-1810
ddev config
```
