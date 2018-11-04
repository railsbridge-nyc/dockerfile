# dockerfile

A Dockerfile we can use as a base for our Rails workshops.

(Still validating the idea).

## Updating the Dockerfile

* To update Ruby, update the base image
* To update Rails, update the `gem install -v *.*.* rails` invocation
* To force the image to rebuild / bust the docker cache for any other reason, increment the number in dockerfile-version
