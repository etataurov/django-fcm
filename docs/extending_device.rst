.. _extending_device:

Extending device model
======================

Allows you to store additional data in the device model (e.g. foreign key to the user)


Device model
------------

In your application, you need to create your own `Device` model. This model has to inherit from `fcm.models.AbstractDevice`.

.. code-block:: python

    # import the AbstractDevice class to inherit from
    from fcm.models import AbstractDevice

    class MyDevice(AbstractDevice):
        pass


Use your model
--------------

In the end, you have to inform `django-fcm` where it can find your model.

Add appropriate path to the ``settings.py`` file:

.. code-block:: python

    FCM_DEVICE_MODEL = 'your_app.models.MyDevice'


