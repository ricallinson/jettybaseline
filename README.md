# javabaseline

This is a simple _hello world_ HTTP Jetty server to find a baseline number for performance comparisons.

## Run Test

Build and start the server;

	jetty-test

The test will print the number of cores and threads the server is using;

	Server started, using 4 cores and 8 threads...

Now run apache bench;

	ab -n 1000000 -c 8 -k http://127.0.0.1:8080/

## Performance Results

The test was run on a MacBook Pro (Retina, 13-inch, Mid 2014), 3 GHz Intel Core i7 with 16 GB 1600 MHz DDR3 memory.

	Concurrency Level:      8
	Time taken for tests:   20.234 seconds
	Complete requests:      1000000
	Failed requests:        0
	Keep-Alive requests:    1000000
	Total transferred:      160000000 bytes
	HTML transferred:       21000000 bytes
	Requests per second:    49420.78 [#/sec] (mean)
	Time per request:       0.162 [ms] (mean)
	Time per request:       0.020 [ms] (mean, across all concurrent requests)
	Transfer rate:          7722.00 [Kbytes/sec] received

## Problems Found

None.
