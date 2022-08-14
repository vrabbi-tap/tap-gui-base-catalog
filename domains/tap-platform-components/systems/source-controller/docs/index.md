# FluxCD Source Controller

The fluxcd-source-controller is a Kubernetes Operator, specialised in artifacts acquisition
from external sources such as Git, Helm repositories and S3 buckets.
The source-controller implements the
[source.toolkit.fluxcd.io](https://github.com/fluxcd/source-controller/tree/master/docs/spec/v1beta1) API in GitHub
and is a core component of the [GitOps toolkit](https://toolkit.fluxcd.io).

# Tanzu Source Controller

Tanzu Source Controller provides a standard interface for artifact acquisition. It supports two resource types:

- ImageRepository
- MavenArtifact

An `ImageRepository` resource can resolve the source from the contents of an image in an image registry. This enables app developers to create and update workloads from local source code or a code repository.

A `MavenArtifact` resource can resolve a binary artifact from a Maven repository. This functionality enables the supply chain to support artifacts produced externally.

>**Note:** Fetching `RELEASE` version from GitHub packages is not currently supported. The metadata.xml in GitHub packages does not have the `release` tag that contains the released version number. For more information, see [Maven-metadata.xml is corrupted on upload to registry](https://github.community/t/maven-metadata-xml-is-corrupted-on-upload-to-registry/177725) on GitHub.

Tanzu Source Controller extends the functionality. For more information about FluxCD Source Controller, see the
[fluxcd/source-controller](https://github.com/fluxcd/source-controller) project on GitHub.
