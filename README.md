FORGE BIRT Reports test
==================

Test cases to verify FORGE BIRT reports

Prerequisites
-------------

### Targe machine (to be tested)

- There is a target machine running Tomcat with birt-viewer web app.
- FORGE birt reports are deployed to birt-viewer into target machine.

### Testing machine (running tests)

- The test machine has either X or virtual fb Xvfb to allow launchig a Firefox browser
- Firefox browser

  $ sudo Xvfb :10 -ac
  $ export DISPLAY=:10
  $ DISP=`shuf -i 15-255 -n 1`
  $ Xvfb :$DISP -ac > /dev/null 2>&1 &
  $ PID=$!
  $ DISPLAY=:$DISP pybot --variable TARGET_IP:$target_ip --variable ENV:$env .
  $ kill -s TERM $PID

### Configuration variables

    TARGET_IP [ip of the BIRT machine to be tested]
    REPORT_URL [the location where the BIRT report can be accessed from]
    ENV  [test, prod]
