# ENV variables is used to set the environment variables.
# Environment variables can be changed when starting the container. 


FROM alpine
ENV TEST='hello'
CMD ["set"]

# To change the env variable

docker container run -it -e "TEST=DONT OPEN DANGER AHEAD" test2 /bin/sh