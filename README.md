# RKVST Documentation

This is the Home of the RKVST Documentation

The RKVST API enables proof of origin, proof of authenticity and proof of provenance for any digital asset.  It is organized around REST (https://en.wikipedia.org/wiki/Representational_state_transfer). 

The RKVST API can easily be connected to existing data in the cloud or on-prem to provide instantly verifiable data integrity, transparency & trust services for private and public assets.

An interactive RKVST API console to run tests and generate code which can be quickly added into any application is a available in the free service we offer at www.rkvst.com.

These docs describe all the capabilities of the RKVST API including the creation & management of provenance metadata, access controls for private and public asset sharing, compliance policies to continuously monitor vulnerabilies and administration controls for account/user/application/3rd party management.

## Contributing

To contribute to these Docs please refer to our [Contributing Guidelines]()

We'll happily review any suggestions!

## Getting Started

1. To begin pull the latest RKVST docs from Github.

```bash
git clone git@github.com:rkvst/rkvst-docs.git
```

2. Move into the directory.

```bash
cd rkvst-doks
```

3. Install the DOKS Dependencies.

```bash
npm install
```

4. To run a local RKVST Docs Server it is advisable to use the `rkvst-doks` wrapper

```bash
rkvst-doks start
```

This will build a local version of the server that can be accessed at [http://localhost:1313](https://localhost:1313).


## Credits

This Documentation was put together using some amazing opensource tools and projects, this is a list of known projects included but is not exhaustive

* The wonderful [Doks Theme](https://github.com/h-enk/doks). License: [MIT](https://github.com/h-enk/doks/blob/master/LICENSE)
* Built on top of [Hugo](https://github.com/gohugoio/hugo). License: [Apache License 2.0](https://github.com/gohugoio/hugo/blob/master/LICENSE)
* With inspiration and examples from the [Kubernetes Docs](https://github.com/kubernetes/website). License: [CC BY-SA 4.0](https://github.com/kubernetes/website/blob/master/LICENSE)
* Screenshotting dynamically handled by the [Robot Framework](https://github.com/robotframework/robotframework) using the [Selenium2](https://github.com/SeleniumHQ/selenium) package. Licenses: [Apache License 2.0](https://github.com/robotframework/robotframework/blob/master/LICENSE.txt) and [Apache License 2.0](https://github.com/SeleniumHQ/selenium/blob/trunk/LICENSE) respectively
* Hosted by GitHub Pages and built using GH Actions
