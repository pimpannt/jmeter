
# The Jmeter Significance :wink:

## Download
(https://jmeter.apache.org/download_jmeter.cgi)

## Exercise
(https://medium.com/selectstarfromweb/performance-testing-using-jmeter-fd083cae68)
(https://medium.com/gradeup/introduction-to-apache-jmeter-beginners-guide-466b741d33e5)

## Tips for Jmeter Beginner
(http://www.testautomationguru.com/jmeter-tips-tricks-for-beginners/)
**1.Exclude static file from test plan** 
    ex. .css/gif, libraly version. but insert it by configuration file

**2.Use Transaction / Simple Controller**
    group request by scenario within Transaction or Simpler Controller

**3.Use HTTP Request Defaults**
    add 'HTTP Request Default' for each environment before Transaction Controller
    enable only use file

**4.Add User Defined Variable (in Config Element)**
    It is the dataset of test data
    Can also import by csv file

**5.Correlation**
    add 'authid' in parameter request to handle client-server communication

**6.Thread Count vs. Loop Count**
    Thread Count : 10 Thread,1 sec,1 Loop  (=> load to much)
    Loop Count   : 1  Thread,1 sec,10 Loop (=> too steady) and set ramp-up = 1 to keep adding 1 user every second

**7.Listener**
    Avoid adding more than 1 listener report
    Result listener can cause performance of testing and memory

**8.Assertion**
    Same ass listener, should not add much
    Every time Jmeter needs to pass whole response object to check for assertion

**9.Run Test**
    ** Run in NON-GUI mode to lessen memory consumption **
    `jmeter -n -t testplan.jmx -l result.jtl`
    or
    `jmeter -n -t testplan.jmx -l result.jtl -Djmeter.save.saveservice.output_format=csv`
    note: 
    - Add jmeter in $PATH
    - File testplan.jmx needs to export Testplan level

**10.Tweaking JVM**
    Check for hardware requirement : 64 bit, RAM




http://www.testautomationguru.com/jmeter-how-to-execute-different-performance-test-strategies/

http://www.vinsguru.com/jmeter/

http://www.testautomationguru.com/how-to-test-rest-api-using-jmeter/
