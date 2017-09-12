## Some key for the docker file

## FROM

Which base image to use to build your image

## LABEL

Provide description of the image

[Schema](http://label-schema.org/)

## RUN

The RUN command is where we interact with our image to install software and run scripts, commands, and other tasks. 

[More help](https://www.packtpub.com/mapt/book/all_books/9781787280243/2/ch02lvl1sec15/introducing-the-dockerfile)

## COPY

Copy is use like any copy command of CLI

## ADD

```ADD files/html.tar.gz /usr/share/nginx/```

ADD automatically uploads, uncompresses, and puts the resulting folders and files at the path we tell it to.

## EXPOSE

Let docker know which port to expose after the command is executed.

