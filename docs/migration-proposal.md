# Migration proposal

## The application

The application is a copy of Medium.com and the features include Authentication,
user management, persistence, and blogging.

![App](./img/app.png)

## The current architecture

![Current architecture](./img/01_architecture_current.png)

We only have 1 frontend application, and 100% traffic should still go to the backend.v1.

We can try with [Canary Release](https://martinfowler.com/bliki/CanaryRelease.html)

> Canary release is a technique to reduce the risk of introducing a new software version in production by slowly rolling out the change to a small subset of users before rolling it out to the entire infrastructure and making it available to everybody.

![Initial Canary](./img/02_architecture_canary.png)

![Later Canary](./img/03_architecture_canary.png)

![Final](./img/04_architecture_final_switch.png)

## Plan of action

![Under construction](https://cdn.pixabay.com/photo/2017/06/16/07/26/under-construction-2408062_1280.png)
