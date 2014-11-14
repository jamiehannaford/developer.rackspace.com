.. code-block:: csharp

  var identity = new CloudIdentity { Username = "{username}", APIKey = "{apiKey}" };
  var provider = new CloudIdentityProvider(identity);

  User user = provider.GetUserByName("{username}", null);
  provider.DeleteRoleFromUser(user.Id, "{roleId}", null);

.. code-block:: go

  err := roles.DeleteUserRole(client, "{userId}", "{roleId}").ExtractErr()

.. code-block:: java

.. code-block:: javascript

  // Not currently supported by this SDK

.. code-block:: php

  $user->removeRole('{roleId}');

.. code-block:: python

  // Not currently supported by this SDK

.. code-block:: ruby

  // Not currently supported

.. code-block:: sh

  curl -s $BASE_URL"users/{userId}/roles/OS-KSADM/{roleId}" \
    -X DELETE -H "X-Auth-Token: $TOKEN"
