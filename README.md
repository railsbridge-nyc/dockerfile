# dockerfile

A Dockerfile we can use as a base for our Rails workshops.

(Still validating the idea).

## Updating the Dockerfile

* To update Ruby, update the base image
* To update Rails, update the `gem install -v *.*.* rails` invocation
* To force the image to rebuild / bust the docker cache for any other reason, increment the number in dockerfile-version

The [image] will rebuild whenever we push to this GitHub repository.

[image]: https://hub.docker.com/r/railsbridgenyc/rails/

## Using the image

Open irb:

```shell
docker run --rm -it railsbridgenyc/rails irb
```

Generate a new Rails app:

```shell
docker run --rm -it -v ${PWD}:/workdir railsbridgenyc/rails rails new testo --database=postgresql
```

With docker-compose

TODO: add example
