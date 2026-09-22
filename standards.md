# Augmented reality standards and primary references

The standards-body pages behind the [readme](readme.md)'s Standards section,
with editions pinned where one is current. This file indexes and links; it
does not host copies, because each body holds copyright over its own text.

## Reference models and terminology

### ISO/IEC 18039:2019 — Mixed and augmented reality (MAR) reference model

- [IEC Webstore](https://webstore.iec.ch/en/publication/64756)

Scope, key concepts, terminology and a generalised system architecture for
MAR applications, components, systems and specifications. ISO's own catalogue
page refused an automated check; the IEC Webstore lists the same joint
standard.

### ISO/IEC 18040:2019 — Live actor and entity representation in MAR

- [IEC Webstore](https://webstore.iec.ch/en/publication/65241)

A reference model, system framework and exchange format for representing and
controlling a live actor or entity inside a MAR scene.

### IEEE 2048.101-2023 — Augmented reality on mobile devices

- [IEEE Standards Association](https://standards.ieee.org/ieee/2048.101/10390)

General requirements for the software framework, components and integration
of AR systems on mobile devices, including functional and performance
requirements and test methods. Approved September 2023, published February
2024, part of the IEEE 2048 VR/AR series.

### ETSI GR ARF 001 V1.1.1 (April 2019) — AR standards landscape

- [ETSI group report (PDF)](https://www.etsi.org/deliver/etsi_gr/ARF/001_099/001/01.01.01_60/gr_arf001v010101p.pdf)

A survey of interoperability and platform standards across AR: a map of the
landscape rather than a normative specification.

## Geospatial anchoring

### OGC ARML 2.0

- [Edition 12-132r4, 24 February 2015](https://docs.ogc.org/is/12-132r4/12-132r4.html)

An XML grammar with ECMAScript bindings for describing an AR scene and
anchoring it to the real world.

### OGC GeoPose 1.0

- [Overview](https://www.ogc.org/standards/geopose/)
- [Edition 21-056r11, 8 September 2023](https://docs.ogc.org/is/21-056r11/21-056r11.html)

The position and orientation ("pose") of real or virtual objects in
earth-anchored or astronomical reference frames, in basic, advanced and
composite forms, encoded as JSON with a schema.

## Browser and runtime APIs

### W3C WebXR Augmented Reality Module

- [Specification](https://www.w3.org/TR/webxr-ar-module-1/)

Adds the `immersive-ar` session mode and environment-blending modes (opaque,
alpha-blend, additive) to the WebXR Device API.

### WebXR Hit Test and Anchors Modules

- [Hit Test](https://immersive-web.github.io/hit-test/)
- [Anchors](https://immersive-web.github.io/anchors/)

Ray casts against real-world geometry, and poses the system keeps updated as
its map of the room changes, so placed content does not drift.

### Khronos OpenXR

- [Registry](https://registry.khronos.org/OpenXR/)

The specification, headers, reference pages and conformance material for the
cross-platform XR runtime API.

## Asset and scene interchange

### glTF 2.0

- [Specification](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html)

Khronos's API-neutral runtime asset format, through which most AR content
pipelines move 3D geometry.

### OpenUSD

- [Alliance for OpenUSD](https://aousd.org/)

The Linux Foundation project standardising OpenUSD, the scene description
behind Apple's USDZ.

### MPEG-I (ISO/IEC 23090)

- [MPEG standards page](https://www.mpeg.org/standards/MPEG-I/)

A multi-part family for coded immersive media: omnidirectional video,
immersive audio, point-cloud compression, immersive video and scene
description.

## Coordination bodies

These write no standards of their own; they coordinate the bodies above.

- [W3C Immersive Web Working Group charter](https://www.w3.org/groups/wg/immersive-web/charters/active) -
  The group producing the WebXR specifications.
- [Metaverse Standards Forum](https://metaverse-standards.org/) - Launched in
  June 2022 to align requirements across standards organisations.
