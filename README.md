# Overview

[GLDF](https://gldf.io) XML templates for learning purposes or an easy start for your own products. Keep in mind that they should only serve as a **starting point**, as in most examples only one specific block is highlighted. Because usually a lot of other data is missing, it is therefore recommended to combine the templates, that are relevant for your own products.

All templates are structured as follows:

- `Name of the folder containing the template`
- A short description
- Inside the folder
  - The example zipped into a `.gldf` container. This is the only file you would distribute finally
  - A `source` folder containing the example data inside the container.
  This folder is only for easier readability and would **not** be distributed

## How to get started

- Choose the template you would like to start with...
- ...or combine multiple templates for your XML as required
- Replace the data inside the `product.xml` with yours
- Replace all files like photometries or images
- Zip the content
  - The `product.xml` should be in the root directory
  - Images, photometries etc. should be in respective subdirectories
  - Finally, change the file extension of the zip archive to `.gldf`
- All templates have an example `.gldf` file created in this way

Many templates focus on a specific area of the format and include only the mandatory fields for the rest. However, since most properties are optional, they should be used as an example only. The goal should be to combine the templates with the parts you need and provide as many information about your product as possible.

## Mandatory fields

### `000_simple_luminaire`

Template for the most basic luminaire without photometry.

### `001_simple_luminaire_ldc`

Template for the most basic luminaire including photometry.

## Geometry possibilities

### `002_simple_geometry`

Minimal luminaire with a simple geometry.

### `003_l3d_geometry`

Minimal luminaire with a L3D geometry.

### `004_geometry_level_of_detail`

A luminaire with multiple L3D level of detail (LoD) geometry.

## Header metadata

### `005_header`

Minimal luminaire extended with a complete `Header` element containing all possible elements.

## Sensor products

### `006_sensor`

The most basic sensor-only product you can create.

### `007_sensor_and_lightemitter`

A luminaire with a sensor and lightemitter combined

## Photometries

### `008_photometry_complete`

Minimal luminaire extended with a `Photometry` element containing all possible elements.

## LightSources

### `009_lightsource_manadatory`

Template with mandatory only elements of a `ChangeableLightSource`. As well as an `Equipment`, which is used to reference the `ChangeableLightSource` inside the luminaires `Variant`.

### `010_lightsource_complete`

Template with a `ChangeableLightSource` element containing all possible elements. As well as an `Equipment`, which is used to reference the `ChangeableLightSource` inside the luminaires `Variant`.

### `011_lightsource_multichannel`

Template with a `MultiChannelLightSource` element, referenced by a `MultiChannelLightEmitter`.

## Spectrum

### `012_spectrum`

Luminaire with a `Spectrum` element. Note in particular how the `Spectrum` is referenced inside a `LightSource`. Which in turn is referenced through an `Equipment` element. And how it is possible to define a `Spectrum` as a file reference (spectrum1) and inside the XML itself (spectrum2).

## ControlGears

### `013_control_gear`

Luminaire with a complete `ControlGear` element containing all possible childs elements. As well as an `Equipment` referencing the `ControlGear` through `ControlGearReference`.

## ProductMetadata

### `014_product_metadata`

Luminaire with a complete `ProductMetaData` element containing all possible child elements. `ProductMetaData` is intended for global properties of a product.

## Variants

### `015_variant_simple_lightemitter`

Luminaire with a complete `Variant` element.

### `016_variant_simple_sensoremitter`

Luminaire with a complete `Variant` element containing a reference to a `SensorEmitter`.

### `017_variant_geometry_reference`

Luminaire with a complete `Variant` element containing all possible elements, a l3d geometry and a sensor.

## DescriptiveAttributes

### `018_descriptive_attributes`

Luminaire with a complete `DescriptiveAttributes` element inside `ProductMetadata` and `Variant`. `DescriptiveAttributes` values inside a `Variant` will override the global defined values in `ProductMetadata`.
