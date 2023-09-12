# Doc 

## File Description 

### start.sh 

- calls install.sh,  test-install.sh,  and runme.sh 

### src/runme.

- removes all previous log files 
- calls automate_soundy.sh and puts output in a new file named automate.log 

### src/RetestAll_seq.sh 

- run all test cases sequentially without any parallelization 

### src/automate_soundy.sh 

## src/PASTE_PROJconfigs 

### /classes/launch.sh 
- runs test cases with PASTE appraoch for given configurations 
### /classesAndMethods/launch.sh 
- runs test cases with PASTE appraoch for given configurations 
### /methods/launch.sh 
- runs test cases with PASTE appraoch for given configurations 

### src/PASTE_PROJ.sh 
- Runs launch.sh with given arguement 

## mvn command info 

### -Dparallel=methods 

While test methods within a class are executed in parallel, the test classes themselves are typically executed sequentially, one after the other, on the same thread. This ensures that there is no interference between different test classes.

### -Dparallel=classes 

Maven will execute these test classes in parallel.For instance, if you specified 4 concurrent threads, Maven will start 4 threads or processes and assign test classes to them as they become available.

Within each test class, the test methods (annotated with @Test for JUnit or similar annotations for other testing frameworks) are typically executed sequentially, one after the other, on the same thread.

### -Dparallel=classesAndMethods

running multiple test classes and test methods concurrently within their respective groups. Within each test class, Maven identifies individual test methods that can be executed in parallel.