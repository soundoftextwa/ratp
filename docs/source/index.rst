.. meta::
    :google-site-verification lang=en:
        qoIbJvneR1qPFrl5BRBgcN0RggPZzu5QMp6-Bhl0XGg

===============================
API Souq by Emirates NBD
===============================

**API Souq** by `Emirates NBD <https://www.emiratesnbd.com/en>`_ is a comprehensive open banking API platform that offers a suite of Application Programming Interfaces (APIs) for developers, businesses, and fintechs. Through API Souq, Emirates NBD provides access to various banking services, enabling seamless integration of financial services into third-party applications.

---------------------------
Overview
---------------------------

API Souq was created to support innovation in the financial sector by giving developers and businesses easy access to Emirates NBD's banking services. By leveraging open banking principles, API Souq facilitates the development of digital financial solutions that can enhance the user experience for customers across the UAE.

**Key Features of API Souq:**

- **Banking APIs:** A wide range of APIs covering multiple services, such as account information, payments, and money transfers.
- **Developer-friendly Platform:** API Souq is designed with developers in mind, offering comprehensive documentation, sandbox environments, and support.
- **Security and Compliance:** Emirates NBD ensures that all APIs meet strict security and compliance standards to protect user data and adhere to UAE financial regulations.
- **Open Banking Innovations:** API Souq encourages collaboration with fintechs and startups, enabling them to create value-added services that can be integrated into various applications.

---------------------------
API Categories
---------------------------

API Souq offers a broad array of APIs, organized into the following categories:

1. **Accounts API**
   - Provides access to account-related information, such as account balance, transaction history, and statements.
   - Allows third-party applications to access real-time account information with customer consent.

2. **Payments API**
   - Facilitates payment processing, including domestic transfers, bill payments, and international money transfers.
   - Enables seamless integration of payment solutions into e-commerce platforms and apps.

3. **Authentication API**
   - Provides secure authentication for customers, ensuring that third-party applications can access data only after proper authorization.
   - Uses strong authentication methods to ensure secure and seamless user access.

4. **Cards API**
   - Offers access to card-related information, such as available credit, transaction history, and reward points.
   - Can be integrated into financial planning and budgeting applications.

5. **Loans and Financing API**
   - Allows developers to access loan-related information, enabling applications that offer loan management and status tracking.
   - Useful for personal finance applications and digital lending platforms.

---------------------------
Benefits of API Souq
---------------------------

API Souq by Emirates NBD provides significant benefits to businesses, developers, and end-users:

- **Enhanced Customer Experience:** By integrating Emirates NBD's banking services into their applications, businesses can provide a more seamless banking experience to customers.
- **Innovation Support:** API Souq encourages the development of new financial products and services, fostering innovation in the fintech space.
- **Time and Cost Efficiency:** Businesses can reduce development time and costs by leveraging existing APIs rather than building their own banking infrastructure.
- **Secure and Compliant:** Emirates NBD ensures that all data shared through API Souq complies with UAE regulations and follows international security standards.

---------------------------
Getting Started with API Souq
---------------------------

To start using API Souq, follow these steps:

1. **Register**: Sign up on the API Souq developer portal to gain access to documentation and sandbox environments.
2. **Explore Documentation**: Review API Souq's comprehensive documentation to understand the integration processes and API functions.
3. **Test in Sandbox**: Use the sandbox environment to test your applications before going live.
4. **Go Live**: After testing and validation, apply for production access and integrate Emirates NBD services into your live application.

===============================
SouqAPI PHP Documentation
===============================

The **SouqAPI** PHP class `SouqAPIResult` is a structured response handler used in the **API Souq** platform by Emirates NBD. It processes API responses, checks for errors, and retrieves data and messages associated with API calls.

---------------------------
Class Properties
---------------------------

- **status (int)**  
  - Default: `200`
  - Holds the HTTP status code of the API response.

- **message (string)**  
  - Stores a message from the API response, often indicating the success or error state of the request.

- **data (mixed)**  
  - Contains the actual data payload returned by the API, if available.

- **callResult (array)**  
  - Holds the entire response array returned by the API, including metadata and data fields.

- **Const MESSAGE (string)**  
  - Constant for the message key, set as `'message'`.

---------------------------
Class Methods
---------------------------

The `Souq API Result` class includes several methods to manage and interpret the API response.

.. _construct:
    - **Parameters:**
        - `$response_code` (int|string): HTTP response code for the API request.
        - `$CallResult` (array): The complete API response array, including metadata and data fields.
    - **Function:** Initializes the class properties based on the API response. The `$status` is set according to `$response_code`, with a default of `500` if invalid. The method checks for `data` and `message` in `$CallResult`.

.. _getStatus:

getStatus()
    - **Return Type:** `int`
    - **Description:** Returns the HTTP status code of the API response.

.. _isResponseOK:

isResponseOK()
    - **Return Type:** `bool`
    - **Description:** Checks if the response status is one of the successful codes (`200`, `201`, or `202`). Returns `true` for success, otherwise `false`.

.. _isAuthenticationFailed:

isAuthenticationFailed()
    - **Return Type:** `bool`
    - **Description:** Checks if the response status is `403`, indicating forbidden access or authentication failure.

.. _isExpiredTokenResponse:

isExpiredTokenResponse()
    - **Return Type:** `bool`
    - **Description:** Checks if the response status is `401`, suggesting that the access token used in the request has expired.

.. _getMessage:

getMessage()
    - **Return Type:** `string`
    - **Description:** Retrieves the message from the API response metadata if available. Useful for debugging or providing user feedback.

.. _getData:

getData()
    - **Return Type:** `mixed`
    - **Description:** Retrieves the data payload from the API response. If no data exists, it returns an empty string.

.. _getCallResult:

getCallResult()
    - **Return Type:** `array`
    - **Description:** Returns the complete response array from the API, including both metadata and data fields.

===============================
Souq API Result Usage Example
===============================

The following example demonstrates how to create a `SouqAPIResult` instance and access various response details:

.. code-block:: php

    use SouqAPI\SouqAPIResult;

    // Sample API response
    $response_code = 200;
    $callResult = [
        'data' => ['id' => 123, 'name' => 'Sample Item'],
        'meta' => ['message' => 'Request successful']
    ];

    // Create a new SouqAPIResult instance
    $souqResult = new SouqAPIResult($response_code, $callResult);

    // Check if the response is successful
    if ($souqResult->isResponseOK()) {
        echo "Status: " . $souqResult->getStatus() . "\n";
        echo "Message: " . $souqResult->getMessage() . "\n";
        echo "Data: ";
        print_r($souqResult->getData());
    } else {
        echo "Error: " . $souqResult->getMessage();
    }

    // Check for specific error codes
    if ($souqResult->isAuthenticationFailed()) {
        echo "Authentication failed.";
    } elseif ($souqResult->isExpiredTokenResponse()) {
        echo "Token expired. Please re-authenticate.";
    }

===============================

API Souq by Emirates NBD is a robust platform that empowers developers and businesses to create innovative financial solutions. By providing secure and accessible banking APIs, `Emirates NBD <https://uaetiming.com/how-to-open-an-nbad-account-in-the-uae/>`_ supports the growth of digital financial services in the UAE, enabling fintechs and businesses to offer a seamless and integrated banking experience.


.. toctree::
   :maxdepth: 2

   verilog/procedure
   verilog/systemverilog
   verilog/designs
   verilog/package
   verilog/fsm
