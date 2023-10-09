# producer-consumer
Designed and implemented a multi-threaded producer-consumer system using C language, featuring a circular buffer for efficient data transfer and synchronisation. The project aimed to demonstrate concurrent programming skills and efficient data management.




      Results
      -------

	The integers were printed in random order. They were not printed in sequential order.
	Below is the output.

**********************
Serial number:1        Consumed Integer:0
Serial number:5        Consumed Integer:5
Serial number:6        Consumed Integer:6
Serial number:7        Consumed Integer:7
Serial number:8        Consumed Integer:8
Serial number:9        Consumed Integer:19
Serial number:10        Consumed Integer:20
Serial number:11        Consumed Integer:21
Serial number:12        Consumed Integer:22
Serial number:13        Consumed Integer:23
Serial number:14        Consumed Integer:24
Serial number:15        Consumed Integer:25
Serial number:2        Consumed Integer:2
Serial number:3        Consumed Integer:3
Serial number:18        Consumed Integer:38
Serial number:19        Consumed Integer:49
Serial number:4        Consumed Integer:4
Serial number:22        Consumed Integer:52
Serial number:23        Consumed Integer:53
Serial number:24        Consumed Integer:54
Serial number:25        Consumed Integer:55
Serial number:27        Consumed Integer:57
Serial number:28        Consumed Integer:58
Serial number:29        Consumed Integer:59
Serial number:31        Consumed Integer:61
Serial number:32        Consumed Integer:62
Serial number:33        Consumed Integer:63
Serial number:35        Consumed Integer:75
Serial number:36        Consumed Integer:76
Serial number:37        Consumed Integer:77
Serial number:38        Consumed Integer:78
Serial number:41        Consumed Integer:91
Serial number:39        Consumed Integer:79
Serial number:42        Consumed Integer:92
Serial number:40        Consumed Integer:90
Serial number:20        Consumed Integer:50
Serial number:45        Consumed Integer:94
Serial number:26        Consumed Integer:56
Serial number:16        Consumed Integer:26
Serial number:34        Consumed Integer:64
Serial number:48        Consumed Integer:98
Serial number:49        Consumed Integer:100
Serial number:50        Consumed Integer:91
Serial number:17        Consumed Integer:37
Serial number:52        Consumed Integer:92
Serial number:53        Consumed Integer:93
Serial number:54        Consumed Integer:94
Serial number:55        Consumed Integer:95
Serial number:57        Consumed Integer:97
Serial number:30        Consumed Integer:60
Serial number:59        Consumed Integer:99
Serial number:60        Consumed Integer:100
Serial number:43        Consumed Integer:93
Serial number:63        Consumed Integer:93
Serial number:64        Consumed Integer:94
Serial number:46        Consumed Integer:96
Serial number:66        Consumed Integer:96
Serial number:51        Consumed Integer:99
Serial number:68        Consumed Integer:98
Serial number:61        Consumed Integer:91
Serial number:70        Consumed Integer:100
Serial number:71        Consumed Integer:91
Serial number:72        Consumed Integer:92
Serial number:73        Consumed Integer:93
Serial number:74        Consumed Integer:94
Serial number:75        Consumed Integer:95
Serial number:76        Consumed Integer:96
Serial number:77        Consumed Integer:97
Serial number:78        Consumed Integer:98
Serial number:56        Consumed Integer:96
Serial number:80        Consumed Integer:100
Serial number:81        Consumed Integer:91
Serial number:67        Consumed Integer:97
Serial number:82        Consumed Integer:92
Serial number:83        Consumed Integer:93
Serial number:84        Consumed Integer:94
Serial number:85        Consumed Integer:95
Serial number:86        Consumed Integer:96
Serial number:87        Consumed Integer:97
Serial number:88        Consumed Integer:98
Serial number:69        Consumed Integer:99
Serial number:89        Consumed Integer:99
Serial number:91        Consumed Integer:92
Serial number:92        Consumed Integer:93
Serial number:58        Consumed Integer:98
Serial number:62        Consumed Integer:92
Serial number:95        Consumed Integer:95
Serial number:44        Consumed Integer:95
Serial number:97        Consumed Integer:97
Serial number:98        Consumed Integer:99
Serial number:99        Consumed Integer:100
Serial number:100        Consumed Integer:98
Serial number:65        Consumed Integer:95
Serial number:79        Consumed Integer:99
Serial number:90        Consumed Integer:100
Serial number:93        Consumed Integer:91
Serial number:94        Consumed Integer:94
Serial number:96        Consumed Integer:96
Serial number:21        Consumed Integer:51
Serial number:47        Consumed Integer:97

**************************************************
 
      Discussion
      ----------

	A	How many of each integer should you see printed?
	
		I expected 100 integers to be printed and there were 100 integers printed in the console.



	A	In what order should you expect to see them printed? Why?

		I expected them to be in random order because there were 10 consumer threads in my program and all of them were accessing the buffer in random order. There is no mechanism in my program to have them access in any particular sequence.They were accessing the buffer in the order they were scheduled which was beyond the scope of this program. So, random order was pretty much expected by me.


	A	Did your results differ from your answers in (1) and (2)?
      Why or why not?

	No, results were pretty much on the expected line. I expected 100 integers to be printed in random order because of the same reason as the above question. There is no mechanism in my program to have them access in any particular sequence.The consumer threads were accessing the buffer in the order they were scheduled which was beyond the scope of this program. So, random order was pretty much expected by me.
       Also, I have added a variable to print serial number, which is in turn, just the order in which the integer is accessed by a any consumer thread. For example, if  output is ((Serial number:47        Consumed Integer:97)), 
 it means that the integer 97, in the buffer, was accessed by its consumer thread on 47th iteration of the while loop in consumer thread. Similarly it can be inferred for other serial numbers also.  

	The serial number print command was just to emphasize and confirm my assumption and expectation that the integers will not be printed in any specific order. The randomness in serial number output can also be explained in the same way.It can be the result of any overhead or any scheduling delays which again is beyond the scope of this program and is totally CPU dependent.


