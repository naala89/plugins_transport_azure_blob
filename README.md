# Transport Azure Blob

Transport for ApiOpenStudio output to an Azure Blob.

# Adding to your project

## Composer

    $ composer require apiopenstudio/transport_azure_blob

# Configuration

Add a remote output processor to your resource.

The output section example below will return the output in the response as well
as upload the response to an Azure Blob:

    output:
        -
            processor: json_remote
            id: example JSON Remote output
            filename: example.json
            transport: ApiOpenStudio\Plugins\TransportAzureBlob
            parameters:
                dsn: my_dsn_string
                container: my_container_name
                prefix: prefix (optional)
        - 
            response

**Note:** the value for the transport is the full namespace path.

## Parameters

### Required

- dsn - The Azure Blob DSN string
- container - The Azure Blob container name

### Optional

- prefix - Optional prefix

# Further information

See [FlySystem documentation][flysystem-docs] and
[The League GitHub][flysystem-github] for more details.

[flysystem-github]: https://github.com/thephpleague/flysystem-azure-blob-storage

[flysystem-docs]: https://flysystem.thephpleague.com/docs/adapter/azure-blob-storage/
