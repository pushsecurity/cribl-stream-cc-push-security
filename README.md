# Push Security
----

## About this pack

This Cribl Stream pack processes events from the Push Security platform. 

It makes it easy to forward/drop different event categories and drops some metadata fields (e.g. event headers) such that you should see ~50% event size reduction using this pack.

For full documentation of events emitted by the Push Security platform, please visit the [Push Security Webhooks documentation](https://pushsecurity.redoc.ly/webhooks-v1/). To learn more about Push Security, please visit [www.pushsecurity.com](www.pushsecurity.com).

## Deployment

1. Configure a Cribl Stream source to receive data over HTTPS. (*The "Raw HTTP" source with TLS configured is suggested. If you don't have your own PKI infrastructure, you can use the built-in `$CRIBL_CLOUD_KEY` and `$CRIBL_CLOUD_CRT` for the private key path and certificate path values.*)
2. Create a webhook in the [Push Security platform](https://pushsecurity.com/app/settings/webhooks) that points to your Cribl Stream source.
3. Download and install the Push Security pack for Cribl Stream (`cc-push-security`)
4. Inside the pack routes, enable or disable routes to control which event categories are forwarded as needed.
5. Create a route that uses a filter to match on your source, set the pipeline to the `cc-push-security` pack, and set your desired output.

## Release Notes

### Version 1.0.0 - 2025-02-06
Initial release

## Contributing to the Pack
To contribute to the Pack, please email Push Security using [support@pushsecurity.com](mailto:support@pushsecurity.com) and outline your proposed contribution.

## Contact
To contact us please email [support@pushsecurity.com](mailto:support@pushsecurity.com).

## License
This Pack uses the following license: [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt).
