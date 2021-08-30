# Suhosin-NG (SNG) Tools Suite for Snuffleupagus

## About

The SNG Tools Suite is a set of tools to ease configuration of the PHP hardening extension [Snuffleupagus](https://github.com/sektioneins/snuffleupagus).

Available tools:

* **SNGGen:** Generate Snuffleupagus configuration files from templates

## Installation

Just clone or download a copy of the software and run it using the PHP CLI with PHP 7 or above.

## SNGGen Examples

* Generate default configuration and print to STDOUT:

  ```
  snggen --gen
  ```

* Complete a questionaire and write configuration file to `prod.rules`:

  ```
  snggen --qa -o prod.rules
  ```

