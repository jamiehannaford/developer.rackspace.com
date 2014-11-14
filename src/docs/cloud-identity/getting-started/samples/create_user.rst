.. code-block:: csharp

  var identity = new CloudIdentity();
  var provider = new CloudIdentityProvider(identity);

  NewUser user = new NewUser("{username}", "{email}", enabled: true);
  user = provider.AddUser(user, null);
  string password = user.Password;

.. code-block:: go

  opts := users.CreateOpts{
    Username: "{username}",
    Email: "{email}",
    Enabled: osUsers.Enabled,
  }

  user, err := users.Create(client, opts).Extract()

.. code-block:: java

.. code-block:: javascript

  // Not currently supported by this SDK

.. code-block:: php

  $user = $service->createUser(array(
    'username' => 'newUser',
    'email'    => 'foo@bar.com',
    'enabled'  => true,
  ));

  echo $user->getPassword();

.. code-block:: python

  // Not currently supported by this SDK

.. code-block:: ruby

  user = @client.users.create(
    :username => "{username}",
    :email => "{email}",
    :enabled => true
  )

.. code-block:: sh

  curl -s $BASE_URL"users" -X POST -d \
  '{
    "user": {
      "username": "jqsmith",
      "email": "john.smith@example.org",
      "enabled": true
      }
   }' -H "Content-Type: application/json" \
   -H "X-Auth-Token: $TOKEN" | python -m json.tool
