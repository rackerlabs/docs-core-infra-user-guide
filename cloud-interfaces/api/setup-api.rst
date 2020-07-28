.. _setup-api:

^^^^^^^^^^^^^^^^^^^^^
Preparing to use APIs
^^^^^^^^^^^^^^^^^^^^^
If you have a Rackspace cloud account, you can use Rackspace APIs
to interact with the cloud services you subscribe to.

The basic process is the same for all Rackspace APIs:

1. Collect the parts that you need for the request:

   * Obtain your account credentials (:how-to:`API key <view-and-reset-your-api-key>` and account number, also called tenant ID) from the `Cloud Control Panel <https://mycloud.rackspace.com/>`__.
   * :rax-dev-devguide:`Use your credentials to authenticate <cloud-identity/v2/developer-guide/#document-quickstart-guide>`, receiving a token and a service catalog as proof of success
   * In the :rax-dev-devguide:`service catalog <cloud-identity/v2/developer-guide/#annotated-authentication-request-and-response>`, find the endpoint for the API to which you want to send a request.
   * Look up the API reference section of your product found in :rax-docs:`API documentation <>`.

2. Assemble the request from its parts. Plug in the values
   that you collected for your credentials, the API's endpoint,
   and any details (such as the ID of a server) specific to your configuration
   and your API request.
3. Send a well-formed request to the service's API endpoint.
4. Process the service's response.


Beyond this general process, the details vary depending
on which service you are working with. For product-specific
introductions to the APIs relevant to
specific core infrastructure products, see:

* :ref:`cloudservers-api`
* :ref:`cloudnetworks-api`
* :ref:`cloudimages-api`
* :ref:`cloudblockstorage-api`
