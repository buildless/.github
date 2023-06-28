<p align="center">
  <a href="https://less.build">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="./images/github-org-masthead-dark@4x.png">
      <source media="(prefers-color-scheme: light)" srcset="./images/github-org-masthead@4x.png">
      <img src="./images/github-org-masthead@4x.png" width="800" alt="Buildless for Gradle" />
    </picture>
    <br />
  </a>
</p>
<br />

> Remote Build Caching as a Service

[Buildless][6] is the world's first build cache CDN. It works as a drop-in remote build cache for tools like [Gradle][1], [Maven][2], [Bazel][3], [CCache][4], and others.


## About Buildless

Welcome! We're glad you're here 👋.

### How does it work?

Many modern build tools calculate hashes of build outputs, and are then able to *cache* those outputs. When a developer returns to that chunk of code, if it hasn't changed, they can fetch the output from a cache and re-use it.

Build caching isn't new. Techniques for build caching have been around for awhile. But there has never been an easy way to equip your cache for success: with Buildless, you don't need to run it yourself. Your builds get faster automatically as we ship new features.

### Is it fast?

**Yes, very.** Buildless is powered by [Cloudflare](https://cloudflare.com)'s top-tier [global network and CDN][5], and a stack of technologies which put performance first:

- [Dragonfly](https://www.dragonflydb.io/), a high-performance in-memory database which speaks Redis protocol
- [Netty](https://netty.io/), the best-of-the-best in networked application performance
- [GraalVM](https://graalvm.org) enables us to compile our software natively
- [Workers](https://workers.cloudflare.com) on the edge enable new levels of cache performance

When you use [Buildless][6], your build automatically gains the performance we bake into our service.

### How do I try it?

Sign up on our [website](https://less.build). **During the public beta, all usage is free!** Once you obtain your API key, you can start caching your favorite projects:

- [In Maven](https://github.com/buildless/sample-maven), using the [Build Cache Extension][2]
- [In Gradle](https://github.com/buildless/plugin-gradle), using our [Gradle Plugin][6]

We are adding more tools all the time. Our [API is well documented](https://docs.less.build/reference/supported-api-interfaces) and supports both [REST](https://docs.less.build/reference/cachegenericfetch) and [gRPC](https://buf.build/buildless/buildless/docs/main:buildless.service.v1).


[1]: https://docs.gradle.org/current/userguide/build_cache.html#sec:build_cache_setup_http_backend
[2]: https://maven.apache.org/extensions/maven-build-cache-extension
[3]: https://bazel.build/remote/caching
[4]: https://ccache.dev
[5]: https://www.cloudflare.com/network/
[6]: https://plugins.gradle.org/search?term=build.less
