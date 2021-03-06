# Closest facility

Find a route to the closest facility from a location.

![](screenshot.png)

## Use case

Quickly and accurately determining the most efficient route between a location and a facility is a frequently encountered task. For example, a paramedic may need to know which hospital in the vicinity offers the possibility of getting an ambulance patient critical medical care in the shortest amount of time. Solving for the closest hospital to the ambulance's location using an impedance of "travel time" would provide this information.

## How to use the sample

Click near any of the hospitals and a route will be displayed from that clicked location to the nearest hospital.

## How it works

1. Create a `ClosestFacilityTask` using an Url from an online service.
2. Get a `ClosestFacilityParameters` from this task, using `createDefaultParameters`.
3. Add a list of facilities to the task parameters, using `ClosestFacilityParameters.setFacilities`.
4. Add an incident to the parameters, using `ClosestFacilityParameters.setIncidents(`.
5. Get the `ClosestFacilityResult` from solving the task with parameters: , `ClosestFacilityTask.solveClosestFacility`.
6. Get the ranked list of the indices of the closest facilities to the incident, `ClosestFacilityResult.rankedFacilities`.
7. Get the index of the closest facility (e.g. the first index in the ranked list).
8. Find the closest facility route, `ClosestFacilityResult.route`.
9. Display the route on the `MapView`:
 - create a `Graphic` from the route geometry, `route.routeGeometry`.
 - add graphic to `GraphicsOverlay` which is attached to the mapview.

## Relevant API

* ClosestFacilityParameters
* ClosestFacilityResult
* ClosestFacilityRoute
* ClosestFacilityTask
* Facility
* Graphic
* GraphicsOverlay
* Incident
* MapView

## Tags

incident, network analysis, route, search
