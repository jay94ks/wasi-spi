# WASI SPI

A proposed [WebAssembly System Interface](https://github.com/WebAssembly/WASI) API.

### Current Phase

[Fill in the current phase, e.g. Phase 1]

### Champions

- jay94ks
- [Champion 2]
- [etc.]

### Phase 4 Advancement Criteria

TODO before entering Phase 2.

### Introduction

The WASI-SPI proposal defines an API for the SPI communication.

### Goals [or Motivating Use Cases, or Scenarios]

The primary goal is to provide an interface that WASI programs can use to read and write data over SPI peripherals.

### Non-goals

SPI interfaces can be covered by GPIO toggling (bitbang) but it cannot be enough to replace hardware SPI's performance.
the purpose of this proposal is to solely focus on SPI.

### API walk-through

The full API documentation can be found [here](wasi-proposal-template.md).

[Walk through of how someone would use this API.]

#### [Use case 1]

[Provide example code snippets and diagrams explaining how the API would be used to solve the given problem]

#### [Use case 2]

[etc.]

### Detailed design discussion

[This section should mostly refer to the .wit.md file that specifies the API. This section is for any discussion of the choices made in the API which don't make sense to document in the spec file itself.]

#### SPI, I2C, GPIO, PWM must be separately provided because concept is different.
In software side, just class or interface type can share methods between different peripherals. but actually, their working ways are quiet different although concept is similar.

#### Why are there no constructors for the SPI interface? How does one obtain an SPI handle?
SPI resources will be constructed in many different ways on different devices, so worlds that include the SPI interface should also include a way to obtain SPI handles. Typically this will either be by having SPI handles passed into exported functions as parameters, or by having SPI handles returned from imported functions.
(this paragraph is copied from wasi-i2c)

### Stakeholder Interest & Feedback

TODO before entering Phase 3.

### References & acknowledgements

This is not an official paper or, not written by expert.
This is just written to fill empty page by hobbyist.

Many thanks for valuable feedback and advice from:

- [Person 1]
- [Person 2]
- [etc.]
