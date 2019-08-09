# Voting App

## Purpose
This voting application should provide you some entry level exercises which allows you to learn how to build Docker images and create Docker Compose files.

## Exercise
Fix all TODOs and `...`'s and check if the whole voting application starts successfully using `docker-compose up`. Also ensure the vote webUI and repost webUI is available by accessing http://localhost:5000 and http://localhost:5001.

The only files which need to be touched are the following ones:

```bash
.
├── docker-compose.yml
└── src
    ├── result
    │   ├── Dockerfile (currently there is nothing to do inside this file)
    ├── vote
    │   ├── Dockerfile
    └── worker
        ├── Dockerfile (currently there is nothing to do inside this file)
```

## Solution
If you would like to see a possible solution please check the following files:

```bash
.
├── solution
│   ├── docker-compose.yml
│   ├── result
│   │   └── Dockerfile
│   ├── vote
│   │   └── Dockerfile
│   └── worker
│       └── Dockerfile
```

If you have some improvements to the solutions, please feel free to create a pull request.

## Credit
Application source code taken from https://github.com/dockersamples/example-voting-app.
