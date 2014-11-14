.. code-block:: csharp

  var identity = new CloudIdentity { Username = "{username}", APIKey = "{apiKey}" };
  var provider = new CloudIdentityProvider(identity);

  User user;

  // retrieve user by name
  user = provider.GetUserByName("{username}", null);

  // or retrieve by ID
  user = provider.GetUser("{userId}", null);

  user.Username = "{newUsername}";
  provider.UpdateUser(user, null);

.. code-block:: go

  opts := users.UpdateOpts{Username: "{newUsername}"}
  user, err := users.Update(client, "{userId}", opts).Extract()

.. code-block:: java

.. code-block:: javascript

  // Not currently supported by this SDK

.. code-block:: php

  $user->update(array(
    'username' => '{newUsername}'
  ));

.. code-block:: python

  // Not currently supported by this SDK

.. code-block:: ruby

  // Retrieve user by name
  user = @client.users.get_by_name("{username}")

  // ... or by ID
  user = @client.users.get("{userId}")

  user.username = "{newUsername}"
  user.save

.. code-block:: sh

  curl -s $BASE_URL"users/{userId}" -X POST -H "X-Auth-Token: $TOKEN" \
    -d '{"user": {"username": "{newUsername}" }}' \
    -H "Content-Type: application/json" | python -m json.tool
