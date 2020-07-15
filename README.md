# B2 storage adapter for Imbo

[B2](https://www.backblaze.com/) storage adapter for Imbo.

## Installation

    composer require imbo/imbo-b2-adapters

## Usage

Create the adapter using a key ID, an application key, a bucket ID, and a bucket name. You can get access to this information in your B2 account.

```php
use Imbo\Storage\B2;

$adapter = new B2($keyId, $applicationKey, $bucketId, $bucketName);
```

Because of a limitation in the underlying library for the B2 integration you will need to specify the key ID and the application key for the `Master Application Key`.

## Running integration tests

If you want to run the integration tests for this adapter you need to export the following environment variables:

- `B2_KEY_ID`
- `B2_APPLICATION_KEY`
- `B2_BUCKET_ID`
- `B2_BUCKET_NAME`

**Warning:** The integration tests will empty the specified bucket, so if you intend to run the integration tests you should create a dedicated bucket for this purpose.

## License

MIT, see [LICENSE](LICENSE).