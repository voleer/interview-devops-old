# Voleer DevOps Challenge

## Preface

This challenge is meant to see how you would approach a problem and not to see
how well you deliver a solution that we think is right. You should not focus on
getting _the_ "right" answer.

For each challenge listed below, you can propose your approach, it's always a
bonus if you can execute your proposal. Some challenges are posted as open-ended
questions and you can answer them inline.

Only the #Instructions section must be followed, the #Challenges are entirely up to you.

The challenges are estimated to take from **1 - 3 days** depending on how familiar
you are with containerization technology, the research time is also accounted for in the
estimated duration.

## Instructions

1. Fork this repo.
2. Provide your answers to the forked repo.
3. Send us the completed repo once you are ready.
4. Wait for our response.

## Questions

### 1. What is even DevOps?

- What is your take on the definition of DevOps?

- What is the responsibility of a DevOps engineer?

- Why has DevOps gained prominence over the last few years?

### 2. Identify your environment

- What is your primary OS?

- What shell do you use on your daily job?

### 3. Weapons of choice?

- What scripting language are you comfortable with?

- Name some tools that you use and why do you use them for?

## Challenges

The following challenges are related to the repo. To provide your take on the
challenges, follow the steps:

1. Fork this repo.
2. Provide your answers to the forked repo.
3. Send us the completed repo once you are ready.

In this repo, you will find:

- [./src](./src):

  - Source code of the applications stack

- [./src/frontend](./src/frontend):

  - Source code for frontend UI application using React.js. You can read more about it in [./src/frontend/README.md](./src/frontend/README.md).
  - Locally, the application runs on http://localhost:4100

- [./src/backend.v1](./src/backend.v1):

  - Source code for legacy backend server code. This is written in Golang, and you can read more about it in [./src/backend.v1/README.md](./src/backend.v1/README.md).
  - Locally, the application runs on http://localhost:8080

- [./src/backend.v2](./src/backend.v2):

  - Source code for new backend server code that we are still developing. This is written in .NET Core, and you can read more about it in [./src/backend.v2/README.md](./src/backend.v2/README.md).
  - Locally, the application runs on http://localhost:5000

- [./docs](./docs):
  - Additional documentations.

### 1. Can we start both frontend and backend at the same time?

Currently, our developers have to go to the backend and frontend folders individually and start the applications.

The commands to start the applications are noted in their respective README.md, but it is still a hassle to do that every time. If only we have some convenient way to start both the frontend and backend together.

**Bonus:** What could be even better is a convenient way to switch between the old and new
version of backend. Right now to switch the backend API in the frontend, the developers have
to comment/uncomment the environment value under [./src/frontend/.env.development](./src/frontend/.env/development) and then restart the frontend server.

### 2. Can we Dockerize the applications?

We have heard good things about Docker and containerization technology, and think what if
we bring in to our applications stack. Can you help Dockerize the `frontend`, `backend.v1` and `backend.v2`?

**Bonus:** It's always good to save developers time with efficient process.

- Is there any optimization that we can do?

### 3. Have you heard of that Kubernetes?

[Kubernetes](https://kubernetes.io/) seems like a great tool to help us with deploying, scaling, and managing the containerized applications. How do we apply it to our stack?

**Bonus:** Infrastructure as code (IaC) recently grows in popularity.

- How is it related to Kubernetes?
- Would IaC help us; if it would; how do we apply it to our stack?

### 5. (Extra) Ship it.

It would be a super cool demo to our stakeholders if we can get the applications online and they can access it from their computer. It's okay if it's a just an IP address or some random domain name.

If you want to take up this challenge. Please send an email to us and we will provide you
with a limited access to a Kubernetes cluster that you can deploy the applications there. But if you have your own solution, go for it.

### 6. (Extra) How can we migrate from the old backend to the new backend?

Each backend uses different SQLite databases, but it's okay to just point the frontend
application to a different API without having to worry about the data. But how do we perform
the migration with minimal down time?

**Bonus 1:** If you're comfortable with SQL, maybe you can help migrate even the data.

**Bonus 2:** If we can fix the code such that both backend versions can communicate with
the same database with the same schema, then we will not have to migrate the data.
