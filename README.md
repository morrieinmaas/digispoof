# PROTOTYPE COMPONENT

Description
----
Next to this JSON REST API is a [graphql](/graphql) interface available.

Additional Information
----

- [Contributing](CONTRIBUTING.md)
- [ChangeLogs](CHANGELOG.md)
- [RoadMap](ROADMAP.md)
- [Security](SECURITY.md)
- [Licence](LICENSE.md)


Installation
----
We differentiate between two ways of installing this component, a local installation as part of the provided developers toolkit or a [Helm](https://helm.sh/) installation on a development or production environment.

#### Local installation
Make sure you have [docker desktop](https://www.docker.com/products/docker-desktop) running on your local machine. Then clone the repository to a directory through the [``git clone`` command](https://github.com/git-guides/git-clone) or [``git kraken``](https://www.gitkraken.com). If successful, navigate to the directory of your cloned repository in the terminal and run:

```CLI
$ docker-compose up
```
This will build the Docker image and run the used containers. When the log from the PHP container: "NOTICE: ready to handle connections" prints, you are ready to view the documentation at [localhost](http://127.0.0.1/).

#### Installation on Kubernetes or Haven
As a Haven compliant Commonground component, this component is installable on Kubernetes through Helm. The Helm files can be found in the API/Helm folder. For installing this component through Helm, open your terminal and run
```CLI
$ helm install [name] ./api/helm --kubeconfig kubeconfig.yaml --namespace [name] --set settings.env=prod,settings.debug=0,settings.cache=1
```
For an in-depth installation guide, you can refer to the [installation guide](/api/helm) included within the Helm files. It also has a short tutorial on getting your cluster ready to expose your installation to the world.

Standards
----

This component adheres to international, national and local standards (in that order), notable standards are:

- Any applicable [W3C](https://www.w3.org) standard, including but not limited to [rest](https://www.w3.org/2001/sw/wiki/REST), [JSON-LD](https://www.w3.org/TR/json-ld11/) and [WEBSUB](https://www.w3.org/TR/websub/)
- Any applicable [schema](https://schema.org/) standard
- [OpenAPI Specification](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md)
- [GAIA-X](https://www.data-infrastructure.eu/GAIAX/Navigation/EN/Home/home.html)
- [Publiccode](https://docs.italia.it/italia/developers-italia/publiccodeyml-en/en/master/index.html), see the [publiccode](api/public/schema/publiccode.yaml) for further information
- [Forum Stanaardisatie](https://www.forumstandaardisatie.nl/open-standaarden)
- [NL API Strategie](https://docs.geostandaarden.nl/api/API-Strategie/)
- [Common Ground Realisatieprincipes](https://componentencatalogus.commonground.nl/20190130_-_Common_Ground_-_Realisatieprincipes.pdf)
- [Haven](https://haven.commonground.nl/docs/de-standaard)
- [NLX](https://docs.nlx.io/understanding-the-basics/introduction)
- [Standard for Public Code](https://standard.publiccode.net/), see the [compliancy scan](publiccode.md) for further information.

This component is based on the following [schema.org](https://schema.org) sources:
- [Address](https://schema.org/PostalAddress)
- [Person](https://schema.org/Person)

Developers toolkit and technical information
----
You can find the data model, OAS documentation, and other helpful materials like a  Postman collection under ``api/public/schema``. Development support is provided through the [samenorganiseren Slack channel](https://join.slack.com/t/samenorganiseren/shared_invite/zt-dex1d7sk-wy11sKYWCF0qQYjJHSMW5Q).

A couple of quick tips when you start developing:
If you have not set up the component locally, read the tutorial to set up your local environment.
	- You can find the other components on [Github](https://github.com/ConductionNL).
	- To prevent development collisions, take a look at the [commonground componenten catalogus](https://componentencatalogus.commonground.nl/componenten?).
	- Use [Commonground.conduction.nl](https://commonground.conduction.nl/) for easy deployment of test environments to deploy your development.
	- For information on how to work with the component, you can refer to the tutorial [here](TUTORIAL.md).


Contributing
----
First of all, please read the [Contributing](CONTRIBUTING.md) guidelines ;)

But most importantly, welcome! We strive to keep an active community at [commonground.nl](https://commonground.nl/). Please drop by and tell us what you are thinking about to help you along.

Credits
----
Information about the authors of this component can be found [here](AUTHORS.md)

Copyright © [Utrecht](https://www.utrecht.nl/) 2019
