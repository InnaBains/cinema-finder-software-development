# Datacom Software Development Job Simulation – Cinema Finder

A software development project completed as part of the **Datacom Software Development Job Simulation on Forage** (October 2026).

## Project overview

The simulation involved reviewing and improving a Cinema Finder web application. I worked through a software review task and a practical debugging task using the existing JavaScript/React codebase.

## Work completed

### 1. Software review
- Tested the Cinema Finder application and reviewed customer feedback.
- Identified and prioritised existing bugs and potential new features.
- Considered issues including cinema map selection, map boundaries, interface behaviour, filtering, cinema details and booking functionality.
- Produced a structured review with suggested priorities for future development.

### 2. Root-cause analysis and bug fix
I investigated the cinema map selection issue using the browser/developer tools and the application source code.

The cinema list was correctly sending the cinema's latitude and longitude to the map. The issue was in the MapLibre map component, where the coordinates were passed to `flyTo` in the wrong order.

**Root cause:**
- The application supplied `[latitude, longitude]`.
- MapLibre expects coordinates as `[longitude, latitude]`.

**Fix applied:**
```javascript
map.flyTo({
  center: [lng, lat],
  zoom: 14,
})
```

I then tested multiple cinema selections and confirmed that the map moved to the correct locations.

## Skills demonstrated

- Software development
- JavaScript
- React
- Developer tools
- Root-cause analysis
- Debugging
- Software evaluation
- Critical thinking
- Written communication

## Project context

This repository contains the working project used for the practical debugging task. The simulation was completed and submitted through Forage, with a **Certificate of Completion issued in October 2026**.

**Simulation:** Datacom – Software Development Job Simulation  
**Platform:** Forage  
**Completed:** October 2026

> This repository is a practical learning/project artefact from the simulation and is presented as part of my software development portfolio.
