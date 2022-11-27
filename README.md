# Multi-stage-builds

Understanding Multistage Docker Build through some examples

Multistage builds use a Dockerfile with multiple FROM statements. Each of these FROM statements is a new compilation 
stage that can COPY artifacts from previous stages. By going and copying the build artifact from the build stage, 
you eliminate all intermediate steps like downloading code, installing dependencies, and testing.
