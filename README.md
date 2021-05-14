# Stepleap starter kit
Project structure to get started with Stepleap

## Usage
To get a running start with Stepleap, either fork this project, or download the sources as a zip file and extract locally.

To run Stepleap you do need to add the credentials for the Gradle plugin repository. Do this by editting the username and password lines in `settings.gradle`.

```groovy
...
maven {
	credentials {
		username "<username>"
		password "<password>"
	}
	url 'https://pbrandwijk.com/maven'
}
...
```

Then open up a terminal, go to the project folder and execute:

```console
$ gradlew tasks -all
```

This will download the plugin and libraries and display all available tasks. To run the importStepxml task on the example STEPXML file in the projec, run:

```console
$ gradlew importStepxml -w
```

This will import all business rules from the STEPXML file and put them under `src/main/js`. The `-w` directive is optional and can be replaced with `-i` for displaying log messages from warning level and above and info level and abve respectively.
