# crispy-parakeet

Welcome to crispy-parakeet, a reposoitory dedicated to reading a writing NASAs Parameter Value Language (PVL).

This repo plans to deilver a light weight and fast PVL parsing tool, built using C/C++ and a single pass approach to reading PVL data to make reads as fast and seemless as possible for users.

For more details regarding PVL and the specification, checkout the language specification provided by NASA [here](https://pvl.readthedocs.io/en/stable/_downloads/3eb86e5f16e283d04719e72d06935e91/CCSDS-641.0-B-2-PVL.pdf). This document covers how to correctly read and write PVL and will be strictly adhered to for development and testing.

### Where is PVL used?

PVL is ubiquotous when working with planetary imagery, specifically imagery built around Planetary Data System 3 (PDS3) standards. These data all use PVL information at the beginning of the file to define metadata. This is commonly known as a PVL "label". Reading these PVL Headers is essential to processing the rest of the file, as it defines how the image data are stored (byte sizes, byte starting locations, endianness etc.).

As PVL was developed in conjunction with NASA, it is not used much outside of the PDS standards.

While this may be a niche set of labels, the volume of data that uses them for processing is immense. To get an idea of scale, the pds image atlas provided by NASA hosts close to 40,000,000 data products, most containing PDS3 labels. This does not cover all missions, missing many of the Japanese and European mission datasets. Providing consitant, reliable and fast access to these headers would be a huge benefit to the planetary community.

## Contributing

We are open to contributions from the community to improve crispy-parakeet. To see our process for handling contributions, please see the [contributing guidelines](CONTRIBUTING.md).

## Code of Conduct

We expect every member of our community to create an open, honest, and welcoming environment. This will allow us all to be as productive as possible. For any questions about our expectations, please see the [code of conduct](CODE_OF_CONDUCT.md).
