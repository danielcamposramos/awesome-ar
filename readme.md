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
- [Communities and archives](#communities-and-archives)
- [In fiction](#in-fiction)
- [Related lists](#related-lists)
- [Events](#events)
- [Known gaps](#known-gaps)

## History

### Optical precursors

- [Pepper's ghost](https://en.wikipedia.org/wiki/Pepper%27s_ghost) - The 1862 stage illusion popularised by John Henry Pepper from Henry Dircks's design: a pane of glass at 45 degrees reflects a hidden, lit figure into the scene. It is the oldest working see-through combiner, and the principle behind most "hologram" performances since.

### Aviation and the military

- [Head-up display](https://en.wikipedia.org/wiki/Head-up_display) - Where the idea starts, in aviation rather than computing: reflector gunsights, then a 1942 British system combining radar with the gunsight, then the Royal Navy's Buccaneer, from whose era the term itself dates. The Oldsmobile Cutlass Supreme put one in a production car in 1988.
- [AIRPASS](https://en.wikipedia.org/wiki/AIRPASS) - Ferranti's interception radar for the English Electric Lightning, in RAF service from 1960, which fed what its history describes as the world's first head-up display.
- [Helmet-mounted display](https://en.wikipedia.org/wiki/Helmet-mounted_display) - The military line of head-worn sights: Hughes's Electrocular in 1962, Honeywell's sight on US Navy F-4Js in the early 1970s, South African helmet sights from 1975, the MiG-29 with the R-73 missile and the Apache's IHADSS in 1985, and Elbit's DASH in the early 1990s.
- [F-35 Gen III helmet display](https://www.rtx.com/collinsaerospace/what-we-do/industries/military-and-defense/displays-and-controls/airborne/helmet-mounted-displays/f-35-gen-iii-helmet-mounted-display-system) - Collins Aerospace's helmet-mounted display for the F-35, drawing flight and sensor information on the visor wherever the pilot looks: the current end of the line that started with gunsights.

### Laboratory origins, 1968–2002

- [Head-mounted display](https://en.wikipedia.org/wiki/Head-mounted_display) - In 1968 Ivan Sutherland and his student Bob Sproull built the first head-mounted display driven by computer graphics, at Harvard. It drew stereoscopic wireframes over the real room through half-silvered mirrors, which makes it an AR display before the phrase existed.
- [A head-mounted three dimensional display](https://www.computerhistory.org/collections/catalog/102792811) - The Computer History Museum's record of Sutherland's 1968 AFIPS paper and the slides he presented with it, naming H. Quintin Foster Jr. as the person wearing the display in the photographs.
- [Augmented reality](https://en.wikipedia.org/wiki/Augmented_reality) - The subject's own overview, and the source of the name: the term is attributed to Thomas Caudell, a Boeing researcher who, with David Mizell, proposed head-worn displays that would show assembly workers where each wire of a 777 harness belonged. AR's first job was maintenance instructions, not games.
- [Caudell and Mizell, 1992](https://ieeexplore.ieee.org/document/183317) - "Augmented reality: an application of heads-up display technology to manual manufacturing processes", the Boeing paper itself.
- [Virtual fixtures](https://en.wikipedia.org/wiki/Virtual_fixture) - Louis Rosenberg's 1992 system at the USAF Armstrong Laboratory, described as the first immersive augmented reality system ever built: overlays that guided a human operator's hands rather than simply informing them.
- [Virtual Fixtures, 1991–1994](https://sites.google.com/view/louisrosenberg/virtual-fixtures-1991-1994) - Louis Rosenberg's own account of the USAF Armstrong Laboratory, Stanford and NASA Ames project, with haptics and 3D audio alongside the visual overlays.
- [Virtual Fixtures technical report](https://web.archive.org/web/20250201172603/https://apps.dtic.mil/sti/pdfs/ADA292450.pdf) - Rosenberg's Armstrong Laboratory report AL/CF-TR-1994-0089, "The Use of Virtual Fixtures as Perceptual Overlays to Enhance Operator Performance in Remote Environments", archived from DTIC.
- [KARMA](https://graphics.cs.columbia.edu/projects/karma/karma.html) - Knowledge-based Augmented Reality for Maintenance Assistance, by Steven Feiner, Blair MacIntyre and Doree Seligmann at Columbia, 1993: a see-through headset that explained how to service a laser printer, and the ancestor of every "AR for field service" pitch since.
- [Reality–virtuality continuum](https://en.wikipedia.org/wiki/Reality%E2%80%93virtuality_continuum) - Milgram, Takemura, Utsumi and Kishino's 1994 framing, which gave the field the vocabulary it still argues in, including where "mixed reality" sits between the two ends.
- [Steve Mann](https://en.wikipedia.org/wiki/Steve_Mann_%28inventor%29) - The wearable-computing pioneer: Digital Eye Glass and EyeTap work from 1978, founder of the MIT Media Lab's wearable computing project, now at the University of Toronto.
- [Thad Starner](https://en.wikipedia.org/wiki/Thad_Starner) - Has worn a self-built wearable computer daily since 1993, co-founded the IEEE International Symposium on Wearable Computers, and was a technical lead on Google's Project Glass: the line from wearable computing to Glass.
- [Glasstron](https://en.wikipedia.org/wiki/Glasstron) - Sony's head-mounted video displays, sold from 1996 into the early 2000s. They had no tracking, but they were a Japanese consumer head-worn display fifteen years before Glass.
- [ARToolKit](https://en.wikipedia.org/wiki/ARToolKit) - Hirokazu Kato's 1999 marker-tracking library from the Nara Institute of Science and Technology, the software that let a generation put a cube on a printed square, and still alive as artoolkitX.
- [Kato and Billinghurst, 1999](https://www.hitl.washington.edu/artoolkit/Papers/IWAR99.kato.pdf) - "Marker Tracking and HMD Calibration for a Video-based Augmented Reality Conferencing System", the paper that became ARToolKit, hosted by the University of Washington lab that co-developed it.
- [ARQuake](https://www.tinmith.net/arquake/) - The University of South Australia's outdoor AR game, from 2000: a modified Quake engine, GPS, an inertial orientation tracker and a backpack computer, played by walking around a campus. The hardware is comical now and the design problems are current.
- [ARQuake paper, 2002](https://www.tinmith.net/papers/thomas-puc-2002.pdf) - The project's own account in Personal and Ubiquitous Computing: the GPS, compass and fiducial tracking architecture behind the game.

### Phones, then headsets

- [Wikitude](https://en.wikipedia.org/wiki/Wikitude) - The Salzburg company that shipped mobile AR from 2008, was bought by Qualcomm in 2021, and shut its services down in September 2024, which is the whole arc of the mobile AR SDK era in one entry.
- [Google Glass](https://en.wikipedia.org/wiki/Google_Glass) - Developer release in 2013, consumer release in 2014, Explorer Edition killed in January 2015, and the enterprise edition finally discontinued in March 2023. The most-discussed failure in the field, and the one that taught it that social acceptability is a hardware requirement.
- [Microsoft HoloLens](https://en.wikipedia.org/wiki/Microsoft_HoloLens) - The 2016 development edition and the 2019 HoloLens 2 at $3,500: the headset that showed what waveguide optics and hand tracking could do, and never shipped a consumer version.
- [Pokémon Go](https://en.wikipedia.org/wiki/Pok%C3%A9mon_Go) - The 2016 game that put AR in hundreds of millions of pockets, using the camera and gyroscope to place a creature in the street, and the reason most people's first AR experience needed no headset at all.
- [ARKit](https://en.wikipedia.org/wiki/ARKit) - Apple's framework, announced in June 2017 with iOS 11, which made phone AR an ordinary platform feature.
- [ARCore](https://en.wikipedia.org/wiki/ARCore) - Google's answer, running on Android 7.0 and later, and the successor that replaced Tango's depth-sensing hardware approach with software on ordinary phones. It appeared as a [developer preview on 29 August 2017](https://android-developers.googleblog.com/2017/08/arcore-augmented-reality-at-android.html) and left preview as [ARCore 1.0 on 23 February 2018](https://developers.googleblog.com/2018/02/announcing-arcore-10-and-new-updates-to.html).
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

### China, Japan and Korea

- [XREAL](https://www.xreal.com/about) - The Chinese maker of the Xreal One above, founded as Nreal in 2017 and renamed in 2023.
- [INMO](https://www.inmo.com/pages/about-us) - Shenzhen maker of wireless AR glasses with on-device SLAM and six-degree-of-freedom tracking.
- [RayNeo](https://www.rayneo.com/pages/about-us) - TCL's AR glasses brand, built on binocular full-colour MicroLED waveguides.
- [OPPO Air Glass](https://www.oppo.com/en/newsroom/press/oppo-air-glass/) - A 30 g monocular waveguide "assisted reality" device announced in December 2021 and sold in mainland China from early 2022.
- [Epson Moverio](https://www.epson.eu/en_EU/moverio-smart-glasses) - Epson's Japanese line of binocular see-through smart glasses with Si-OLED displays, used for remote assistance, guided work and captioning, with a [developer portal](https://tech.moverio.epson.com/en/).
- [Canon MREAL](https://global.canon/en/technology/canon-tech/tech/mr/) - Canon's video see-through mixed-reality headsets, prototyped from 2007; the MREAL X1 registers its position from ordinary floor patterns, with no markers.
- [Sony and Siemens XR headset](https://www.sony.co.jp/en/news-release/202401/24-001E/) - Sony's January 2024 announcement of a video see-through headset with 4K OLED microdisplays, developed with Siemens for industrial design work.
- [Sharp and NTT Docomo MiRZA](https://roadtovr.com/sharp-ntt-docomo-mizra-ar-glasses/) - 125 g AR glasses from Sharp and NTT Docomo's XR venture, with a 45° field of view through LetinAR optics, launched in Japan in autumn 2024.
- [LetinAR](https://letinar.com/) - South Korean maker of "pin mirror" AR combiner optics, used by several Asian glasses makers.
- [Shadow Creator](https://web.archive.org/web/20200806125327/http://www.shadowcreator.com:80/) - Shanghai maker of the JIMO and Action One mixed-reality glasses and the Halo Mini, whose tagline promised to let you "see the world like Iron Man". Its domain now serves unrelated content, so this is the archived 2020 site.
- [Baidu DuSee](https://venturebeat.com/2016/08/03/baidu-augmented-reality/) - Baidu's 2016 AR platform inside its mobile search app, relying on computer vision on ordinary phones rather than depth hardware.
- [Lenovo ThinkReality A3](https://news.lenovo.com/pressroom/press-releases/thinkreality-a3-most-versatile-smart-glasses-ever-designed-for-the-enterprise/) - Lenovo's January 2021 enterprise AR glasses, in PC and Industrial editions.

## Open hardware

- [Project North Star](https://github.com/leapmotion/ProjectNorthStar) - Leap Motion's open AR headset design from 2018, over 100° field of view and 3D printable, still the reference point for anyone building their own. Its licence changed between announcement and release: Leap Motion's 2018 launch described an Apache-2.0 release, but the repository's LICENSE file is GPL-3.0, and the file is what applies.
- [Brilliant Labs Frame](https://github.com/brilliantlabsAR/frame-codebase) - The published codebase for Frame, the company's 2024 glasses, from a Hong Kong maker that has consistently opened its hardware and firmware.
- [Monocle](https://github.com/brilliantlabsAR/monocle-micropython) - MicroPython for the clip-on display that preceded Frame, and the easiest way into hackable AR hardware.

## SDKs and frameworks

- [ARCore SDK for Android](https://github.com/google-ar/arcore-android-sdk) - Google's SDK, actively developed, and the practical baseline for phone AR outside Apple's platforms.
- [Android XR](https://blog.google/products/android/android-xr/) - Google's XR platform, announced in December 2024 with Samsung, naming XREAL and Sony among its device partners.
- [Huawei AR Engine](https://developer.huawei.com/consumer/en/hms/huawei-arengine/) - Huawei's AR SDK for HarmonyOS and Android: motion, environment, body and face tracking.
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

The editions and what each document covers are pinned in [standards.md](standards.md).

- [OGC ARML 2.0](https://www.ogc.org/standards/arml/) - The Open Geospatial Consortium's Augmented Reality Markup Language, approved in 2015, which describes virtual objects in a scene and anchors them to the real world.
- [WebXR Augmented Reality Module](https://www.w3.org/TR/webxr-ar-module-1/) - The W3C specification extending the WebXR Device API to AR hardware.
- [OpenXR Spatial Entities Extensions](https://www.khronos.org/blog/openxr-spatial-entities-extensions-released-for-developer-feedback) - Khronos's first open standard for spatial computing: plane and marker detection, spatial anchors, and persistence across sessions, so an anchor placed today survives until tomorrow on hardware from more than one vendor.
- [XR Accessibility User Requirements](https://www.w3.org/TR/xaur/) - The W3C note on what people with disabilities need from immersive environments. It is a Working Group Note rather than a Recommendation, and it is still the best starting point.
- [ISO/IEC 18039:2019](https://webstore.iec.ch/en/publication/64756) - The mixed and augmented reality reference model: concepts, terms and a generalised system architecture.
- [ISO/IEC 18040:2019](https://webstore.iec.ch/en/publication/65241) - Representing live actors and other live entities inside a mixed or augmented reality scene.
- [IEEE 2048.101-2023](https://standards.ieee.org/ieee/2048.101/10390) - Augmented reality on mobile devices: requirements for the software framework and its integration.
- [ETSI GR ARF 001](https://www.etsi.org/deliver/etsi_gr/ARF/001_099/001/01.01.01_60/gr_arf001v010101p.pdf) - ETSI's April 2019 survey of the AR standards landscape.
- [OGC GeoPose](https://www.ogc.org/standards/geopose/) - The 2023 OGC standard for exchanging the position and orientation of real or virtual objects in earth-anchored frames.
- [WebXR Hit Test Module](https://immersive-web.github.io/hit-test/) - Ray casts against real-world geometry, so content can be placed on detected floors and walls.
- [WebXR Anchors Module](https://immersive-web.github.io/anchors/) - Poses the XR system keeps updated as its understanding of the room changes, so placed content does not drift.
- [Khronos OpenXR Registry](https://registry.khronos.org/OpenXR/) - The OpenXR specification itself, with headers and conformance material.
- [glTF 2.0](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html) - Khronos's runtime 3D asset format, the one most AR content pipelines move geometry through.
- [Alliance for OpenUSD](https://aousd.org/) - The Linux Foundation body standardising OpenUSD, the scene format behind Apple's USDZ.
- [MPEG-I](https://www.mpeg.org/standards/MPEG-I/) - ISO/IEC 23090, the family of coded immersive media standards: omnidirectional video, immersive audio, point clouds and scene description.
- [W3C Immersive Web Working Group](https://www.w3.org/groups/wg/immersive-web/charters/active) - The charter of the group that writes the WebXR specifications.
- [Metaverse Standards Forum](https://metaverse-standards.org/) - A coordination forum launched in June 2022; it aligns requirements across standards bodies rather than publishing standards itself.
- [Open AR Cloud](https://openarcloud.org/about/) - The organisation pushing for open, interoperable spatial computing data and standards, including GeoPose and a spatial content discovery protocol, against a default future in which each vendor owns its own map of your city.

## Where it is actually used

- [Augmented reality in oncological surgery](https://pmc.ncbi.nlm.nih.gov/articles/PMC10702732/) - A systematic review that is worth reading for its numbers rather than its enthusiasm: registration error under 3 mm in orthopaedic work, and from under 1 mm to 2 cm in maxillofacial work depending on method. It concludes AR is viable when paired with external navigation, and that more pre-clinical testing is needed first.
- [XR technology trends in surgery](https://pmc.ncbi.nlm.nih.gov/articles/PMC11763273/) - The companion review, useful for the division of labour it describes: AR and mixed reality for guidance during an operation, VR for planning and training before it.
- [HoloAnatomy](https://case.edu/holoanatomy/) - Case Western Reserve's mixed-reality anatomy teaching, the first third-party HoloLens application, now licensed to institutions beyond its own. Its claim, that students learn up to twice as fast as with traditional dissection, is the strongest education result the field has.
- [Google Maps Live View](https://techcrunch.com/2020/10/01/google-maps-gets-improved-live-view-ar-directions/) - Camera and GPS combined to paint directions onto the street, and the most-used consumer AR feature that nobody calls AR.
- [AR in heritage museum exhibits](https://hrmars.com/papers_submitted/23447/exploring-augmented-reality-integration-for-enhancing-heritage-museum-exhibits-a-focus-on-innovative-display-design.pdf) - An open-access 2024 study of how AR changes exhibit design and visitor engagement, for the cultural-heritage side of the subject.

### Industry

- [Google Glass takes flight at Boeing](https://www.cio.com/article/238599/google-glass-takes-flight-at-boeing.html) - CIO's 2016 report on Boeing's wire-harness pilot with Glass Enterprise and Upskill's Skylight: assembly time down 25% and errors roughly halved, twenty-four years after Caudell and Mizell proposed the same job.
- [Lockheed Martin embraces AR on the shop floor](https://www.eetimes.com/lockheed-martin-embraces-ar-on-the-shop-floor/) - EE Times' 2019 report on HoloLens work instructions for NASA's Orion spacecraft, with Lockheed reporting a 95% cut in the time to interpret instructions and 85% in training time.
- [AR in manufacturing and Industry 4.0](https://arxiv.org/abs/2112.11190) - Ziaee and Hamedi's survey of AR's industrial track record and open problems.

### Automotive

- [Panasonic AR head-up display](https://na.panasonic.com/news/panasonic-automotive-brings-expansive-artificial-intelligence-enhanced-situational-awareness-to-the-driver-experience-with-augmented-reality-head-up-display) - Panasonic's January 2021 announcement of an AR-HUD with 3D overlays for hazards and route guidance, using Envisics holographic optics and Phiar navigation.
- [WayRay](https://wayray.com/technology/) - Swiss maker of holographic AR windshield displays, which place the image ahead of the car using holographic optical elements instead of a bulky projector housing.
- [Hyundai Mobis holographic windshield](https://www.mobis.com/en/aboutus/press.do?category=press&idx=6003) - Hyundai Mobis's January 2025 announcement with ZEISS of a film that turns the whole windshield into a display, targeted at mass production in 2027.
- [Automotive AR head-up displays](https://pmc.ncbi.nlm.nih.gov/articles/PMC11052328/) - A 2024 review of AR-HUD optics: picture generation, the trade-offs between field of view, eyebox and image distance, and the case for full-windshield 3D displays.

## Human factors

- [Vergence–accommodation conflict](https://en.wikipedia.org/wiki/Vergence-accommodation_conflict) - Your eyes converge at the virtual distance and focus at the real one, and every fixed-focus headset creates the mismatch. It causes eye strain and fatigue, and it is the reason varifocal optics keep being attempted.
- [Registration errors in augmented reality systems](https://www.cs.unc.edu/techreports/95-016.pdf) - Richard Holloway's 1995 UNC dissertation, still the foundational measurement of why the image does not sit still: system delay, optical distortion and tracker error, with delay dominating everything else at moderate head speeds.
- [Death by Pokémon GO](https://www.nber.org/system/files/working_papers/w24308/w24308.pdf) - An NBER working paper measuring crashes, injuries and deaths near locations where the game could be played while driving. It belongs in an AR list precisely because it is not about headsets: attention is the resource this medium spends.
- [Inattentional blindness with AR head-up displays](https://arxiv.org/abs/2505.00879) - A 2025 on-road study: as AR-HUD tasks get harder, drivers notice fewer real-world events in their central field of view.
- [Distraction potential of AR head-up displays](https://journals.sagepub.com/doi/10.1177/0018720819844845) - Kim and Gabbard's study in *Human Factors* of how AR-HUD graphics compete for a driver's attention (paywalled).
- [XR Access](https://xraccess.org/about/) - The Cornell Tech consortium founded in 2019 to build shared accessibility knowledge, tools and code for XR.

## Platforms that closed

AR has buried more products than it ships, and the dates matter for anyone deciding what to build on.

- [Google Tango](https://en.wikipedia.org/wiki/Tango_(platform)) - Depth-sensing phone AR from 2014, ended in March 2018 in favour of ARCore, which is the moment the field decided special hardware in the phone was not the way.
- [HoloLens 2 discontinuation](https://techcrunch.com/2024/10/01/microsoft-hololens-2-discontinued-with-no-successor-in-site/) - Confirmed in October 2024 with no successor, updates promised to the end of 2027. The most capable AR headset ever sold has no replacement from its maker.
- [Meta Spark](https://spark.meta.com/blog/meta-spark-announcement/) - Meta's AR creation platform for Instagram and Facebook effects, shut to third-party creators on 14 January 2025, taking a large body of creator work with it.
- [Glass Enterprise Edition end of sale](https://support.google.com/glass-enterprise/customer/answer/13417888?hl=en) - Google's notice: sales stopped on 15 March 2023 and support on 15 September 2023, with no further software updates.
- [Magic Leap 1 end of life](https://www.magicleap.care/hc/en-us/articles/18878883445645-Magic-Leap-1-End-of-Life) - Magic Leap's notice that the first headset's cloud services and core functions would stop after 31 December 2024, as [reported by TechCrunch](https://techcrunch.com/2023/09/01/magic-leaps-original-headset-will-stop-working-at-the-end-of-2024).
- [Daqri](https://en.wikipedia.org/wiki/Daqri) - Maker of the industrial Smart Helmet (2014) and Smart Glasses (2017), which announced the shutdown of its hardware and cloud platforms in September 2019.
- [An AR glasses pioneer collapses](https://techcrunch.com/2019/01/10/an-ar-glasses-pioneer-collapses/) - How Osterhout Design Group, after raising $58m in 2016, never shipped its R-8 or R-9 glasses and sold its patents in January 2019.
- [Layar](https://en.wikipedia.org/wiki/Layar) - The Amsterdam AR browser of 2009, acquired in 2014 and wound down by 2016, and the clearest artefact of the era when AR was going to be a browser.
- [Metaio](https://en.wikipedia.org/wiki/Metaio) - The Munich SDK maker bought by Apple in May 2015, which stopped selling to everyone else immediately. Two years later the same technology surfaced as ARKit.
- [8th Wall](https://www.8thwall.com/blog/post/200330871818/agog-supports-8th-walls-next-chapter) - The exception, and the reason this section is not simply a graveyard. Niantic wound the commercial WebAR platform down, but rather than switching it off, nearly a decade of XR engine and WebAR tooling was released as open source in March 2026, with the company Agog backing its continuation.

## Communities and archives

- [AREA](https://thearea.org/about-us/) - The Augmented Reality for Enterprise Alliance, a non-profit that brings vendors, enterprise adopters and researchers together on interoperable industrial AR.
- [XR Association](https://xra.org/about/) - The industry association of headset and platform makers, founded by Google, HTC Vive, Microsoft, Meta and Sony Interactive Entertainment.
- [r/augmentedreality](https://www.reddit.com/r/augmentedreality/) - The main AR discussion subreddit.
- [VR/AR Association](https://www.thevrara.com/) - A global member network with city chapters, connecting XR businesses, researchers and professionals.

## In fiction

Fiction reached augmented reality first and got as much wrong as right. Each entry says which.

- [Star Wars](https://en.wikipedia.org/wiki/Holography_in_fiction) - Princess Leia's 1977 message, a figure standing in empty air and visible from any side, is the image most people mean by "hologram". Real holograms need a surface or plate to form on; stage "holograms" are Pepper's ghost (see History), and depth without glasses is the subject of [awesome-stereoscopy](https://github.com/danielcamposramos/awesome-stereoscopy) and [awesome-holography](https://github.com/bchao1/awesome-holography).
- [The Terminator](https://www.pagetable.com/?p=64) - The T-800's 1984 point-of-view display overlays text and targeting on the scene, a head-up display in all but name (see the F-35 helmet above). Its scrolling "code" is real Apple II 6502 assembly taken from *Nibble* magazine.
- [Back to the Future Part II](https://en.wikipedia.org/wiki/Back_to_the_Future_Part_II) - The 1989 film's "Jaws 19" shark lunges out of a cinema front in its imagined 2015. It was ILM computer imagery added in post-production, and the joke leans on the real stereoscopic [Jaws 3-D](https://en.wikipedia.org/wiki/Jaws_3-D). Phones put creatures in the street today (Pokémon Go, above), but only on a screen.
- [Minority Report](https://www.technologyreview.com/2011/04/22/195179/the-struggle-to-spread-the-minority-report-interface/) - The 2002 film's gestural interface "wasn't a special-effects fantasy", in MIT Technology Review's words: it was g-speak, a working system by MIT Media Lab researcher John Underkoffler, the film's science adviser, later built out at Oblong Industries. His own account is in his [TED profile](https://www.ted.com/speakers/john_underkoffler).
- [Den-noh Coil](https://en.wikipedia.org/wiki/Den-noh_Coil) - NHK's 2007 anime of children wearing AR glasses in a city where network layers are superimposed on the real world. Shared, persistent layers are exactly what geospatial anchoring (GeoPose, Open AR Cloud, above) is still trying to make real.
- [Iron Man](https://en.wikipedia.org/wiki/Iron_Man_%282008_film%29) - The 2008 film's helmet display has a working counterpart in fighter helmets (the F-35's above). The workshop Stark sculpts in mid-air does not: without a surface or medium, there is nothing for the light to form on.

## Related lists

- [awesome-webxr](https://github.com/msub2/awesome-webxr) - The browser side: WebXR engines, frameworks and communities, which this list leaves to it.
- [awesome-vr](https://github.com/danielcamposramos/awesome-vr) - Virtual reality: headsets, open runtimes, standards and the platforms that were switched off.
- [awesome-stereoscopy](https://github.com/danielcamposramos/awesome-stereoscopy) - The stereo medium itself, from Wheatstone in 1838 to spatial video: formats, packings, signalling and 3D cinema.
- [Awesome-ARKit](https://github.com/olucurious/Awesome-ARKit) - A large iOS-specific collection, for Apple platform work in particular.
- [awesome-mixed-reality](https://github.com/saurabhchalke/awesome-mixed-reality) - Mixed reality development resources spanning both sides of the passthrough line.
- [awesome-visionOS](https://github.com/tomkrikorian/awesome-visionOS) - Apple's platform in depth, including its passthrough approach.
- [awesome-lidar](https://github.com/szenergy/awesome-lidar) - Lidar sensors and datasets, for the depth-sensing hardware behind much of the tracking above.
- [awesome-computer-vision](https://github.com/jbhuang0604/awesome-computer-vision) - The research field underneath the SLAM and tracking section.
- [awesome-linux-hdr](https://github.com/danielcamposramos/awesome-linux-hdr) - HDR and deep colour on Linux, from specification to photons: the display chain behind any screen, headset panels included.
- [awesome-WebAR](https://github.com/tobiasbueschel/awesome-WebAR) - Browser-based AR projects and libraries, the AR-specific counterpart to awesome-webxr.
- [Awesome-ARCore](https://github.com/olucurious/Awesome-ARCore) - Projects and resources for Google's ARCore, the Android counterpart of Awesome-ARKit; dormant since 2021.
- [awesome-slam](https://github.com/kanster/awesome-slam) - SLAM tutorials, projects and communities behind the tracking section; dormant since 2020.
- [awesome-point-cloud-processing](https://github.com/mmolero/awesome-point-cloud-processing) - Point cloud libraries and software, the data that lidar and depth sensors hand to AR tracking.
- [awesome-a11y](https://github.com/brunopulis/awesome-a11y) - Accessibility resources in general, for the principles behind this list's accessibility entries.

## Events

- [Augmented World Expo](https://www.awexr.com/about_awe) - Founded in 2010 by Ori Inbar, the long-running industry gathering for AR and VR, and the most reliable annual snapshot of what is actually shipping.

## Known gaps

Stated openly, because a list that hides its blind spots is worse than one that names them. These are the places this list is weakest, and the contributions most wanted:

**Chinese, Japanese and Korean AR** now has its own section, but it is built from English-language official pages. Makers publishing mainly in their own languages are still missing, and so is Shadow Creator, whose site refused an automated check. Contributions in any language are wanted; cite what you can.

**Industrial deployments** have a first measured account (Boeing's 2016 wire-harness pilot) and a survey, but still too few independent results on what current factory and field-service AR achieves.

**Communities** are represented by their associations. The active discussion forums sit mostly on platforms whose pages could not be verified in the ordinary way, and an unverified link is worse than an admitted gap.

**Automotive AR** has its own section now, from suppliers and a review. Carmakers' own documentation of production AR-HUDs could not be verified yet.

**Two former discrepancies are resolved** from primary sources: Project North Star was announced as Apache-2.0 but ships GPL-3.0, and ARCore appeared as a preview in August 2017 and as 1.0 in February 2018. Both entries now say so.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.
