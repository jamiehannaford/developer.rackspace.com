.. code-block:: csharp

.. code-block:: java

.. code-block:: javascript

.. code-block:: php

    $image = $service->getImage('{imageId}');

.. code-block:: python

  # After authenticating, get a reference to the client
  imgs = pyrax.images
  img = imgs.get("{imageId}")

.. code-block:: ruby

  # N/A

.. code-block:: sh

  curl -s $ENDPOINT/images/{imageId} \
    -H "X-Auth-Token: $TOKEN" | python -m json.tool

  # NOTE: {imageId} is a placeholder: Replace it with
  # an actual value and do not enclose it with {}.
