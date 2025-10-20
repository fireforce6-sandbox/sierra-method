# Sierra Method

[![Build Status](https://github.com/fireforce6/sierra-method/actions/workflows/ci.yml/badge.svg)](https://github.com/fireforce6/sierra-method/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/fireforce6/sierra-method?label=Release)](https://github.com/fireforce6/sierra-method/releases/latest)


An [OML](https://github.com/opencaesar/oml)-based systems engineering methodology for modeling and analyzing complex systems.

## Clone

```bash
git clone https://github.com/fireforce6/sierra-method.git
cd sierra-method
```

## Build

Validate the consistency and correctness of the OML vocabularies:

```bash
./gradlew build
```

## Generate Documentation

Generate HTML documentation from the OML vocabularies:

```bash
./gradlew docs
```

Output will be available in `build/docs/`.

## Explore with Fuseki

### Start Fuseki Server

Start the Apache Fuseki triple store:

```bash
./gradlew startFuseki
```

Navigate to http://localhost:3030 and verify the dataset is available.

### Load Dataset

Load the OML dataset into Fuseki:

```bash
./gradlew load
```

View dataset statistics by navigating to http://localhost:3030/#/ then clicking the `Info` button followed by the `Count triples in all graphs` button.

### Run SPARQL Queries

Run the SPARQL queries

```bash
./gradlew query
```

Inspect the results in the folder `build/results`

### Stop Fuseki Server

Stop the Fuseki triple store:

```bash
./gradlew stopFuseki
```

## Publish to Maven Local

Publish the OML dataset as an archive to Maven Local:

```bash
./gradlew publishToMavenLocal
```

The archive will be available at:

```bash
ls ~/.m2/repository/io/github/fireforce6/sierra-method
```

### Publishing to GitHub Packages

This repository publishes a Maven artifact to GitHub Packages automatically when a GitHub Release is published. 

## License

Commercial License - All rights reserved. See LICENSE file for details.

## Support

For questions or contributions, please contact the project maintainers.