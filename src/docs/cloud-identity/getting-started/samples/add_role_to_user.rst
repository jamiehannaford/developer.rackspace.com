.. code-block:: csharp

  var identity = new CloudIdentity { Username = "{username}", APIKey = "{apiKey}" };
  var provider = new CloudIdentityProvider(identity);

  User user = provider.GetUserByName("{username}", null);
  provider.AddRoleToUser(user.Id, "{roleId}", null);

.. code-block:: go

  err := roles.AddUserRole(client, "{userId}", "{roleId}").ExtractErr()

.. code-block:: java

.. code-block:: javascript

  // Not currently supported by this SDK

.. code-block:: php

  $user->addRole('{roleId}');

.. code-block:: python

  // Not currently supported by this SDK

.. code-block:: ruby

  // This operation is not currently supported.

.. code-block:: sh

  curl -s $BASE_URL"users/{userId}/roles/OS-KSADM/{roleId}" \
     -X PUT -H "X-Auth-Token: $TOKEN"
