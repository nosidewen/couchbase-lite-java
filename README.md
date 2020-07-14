# couchbase-lite-java

This is a forked version of [couchbase-lite-java](https://github.com/couchbase/couchbase-lite-java) with modifications made off of the `v1x/master` branch in order to add Linux ARM native binaries. For this project, this build includes ARM binaries sepcifically for the Cortex-A7. In order to build this library with ARM support for different processors, see more details about building the binaries in [couchbase-lite-java-native](https://github.com/nosidewen/couchbase-lite-java-native).

## Build
This version of the library includes the `couchbase-lite-java-core`, `couchbase-lite-java-native`, and `couchbase-lite-java-javascript` submodules. To add other couchbase lite sub-projects to the build (like `couchbase-lite-java-listener`, etc.), add a submodule and ensure that it is checked out to `release1.4.1`, or your own forked version.

To build the library, run the following commands:
```
git clone https://github.com/nosidewen/couchbase-lite-java.git
git clone https://github.com/couchbase/couchbase-lite-android.git
cd couchbase-lite-java/
git submodule update --init --recursive
./gradlew clean && ./gradlew test
./gradlew distZip
```

The packaged file will be located at `build/distributions`.
