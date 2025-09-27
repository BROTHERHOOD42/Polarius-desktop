# Polarius Desktop

## Getting Started

Polarius users can get started by accessing https://brotherhood42.github.io.

### The recommended development settings are as follows.

1. Dendrite Setting [(guide)](https://element-hq.github.io/dendrite/)
2. Clone Polarius-web and Polarius-desktop
3. Build Polarius-web, copy to Polarius-desktop/webapp
4. Start Polarius-desktop, go to localhost:port
  
For detailed commands, refer to the [Beginner Development Guide.](https://github.com/BROTHERHOOD42/Polarius-web/blob/main/docs/Beginner_Development_Setting_Guide.md)

## Workflow
   
When a release is created on polarius-web, a corresponding release is automatically generated for polarius-desktop, and it is deployed to https://brotherhood42.github.io

### Details
   
1. Triggering a Web Release  
   When a release is published on the polarius-web repository with a tag that starts with v, it automatically triggers a build process.  
   As part of this process, the webapp folder in the polarius-web repository is updated with the latest build.  
  
2. Desktop Release Automation  
   Once the webapp folder is updated, a signal is sent to the polarius-desktop repository.  
   This triggers a build process for all supported platforms, using the updated webapp and the generated webapp.asar:  
   + Windows (x64, ARM64)  
   + macOS  
   + Linux (amd64, ARM64)
     
   After the builds complete, a new release is automatically created in the polarius-desktop repository.
