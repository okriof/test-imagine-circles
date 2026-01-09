FROM okriof/imagel:build-2 AS buildim

COPY hellosrc.cpp /project/src/

RUN g++ -Wall -o /project/build/helloBin -O2 /project/src/hellosrc.cpp



# generate runtime image
FROM ubuntu:latest
COPY --from=buildim /project/build/ /bin/
CMD ["/bin/helloBin"]

