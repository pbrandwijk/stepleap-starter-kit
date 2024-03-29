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

Then open up a terminal, go to the project folder and execute (use `.\gradlew.bat` when on Windows):

```console
$ ./gradlew tasks --all
```

This will download the plugin and libraries and display all available tasks. To run the transform task on the example `stepxml.xml` file in the project, run:

```console
$ ./gradlew transform -w
```

This will import all business rules from the `stepxml.xml` file and put them under `src/main/js`. The `-w` directive is optional and can be replaced with `-i` for displaying log messages from warning level and above and info level and above respectively.
