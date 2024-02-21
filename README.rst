rpi-lcd
=======
⚠️ this is a fork from [badgal/rpi-lcd](https://github.com/bogdal/rpi-lcd)
===========================================================================
⚠️⚠️please pake sure not to cantact him if there are any bugs or errors that i may cause.⚠️⚠️

in this fork i will attempt to make it dynamic by adding the bility to add an address for the LCD
and add diffrint size LCD

original readme 
=======

This library supports LCD text displays (20x4, 16x2 and other) via I²C converter.

It requires the ``python-smbus`` package installed on your Raspberry Pi and enabled ``ARM I2C`` interface.

Installation
------------

Get the package from ``pypi``::

    pip install rpi-lcd

Usage
-----

.. code-block:: python

    from rpi_lcd import LCD
    from time import sleep

    lcd = LCD()
    
    lcd.text('Hello World!', 1)
    lcd.text('Raspberry Pi', 2)
    lcd.text('is really', 3, 'center')
    lcd.text('awesome', 4, 'right')

    sleep(5)
    lcd.clear()
    
``rpi-lcd`` handles multiline texts::

    from rpi_lcd import LCD
    
    lcd = LCD()
    lcd.text('This is a message that has more than 20 chars and does not fit in one line', 1)
    
.. image:: https://github-bogdal.s3.amazonaws.com/rpi-lcd/lcd_text.jpeg

