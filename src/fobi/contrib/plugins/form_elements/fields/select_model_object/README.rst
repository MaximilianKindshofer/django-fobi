=============================================================
fobi.contrib.plugins.form_elements.fields.select_model_object
=============================================================
A ``Fobi`` Select Model Object form field plugin. Makes use of the
``django.forms.models.ModelChoiceField`` and ``django.forms.widgets.Select``.

Installation
===============================================
1. Add ``fobi.contrib.plugins.form_elements.fields.select_model_object`` to the
   ``INSTALLED_APPS`` in your ``settings.py``.

.. code-block:: python

    INSTALLED_APPS = (
        # ...
        'fobi.contrib.plugins.form_elements.fields.select_model_object',
        # ...
    )

2. In the terminal type:

.. code-block:: none

    $ ./manage.py fobi_sync_plugins

3. Assign appropriate permissions to the target users/groups to be using
   the plugin if ``FOBI_RESTRICT_PLUGIN_ACCESS`` is set to True.

4. Make sure to take a look at ``fobi.contrib.plugins.form_elements.fields.select_model_object.defaults.IGNORED_MODELS``.
   If necessary, override it in your `settings` as shown in the example below:

.. code-block:: python

    FOBI_FORM_ELEMENT_SELECT_MODEL_OBJECT_IGNORED_MODELS = [
        'auth.User',
        'auth.Group',
        ]
