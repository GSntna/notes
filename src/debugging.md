# Debugging

## Index

* [Assertions](#assertions)
* [Logging](#logging)
    * [using the logging module](#using-the-logging-module)
    * [logging levels](#logging-levels)
    * [disable logging](#disable-logging)
* [Summary](#summary)

## Assertions

It is a sanity check to make sure the code is not doing something obviously
wrong. These are done with `assert` statements. If the sanity check fails,
then an `assertError` exception is raised.

## Logging

Logging is used to debug the code. It can print information, warnings, debugging
and errors while the script is running.

### Using the logging module

To set the logging messages the following syntax is used:

```py
import logging
logging.basicConfig(
    filename='my_log.txt',
    level=logging.DEBUG,
    format=' %(asctime)s -  %(levelname)s -  %(message)s'
)
```

The `basicConfig` parameters do the following:

* **filename**: the file to store the logs (optional)
* **level**: priority of message to show (starting from)
* **format**: how to show the log
    * %(asctime)s: date time
    * %(levelname)s: logging level
    * %(message)s: message specified in the log

### Logging levels

There are several types of logging:

| Logging function | Description |
| ---------------- | ----------- |
| `logging.debug()` | Lowest level. Used for small details, mostly when diagnosing problems |
| `logging.info()` | Used to record information on general events, confirm that things are working as expected |
| `logging.warning()` | Indicate potential problem that doesn't prevent the program from working |
| `logging.error()` | Used to record an error that caused the program to fail |
| `logging.critical()` | Highest leve, used to indicate fatal aerror that has caused or is about to crash the program |

### Disable logging

Using `logging.disable(logging.CRITICAL)` will disable the logs starting from the
level passed as an argument. This is useful when the code has been tested and
we don't want all the logs to be passed.


## Summary

| Function | Description |
| -------- | ----------- |
| `raise Exception('Error message')` | Interrupts the code and raises the given error message |
