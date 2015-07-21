# PHPUnit Docker Container

[Docker](https://www.docker.com) container to install and run [PHPUnit](https://phpunit.de/).

## Features

* [PHPUnit](https://www.phpunit.de/)
  * Latest snapshot (master)
  * [`4.6.6`](https://github.com/sebastianbergmann/phpunit/blob/master/ChangeLog-4.6.md#phpunit-466)
* [PHP](http://php.net) [5.6](http://php.net/ChangeLog-5.php)

## Installation / Usage

1. Install the phpunit/phpunit container:

    ``` sh
	$ docker pull phpunit/phpunit
	```

2. Create a phpunit.xml defining your spec suites.

    ``` xml
...
    ```

3. Run PHPUnit through the PHPUnit container:

    ``` sh
	$ docker run -v $(pwd):/app phpunit/phpunit run
    ```

To run, test and develop the PHPUnit Dockerfile itself, you must use the source directly:

1. Download the source:

    ``` sh
	$ git clone https://github.com/JulienBreux/phpunit-docker.git
    ```

2. Switch to the phpunit-docker directory:

    ``` sh
	$ cd phpunit-docker
    ```

3. Build the container:

    ``` sh
	$ docker build -t phpunit/phpunit .
    ```

4. Test running the container:

    ``` sh
	$ docker run phpunit/phpunit --help
	```