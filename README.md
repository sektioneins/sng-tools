# Suhosin-NG (SNG) Tools Suite for Snuffleupagus

## About

The SNG Tools Suite is a set of tools to ease configuration of the PHP hardening extension [Snuffleupagus](https://github.com/sektioneins/snuffleupagus).

Available tools:

* **SNGGen:** Generate Snuffleupagus configuration files from templates
* **SNGCheck:** Check Snuffleupagus runtime configuration for common configuration mistakes

## Installation

Just clone or download a copy of the software and run it using the PHP CLI with PHP 7 or above.

## Additional documentation
Please have a look in [wiki](https://github.com/sektioneins/sng-tools/wiki) or go directly to [SNGCheck documentation](https://github.com/sektioneins/sng-tools/wiki/SNGCheck).

## SNGGen Examples

* Generate default configuration and print to STDOUT:

  ```
  ./snggen --gen
  ```

* Complete a questionnaire and write configuration file to `prod.rules`:

  ```
  ./snggen --qa -o prod.rules
  ```

## SNGCheck Examples

* Show SNGCheck help once with a default installation, then with a non-standard PHP installation located in `/opt/php`

  ```
  ./sngcheck -h
  /opt/php/root/8.1.8-64bit/bin/php -f sngcheck -- -h
  ```

* Run checks against a configuration file (requires snuffleupagus > 0.8 installed in the default extension directory)

  ```
  ./sngcheck -c /etc/php/snuffleupagus.ini
  ```

* Run checks in debug mode with custom PHP and snuffleupagus not installed (useful for development/debugging)

  ```
  /opt/php/root/8.1.8-64bit/bin/php -f sngcheck -- -m ../snuffleupagus/src/modules/snuffleupagus.so -c ./test.rules -D
  ```
