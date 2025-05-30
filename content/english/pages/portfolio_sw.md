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
  - title: "scope"
    # image: "/images/hdr_software_inflight.jpg"
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


---
