# A React Portfolio Site

[![style: styled-components](https://img.shields.io/badge/style-%F0%9F%92%85%20styled--components-orange.svg?colorB=daa357&colorA=db748e)](https://github.com/styled-components/styled-components)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/xojs/xo)

## Summary

This project is a sample portfolio page setup with [React](https://reactjs.org/) & [React Router](https://github.com/ReactTraining/react-router).
It takes advantage of multiple styling libraries including [Styled Components](https://www.styled-components.com/) & [Grid Styled](http://jxnblk.com/grid-styled/).

[Prettier](https://github.com/prettier/prettier) was used for code styling throughout the project, and [XO](https://github.com/xojs/xo) was added in combination with [pre-commit](https://www.npmjs.com/package/pre-commit) to improve code quality through [eslinting](https://eslint.org/).

Continuous Integration is planned through [Circle CI](https://circleci.com/) & [Jest](https://facebook.github.io/jest/) Tests.

## Running Locally

```bash
npm install
npm start
```

## Using Docker

An additional Dockerfile has been added to the repo. If you wish to run the application via Docker:

```bash
# build docker image
docker build . # or you can run the command

# run docker container and portforward port 3000
docker run -ti -p 3000:3000 <docker-image-id>

# publish docker image to docker hub
docker push <docker-repo>
```

A handy makefile has been setup for ease of use as well

```bash
# this will default to 'build' command
make

# this will push the image to docker hub
make push

# this will both build and publish for expediency
make deploy
```

## Deployment:
The package.json deploy script is setup for gh-pages deployment. Plans are in place to allow auto publication of updates on merge to master via Circle CI.
Currently run the following to update the gh-pages branch:

```bash
npm run deploy
```

An 'aws-deploy' branch is also available if you wish to run a local build of the repo and upload it to AWS s3 for [static website hosting](https://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html).
