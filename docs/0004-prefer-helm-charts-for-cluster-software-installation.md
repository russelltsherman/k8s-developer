# 2. prefer helm charts for cluster software installation

Date: 2022-09-05

## Status

Accepted

## Context

It can be complex to install and manage an applications required resources using only individual kubernetes manifests
Helm charts provide a low entry bar for deploying complex applications.

## Decision

Whenever possible use helm charts for cluster software installations

## Consequences

Helm charts remove the guess work about application requirements
