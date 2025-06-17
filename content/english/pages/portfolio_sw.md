---
layout: portfolio

# Banner
banner:
  title: "Soren Leanza Rademacher"
  content: >
    Software Portfolio
  image: "/images/banner.png"

# Features
features:
  - title: "Airhart"
    video: /images/swe/software_inflight.mp4
    content: >
      At Airhart, our avionics stack is fully vertically integrated. Everything from
      the sensor suite to the servos that actuate control surfaces is built in-house.
      I lead the software team here and wrote our vehicle ‘OS’, which runs GNC control
      code and provides an interface between our UI and hardware. In February of 2025,
      after 3 years of development, we flew our prototype aircraft from Los Angeles
      to Raleigh, NC. Aside from takeoff and landing, the entire flight was under
      the control of my Rust-based software stack.


      This video was recorded in the winter of ‘23 before the development of our UI and
      demonstrates a simple Fly-by-Wire control law where the digital
      sick (right hand) is interpreted as an absolute angle to hold relative to
      the horizon. Therefore, releasing the stick levels the aircraft.

  - title: "Scope"
    video: "/images/swe/scope.mp4"
    content: >
      In 2018, I was debugging an aspect of a game I was building and needed
      to see a real-time plot of a parameter. Copy-pasting chunks of data to Excel
      or arcane matplotlib scripts were the only options available at the time. The
      activation energy to use these tools was too high, so generally my strategy in
      similar situations as to simply to print these numbers to the terminal and do my
      best to interpret them that way.  I was struck by a sudden frustration about the
      idea of struggling with this for the rest of my life. If I had a visualization
      tool designed to ingest, display, and explore  data from stdin in real time, I
      could instantly turn any print debugging session into an intuitive explorable
      plot. I was curious about Rust at the time, so I built scope as a way to learn
      Rust. I implemented the tool using chunked vertex buffers in OpenGL to maintain
      high framerates, even when handling large data streams. As a learning project,
      it's an unpolished mess, but I still find myself reaching for it regularly at
      work. 

  - title: "Slice Viewer"
    video: "/images/swe/qd.mp4"
    content: >
      Carbon’s 3D printers work by constructing parts one slice at a time. When I
      created a tool to add textures to the outer surfaces of printed parts, the
      complexity of these parts increased, and our existing slice viewer became a
      bottleneck, taking up to a second to tessellate and render each slice. To solve
      this, I built Quickdraw using Rust and Bevy. The new viewer tessellated slices
      in parallel and cached the tesselated geometry on the GPU, enabling smooth,
      real-time scrolling through slices at 60 FPS. On the side, you will see a
      "parallel loading bar" in purple. Since slices are dispatched to all available
      cores to be tessellated, the part loads in a nonlinear fashion. The user can
      still view the part as soon as the section they care about loads.
      
  - title: "Games and Simulation"
    video: "/images/swe/nc.mp4"
    content: >
      I've always loved building physics-based games and models. This video is
      one of many such abandoned projects. Here, I modeled 800 spacecraft (rectangles)
      orbiting a central gravitational body. The player is the green-highlighted
      craft, and visibility is restricted to ships for which it has line of sight.
      The simulation is run on an authoritative Rust-based server using a custom ECS.
      Updates are streamed to an HTML canvas using websockets.

  - title: "3D Printing Research Tool"
    video: "/images/swe/webui-log-filter.mp4"
    content: >
      I developed a web-based GUI for prototype 3D printers to improve experiment
      reproducibility and documentation. I observed that our research engineers
      often lost data or became confused about experimental outcomes because
      key details—like firmware versions, model variations, or tunable process
      parameters—were forgotten or incorrectly assumed to be irrelevant. I got the
      go-ahead from my boss to spend some work hours fixing this problem. I built a
      Git-backed system that tracks all facets of the print process. The interface
      captures firmware, 3D models, parameter settings, and outcomes, and makes them
      searchable, ensuring any experiment can be precisely reviewed or repeated. The
      server itself is written in Rust and uses Diesel to manage state in a Postgres
      database. The front end is handwritten HTML/CSS/JavaScript.


      It's hard to demo this software without revealing proprietary information,
      so I’ve only included a short clip of the print log filtering system.
      Here, I’m filtering down prints that lasted more than 1000 seconds
      and were started by me (SLR). This is just one aspect of the software.
      There are also pages to view live video and telemetry as a print runs,
      pages to manage models and script files, a built in script editor which
      enforces that changes are documented and versioned, printer settings, user
      management, and more.
---
