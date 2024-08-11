# 2. prefer minikube with docker driver

Date: 2024-08-11

## Status

Accepted

## Context

Minikube requires specific configuration for compatibility with arm macos

## Decision

Utilize minikube with docker driver, and integrate local systel dns resolver with kubernetes cluster

## Consequences

This should allow consistent function across development environments
