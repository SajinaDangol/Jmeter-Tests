# JMeter API Server Test

A lightweight Apache JMeter test suite for smoke-testing the API Server's Posts endpoints.

## Overview

This test suite validates the basic functionality of the Posts API by:

- Fetching the list of posts
- Extracting the first post ID from the response
- Validating the HTTP response code
- Validating the first post ID and title
- Fetching post details using the extracted post ID
- Displaying test results and JMeter variables for debugging

## Requirements

- [Apache JMeter](https://jmeter.apache.org/) **5.6.3**
- Internet access to reach the configured API endpoint

## Test Configuration

| Setting | Value |
|---|---|
| Test Plan | APIServer Performance Testing |
| Thread Group | Smoke Tests |
| Threads / Users | 1 |
| Ramp-up | 1 second |
| Loop Count | 1 |
| HTTP Protocol | HTTPS |
| HTTP Implementation | HttpClient4 |

> **Note:** Despite the test plan being named "Performance Testing", this suite currently runs only a single user for a single iteration and is primarily intended for smoke/API validation.

## Base URL

The default `BASE_URL` is:

```text
my-json-server.typicode.com
