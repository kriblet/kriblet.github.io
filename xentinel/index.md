---
title: Xentinel
description: Xentinel API Documentation
layout: default
info:
    title: Xentinel
    description: Xentinel API Documentation
    favicon: /img/xentinel.png
    logo: /img/xentinel.png
---

# Overall
This is a GPS Tracking software light and powerful, made to support [xentinel.io](https://xentinel.io) platform

## Content

| Content | Description | 
|---|---|
| [General](#general) | General information about Xentinel Api |
| [Conventions](conventions) | Conventions to consider to properly use Xentinel api |
| [Login](login) | How to login into Xentinel api?  |
| [CRUD](crud) | How CRUD operations are made with Xentinel api |
| [Available Models](models) | Available generic CRUD operations with Models |
| [Special Endpoints](endpoints) | Available endpoints to manage history, events and more |
| [Embedded Map](map) | Comming soon |


## General

This api is powered by NodeJs Custom architecture, light and powerful, runs in cluster servers hosted by AWS.

Xentiel api provides 30 minutes sessions, which must refresh before 30 minutes doing any request to our api.

Sessions are domain restricted and client restricted.

