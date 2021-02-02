FROM busybox:latest

# The  argument "flag" is passed at build time using --build-arg
# The data is added to one of the image layers as an environment variable
# It's bad practice to add any sensitive data within a container image!
ARG flag
RUN echo $flag > /flag

# The entrypoint, unless changed, will cause the container to run:
# <ENTRYPOINT> <CMD>
# where <CMD> are passed as parameters to <ENTRYPOINT>
ENTRYPOINT  ["/bin/echo"]
CMD         ["try again"]