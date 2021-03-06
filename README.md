# SpigotResourcesAPI
a Java wrapper of the Spigot resources REST API ([XenforoResourceManagerAPI](https://github.com/SpigotMC/XenforoResourceManagerAPI))

[![Release](https://jitpack.io/v/robertlit/SpigotResourcesAPI.svg)](https://jitpack.io/#robertlit/SpigotResourcesAPI)

[Javadoc](https://jitpack.io/com/github/robertlit/SpigotResourcesAPI/1.0/javadoc/)

SpigotResourcesAPI aims to be simple, thread-safe and efficient.

# How to use
Currently, SpigotResourcesAPI is only available through JitPack.
In the future, it may be deployed to maven central, and will be deployed to GitHub Packages if authentication will not be required.

## Maven
Add JitPack as a repository
```
<!--   it is recommended to specify JitPack after all other repositories   -->
<repository>
	<id>jitpack.io</id>
	<url>https://jitpack.io</url>
</repository>
```
Add SpigotResourcesAPI as a dependency
```
<dependency>
  <groupId>com.github.robertlit</groupId>
  <artifactId>SpigotResourcesAPI</artifactId>
  <version>1.0</version>
</dependency>
```

## Gradle
Add JitPack as a repository
```
repositories {
	...
	maven { url 'https://jitpack.io' }
}
```
Add SpigotResourcesAPI as a dependency
```
dependencies {
		implementation 'com.github.robertlit:SpigotResourcesAPI:1.0'
	}
```

# Code exmaples
``` Java
SpigotResourcesAPI api = new SpigotResourcesAPI(false);

// Get Author by id
CompletableFuture<Author> future = api.getAuthor(740512);
future.thenAccept(author -> {
  // ...
});

// Get Resources by Author id
CompletableFuture<Collection<Resource>> future = api.getResourcesByAuthor(740512);
future.thenAccept(resources -> {
  // ...
});

// Get Resource by id
CompletableFuture<Resource> future = api.getResource(72343);
future.thenAccept(resource -> {
  // ...
});
```


If this has helped you, please consider [donating via PayPal](https://www.paypal.me/robertlitmc).