# Simple Webflux Project

**We use [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)** so stick with it.

Feel free to copy and alter anything I've coded here, the main purpose of this repository is to serve as a template and reference for something you're doing. Check our [changelog](CHANGELOG.md) file to find out what was implemented.

    If you're not sure on how to grab a copy of something you've seen here, try checking old commits to see how it was and how it is now, that should help you understand my disturbed way of thinking things out.

## Features so far

Here is a summarized feature list of what is already implemented or is part of out "road map". Please keep in mind that so far I'm not documenting anything, but I plan to do it in the future.

- [x] Github Actions
- [x] SonarCloud
- [x] Auto Changelog
- [x] Docker Release
- [x] Project Reactor
- [x] Webflux.fn
- [x] r2dbc with Postgres
- [x] Testcontainer
- [x] Actuator
- [x] Validator
- [x] Metrics
- [x] Tracing
- [x] BDD with Cucumber
- [x] Security with OAuth2 and JWT (at the moment using it from Keycloak)
- [x] Consul
- [ ] Remote Configuration
- [ ] Cache

Also we will introduce some other services to the stack to act as external services. With that we will also introduce:

- [ ] LoadBalancing
- [ ] Kubernetes
- [ ] Environment Deployment

## How to manage everything

### Keycloak

To export your current Banter realm, execute the following command:

```shell
docker exec -it infra-keycloak-1 /opt/keycloak/bin/kc.sh export \
--dir /tmp/export \
--realm Banter \
--users realm_file
```

Remember to lookup inside the exported realm from type: js to type: resource