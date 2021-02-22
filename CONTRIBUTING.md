# Contributing to this project

The following is a set of guidelines for contributing to this project. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

## Versioning

This project wants to strictly adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html). Please read the document carefully. Here is a brief summary for the impatient:

> Given a version number MAJOR.MINOR.PATCH:
>
> 1. a MAJOR version includes incompatible API changes,
> 2. a MINOR version adds functionality in a backwards compatible manner, and
> 3. a PATCH version includes backwards compatible bug fixes.

I want to stress the fact that a MAJOR version is published *only* if we make changes that are not backwards compatible.

## Requirements

Wherever this is possible, pip requirements should not be strict, i.e., you should not specify all requirements with exact versions. Indeed, we want to decrease the probability of conflicts when installing this package alongside other packages. Ideally, you should always specify the minimum and the maximum version, keeping the requirements relaxed.
