# cross-river-postman
Cross River Postman collection

## Cross River Postman Collection

To make development easier, we’ve put together a [**Postman collection**](https://www.postman.com/cross-river/cross-river-apis/overview) with pre-built requests for all the Cross River [**APIs intro**](docId\:sfnHqbapK4Sg6QBZw9P8y). Use this collection to explore, test, and build your integration directly in Postman with minimal extra coding and setup required.

If you're not interested in reading these instructions, you can go directly to the Cross River Postman collection.

To immediately fork our collection, [Run this collection in Postman](https://www.postman.com/collections/47019181-21421164-5987-44e5-b242-84890920c4a0)


Just complete the [**Postman collection**](docId\:Fb95IuTT_D2JMljOJPHHb) setup details, and start making calls in Sandbox through [**Postman**](https://www.postman.com/downloads/).&#x20;

## Access (Bearer) Token

We've created our Postman developer sandbox environment to provide a safe space to test the Cross River APIs. In the Cross River Postman collection, you perform authentication using a bearer token.&#x20;

To get the IDs you need to set up the access (bearer) token required to run the collection:

1. [**Get API credentials**](docId\:Z-MVwOV-p00-xX082NabK): With these credentials you request and receive an access token to use for sending APIs in our sandbox environment
2. [**Get access token**](docId\:kP_8xNEZDhnaTwYlGXt22): Once you receive your API credentials and before you can use our APIs, you get an access token using the `client_id` and `client_secret` you received when you registered.&#x20;

## Fork Cross River Collection

Head straight to our [**Postman workspace**](https://www.postman.com/cross-river/cross-river-apis/overview) to fork our collection.&#x20;

:::hint{type="warning"}
Once forked, don’t forget to set your environment variables for sandbox.
:::

## Configure Your Postman Environment

To use the collection you just created, navigate to it, click **Environments,** and select **Sandbox**. Copy your Cross River client ID and client secret, and paste them into the `client_Id` and `client_secret` fields.   For Card Payments, paste them into the `ptpe_client_id` and `ptpe_client_secret` fields. &#x20;

Now you’re ready obtain a token and begin to send requests.&#x20;

1. Run `Authorization/Obtain token` to generate your token. For Card Payments, run `Card Payments/Authorization/Get P2PE token`.
2. The variable `{{token}}` (or `ptpe_token` for Card Payments) is added automatically to your environment by a post reponse script.  When the token expires you need to follow step 1 again.
3. There are several variables that you might need to populate depending on which endpoint you're exercising.  For example, `partner_id`, `product_id`, `configuration_id `and `callback_url`.
4. There are also some variables that are populated through scripts, such as `token` and `ptpe_token` that should not be populated manually.

## Modify Requests

To update a request, make your changes on the **Body** tab. Values in double curly brackets pull from your environment variables. Check our [**APIs intro**](docId\:sfnHqbapK4Sg6QBZw9P8y) to see which fields each endpoint accepts, and view requests in your preferred language.
