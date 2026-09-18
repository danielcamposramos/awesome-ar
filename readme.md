# Awesome AR [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Augmented reality: the see-through optics, the tracking that decides where the world is, the standards built on top, and sixty years of demos behind them.

Augmented reality is the harder half of the problem, because you cannot fake the world. A virtual reality headset only has to be convincing; an AR display has to agree with the room, frame after frame, while your head moves. That agreement is called registration, and it has been the subject's central difficulty since Ivan Sutherland hung a see-through display from a ceiling in 1968. Richard Holloway measured it in 1995 and reached a conclusion the field still lives with: even at moderate head speeds, system delay causes more registration error than every other source combined.

This list collects the optics, the tracking, the SDKs and the standards, with the history that explains the vocabulary and the closures that explain the caution.

*AI was leveraged as a partner in the development of this work — [more information here](PROVENANCE.md).*

## Contents

- [History](#history)
- [Display optics](#display-optics)
- [Glasses and headsets](#glasses-and-headsets)
- [Open hardware](#open-hardware)
- [SDKs and frameworks](#sdks-and-frameworks)
- [Tracking and mapping](#tracking-and-mapping)
- [Standards](#standards)
- [Where it is actually used](#where-it-is-actually-used)
- [Human factors](#human-factors)
- [Platforms that closed](#platforms-that-closed)
- [Related lists](#related-lists)
- [Events](#events)
- [Known gaps](#known-gaps)

## History

- [Head-up display](https://en.wikipedia.org/wiki/Head-up_display) - Where the idea starts, in aviation rather than computing: reflector gunsights, then a 1942 British system combining radar with the gunsight, then the Royal Navy's Buccaneer, from whose era the term itself dates. The Oldsmobile Cutlass Supreme put one in a production car in 1988.
- [Head-mounted display](https://en.wikipedia.org/wiki/Head-mounted_display) - In 1968 Ivan Sutherland and his student Bob Sproull built the first head-mounted display driven by computer graphics, at Harvard. It drew stereoscopic wireframes over the real room through half-silvered mirrors, which makes it an AR display before the phrase existed.
- [Augmented reality](https://en.wikipedia.org/wiki/Augmented_reality) - The subject's own overview, and the source of the name: the term is attributed to Thomas Caudell, a Boeing researcher who, with David Mizell, proposed head-worn displays that would show assembly workers where each wire of a 777 harness belonged. AR's first job was maintenance instructions, not games.
- [Virtual fixtures](https://en.wikipedia.org/wiki/Virtual_fixture) - Louis Rosenberg's 1992 system at the USAF Armstrong Laboratory, described as the first immersive augmented reality system ever built: overlays that guided a human operator's hands rather than simply informing them.
- [KARMA](https://graphics.cs.columbia.edu/projects/karma/karma.html) - Knowledge-based Augmented Reality for Maintenance Assistance, by Steven Feiner, Blair MacIntyre and Doree Seligmann at Columbia, 1993: a see-through headset that explained how to service a laser printer, and the ancestor of every "AR for field service" pitch since.
- [Reality–virtuality continuum](https://en.wikipedia.org/wiki/Reality%E2%80%93virtuality_continuum) - Milgram, Takemura, Utsumi and Kishino's 1994 framing, which gave the field the vocabulary it still argues in, including where "mixed reality" sits between the two ends.
- [ARToolKit](https://en.wikipedia.org/wiki/ARToolKit) - Hirokazu Kato's 1999 marker-tracking library from the Nara Institute of Science and Technology, the software that let a generation put a cube on a printed square, and still alive as artoolkitX.
- [ARQuake](https://www.tinmith.net/arquake/) - The University of South Australia's outdoor AR game, from 2000: a modified Quake engine, GPS, an inertial orientation tracker and a backpack computer, played by walking around a campus. The hardware is comical now and the design problems are current.
- [Wikitude](https://en.wikipedia.org/wiki/Wikitude) - The Salzburg company that shipped mobile AR from 2008, was bought by Qualcomm in 2021, and shut its services down in September 2024, which is the whole arc of the mobile AR SDK era in one entry.
- [Google Glass](https://en.wikipedia.org/wiki/Google_Glass) - Developer release in 2013, consumer release in 2014, Explorer Edition killed in January 2015, and the enterprise edition finally discontinued in March 2023. The most-discussed failure in the field, and the one that taught it that social acceptability is a hardware requirement.
- [Microsoft HoloLens](https://en.wikipedia.org/wiki/Microsoft_HoloLens) - The 2016 development edition and the 2019 HoloLens 2 at $3,500: the headset that showed what waveguide optics and hand tracking could do, and never shipped a consumer version.
- [Pokémon Go](https://en.wikipedia.org/wiki/Pok%C3%A9mon_Go) - The 2016 game that put AR in hundreds of millions of pockets, using the camera and gyroscope to place a creature in the street, and the reason most people's first AR experience needed no headset at all.
- [ARKit](https://en.wikipedia.org/wiki/ARKit) - Apple's framework, announced in June 2017 with iOS 11, which made phone AR an ordinary platform feature.
- [ARCore](https://en.wikipedia.org/wiki/ARCore) - Google's answer, running on Android 7.0 and later, and the successor that replaced Tango's depth-sensing hardware approach with software on ordinary phones.
- [Magic Leap](https://en.wikipedia.org/wiki/Magic_Leap) - Founded in 2010, the most heavily funded promise in the field's history: Magic Leap One in 2018, Magic Leap 2 in 2022, a pivot to enterprise, and end of life for the first headset's cloud services at the end of 2024.

## Display optics

- [Optical head-mounted display](https://en.wikipedia.org/wiki/Optical_head-mounted_display) - The optics that let you see the room and the image at once, and the four families of waveguide that do it: diffractive, holographic, polarized and reflective. Which family a product uses predicts most of its field of view, weight and price.
- [Virtual retinal display](https://en.wikipedia.org/wiki/Virtual_retinal_display) - Drawing the image directly on the retina, invented by Kazuo Yoshinaka at NEC in 1986 and developed at the University of Washington from 1991. It reappears in Intel's abandoned Vaunt glasses and in QD Laser's RETISSA, which is used as a sight aid rather than a display.
- [Birdbath optics](https://vrarwiki.com/wiki/Birdbath_optics) - The combiner architecture behind most viewer-style AR glasses: a flat beam splitter plus a curved partially reflective mirror. It buys brightness and colour at the cost of bulk, which is why the glasses that use it look like sunglasses and the waveguide ones look like spectacles.

## Glasses and headsets

- [Apple Vision Pro](https://en.wikipedia.org/wiki/Apple_Vision_Pro) - Video passthrough rather than see-through optics, with twelve cameras reconstructing the room. Worth noting for vocabulary as much as hardware: Apple avoids the term VR entirely, and the device is usually classified as mixed reality.
- [Snap Spectacles](https://en.wikipedia.org/wiki/Spectacles_(product)) - The fifth-generation standalone AR glasses: waveguide displays at a 46° diagonal field of view, four cameras for hand tracking and mapping, running Snap's own OS, with a consumer version slated for 2026.
- [Meta Orion](https://www.uploadvr.com/meta-connect-2024-orion-prototype-ar-glasses/) - The prototype Meta showed in September 2024 at a 70° field of view, and explicitly did not sell: around $10,000 a unit to build. Included because the honest state of the art is a prototype, not a product.
- [Xreal One](https://tutorials.xreal.com/docs/glasses/one-series/spec/) - Birdbath viewer glasses with 1920×1080 micro-OLED per eye at 50°, up to 120 Hz: the category that is really a wearable monitor, and the most widely sold AR hardware by far.
- [Viture Pro 2](https://www.viture.com/pro2) - The same category from a different maker, at 63 grams, with dioptre adjustment built in so glasses wearers do not need inserts.
- [Rokid Glasses](https://global.rokid.com/products/rokid-glasses) - Binocular micro-LED waveguides at 30° and 49 grams, aimed at information rather than immersion: notifications, a camera, and live translation.
- [Even Realities G1](https://www.evenrealities.com/g1) - The minimal end: a micro-LED waveguide at 25° and 640×200 per eye, claiming 98% passthrough clarity and over a day of battery. It shows text, and that is the point.

## Open hardware

- [Project North Star](https://github.com/leapmotion/ProjectNorthStar) - Leap Motion's open AR headset design from 2018, over 100° field of view and 3D printable, still the reference point for anyone building their own. Note the licence discrepancy: the repository is marked GPL-3.0, while much of the original coverage described the release as Apache-2.0.
- [Brilliant Labs Frame](https://github.com/brilliantlabsAR/frame-codebase) - The published codebase for Frame, the company's 2024 glasses, from a Hong Kong maker that has consistently opened its hardware and firmware.
- [Monocle](https://github.com/brilliantlabsAR/monocle-micropython) - MicroPython for the clip-on display that preceded Frame, and the easiest way into hackable AR hardware.

## SDKs and frameworks

- [ARCore SDK for Android](https://github.com/google-ar/arcore-android-sdk) - Google's SDK, actively developed, and the practical baseline for phone AR outside Apple's platforms.
- [OpenXR SDK](https://github.com/KhronosGroup/OpenXR-SDK) - The Khronos loader and headers. For AR specifically, this is where the spatial-entity extensions arrive.
- [WebXR AR Module repository](https://github.com/immersive-web/webxr-ar-module) - The working repository behind the browser's AR capabilities, for following how the specification is actually being argued.
- [Vuforia](https://www.ptc.com/en/products/vuforia) - PTC's proprietary enterprise AR platform, and the one most industrial deployments are actually built on, whatever the open-source alternatives.
- [artoolkitX](https://github.com/artoolkitx/artoolkitx) - The maintained continuation of ARToolKit, still the reference implementation for marker tracking.
- [AR.js](https://github.com/AR-js-org/AR.js) - Image tracking, location-based AR and marker tracking in a browser, with no app to install.
- [MindAR](https://github.com/hiukim/mind-ar-js) - Web image and face tracking built on TensorFlow.js, the lighter-weight route to the same place.
- [ArUco](https://www.uco.es/investiga/grupos/ava/portfolio/aruco/) - The square-marker library from the University of Córdoba, designed for camera pose estimation and robust under partial occlusion. When something needs to know exactly where a surface is, this is still the cheap answer.
- [AprilTag](https://april.eecs.umich.edu/software/apriltag) - The University of Michigan's fiducial system, used across AR, robotics and camera calibration, with an [implementation](https://github.com/AprilRobotics/apriltag) that remains actively maintained.

## Tracking and mapping

Registration is a tracking problem before it is a graphics problem. These are the systems that answer "where am I, and where is the world".

- [Simultaneous localization and mapping](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping) - Building a map of an unknown space while tracking yourself inside it. It is what makes inside-out headsets and phone AR possible at all.
- [Visual odometry](https://en.wikipedia.org/wiki/Visual_odometry) - Position and orientation from camera images alone; add an inertial measurement unit and it becomes visual-inertial odometry, which is what every current device actually runs.
- [ORB-SLAM3](https://github.com/UZ-SLAMLab/ORB_SLAM3) - The best-known open visual SLAM system, covering monocular, stereo and RGB-D input with inertial fusion.
- [OpenVINS](https://github.com/rpng/open_vins) - A filter-based visual-inertial estimator from the University of Delaware, widely used as a research baseline.
- [VINS-Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono) - HKUST's monocular visual-inertial system, one of the most cited implementations in the field.
- [VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion) - Its multi-sensor successor, adding stereo and GPS fusion.
- [Basalt](https://github.com/VladyslavUsenko/basalt) - Visual-inertial odometry and mapping with an emphasis on accuracy and calibration, and the tracking used by several Linux XR projects.
- [Kimera](https://github.com/MIT-SPARK/Kimera-VIO) - MIT's real-time metric-semantic system: not just where things are, but what they are, which is where AR tracking is heading.
- [RTAB-Map](https://github.com/introlab/rtabmap) - Appearance-based mapping with loop closure, long-lived and still actively developed, and the most practical of these to simply run.

## Standards

- [OGC ARML 2.0](https://www.ogc.org/standards/arml/) - The Open Geospatial Consortium's Augmented Reality Markup Language, approved in 2015, which describes virtual objects in a scene and anchors them to the real world.
- [WebXR Augmented Reality Module](https://www.w3.org/TR/webxr-ar-module-1/) - The W3C specification extending the WebXR Device API to AR hardware.
- [OpenXR Spatial Entities Extensions](https://www.khronos.org/blog/openxr-spatial-entities-extensions-released-for-developer-feedback) - Khronos's first open standard for spatial computing: plane and marker detection, spatial anchors, and persistence across sessions, so an anchor placed today survives until tomorrow on hardware from more than one vendor.
- [XR Accessibility User Requirements](https://www.w3.org/TR/xaur/) - The W3C note on what people with disabilities need from immersive environments. It is a Working Group Note rather than a Recommendation, and it is still the best starting point.
- [Open AR Cloud](https://openarcloud.org/about/) - The organisation pushing for open, interoperable spatial computing data and standards, including GeoPose and a spatial content discovery protocol, against a default future in which each vendor owns its own map of your city.

## Where it is actually used

- [Augmented reality in oncological surgery](https://pmc.ncbi.nlm.nih.gov/articles/PMC10702732/) - A systematic review that is worth reading for its numbers rather than its enthusiasm: registration error under 3 mm in orthopaedic work, and from under 1 mm to 2 cm in maxillofacial work depending on method. It concludes AR is viable when paired with external navigation, and that more pre-clinical testing is needed first.
- [XR technology trends in surgery](https://pmc.ncbi.nlm.nih.gov/articles/PMC11763273/) - The companion review, useful for the division of labour it describes: AR and mixed reality for guidance during an operation, VR for planning and training before it.
- [HoloAnatomy](https://case.edu/holoanatomy/) - Case Western Reserve's mixed-reality anatomy teaching, the first third-party HoloLens application, now licensed to institutions beyond its own. Its claim, that students learn up to twice as fast as with traditional dissection, is the strongest education result the field has.
- [Google Maps Live View](https://techcrunch.com/2020/10/01/google-maps-gets-improved-live-view-ar-directions/) - Camera and GPS combined to paint directions onto the street, and the most-used consumer AR feature that nobody calls AR.
- [AR in heritage museum exhibits](https://hrmars.com/papers_submitted/23447/exploring-augmented-reality-integration-for-enhancing-heritage-museum-exhibits-a-focus-on-innovative-display-design.pdf) - An open-access 2024 study of how AR changes exhibit design and visitor engagement, for the cultural-heritage side of the subject.

## Human factors

- [Vergence–accommodation conflict](https://en.wikipedia.org/wiki/Vergence-accommodation_conflict) - Your eyes converge at the virtual distance and focus at the real one, and every fixed-focus headset creates the mismatch. It causes eye strain and fatigue, and it is the reason varifocal optics keep being attempted.
- [Registration errors in augmented reality systems](https://www.cs.unc.edu/techreports/95-016.pdf) - Richard Holloway's 1995 UNC dissertation, still the foundational measurement of why the image does not sit still: system delay, optical distortion and tracker error, with delay dominating everything else at moderate head speeds.
- [Death by Pokémon GO](https://www.nber.org/system/files/working_papers/w24308/w24308.pdf) - An NBER working paper measuring crashes, injuries and deaths near locations where the game could be played while driving. It belongs in an AR list precisely because it is not about headsets: attention is the resource this medium spends.

## Platforms that closed

AR has buried more products than it ships, and the dates matter for anyone deciding what to build on.

- [Google Tango](https://en.wikipedia.org/wiki/Tango_(platform)) - Depth-sensing phone AR from 2014, ended in March 2018 in favour of ARCore, which is the moment the field decided special hardware in the phone was not the way.
- [HoloLens 2 discontinuation](https://techcrunch.com/2024/10/01/microsoft-hololens-2-discontinued-with-no-successor-in-site/) - Confirmed in October 2024 with no successor, updates promised to the end of 2027. The most capable AR headset ever sold has no replacement from its maker.
- [Meta Spark](https://spark.meta.com/blog/meta-spark-announcement/) - Meta's AR creation platform for Instagram and Facebook effects, shut to third-party creators on 14 January 2025, taking a large body of creator work with it.
- [Layar](https://en.wikipedia.org/wiki/Layar) - The Amsterdam AR browser of 2009, acquired in 2014 and wound down by 2016, and the clearest artefact of the era when AR was going to be a browser.
- [Metaio](https://en.wikipedia.org/wiki/Metaio) - The Munich SDK maker bought by Apple in May 2015, which stopped selling to everyone else immediately. Two years later the same technology surfaced as ARKit.
- [8th Wall](https://www.8thwall.com/blog/post/200330871818/agog-supports-8th-walls-next-chapter) - The exception, and the reason this section is not simply a graveyard. Niantic wound the commercial WebAR platform down, but rather than switching it off, nearly a decade of XR engine and WebAR tooling was released as open source in March 2026, with the company Agog backing its continuation.

## Related lists

- [awesome-webxr](https://github.com/msub2/awesome-webxr) - The browser side: WebXR engines, frameworks and communities, which this list leaves to it.
- [awesome-vr](https://github.com/danielcamposramos/awesome-vr) - Virtual reality: headsets, open runtimes, standards and the platforms that were switched off.
- [awesome-stereoscopy](https://github.com/danielcamposramos/awesome-stereoscopy) - The stereo medium itself, from Wheatstone in 1838 to spatial video: formats, packings, signalling and 3D cinema.
- [Awesome-ARKit](https://github.com/olucurious/Awesome-ARKit) - A large iOS-specific collection, for Apple platform work in particular.
- [awesome-mixed-reality](https://github.com/saurabhchalke/awesome-mixed-reality) - Mixed reality development resources spanning both sides of the passthrough line.
- [awesome-visionOS](https://github.com/tomkrikorian/awesome-visionOS) - Apple's platform in depth, including its passthrough approach.
- [awesome-lidar](https://github.com/szenergy/awesome-lidar) - Lidar sensors and datasets, for the depth-sensing hardware behind much of the tracking above.
- [awesome-computer-vision](https://github.com/jbhuang0604/awesome-computer-vision) - The research field underneath the SLAM and tracking section.

## Events

- [Augmented World Expo](https://www.awexr.com/about_awe) - Founded in 2010 by Ori Inbar, the long-running industry gathering for AR and VR, and the most reliable annual snapshot of what is actually shipping.

## Known gaps

Stated openly, because a list that hides its blind spots is worse than one that names them. These are the places this list is weakest, and the contributions most wanted:

**Chinese and Japanese AR** is barely here. Rokid appears, but the wider ecosystem — including makers publishing mainly in their own languages — is missing. Contributions in any language are wanted; cite what you can.

**Industrial deployments** are represented by their vendors rather than by evidence. Boeing's wiring harnesses started this field, and there is no good public account here of what current factory and field-service AR actually achieves.

**Communities** are not listed yet, beyond one annual event. The active ones sit mostly on platforms whose pages could not be verified in the ordinary way, and an unverified link is worse than an admitted gap.

**Automotive AR** gets one line in the head-up display entry. Windshield AR is shipping in production cars now and deserves its own sources.

**Two open discrepancies**, left visible rather than resolved by guesswork: Project North Star's licence is marked GPL-3.0 on GitHub but was widely reported as Apache-2.0, and ARCore's first public appearance is dated to 2018 here, though a developer preview is generally reported in 2017.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.
