# Specmatic custom auth header demo
 
## Overview
This sample project showcases use of a custom authentication header for secure communication. Below are the key details about authentication and testing:

### Authentication
* The API requires a custom authorization header named X-Microtoken to authenticate requests.
* To facilitate this, a security scheme named MicroToken has been defined in the API specification.
* This header should be populated with a valid token during API calls to ensure successful authentication.

### Specmatic - Testing with Authorization Header
Here's a quick overview on how to test this API using Specmatic:
* Set the Security Scheme - Export the security token as an environment variable. For example:

```bash
export MicroToken=YOUR_VALID_TOKEN
```

* Start Specmatic Test - Run your Specmatic tests. 

```bash
java -jar specmatic test
```

Specmatic will automatically pick up the MicroToken environment variable and apply it as the custom security header (X-Microtoken) to all API calls.

For more details please refer to the [Specmatic Auth & Auth documentation](https://specmatic.io/documentation/authentication.html#testing-with-real-auth)