.. code-block:: csharp

.. code-block:: java

.. code-block:: javascript

.. code-block:: php

    $notification = $service->getNotification();

    $params = array(
        'label' => 'My webhook #1',
        'type'  => 'webhook',
        'details' => array(
            'url' => 'http://example.com'
        )
    );

    // Test these params
    $response = $notification->testParams($params);

    echo $response->status; // Was it successful?

    // Now create the notification
    $notification->create($params);

.. code-block:: python

.. code-block:: ruby

  # :label is a String that's a friendly name for the notification.
  # :type is one of 'webhook', 'email', or 'pagerduty'.
  # :details is a :type-specific Hash of configuration options.
  notification = @client.notifications.create(
    :label => 'tell the world',
    :type => 'email',
    :details => { :address => '{emailAddress}' }
  )

.. code-block:: sh

  $ curl -X POST -d \
    '{
      "label": "{webhookNotificationLabel}",
      "type": "webhook",
      "details": {
        "url": "{webhookUrl}"
      }
    }' \
    -H "X-Auth-Token: $TOKEN" \
    -H "Content-Type: application/json" \
    $ENDPOINT/notifications | python -m json.tool