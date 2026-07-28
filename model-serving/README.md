# model-serving

<!-- TODO 1: Update the description of the service and the link to the documentation. -->
_Check the [related documentation](https://docs.swiss-ai-center.ch/reference/core-concepts/service/) for more information._

## Storage

Services do not access the Core Engine's S3-compatible storage directly and
do not receive storage credentials. Each task contains a `storage_url` exposed
by the Core Engine. The shared `common-code` package downloads task inputs from
`GET {storage_url}/{key}` and uploads task outputs to `POST {storage_url}`.

The service therefore needs outbound HTTP access to every Core Engine to which
it is registered.
