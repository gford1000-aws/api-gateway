# api-gateway

AWS CloudFormation script that creates an internet facing API using AWS API Gateway and AWS Lambda.

The script demonstrates how to create an API Gateway with optional Lambda based authorization, based
on a header that contains an authorization token.

The API accepts a POST request, disregarding the posted body and returning the current datetime.

## Arguments

| Argument                     | Description                                                                 |
| ---------------------------- |:---------------------------------------------------------------------------:|
| APIName                      | Name of the REST API                                                        |
| APIDescription               | Description of the REST API                                                 |
| ResourceName                 | Name of the resource to be created (one resource from the root resource)    |
| StageName                    | Name of the stage to be created                                             |
| AuthorisationTokenHeaderName | Name of the header containing the auth token (leave blank for no auth)      |
| AuthorisationTimeout         | TTL of cache for authorisations (set to 0 for no caching)                   |


## Outputs

| Output                  | Description                                                    |
| ----------------------- |:--------------------------------------------------------------:|
| URL                     | The URL of the deployed REST API                               |

AWS X-Ray is enabled on the API Gateway and Lambda functions.

## Licence

This project is released under the MIT license. See [LICENSE](LICENSE) for details.
