---
title: "错误代码"
description: "控制平面故障排查的错误代码"
aliases: ["/docs/troubleshooting/observability/errorcodes/"]
type: docs
weight: 5
---

# 故障排查

## 错误代码描述

The following table is generated by running `osm support error-info`，可以使用命令行工具 `osm support error-info`获取错误代码相关的信息。

---------------------------------------------------------------------------+
| E2009      | The inbound TrafficTargets composed of their routes for a given destination      |
|            | ServiceIdentity could not be configured.                                         |
+------------+----------------------------------------------------------------------------------+
| E2010      | An applied SMI TrafficTarget policy has an invalid destination kind.             |
+------------+----------------------------------------------------------------------------------+
| E2011      | An applied SMI TrafficTarget policy has an invalid source kind.                  |
+------------+----------------------------------------------------------------------------------+
| E3000      | The system found 0 endpoints to be reached when the service's FQDN was resolved. |
+------------+----------------------------------------------------------------------------------+
| E3001      | A Kubernetes resource could not be marshalled.                                   |
+------------+----------------------------------------------------------------------------------+
| E3002      | A Kubernetes resource could not be unmarshalled.                                 |
+------------+----------------------------------------------------------------------------------+
| E4000      | The Kubernetes secret containing the certificate could not be retrieved by the   |
|            | system.                                                                          |
+------------+----------------------------------------------------------------------------------+
| E4001      | The certificate specified by name could not be obtained by key from the secret's |
|            | data.                                                                            |
+------------+----------------------------------------------------------------------------------+
| E4002      | The private key specified by name could not be obtained by key from the secret's |
|            | data.                                                                            |
+------------+----------------------------------------------------------------------------------+
| E4003      | The certificate expiration specified by name could not be obtained by key from   |
|            | the secret's data.                                                               |
+------------+----------------------------------------------------------------------------------+
| E4004      | The certificate expiration obtained from the secret's data by name could not be  |
|            | parsed.                                                                          |
+------------+----------------------------------------------------------------------------------+
| E4005      | The secret containing a certificate could not be created by the system.          |
+------------+----------------------------------------------------------------------------------+
| E4006      | A private key failed to be generated.                                            |
+------------+----------------------------------------------------------------------------------+
| E4007      | The specified private key could be be could not be converted from a DER encoded  |
|            | key to a PEM encoded key.                                                        |
+------------+----------------------------------------------------------------------------------+
| E4008      | The certificate request fails to be created when attempting to issue a           |
|            | certificate.                                                                     |
+------------+----------------------------------------------------------------------------------+
| E4009      | When creating a new certificate authority, the root certificate could not be     |
|            | obtained by the system.                                                          |
+------------+----------------------------------------------------------------------------------+
| E4010      | The specified certificate could not be converted from a DER encoded certificate  |
|            | to a PEM encoded certificate.                                                    |
+------------+----------------------------------------------------------------------------------+
| E4011      | The specified PEM encoded certificate could not be decoded.                      |
+------------+----------------------------------------------------------------------------------+
| E4012      | The specified PEM privateKey for the certificate authority's root certificate    |
|            | could not be decoded.                                                            |
+------------+----------------------------------------------------------------------------------+
| E4013      | An unspecified error occurred when issuing a certificate from the certificate    |
|            | manager.                                                                         |
+------------+----------------------------------------------------------------------------------+
| E4014      | An error occurred when creating a certificate to issue from the certificate      |
|            | manager.                                                                         |
+------------+----------------------------------------------------------------------------------+
| E4015      | The certificate authority privided when issuing a certificate was invalid.       |
+------------+----------------------------------------------------------------------------------+
| E4016      | The specified certificate could not be rotated.                                  |
+------------+----------------------------------------------------------------------------------+
| E4100      | Failed parsing object into PubSub message.                                       |
+------------+----------------------------------------------------------------------------------+
| E4150      | Failed initial cache sync for MeshConfig informer.                               |
+------------+----------------------------------------------------------------------------------+
| E4151      | Failed to cast object to MeshConfig.                                             |
+------------+----------------------------------------------------------------------------------+
| E4152      | Failed to fetch MeshConfig from cache with specific key.                         |
+------------+----------------------------------------------------------------------------------+
| E4153      | Failed to marshal MeshConfig into other format.                                  |
+------------+----------------------------------------------------------------------------------+
| E5000      | A XDS resource could not be marshalled.                                          |
+------------+----------------------------------------------------------------------------------+
| E5001      | The XDS certificate common name could not be parsed. The CN should be of the     |
|            | form <proxy-UUID>.<kind>.<proxy-identity>.                                       |
+------------+----------------------------------------------------------------------------------+
| E5002      | The proxy UUID obtained from parsing the XDS certificate's common name did not   |
|            | match the osm-proxy-uuid label value for any pod. The pod associated with the    |
|            | specified Envoy proxy could not be found.                                        |
+------------+----------------------------------------------------------------------------------+
| E5003      | A pod in the mesh belongs to more than one service. By Open Service Mesh         |
|            | convention the number of services a pod can belong to is 1. This is a limitation |
|            | we set in place in order to make the mesh easy to understand and reason about.   |
|            | When a pod belongs to more than one service XDS will not program the Envoy       |
|            | proxy, leaving it out of the mesh.                                               |
+------------+----------------------------------------------------------------------------------+
| E5004      | The Envoy proxy data structure created by ADS to reference an Envoy proxy        |
|            | sidecar from a pod's osm-proxy-uuid label could not be configured.               |
+------------+----------------------------------------------------------------------------------+
| E5005      | A GRPC connection failure occurred and the ADS is no longer able to receive      |
|            | DiscoveryRequests.                                                               |
+------------+----------------------------------------------------------------------------------+
| E5006      | The DiscoveryResponse configured by ADS failed to send to the Envoy proxy.       |
+------------+----------------------------------------------------------------------------------+
| E5007      | The resources to be included in the DiscoveryResponse could not be generated.    |
+------------+----------------------------------------------------------------------------------+
| E5008      | The aggregated resources generated for a DiscoveryResponse failed to be          |
|            | configured as a new snapshot in the Envoy xDS Aggregate Discovery Services       |
|            | cache.                                                                           |
+------------+----------------------------------------------------------------------------------+
| E5009      | The ServiceIdentity specified in the XDS certificate CN could not be obtained    |
|            | when creating SDS DiscoveryRequests corresponding to all types of secrets        |
|            | associated with the proxy.                                                       |
+------------+----------------------------------------------------------------------------------+
| E5010      | The Aggregate Discovery Server (ADS) created by the OSM controller failed to     |
|            | start.                                                                           |
+------------+----------------------------------------------------------------------------------+
| E5011      | An Envoy proxy data structure representing a newly connected envoy proxy to the  |
|            | XDS server could not be initialized.                                             |
+------------+----------------------------------------------------------------------------------+
| E5012      | The ServiceAccount referenced in the NodeID does not match the ServiceAccount    |
|            | specified in the proxy certificate. The proxy was not allowed to be a part of    |
|            | the mesh.                                                                        |
+------------+----------------------------------------------------------------------------------+
| E5013      | The gRPC stream was closed by the proxy and no DiscoveryRequests can be          |
|            | received. The Stream Agreggated Resource server was terminated for the specified |
|            | proxy.                                                                           |
+------------+----------------------------------------------------------------------------------+
| E5014      | The envoy proxy has not completed the initialization phase and it is not ready   |
|            | to receive broadcast updates from control plane related changes. New versions    |
|            | should not be pushed if the first request has not be received. The broadcast     |
|            | update was ignored for that proxy.                                               |
+------------+----------------------------------------------------------------------------------+
| E5015      | The TypeURL of the resource being requested in the DiscoveryRequest is invalid.  |
+------------+----------------------------------------------------------------------------------+
| E5016      | The version of the DiscoveryRequest could not be parsed by ADS.                  |
+------------+----------------------------------------------------------------------------------+
| E5017      | An Envoy egress cluster which routes traffic to its original destination could   |
|            | not be configured. When a Host is not specified in the cluster config, the       |
|            | original destination is used.                                                    |
+------------+----------------------------------------------------------------------------------+
| E5018      | An Envoy egress cluster that routes traffic based on the specified Host resolved |
|            | using DNS could not be configured.                                               |
+------------+----------------------------------------------------------------------------------+
| E5019      | An Envoy cluster that corresponds to a specified upstream service could not be   |
|            | configured.                                                                      |
+------------+----------------------------------------------------------------------------------+
| E5020      | The meshed services corresponding a specified Envoy proxy could not be listed.   |
+------------+----------------------------------------------------------------------------------+
| E5021      | Multiple Envoy clusters with the same name were configured. The duplicate        |
|            | clusters will not be sent to the Envoy proxy in a ClusterDiscovery response.     |
+------------+----------------------------------------------------------------------------------+
| E5022      | The application protocol specified for a port is not supported for ingress       |
|            | traffic. The XDS filter chain for ingress traffic to the port was not created.   |
+------------+----------------------------------------------------------------------------------+
| E5023      | An XDS RBAC policy could not be generated from the specified traffic target      |
|            | policy.                                                                          |
+------------+----------------------------------------------------------------------------------+
| E5024      | An XDS filter chain could not be constructed for ingress.                        |
+------------+----------------------------------------------------------------------------------+
| E5025      | A traffic policy rule could not be configured as an RBAC rule on the proxy.      |
|            | The corresponding rule was ignored by the system.                                |
+------------+----------------------------------------------------------------------------------+
| E5026      | The SDS certificate resource could not be unmarshalled. The                      |
|            | corresponding certificate resource was ignored by the system.                    |
+------------+----------------------------------------------------------------------------------+
| E5027      | An XDS secret containing a TLS certificate could not be retrieved.               |
|            | The corresponding secret request was ignored by the system.                      |
+------------+----------------------------------------------------------------------------------+
| E5028      | The SDS secret does not correspond to a MeshService.                             |
+------------+----------------------------------------------------------------------------------+
| E5029      | The SDS secret does not correspond to a ServiceAccount.                          |
+------------+----------------------------------------------------------------------------------+
| E5030      | The identity obtained from the SDS certificate request does not match the        |
|            | identity of the proxy. The corresponding certificate request was ignored         |
|            | by the system.                                                                   |
+------------+----------------------------------------------------------------------------------+
| E6100      | A protobuf ProtoMessage could not be converted into YAML.                        |
+------------+----------------------------------------------------------------------------------+
| E6101      | The mutating webhook certificate could not be parsed.                            |
|            | The mutating webhook HTTP server was not started.                                |
+------------+----------------------------------------------------------------------------------+
| E6102      | The sidecar injection webhook HTTP server failed to start.                       |
+------------+----------------------------------------------------------------------------------+
| E6103      | An AdmissionRequest could not be decoded.                                        |
+------------+----------------------------------------------------------------------------------+
| E6104      | The timeout from an AdmissionRequest could not be parsed.                        |
+------------+----------------------------------------------------------------------------------+
| E6105      | The AdmissionRequest's header was invalid. The content type obtained from the    |
|            | header is not supported.                                                         |
+------------+----------------------------------------------------------------------------------+
| E6106      | The AdmissionResponse could not be written.                                      |
+------------+----------------------------------------------------------------------------------+
| E6107      | The AdmissionRequest was empty.                                                  |
+------------+----------------------------------------------------------------------------------+
| E6108      | It could not be determined if the pod specified in the AdmissionRequest is       |
|            | enabled for sidecar injection.                                                   |
+------------+----------------------------------------------------------------------------------+
| E6109      | It could not be determined if the namespace specified in the                     |
|            | AdmissionRequest is enabled for sidecar injection.                               |
+------------+----------------------------------------------------------------------------------+
| E6110      | The port exclusions for a pod could not be obtained. No                          |
|            | port exclusions are added to the init container's spec.                          |
+------------+----------------------------------------------------------------------------------+
| E6111      | The AdmissionRequest body could not be read.                                     |
+------------+----------------------------------------------------------------------------------+
| E6112      | The AdmissionRequest body was nil.                                               |
+------------+----------------------------------------------------------------------------------+
| E6113      | The MutatingWebhookConfiguration could not be created.                           |
+------------+----------------------------------------------------------------------------------+
| E6114      | The MutatingWebhookConfiguration could not be updated.                           |
+------------+----------------------------------------------------------------------------------+
| E6700      | An error occurred when shutting down the validating webhook HTTP server.         |
+------------+----------------------------------------------------------------------------------+
| E6701      | The validating webhook HTTP server failed to start.                              |
+------------+----------------------------------------------------------------------------------+
| E6702      | The validating webhook certificate could not be parsed.                          |
|            | The validating webhook HTTP server was not started.                              |
+------------+----------------------------------------------------------------------------------+
| E6703      | The ValidatingWebhookConfiguration could not be created.                         |
+------------+----------------------------------------------------------------------------------+
| E7000      | An error occurred while reconciling the updated CRD to its original state.       |
+------------+----------------------------------------------------------------------------------+
| E7001      | An error occurred while reconciling the deleted CRD.                             |
+------------+----------------------------------------------------------------------------------+
| E7002      | An error occurred while reconciling the updated mutating webhook to its original |
|            | state.                                                                           |
+------------+----------------------------------------------------------------------------------+
| E7003      | An error occurred while reconciling the deleted mutating webhook.                |
+------------+----------------------------------------------------------------------------------+
| E7004      | An error occurred while while reconciling the updated validating webhook to its  |
|            | original state.                                                                  |
+------------+----------------------------------------------------------------------------------+
| E7005      | An error occurred while reconciling the deleted validating webhook.              |
+------------+----------------------------------------------------------------------------------+
```

指定错误编码的详细信息可以通过执行命令 `osm support error-info <error-code>` 获取。例如：

```console
osm support error-info E1000

+------------+-----------------------------------------------------------------+
| ERROR CODE |                           DESCRIPTION                           |
+------------+-----------------------------------------------------------------+
| E1000      |  An invalid command line argument was passed to the             |
|            | application.                                                    |
+------------+-----------------------------------------------------------------+
```