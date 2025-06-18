---
layout: portfolio

# Banner
banner:
  title: "Hardware Portfolio"
  content: >
    8+ years of experience designing, building, and testing prototype-level mechanatronic systems.
  resume_title: Hardware Resume
  resume_link: /Soren-Rademacher-HWE.pdf
  image: "/images/banner.png"

# Features
features:
  - title: "Force Feedback Yoke"
    image: "/images/hwe/motor.jpg"
    content: >
      Building a force feedback yoke poses an interesting challenge. The torque
      required to provide good feedback is not insignificant. Usually, adding a
      gearbox to the system is an easy fix; however, increasing the gear ratio is
      a double-edged sword because the gearbox must be back-driven by the pilot.
      The more leverage you provide to the motor, the less leverage the pilot has
      to back-drive it. Our goal is to allow smooth, precise micro-adjustments by
      the pilot, but any stiction in the motor and gearbox assembly is amplified
      by the gearbox. I evaluated several gear train options and then carefully
      designed parts that could be machined to high precision in order to minimize
      any misalignment that might cause stiction.


      The design is proprietary, so I’ve
      included a motor housing I designed and built for another prototype.


  - title: "FLIP"
    video: "/images/hwe/FLIP.mp4"
    content: >
        FLIP was my first project as a full-time engineer in 2018. My goal was to build
        a 3D printer capable of producing parts at record-breaking speeds, measured by
        volumetric flow rate. This prototype was intentionally scaled down to minimize
        resin usage and reduce R&D costs. It could produce parts at 4 L/hr but could
        easily be scaled to exceed 24 L/hr. As far as I’m aware, the latter figure would
        still be a world record in 2024, though with the important caveat that this
        technology cannot print extreme overhangs. I acted as the RE for nearly all
        aspects of this project: I designed all the mechanical parts, machined them,
        programmed the processes, and ran experiments to test and refine the system.
        [Patent here.](https://patents.google.com/patent/US20210308943A1).


  - title: "Dental Crown Printer"
    image: "/images/hwe/dental.jpg"
    content: >
      The dental crown printer was a process I developed by adapting the FLIP process
      for a specific application. Dental prosthetics can be produced without extreme
      overhangs and require the use of highly viscous, shear-thinning resins, which
      made FLIP an ideal starting point. I scaled down the system and tweaked the
      process so I could minimize the part count, trading speed for compactness and
      simplicity. I also improved the machine’s precision, as the high opacity of the
      resin required parts to be produced with layer heights of approximately 15 µm.
      [Patent here.](https://patents.google.com/patent/WO2020256825A1)

---
