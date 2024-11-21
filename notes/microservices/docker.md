## Docker

## Containers

### Stateless

Instead of storing persistent data within the container, data should be stored outside, either within cloud storage or on external disks.

Designing containers to be stateless ensures that they can be destroyed or rebuilt as needed without worrying about losing crucial information.

### Immutable:

The container should not be modified while it exists. If you need to update content within the container, destroy it, make your changes, build a new image, and redeploy it.

This ensures that containers remain identical when deployed across multiple environments. It also makes rolling back to previous images easier if problems are discovered within more recent versions.

### Build Cache:

Optimize your build times.

Docker images are powered by Dockerfiles, which describe the instructions for building the container. When building an image, Docker constructs it in layers. Docker can reuse layers from a previous build to speed up build times. Using the command --cache-from in your Dockerfile will tell Docker to use the specified image as a source to cache build commands from, helping you speed up future build times.

To get the most out of the build cache, put build steps that change often at the bottom of the Dockerfile. Because Docker builds images in layers, it will use its build cache for earlier build steps that change less frequently, helping to reduce build times more reliably.


### Reduce Image Size:
Reduce download and upload times, enabling you to operate more efficiently.

Smaller images tend to be less complex and rely on fewer dependencies to run. Plus, smaller images tend to have less bloat, reducing the potential attack surface for malicious actors.

Rely on the following techniques to make your container images as small as possible:

Use multi-stage builds to create a cleaner separation between the building of the image  and the final output. 
Multi-stage builds also make Dockerfiles easier to maintain.
Use the .dockerignore file to exclude files not relevant to the build, ensuring your image only contains the files it needs to run.
Remove unnecessary tools from the containers. For example, you don’t need a text editor in a database image, so don’t include it. Examine what you want your container to accomplish and only have the necessary tools to achieve that task

### Security

Dont use priviligies container as "root"
Integrate automated vulnerability scanning to reduce the likelihood of attack. Regular scans will help inform you of potential vulnerabilities, allowing you to plug these security holes as they arise.


### Tag Images:
Robust version control and naming conventions


### Build Logging and Monitoring Standards 
 Docker provides a standardized way to record logs using the “docker logs” command. Use this native logging mechanism instead of external ones to get the best insight into individual Docker container performance
