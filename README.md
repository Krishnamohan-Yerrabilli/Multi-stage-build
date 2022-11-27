# Multi-stage-builds

Understanding Multistage Docker Build through some examples

Multistage builds use a Dockerfile with multiple FROM statements. Each of these FROM statements is a new compilation 
stage that can COPY artifacts from previous stages. By going and copying the build artifact from the build stage, 
you eliminate all intermediate steps like downloading code, installing dependencies, and testing.

# Docker geoloc regular image Size is > 90mb

![docker-geoloc-image-size](https://user-images.githubusercontent.com/58173938/204132827-cfb789b9-12da-4ae3-a66b-b89520e70c3a.png)

