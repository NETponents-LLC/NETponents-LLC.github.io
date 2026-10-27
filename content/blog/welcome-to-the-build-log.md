+++
title = 'Welcome to the Build Log'
date = 2026-10-27T00:00:00-04:00
draft = false
tags = ['build-log', 'kicad', 'embedded']
summary = 'What this blog covers and how a typical edge-to-cloud project is structured.'
+++

This blog collects the engineering behind our client work: design decisions, mistakes, and measurements.

## A typical edge-to-cloud pipeline

A device samples a sensor, packages the reading, and posts it to a service that validates and stores it:

```go
type Reading struct {
	DeviceID string    `json:"device_id"`
	Value    float64   `json:"value"`
	At       time.Time `json:"at"`
}
```

Expect posts on schematic and layout choices in KiCad, firmware notes, and cloud ingestion patterns.
