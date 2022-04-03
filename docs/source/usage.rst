Usage
=====
Authorization
----------------
Main URL: **https://hotify.pw/api/v1/**

With each request in the header you need to send an API token

.. code-block:: console

   Authorization: YOUR_API_TOKEN_HERE
   
Creating a notification
----------------
To create a notification, you must send a **POST** request to

**https://hotify.pw/api/v1/notifications**

with the following parameters

+-------------+------------+-----------------------+
| Parameter   | Type       | Required              |
+=============+============+=======================+
| app_id      | Int        | Yes (If no tag)       |
+-------------+------------+-----------------------+
| tag         | String     | Yes (If no app_id)    |
+-------------+------------+-----------------------+
| title       | String     | No                    |
+-------------+------------+-----------------------+
| text        | String     | Yes                   |
+-------------+------------+-----------------------+

You can pass **app_id** or **tag**. You can assign the tag yourself in your dashboard.

For example:

.. code-block:: json

   {
      "app_id": 1,
      "title": "First notification",
      "text": "Hello world!"
   }

Successful response example:


.. code-block:: json

   {
      "success": true
   }

Error response example:


.. code-block:: json

   {
      "success": false,
      "error": "Ошибка"
   }
   
PHP package
----------------
If you are using PHP, you can use our package

https://packagist.org/packages/hotifyru/hotify
