# Multi-stage-builds

Understanding Multistage Docker Build through some examples

Multistage builds use a Dockerfile with multiple FROM statements. Each of these FROM statements is a new compilation 
stage that can COPY artifacts from previous stages. By going and copying the build artifact from the build stage, 
you eliminate all intermediate steps like downloading code, installing dependencies, and testing.

some key points:

Reduced Image Size: Multi-stage Dockerfiles can significantly reduce the size of the final Docker image by only copying the necessary files from each build stage to the final stage.

Clean Build Environment: Multi-stage Dockerfiles allow you to build your application in one stage and then copy the compiled artifacts to another stage that is used to create the final Docker image. This keeps the final image smaller and cleaner.

Better Security: Multi-stage Dockerfiles can also improve security by only copying the required files and not including any build-time dependencies, such as compilers and libraries, in the final image.

Multiple Build Stages: Multi-stage Dockerfiles can have multiple build stages, allowing you to perform different tasks in each stage and take advantage of the benefits of each stage.

Reuse of Build Artifacts: Multi-stage Dockerfiles can also reuse build artifacts from previous stages, reducing build time and allowing for faster builds.

Improved Build Process: Multi-stage Dockerfiles can improve the overall build process by making it more efficient, streamlined, and secure.

## Docker geoloc regular image size is around 98mb

![docker-geoloc-image-size](https://user-images.githubusercontent.com/58173938/204132827-cfb789b9-12da-4ae3-a66b-b89520e70c3a.png)

## Multi-Stage-Build

As we can see the new dockerimage is around 76mb

![d](https://user-images.githubusercontent.com/58173938/204134723-78c2e02e-f0c2-4755-8c1b-924294816a47.png)
